---
title: ASP.NET Core ile Docker için Visual Studio Araçları
author: ghogen
description: Visual Studio 2017 araçları ve Docker için Windows kullanmayı öğrenin
ms.author: ghogen
ms.date: 02/01/2019
ms.prod: visual-studio-dev16
ms.technology: vs-azure
ms.topic: include
ms.openlocfilehash: 0d6e61fc4f41284b7ca9a551712542ad1e74af5d
ms.sourcegitcommit: 0f7411c1a47d996907a028e920b73b53c2098c9f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/04/2019
ms.locfileid: "55702040"
---
Visual Studio ile kolayca oluşturun, hata ayıklama ve kapsayıcılı ASP.NET Core uygulamaları çalıştırın ve Azure Container Registry (ACR), Docker Hub, Azure App Service veya kendi kapsayıcı kayıt defteri yayımlarsınız. Bu makalede, biz ACR'ye yayınlayacaksınız.

## <a name="prerequisites"></a>Önkoşullar

* [Docker Masaüstü](https://hub.docker.com/editions/community/docker-ce-desktop-windows)
* [Visual Studio 2019 Önizleme](https://visualstudio.microsoft.com/vs/preview/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2019+preview) ile **Web geliştirme**, **Azure Araçları** iş yükünü ve/veya **.NET Core çoklu platform geliştirme** iş yükü yüklenmiş
* [.NET core 2.2 geliştirme araçları](https://dotnet.microsoft.com/download/dotnet-core/2.2) geliştirme ile .NET Core 2.2
* Azure Container Registry, Azure aboneliğinin yayınlamak için. [Ücretsiz deneme için kaydolun](https://azure.microsoft.com/en-us/offers/ms-azr-0044p/).

## <a name="installation-and-setup"></a>Yükleme ve Kurulum

Docker yükleme için bölümündeki bilgileri gözden geçirin [için Docker Masaüstü Windows: Yüklemeden önce bilinmesi gerekenler](https://docs.docker.com/docker-for-windows/install/#what-to-know-before-you-install). Ardından, yükleme [Docker Masaüstü](https://hub.docker.com/editions/community/docker-ce-desktop-windows).

## <a name="add-a-project-to-a-docker-container"></a>Bir Docker kapsayıcısı için bir proje ekleyin

1. Visual Studio menüden **Dosya > Yeni > Proje**.
1. Altında **şablonları** bölümünü **yeni proje** iletişim kutusunda **Visual C# > Web**.
1. Seçin **ASP.NET Core Web uygulaması**.
1. Uygulamanızı yeni bir ad verin (veya varsayılan olması) seçip **Tamam**.
1. Seçin **Web uygulaması**.
1. Denetleme **Docker desteğini etkinleştir** onay kutusu.

   ![Docker desteği onay kutusunu etkinleştirin](../../media/docker-tools/enable-docker-support.PNG)

1. (Windows veya Linux) istediğiniz kapsayıcı türü seçin **Tamam**.

## <a name="dockerfile-overview"></a>Dockerfile genel bakış

A *Dockerfile*, son bir Docker görüntüsü oluşturmak için tarif projede oluşturulur. Başvurmak [Dockerfile başvurusunu](https://docs.docker.com/engine/reference/builder/) içindeki komutları anlaşılması için.:

```
FROM microsoft/dotnet:2.2-aspnetcore-runtime-stretch-slim AS base
WORKDIR /app
EXPOSE 80
EXPOSE 443

FROM microsoft/dotnet:2.2-sdk-stretch AS build
WORKDIR /src
COPY ["HelloDockerTools/HelloDockerTools.csproj", "HelloDockerTools/"]
RUN dotnet restore "HelloDockerTools/HelloDockerTools.csproj"
COPY . .
WORKDIR "/src/HelloDockerTools"
RUN dotnet build "HelloDockerTools.csproj" -c Release -o /app

FROM build AS publish
RUN dotnet publish "HelloDockerTools.csproj" -c Release -o /app

FROM base AS final
WORKDIR /app
COPY --from=publish /app .
ENTRYPOINT ["dotnet", "HelloDockerTools.dll"]
```

Önceki *Dockerfile* dayanır [microsoft/aspnetcore](https://hub.docker.com/r/microsoft/aspnetcore/) görüntü ve projenizi oluşturma ve kapsayıcıya ekleyerek temel görüntü değiştirmek için yönergeler içerir. 

Yeni Proje iletişim kutusunun **HTTPS için Yapılandır** onay kutusunu işaretli *Dockerfile* iki bağlantı noktalarını kullanıma sunar. Bir bağlantı noktası, HTTP trafiği için kullanılır. diğer bağlantı noktasını, HTTPS için kullanılır. Onay kutusu işaretli değilse, HTTP trafiği için tek bir bağlantı noktası (80) sunulur.

## <a name="debug"></a>Hata ayıklama

Seçin **Docker** gelen hata ayıklama açılır araç ve uygulama hata ayıklamayı başlatın. Bir sertifikaya güvenme hakkında bir istem içeren bir ileti görebilirsiniz; devam etmek için bu sertifikaya güvenmek seçin.

**Kapsayıcı Araçları** seçeneğini **çıkış** penceresi, hangi eylemlerin gerçekleşen gösterir.

Açık **Paket Yöneticisi Konsolu** (PMC) menüsünde **Araçları**> NuGet Paket Yöneticisi **Paket Yöneticisi Konsolu**.

Uygulamasının elde edilen Docker görüntüsü olarak etiketlenmiş *geliştirme*. Görüntü dayanır *aspnetcore-2.2-çalışma zamanı* etiketi *microsoft/dotnet* temel görüntü. Çalıştırma `docker images` komutunu **Paket Yöneticisi Konsolu** (PMC) penceresi. Makine görüntülerinde görüntülenir:

```console
REPOSITORY        TAG                     IMAGE ID      CREATED         SIZE
hellodockertools  dev                     d72ce0f1dfe7  30 seconds ago  255MB
microsoft/dotnet  2.2-aspnetcore-runtime  fcc3887985bb  6 days ago      255MB
```

> [!NOTE]
> **Geliştirme** görüntü içermiyor uygulama ikili dosyalarını ve diğer içerik olarak **hata ayıklama** yapılandırmaları yinelemeli düzenleme ve hata ayıklama deneyimi sağlamak için birim bağlama kullanın. Tüm içeriği içeren bir üretim görüntüsü oluşturmak için kullanmak **yayın** yapılandırma.

Çalıştırma `docker ps` PMC komutunu. Uygulamayı kullanarak kapsayıcı çalıştırma dikkat edin:

```console
CONTAINER ID        IMAGE                  COMMAND               CREATED             STATUS              PORTS                                           NAMES
cf5d2ef5f19a        hellodockertools:dev   "tail -f /dev/null"   2 minutes ago       Up 2 minutes        0.0.0.0:52036->80/tcp, 0.0.0.0:44342->443/tcp   priceless_cartwright
```

## <a name="publish-docker-images"></a>Docker görüntülerini yayımlama

Uygulama geliştirme ve hata ayıklama döngüsünü tamamlandıktan sonra uygulamayı bir üretim görüntüsünü oluşturabilirsiniz.

1. Aşağı açılan yapılandırmasını değiştirmek **yayın** ve bir uygulama geliştirin. 
1. Projenize sağ tıklayın **Çözüm Gezgini** ve **Yayımla**.
1. Yayımlama hedefi iletişim kutusunda seçin **kapsayıcı kayıt defteri** sekmesi.
1. Seçin **yeni Azure Container Registry oluşturma** tıklatıp **Yayımla**.
1. İstenen değerleri doldurun **yeni bir Azure Container Registry oluşturma**.

    | Ayar      | Önerilen değer  | Açıklama                                |
    | ------------ |  ------- | -------------------------------------------------- |
    | **DNS ön eki** | Genel olarak benzersiz bir ad | Kapsayıcı kayıt defterinizde benzersiz olarak tanımlayan ad. |
    | **Abonelik** | Aboneliğinizi seçin | Kullanılacak Azure aboneliği. |
    | **[Kaynak grubu](/azure/azure-resource-manager/resource-group-overview)** | myResourceGroup |  Kapsayıcı kayıt defterinizde oluşturulacağı kaynak grubunun adı. Seçin **yeni** yeni bir kaynak grubu oluşturmak için.|
    | **[SKU](https://docs.microsoft.com/azure/container-registry/container-registry-skus)** | Standart | Hizmet katmanı kapsayıcı kayıt defterinin  |
    | **Kayıt defteri konumu** | Size yakın bir konum | Bir konumdan seçin bir [bölge](https://azure.microsoft.com/regions/) yakınınızdaki veya kapsayıcı kayıt defterinizi kullanacak diğer hizmetlere yakın. |

    ![Visual Studio'nun iletişim Azure Container Registry oluşturma][0]

1. **Oluştur**'a tıklayın.

   ![Yayımlama başarılı gösteren ekran görüntüsü](../../media/docker-tools/publish-succeeded.png)

## <a name="next-steps"></a>Sonraki Adımlar

Artık kapsayıcı kayıt defterinden herhangi bir konağa Docker görüntüleri, örneğin çalıştırma yeteneğine çekebilirsiniz [Azure Container Instances](/azure/container-instances/container-instances-tutorial-deploy-app).

## <a name="additional-resources"></a>Ek kaynaklar

* [Visual Studio ile kapsayıcı geliştirme](/visualstudio/containers)
* [Visual Studio 2017 geliştirme Docker ile ilgili sorunları giderme](../../vs-azure-tools-docker-troubleshooting-docker-errors.md)
* [Docker GitHub deposu için Visual Studio Araçları](https://github.com/Microsoft/DockerTools)

[0]:../../media/vs-azure-tools-docker-hosting-web-apps-in-docker/vs-acr-provisioning-dialog-2019.png
