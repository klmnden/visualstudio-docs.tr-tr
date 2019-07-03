---
title: Visual Studio kapsayıcı araçları derleme genel bakış
author: ghogen
description: Kapsayıcı Araçları yapı işlemine genel bakış
ms.author: ghogen
ms.date: 06/06/2019
ms.technology: vs-azure
ms.topic: conceptual
ms.openlocfilehash: 9f2da112bfeebe4e0bce976736eee5696d888105
ms.sourcegitcommit: c7b9ab1bc19d74b635c19b1937e92c590dafd736
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/03/2019
ms.locfileid: "67552822"
---
# <a name="building-containerized-apps-using-visual-studio-or-the-command-line"></a>Visual Studio veya komut satırını kullanarak uygulamaları kapsayıcıya alınmış oluşturma

Visual Studio IDE içinden oluştururken veya bir komut satırı derleme ayarlamaya, Visual Studio nasıl derler bilmeniz gereken olup olmadığını projelerinizi oluşturmaya Dockerfile'ı kullanır.  Performansla ilgili nedenlerden dolayı Visual Studio kapsayıcı uygulamaları için özel bir işlemi izler. Visual Studio projelerinizin nasıl derler anlama Dockerfile değiştirerek yapı işleminizi özelleştirme, özellikle önemlidir.

Visual Studio, Docker kapsayıcıları kullanmayan bir projeyi oluşturduğunda, yerel makinede MSBuild çağırır ve bir klasörde Çıkış dosyalarını oluşturur (genellikle `bin`) yerel Çözüm klasörünüz altında. Kapsayıcılı bir proje için ancak, kapsayıcılı uygulama oluşturma yönergeleri Dockerfile'nın hesabını oluşturma işlemi alır. Visual Studio kullanan Dockerfile, birden çok aşamalara bölünmüştür. Bu işlem üzerinde Docker's dayanır *aşamalı derleme* özelliği.

## <a name="multistage-build"></a>Aşamalı derleme

Aşamalı yapı özelliği kapsayıcılar daha verimli oluşturma işleminin olmasına yardımcı olur ve uygulamanızın çalışma zamanında gereken BITS içermesini sağlayarak kapsayıcıları daha küçük yapar. Aşamalı bir derleme, .NET Framework projeleri .NET Core projeleri için kullanılır.

Aşamalı derleme Ara görüntüleri oluşturmak ve aşamalar halinde oluşturulacak kapsayıcı görüntüleri sağlar. Örnek olarak, Visual Studio tarafından oluşturulan tipik bir Dockerfile göz önünde bulundurun - ilk aşama `base`:

```
FROM mcr.microsoft.com/dotnet/core/aspnet:2.2-stretch-slim AS base
WORKDIR /app
EXPOSE 80
EXPOSE 443
```

Dockerfile satırları Nanoserver görüntünün Microsoft Container registry'den (mcr.microsoft.com) ile başlayan ve Ara görüntü oluşturma `base` 80 ve 443 bağlantı noktalarını kullanıma sunar ve çalışma dizinini ayarlar `/app`.

Sonraki aşamasıdır `build`, şu şekilde görünür:

```
FROM mcr.microsoft.com/dotnet/core/sdk:2.2-stretch AS build
WORKDIR /src
COPY ["WebApplication43/WebApplication43.csproj", "WebApplication43/"]
RUN dotnet restore "WebApplication43/WebApplication43.csproj"
COPY . .
WORKDIR "/src/WebApplication43"
RUN dotnet build "WebApplication43.csproj" -c Release -o /app
```

Gördüğünüz gibi `build` aşaması başlar kayıt defterinden farklı orijinal görüntüden (`sdk` yerine `aspnet`), temel etmeden yerine.  `sdk` Görüntüsü bulunan tüm derleme araçları ve ASP.NET görüntüden daha çok büyük olduğu bu nedenle, yalnızca içeren çalışma zamanı bileşenleri. Dockerfile bekleyen baktığınızda ayrı bir görüntü kullanma nedenleri belirgin bir hale gelir:

```
FROM build AS publish
RUN dotnet publish "WebApplication43.csproj" -c Release -o /app

FROM base AS final
WORKDIR /app
COPY --from=publish /app .
ENTRYPOINT ["dotnet", "WebApplication43.dll"]
```

Son aşama yeniden başlatılır `base`ve içerir `COPY --from=publish` yayımlanan çıkış son görüntüyü kopyalamak için. Bu işlem tüm olan derleme Araçları eklemek gerekli olmayan olduğundan çok daha küçük olacak şekilde son görüntü mümkün kılar `sdk` görüntü.

## <a name="faster-builds-for-the-debug-configuration"></a>Hata ayıklama yapılandırması daha hızlı yapılar

Visual Studio ile kapsayıcılı projeler için derleme işleminin performansını yardımcı uğramadığını çeşitli iyileştirmeler vardır. Mümkünse, hata ayıklama (F5) başlattığınızda, önceden oluşturulmuş bir görüntüyü yeniden kullanılır. Önceki kapsayıcı yeniden kullanmak istemiyorsanız, kullanabileceğiniz **yeniden** veya **temiz** yeni bir kapsayıcı kullanmak için Visual Studio zorlamak için Visual Studio komutları.

Ayrıca, performansı artırmak için kapsayıcı uygulamaları için derleme işlemi yalnızca bir Dockerfile içinde ana hatlarıyla belirtilen adımları izleyerek olarak basit değildir. Bir kapsayıcıyı, yerel makinede yapılandırmaktan çok yavaştır.  Bunu, derlerken **hata ayıklama** yapılandırma, Visual Studio projelerinizin yerel makinede geçilmişse ve ardından birim bağlama kullanarak kapsayıcıyı çıktı klasörüne paylaşır. Bu iyileştirme, etkin bir derleme olarak adlandırılan bir *hızlı* modu derleme.

İçinde **hızlı** modu, Visual Studio çağrıları `docker build` yalnızca oluşturmak için Docker söyleyen bir bağımsız değişkenli `base` aşaması.  Visual Studio Dockerfile içeriğini bakılmaksızın işleminin geri kalanı işler. Bu nedenle, Dockerfile, gibi kapsayıcı ortamı özelleştirmek veya ek bağımlılıklar'ı yüklemek için değiştirdiğinizde, ilk aşamada, değişikliklerinizi koymanız gerekir.  Herhangi bir özel adım yerleştirilen Dockerfile'da 's `build`, `publish`, veya `final` aşamaları yürütülmez.

Bu performans iyileştirmesi, yalnızca yapı içinde oluşur **hata ayıklama** yapılandırma. İçinde **yayın** Dockerfile içinde belirtildiği gibi kapsayıcı yapılandırması, yapı oluşuyor.

Performans İyileştirme devre dışı bırakmak istediğiniz ve derleme Dockerfile belirtildiği gibi ardından ayarlarsanız **ContainerDevelopmentMode** özelliğini **normal** dosya projede aşağıdaki gibi:

```xml
<PropertyGroup>
   <ContainerDevelopmentMode>Regular</ContainerDevelopmentMode>
</PropertyGroup>
```

Performans iyileştirmesi geri yüklemek için proje dosyasından özelliği kaldırın.

## <a name="building-from-the-command-line"></a>Komut satırından derleme

Kullanabileceğiniz `docker build` veya `MSBuild` komut satırından oluşturmak için.

### <a name="docker-build"></a>docker derleme

Komut satırından kapsayıcılı bir çözüm oluşturmak için genellikle komutunu kullanabilirsiniz `docker build <context>` çözümde her proje için. Sağladığınız *bağlam yapı* bağımsız değişken. *Bağlam yapı* için bir Dockerfile klasörü yerel makinede çalışma klasörü olarak görüntü oluşturmak için kullanılır. Örneğin, bu kapsayıcıya kopyaladığınızda gelen dosyaları kopyalayın klasördür.  .NET Core projelerinde, çözüm (.sln) dosyasını içeren klasörü kullanın.  Göreli bir yol ifade edilen, bu bağımsız değişken genellikle ise "..." için bir Dockerfile içinde bir proje klasörü ve kendi üst klasördeki çözüm dosyası.  .NET Framework projeleri için proje klasörü, Çözüm klasörü değil derleme bağlamıdır.

```cmd
docker build -f Dockerfile ..
```

### <a name="msbuild"></a>MSBuild

Dockerfile'ları için .NET Framework projeleri (ve Visual Studio 2017 güncelleştirme 4'ün önceki Visual Studio sürümleriyle oluşturulan .NET Core projeleri için) Visual Studio tarafından oluşturulan aşamalı dockerfile'ları değildir.  Bu dockerfile'ları adımlarda kod derlenmiyor.  Bunun yerine, Visual Studio .NET Framework Dockerfile oluşturduğunda, ilk projenizi MSBuild kullanarak derler.  Visual Studio, sonra başarılı olduğunda, yalnızca yapı çıkışını MSBuild'den elde edilen bir Docker görüntüsü halinde kopyalar Dockerfile oluşturur.  Kodunuzu derlemek için adımları Dockerfile içinde yer almayan için .NET Framework kullanarak dockerfile'ları oluşturamaz `docker build` komut satırından. Bu projeleri derlemek için MSBuild kullanmanız gerekir.

Bir görüntü için tek bir docker kapsayıcı proje derlemek için MSBuild ile kullanabilirsiniz `/t:ContainerBuild` seçeneği komutu. Örneğin:

```cmd
MSBuild MyProject.csproj /t:ContainerBuild /p:Configuration=Release
```

İçinde gördükleri için benzer bir çıktı görürsünüz **çıkış** penceresini Visual Studio IDE içinden çözümünüzü oluşturun. Her zaman `/p:Configuration=Release`, burada Visual Studio kullanan çok yapı durumlarda en iyi duruma getirme, sonuçları bu yana oluştururken **hata ayıklama** yapılandırma beklendiği gibi olmayabilir.

Bir Docker Compose proje kullanıyorsanız, görüntüleri oluşturmak için komutu kullanın:

```cmd
msbuild /p:SolutionPath=<solution-name>.sln /p:Configuration=Release docker-compose.dcproj
```

## <a name="next-steps"></a>Sonraki adımlar

Daha fazla proje dosyalarınızı ek MSBuild özellikleri ayarlayarak derlemelerinizi özelleştirmeyi öğrenin. Bkz: [kapsayıcı projeleri için MSBuild özellikleri](container-msbuild-properties.md).

## <a name="see-also"></a>Ayrıca bkz.

[MSBuild](../msbuild/msbuild.md)
[Windows üzerinde Dockerfile](/virtualization/windowscontainers/manage-docker/manage-windows-dockerfile)
[Windows üzerinde Linux kapsayıcıları](/virtualization/windowscontainers/deploy-containers/linux-containers)
