---
title: Mac için Visual Studio Docker kullanmaya başlama
description: Mac için Visual Studio'da projelerinize Docker eklemeyi öğrenin
author: bytesguy
ms.author: adhartle
ms.date: 06/17/2019
ms.openlocfilehash: 8760bd048e23675c72fb7635587ca1c522b14259
ms.sourcegitcommit: fd5a5b057df3d733f5224c305096907989811f85
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/18/2019
ms.locfileid: "67196413"
---
# <a name="get-started-with-docker-in-visual-studio-for-mac"></a>Mac için Visual Studio Docker kullanmaya başlama

Mac için Visual Studio ile kolayca oluşturun, hata ayıklama ve kapsayıcılı ASP.NET Core uygulamaları çalıştırma ve bunları Azure'a yayımlayın.

## <a name="prerequisites"></a>Önkoşullar

* [Docker Masaüstü](https://hub.docker.com/editions/community/docker-ce-desktop-mac)
* [2019 Mac için Visual Studio](https://visualstudio.microsoft.com/vs/mac)

## <a name="installation-and-setup"></a>Yükleme ve Kurulum

Docker yükleme için gözden geçirin ve bilgileri izleyin [Mac için Docker Masaüstü yükleme](https://docs.docker.com/docker-for-mac/install/).

## <a name="creating-an-aspnet-core-web-application-and-adding-docker-support"></a>Bir ASP.NET Core Web uygulaması oluşturma ve Docker desteği ekleme

1. Giderek yeni bir çözüm oluşturmak **Dosya > Yeni Çözüm**.
1. Altında **.NET Core > Uygulama** seçin **Web uygulaması** şablonu: ![Yeni bir ASP.NET uygulaması oluşturma](media/docker-quickstart-1.png)
1. Hedef Framework'ü seçin. Bu örnekte, .NET Core 2.2 kullanacağız: ![Hedef Framework'ü ayarlama](media/docker-quickstart-2.png)
1. Proje adı gibi ayrıntıları girin (_DockerDemo_ Bu örnekte). Oluşturulan projeyi derlemek ve bir ASP.NET Core web sitesini çalıştırmak için gereken tüm temel öğeleri içerir.
1. Çözüm panelinde DockerDemo projeyi sağ tıklatın ve seçin **Ekle > Docker desteği Ekle**: ![Docker desteği Ekle](media/docker-quickstart-3.png)

Mac için Visual Studio otomatik olarak olarak adlandırılan çözümünüze yeni bir proje ekleyecek **docker-compose** ve ekleme bir **Dockerfile** mevcut projenize.

![Oluşturulan docker destek dosyaları](media/docker-quickstart-4.png)

## <a name="dockerfile-overview"></a>Dockerfile genel bakış

Bir Dockerfile, son bir Docker görüntüsü oluşturmak için tarif olur. Başvurmak [Dockerfile başvurusunu](https://docs.docker.com/engine/reference/builder/) içindeki komutları anlaşılması için.

```
FROM microsoft/dotnet:2.2-aspnetcore-runtime AS base
WORKDIR /app
EXPOSE 80

FROM microsoft/dotnet:2.2-sdk AS build
WORKDIR /src
COPY DockerDemo/DockerDemo.csproj DockerDemo/
RUN dotnet restore DockerDemo/DockerDemo.csproj
COPY . .
WORKDIR /src/DockerDemo
RUN dotnet build DockerDemo.csproj -c Release -o /app

FROM build AS publish
RUN dotnet publish DockerDemo.csproj -c Release -o /app

FROM base AS final
WORKDIR /app
COPY --from=publish /app .
ENTRYPOINT ["dotnet", "DockerDemo.dll"]
```

Önceki *Dockerfile* dayanır [microsoft/aspnetcore](https://hub.docker.com/r/microsoft/aspnetcore/) görüntü ve projenizi oluşturma ve kapsayıcıya ekleyerek temel görüntü değiştirmek için yönergeler içerir.

> [!NOTE]
> Mac için Visual Studio tarafından oluşturulan Dockerfile varsayılan HTTP trafiği için 80 numaralı bağlantı noktasına kullanıma sunar. HTTPS trafiğini etkinleştirmek için ekleme `Expose 443` dockerfile.

## <a name="debugging"></a>Hata Ayıklama

Seçin `docker-compose` projesini başlangıç projesi olarak ve hata ayıklamayı Başlat (**çalıştırın > hata ayıklamayı Başlat**). Bu yapı, dağıtır ve bir kapsayıcıdaki ASP.NET projesi başlatın.

> [!TIP]
> Docker Desktop yüklendikten sonra ilk çalıştırılmasında, hata ayıklamaya çalışılırken aşağıdaki hata iletisini alabilirsiniz: `Cannot start service dockerdemo: Mounts denied`
> 
> Ekleme `/usr/local/share/dotnet/sdk/NuGetFallbackFolder` Docker Desktop dosya paylaşımı sekmesine:
>
> ![Dosya Paylaşımı için NuGetFallbackFolder klasörü ekleme](media/docker-quickstart-5.png)

Derleme tamamlandığında uygulamayı Safari'ye başlatılır:

![Safari'de çalıştıran varsayılan Docker projesi](media/docker-quickstart-6.png)

Kapsayıcı bir bağlantı noktasında dinleme Not `http://localhost:32768` için örnek ve bu bağlantı noktası farklı olabilir.

Çalışan kapsayıcılar listesi görmek için `docker ps` terminalde komutu.

Aşağıdaki ekran görüntüsünde gösterilen bağlantı noktası geçişi unutmayın (altında **bağlantı noktaları**). Bu, kapsayıcı üstünde Safari ve bağlantı noktası 80 (Dockerfile içinde tanımlandığı şekilde) üzerinde iç Web sunucusu istekleri geçişini gördüğümüz bağlantı noktasını dinleyen olduğunu gösterir. Uygulamanın perspektifinden, 80 numaralı bağlantı noktasında dinliyor:

![Docker kapsayıcı listesi](media/docker-quickstart-7.png)
