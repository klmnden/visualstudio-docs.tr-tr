---
title: Visual Studio kapsayıcı araçları derleme genel bakış
author: ghogen
description: Kapsayıcı Araçları yapı işlemine genel bakış
ms.author: ghogen
ms.date: 06/06/2019
ms.technology: vs-azure
ms.topic: conceptual
ms.openlocfilehash: 26b9bab096c65ff987d4e7c824555544a7e38cd6
ms.sourcegitcommit: 0cd282a7584b9bfd4df7882f8fdf3ad8a270e219
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/28/2019
ms.locfileid: "67467406"
---
# <a name="building-containerized-apps-using-visual-studio-or-the-command-line"></a>Visual Studio veya komut satırını kullanarak uygulamaları kapsayıcıya alınmış oluşturma

Visual Studio IDE içinden oluştururken veya bir komut satırı derleme ayarlamaya, Visual Studio nasıl derler bilmeniz gereken olup olmadığını projelerinizi oluşturmaya Dockerfile'ı kullanır.  Performansla ilgili nedenlerden dolayı Visual Studio kapsayıcı uygulamaları için özel bir işlemi izler. Visual Studio projelerinizin nasıl derler anlama Dockerfile değiştirerek yapı işleminizi özelleştirme, özellikle önemlidir.

Visual Studio, Docker kapsayıcıları kullanmayan bir projeyi oluşturduğunda, yerel makinede MSBuild çağırır ve bir klasörde Çıkış dosyalarını oluşturur (genellikle `bin`) yerel Çözüm klasörünüz altında. Kapsayıcılı bir proje için ancak, kapsayıcılı uygulama oluşturma yönergeleri Dockerfile'nın hesabını oluşturma işlemi alır. Visual Studio kullanan Dockerfile, birden çok aşamalara bölünmüştür. Bu işlem üzerinde Docker's dayanır *aşamalı derleme* özelliği.

## <a name="multistage-build"></a>Aşamalı derleme

Aşamalı yapı özelliği kapsayıcılar daha verimli oluşturma işleminin olmasına yardımcı olur ve uygulamanızın çalışma zamanında gereken BITS içermesini sağlayarak kapsayıcıları daha küçük yapar.

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

Performansla ilgili nedenlerle, kapsayıcılı uygulamaları için derleme işlemi yalnızca bir Dockerfile içinde ana hatlarıyla belirtilen adımları izleyerek olarak basit değildir. Bir kapsayıcıyı, yerel makinede yapılandırmaktan çok yavaştır.  Bunu, derlerken **hata ayıklama** yapılandırma, Visual Studio projelerinizin yerel makinede geçilmişse ve ardından birim bağlama kullanarak kapsayıcıyı çıktı klasörüne paylaşır. Bu iyileştirme, etkin bir derleme olarak adlandırılan bir *hızlı* modu derleme.

İçinde **hızlı** modu, Visual Studio çağrıları `docker build` yalnızca oluşturmak için Docker söyleyen bir bağımsız değişkenli `base` aşaması.  Visual Studio Dockerfile içeriğini bakılmaksızın işleminin geri kalanı işler. Bu nedenle, Dockerfile, gibi kapsayıcı ortamı özelleştirmek veya ek bağımlılıklar'ı yüklemek için değiştirdiğinizde, ilk aşamada, değişikliklerinizi koymanız gerekir.  Herhangi bir özel adım yerleştirilen Dockerfile'da 's `build`, `publish`, veya `final` aşamaları yürütülmez.

Bu performans iyileştirmesi, yalnızca yapı içinde oluşur **hata ayıklama** yapılandırma. İçinde **yayın** Dockerfile içinde belirtildiği gibi kapsayıcı yapılandırması, yapı oluşuyor.

Performans İyileştirme devre dışı bırakmak istediğiniz ve derleme Dockerfile belirtildiği gibi ardından ayarlarsanız **ContainerDevelopmentMode** özelliğini **normal** dosya projede aşağıdaki gibi:

```xml
<PropertyGroup>
   <ContainerDevelopmentMode>Regular</ContainerDevelopmentMode>
</PropertyGroup>
```

Performans iyileştirmesi geri yüklemek için değeri ayarlamak **hızlı**.

## <a name="building-from-the-command-line"></a>Komut satırından derleme

Kullanabileceğiniz `docker build` veya `MSBuild` komut satırından oluşturmak için.

### <a name="docker-build"></a>docker derleme

Komut satırından kapsayıcılı bir çözüm oluşturmak için genellikle komutunu kullanabilirsiniz `docker build <context>` çözümde her proje için. Sağladığınız *bağlam yapı* bağımsız değişken. *Bağlam yapı* için bir Dockerfile klasörü yerel makinede çalışma klasörü olarak görüntü oluşturmak için kullanılır. Örneğin, kapsayıcıya kopyaladığınızda gelen dosyaları kopyalayın f'older olur.  .NET Core projelerinde, çözüm (.sln) dosyasını içeren klasörü kullanın.  Göreli bir yol ifade edilen, bu bağımsız değişken genellikle ise "..." için bir Dockerfile içinde bir proje klasörü ve kendi üst klasördeki çözüm dosyası.  .NET Framework projeleri için proje klasörü, Çözüm klasörü değil derleme bağlamıdır.

> [!NOTE] 
> .NET Framework projeleri ve Visual Studio 2017 güncelleştirme 4'ün önceki Visual Studio sürümleriyle oluşturulan .NET Core projeleri için Dockerfile aşamalı yapılar kullanmadı. Visual Studio, Dockerfile içinde bir proje oluşturmak yerine bu dockerfile'ları ile oluşturduğunda Visual Studio her projeyi oluşturur ve ardından sonuçları kapsayıcıya kopyalar. Derleme adımları Dockerfile içinde yer almayan çünkü kullanarak bu tür projeleri derlenemiyor `docker build` komut satırından. Bu projeleri derlemek için MSBuild kullanmanız gerekir.

### <a name="msbuild"></a>MSBuild

Bir proje veya çözüm için tek bir docker kapsayıcısı oluşturmak için MSBuild ile kullanabileceğiniz `/t:ContainerBuild` seçeneği komutu.

```cmd
MSBuild <solution_name>.sln /t:ContainerBuild /p:Configuration=Debug
```

İçinde gördükleri için benzer bir çıktı görürsünüz **çıkış** penceresini Visual Studio IDE içinden çözümünüzü oluşturun.

Zaman **hata ayıklama** yapılandırma belirtilirse (ve **ContainerDevelopmentMode** özelliği **hızlı**), Visual Studio kullanan açıklanan derleme iyileştirme Böylece projeniz yerel makinede daha hızlı yapılar ve kapsayıcıya kopyalanır bu makalede.  Zaman **yayın** yapılandırma belirtilirse, yapı kapsayıcıda gerçekleşir ve daha yavaş olabilir.

Bir Docker Compose proje kullanıyorsanız, komutu kullanın:

```
msbuild /t:DockerPackageService /p:DockerAppType=AspNet /p:Configuration=Release <project_name>\<project_name>.csproj
msbuild /p:Configuration=Release docker-compose.dcproj
```

## <a name="scripting-a-containerized-build-using-azure-devops"></a>Azure DevOps kullanarak kapsayıcılı bir yapı komut dosyası

Azure işlem hatları, kapsayıcıya alınmış uygulamalarınızı oluşturun ve Docker Hub veya Azure Container Registry yayınlamak için kullanabilirsiniz. Bu makalede bir Azure işlem hattı ayarlamaya yönelik yönergeleri izleyin: [Derleme, test etme ve Docker kapsayıcı uygulaması anında iletme](/azure/devops/pipelines/languages/docker?view=azure-devops). Ancak, çözümünüzü derlemek için ardışık düzeninize bir MSBuild görevi ekleyin. MSBuild düzenlenmemeli `docker build` kapsayıcılarınızı oluşturulacak.

Bir MSBuild görevi ardışık düzeninize aşağıdaki şekilde ekleyin:

```
- task: MSBuild@1
  displayName: 'Build Application and main Docker Image'
  inputs:
    solution: '**/*.sln'
    msbuildArguments: '/t:ContainerBuild /p:Configuration=$(buildConfiguration)'
```

Daha fazla bilgi için [MSBuild görevi](/azure/devops/pipelines/tasks/build/msbuild?view=azure-devops).

## <a name="next-steps"></a>Sonraki adımlar

Daha fazla proje dosyalarınızı ek MSBuild özellikleri ayarlayarak derlemelerinizi özelleştirmeyi öğrenin. Bkz: [derleme özellikleri kapsayıcı Araçları](container-msbuild-properties.md).

## <a name="see-also"></a>Ayrıca bkz.

[MSBuild](../msbuild/msbuild.md)
[Windows üzerinde Dockerfile](/virtualization/windowscontainers/manage-docker/manage-windows-dockerfile)
[Windows üzerinde Linux kapsayıcıları](/virtualization/windowscontainers/deploy-containers/linux-containers)
