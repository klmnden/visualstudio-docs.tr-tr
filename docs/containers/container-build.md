---
title: Visual Studio kapsayıcı araçları oluşturmaya genel bakış
author: ghogen
description: Kapsayıcı araçları derleme işlemine genel bakış
ms.author: ghogen
ms.date: 06/06/2019
ms.technology: vs-azure
ms.topic: conceptual
ms.openlocfilehash: edc4674e2468124ecb46b25a1411043ed4b66a2a
ms.sourcegitcommit: e98db44f3a33529b0ba188d24390efd09e548191
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71253113"
---
# <a name="building-containerized-apps-using-visual-studio-or-the-command-line"></a>Visual Studio veya komut satırı kullanarak Kapsayıcılı uygulamalar oluşturma

Visual Studio IDE 'den oluşturuluyor veya bir komut satırı derlemesi ayarlıyoruz, Visual Studio derlemelerinizin projelerinizi oluşturmak için Dockerfile 'ı nasıl kullandığını bilmeniz gerekir.  Performans nedenleriyle, Visual Studio Kapsayıcılı uygulamalar için özel bir işlem izler. Visual Studio 'Nun projelerinizi nasıl derlemediğini anlamak, Dockerfile dosyasını değiştirerek yapı işleminizi özelleştirirken özellikle önemlidir.

Visual Studio, Docker Kapsayıcıları kullanmayan bir proje oluşturduğunda, yerel makinede MSBuild 'i çağırır ve çıkış dosyalarını yerel çözüm klasörünüzün altında bir klasörde (genellikle `bin`) oluşturur. Bununla birlikte, kapsayıcılı bir proje için yapı işlemi, Dockerfile 'ın Kapsayıcılı uygulama oluşturma yönergelerinin bir hesabını alır. Visual Studio 'Nun kullandığı Dockerfile birden çok aşamaya bölünmüştür. Bu işlem Docker 'ın *çok aşamalı derleme* özelliğini kullanır.

## <a name="multistage-build"></a>Çok aşamalı derleme

Çoklu aşama oluşturma özelliği, kapsayıcıları oluşturma işleminin daha verimli olmasına yardımcı olur ve yalnızca uygulamanızın çalışma zamanında ihtiyaç duyacağı bitleri içermesine izin vererek kapsayıcıları daha küçük hale getirir. MultiStage derlemesi, .NET Framework projeleri değil .NET Core projeleri için kullanılır.

Hatlarında derlemesi, ara görüntü üreten aşamalarda kapsayıcı görüntülerinin oluşturulmasına izin verir. Örnek olarak, Visual Studio tarafından oluşturulan tipik bir Dockerfile 'ı düşünün; ilk aşama `base`:

```
FROM mcr.microsoft.com/dotnet/core/aspnet:2.2-stretch-slim AS base
WORKDIR /app
EXPOSE 80
EXPOSE 443
```

Dockerfile içindeki satırlar, Microsoft Container Registry (MCR.Microsoft.com) Nanoserver görüntüsünden başlar ve 80 ve 443 bağlantı noktalarını kullanıma sunan bir `base` ara görüntü oluşturur ve çalışma dizinini olarak `/app`ayarlar.

Sonraki aşama `build`aşağıdaki gibi görünür:

```
FROM mcr.microsoft.com/dotnet/core/sdk:2.2-stretch AS build
WORKDIR /src
COPY ["WebApplication43/WebApplication43.csproj", "WebApplication43/"]
RUN dotnet restore "WebApplication43/WebApplication43.csproj"
COPY . .
WORKDIR "/src/WebApplication43"
RUN dotnet build "WebApplication43.csproj" -c Release -o /app
```

`build` Aşamanın, temelden devam etmek yerine, kayıt defterinden (`sdk` `aspnet`yerine) farklı bir orijinal görüntüden başlatıldığını görebilirsiniz.  `sdk` Görüntüde tüm derleme araçları bulunur ve bu nedenle yalnızca çalışma zamanı bileşenleri içeren ASPNET görüntüsünden çok daha büyük bir büyük olur. Dockerfile ' ın geri kalanına göz atadığınızda ayrı bir görüntü kullanmanın nedeni açık olur:

```
FROM build AS publish
RUN dotnet publish "WebApplication43.csproj" -c Release -o /app

FROM base AS final
WORKDIR /app
COPY --from=publish /app .
ENTRYPOINT ["dotnet", "WebApplication43.dll"]
```

Son aşama öğesinden `base`bir kez daha başlar ve yayımlanan çıktıyı `COPY --from=publish` son görüntüye kopyalamak için içerir. Bu işlem, `sdk` görüntüde bulunan tüm derleme araçlarını içermesi gerekmiyorsa nihai görüntünün çok daha küçük olmasını mümkün kılar.

## <a name="faster-builds-for-the-debug-configuration"></a>Hata ayıklama yapılandırması için daha hızlı yapılar

Visual Studio 'nun Kapsayıcılı projelere yönelik yapı sürecinin performansına yardımcı olan birkaç iyileştirmesi vardır. Hata ayıklamayı başlattığınızda (F5), mümkünse önceden oluşturulmuş bir görüntü yeniden kullanılır. Önceki kapsayıcıyı yeniden kullanmak istemiyorsanız, Visual Studio 'Nun yeni bir kapsayıcı kullanmasını zorlamak için Visual Studio 'da **yeniden oluşturma** veya **Temizleme** komutlarını kullanabilirsiniz.

Ayrıca, performansı artırmak için Kapsayıcılı uygulamalar için derleme işlemi, Dockerfile içinde özetlenen adımları takip etmek kadar basittir. Kapsayıcıda derleme, yerel makinede oluşturmaktan çok daha yavaştır.  Bu nedenle, **hata ayıklama** yapılandırmasında derleme yaparken, Visual Studio projelerinizi gerçekten yerel makinede oluşturur ve ardından çıkış klasörünü birim bağlama kullanarak kapsayıcınıza paylaşır. Bu iyileştirme etkin olan bir yapıya *hızlı* mod oluşturma denir.

**Hızlı** modda, Visual Studio, Docker 'ın yalnızca `docker build` `base` aşamayı oluşturmasını söyleyen bir bağımsız değişkenle çağırır.  Visual Studio, Dockerfile içeriğiyle ilgili olarak işlemin geri kalanını işler. Bu nedenle, kapsayıcı ortamını özelleştirmek veya ek bağımlılıklar yüklemek gibi Dockerfile 'ı değiştirdiğinizde, değişikliklerinizi ilk aşamada koymanız gerekir.  Dockerfile 'ın `build`, `publish`veya `final` aşamalarına yerleştirilmiş özel adımlar yürütülmez.

Bu performans iyileştirmesi yalnızca **hata ayıklama** yapılandırmasında derleme yaparken oluşur. **Yayın** yapılandırmasında, yapı, Dockerfile içinde belirtildiği gibi kapsayıcıda oluşur.

Dockerfile tarafından belirtildiği gibi performans iyileştirmesini ve derlemeyi devre dışı bırakmak istiyorsanız, proje dosyasında şu şekilde **Containerdevelopmentmode** özelliğini **normal** olarak ayarlayın:

```xml
<PropertyGroup>
   <ContainerDevelopmentMode>Regular</ContainerDevelopmentMode>
</PropertyGroup>
```

Performans iyileştirmesini geri yüklemek için, özelliği proje dosyasından kaldırın.

## <a name="building-from-the-command-line"></a>Komut satırından oluşturma

Komut satırından oluşturmak `docker build` için `MSBuild` veya kullanabilirsiniz.

### <a name="docker-build"></a>Docker derlemesi

Komut satırından kapsayıcılı bir çözüm oluşturmak için, genellikle komutunu `docker build <context>` çözümdeki her proje için kullanabilirsiniz. *Yapı bağlamı* bağımsız değişkenini sağlarsınız. Dockerfile için *derleme bağlamı* , yerel makinedeki, görüntüyü oluşturmak için çalışma klasörü olarak kullanılan klasördür. Örneğin, kapsayıcıya kopyaladığınız sırada dosyaları kopyaladığınız klasördür.  .NET Core projelerinde, çözüm dosyasını (. sln) içeren klasörü kullanın.  Göreli yol olarak ifade edilen bu bağımsız değişken, genellikle proje klasöründeki bir Dockerfile ve onun üst klasöründeki çözüm dosyası için ".." olur.  .NET Framework projeleri için, yapı bağlamı çözüm klasörü değil, proje klasörüdür.

```cmd
docker build -f Dockerfile ..
```

### <a name="msbuild"></a>MSBuild

.NET Framework projeleri için Visual Studio tarafından oluşturulan dockerfiles (ve Visual Studio 2017 güncelleştirme 4 ' ten önceki Visual Studio sürümleriyle oluşturulan .NET Core projeleri için) çok aşamalı Dockerfiles değildir.  Bu Dockerfiles içindeki adımlar kodunuzu derlemez.  Bunun yerine, Visual Studio .NET Framework Dockerfile oluşturduğunda, öncelikle projenizi MSBuild kullanarak derler.  Bu başarılı olduğunda Visual Studio, yapı çıkışını MSBuild 'ten elde edilen Docker görüntüsüne kopyalayan Dockerfile öğesini oluşturur.  Kodunuzu derlemek için gereken adımlar dockerfile 'a dahil edilmediğinden, komut satırından kullanarak `docker build` .NET Framework dockerfiles derlenemez. Bu projeleri derlemek için MSBuild 'i kullanmanız gerekir.

Tek Docker kapsayıcı projesi için bir görüntü oluşturmak üzere, MSBuild `/t:ContainerBuild` 'i komut seçeneğiyle kullanabilirsiniz. Örneğin:

```cmd
MSBuild MyProject.csproj /t:ContainerBuild /p:Configuration=Release
```

Visual Studio IDE 'den Çözümünüzü oluştururken **Çıkış** penceresinde gördüklerinize benzer bir çıktı görürsünüz. Her zaman `/p:Configuration=Release`kullanın, Visual Studio 'nun çok aşamalı derleme iyileştirmesini kullandığı durumlarda, **hata ayıklama** yapılandırmasını oluştururken sonuçlar beklendiği gibi olmayabilir.

Docker Compose projesi kullanıyorsanız, görüntüleri derlemek için komutunu kullanın:

```cmd
msbuild /p:SolutionPath=<solution-name>.sln /p:Configuration=Release docker-compose.dcproj
```

## <a name="next-steps"></a>Sonraki adımlar

Proje dosyalarınızda ek MSBuild özellikleri ayarlayarak derlemelerinizi nasıl özelleştireceğinizi öğrenin. Bkz. [kapsayıcı projeleri Için MSBuild özellikleri](container-msbuild-properties.md).

## <a name="see-also"></a>Ayrıca bkz.

[](../msbuild/msbuild.md)
[Windows Linux kapsayıcılarındaki](/virtualization/windowscontainers/deploy-containers/linux-containers) MSBuild
[dockerfile](/virtualization/windowscontainers/manage-docker/manage-windows-dockerfile)
