---
title: ASP.NET Core Docker için Visual Studio Araçları
author: ghogen
description: Visual Studio 2019 araçları 'nı ve Docker for Windows kullanmayı öğrenin
ms.author: ghogen
ms.date: 02/01/2019
ms.prod: visual-studio-dev16
ms.technology: vs-azure
ms.topic: include
ms.openlocfilehash: 124f60a4a632115625524b4e30ab28f795d41660
ms.sourcegitcommit: 44e9b1d9230fcbbd081ee81be9d4be8a485d8502
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/30/2019
ms.locfileid: "70197194"
---
Visual Studio ile Kapsayıcılı ASP.NET Core uygulamaları kolayca oluşturabilir, ayıklayabilir ve çalıştırabilir ve bunları Azure Container Registry (ACR), Docker Hub, Azure App Service veya kendi kapsayıcı kayıt defterinizde yayımlayabilirsiniz. Bu makalede ACR 'ye yayımlanacak.

## <a name="prerequisites"></a>Önkoşullar

* [Docker Masaüstü](https://hub.docker.com/editions/community/docker-ce-desktop-windows)
* **Web geliştirme**, **Azure Araçları** iş yükü ve/veya **.NET Core platformlar arası geliştirme** iş yükü yüklü olan [Visual Studio 2019](https://visualstudio.microsoft.com/downloads)
* .NET Core 2,2 ile geliştirme için [.net core 2,2 geliştirme araçları](https://dotnet.microsoft.com/download/dotnet-core/2.2)
* Bir Azure aboneliği Azure Container Registry yayımlamak için. [Ücretsiz deneme için kaydolun](https://azure.microsoft.com/offers/ms-azr-0044p/).

## <a name="installation-and-setup"></a>Yükleme ve kurulum

Docker yüklemesi için, önce Windows için Docker [Desktop 'taki bilgileri gözden geçirin: ' İ yüklemeden önce](https://docs.docker.com/docker-for-windows/install/#what-to-know-before-you-install)bilmeniz gerekenler. Sonra [Docker Desktop](https://hub.docker.com/editions/community/docker-ce-desktop-windows)'ı yükler.

## <a name="add-a-project-to-a-docker-container"></a>Docker kapsayıcısına proje ekleme

1. **ASP.NET Core Web uygulaması** şablonunu kullanarak yeni bir proje oluşturun.
1. **Web uygulaması**' nı seçin ve **Docker desteğini etkinleştir** onay kutusunun seçili olduğundan emin olun.

   ![Docker desteğini etkinleştir onay kutusu](../../media/container-tools/vs-2019/create-new-web-application.PNG)

1. İstediğiniz kapsayıcı türünü (Windows veya Linux) seçin ve **Oluştur**' a tıklayın.

## <a name="dockerfile-overview"></a>Dockerfile genel bakış

Bir *Dockerfile*, son bir Docker görüntüsü oluşturmaya yönelik tarif, projede oluşturulur. İçindeki komutları anlamak için [Dockerfile başvurusuna](https://docs.docker.com/engine/reference/builder/) bakın.

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

Yukarıdaki *Dockerfile* , [Microsoft/aspnetcore](https://hub.docker.com/r/microsoft/aspnetcore/) görüntüsünü temel alır ve projenizi oluşturup kapsayıcıya ekleyerek temel görüntüyü değiştirmeye yönelik yönergeler içerir.

Yeni proje iletişim kutusunun **https Için Yapılandır** onay kutusu Işaretlendiğinde, *dockerfile* iki bağlantı noktasını kullanıma sunar. HTTP trafiği için bir bağlantı noktası kullanılır; diğer bağlantı noktası HTTPS için kullanılır. Onay kutusu işaretli değilse, HTTP trafiği için tek bir bağlantı noktası (80) gösterilir.

## <a name="debug"></a>Hata ayıklama

Araç çubuğundaki hata ayıklama açılır listesinden **Docker** ' ı seçin ve uygulamada hata ayıklamayı başlatın. Bir sertifikaya güvenmek üzere bir istem içeren bir ileti görebilirsiniz. devam etmek için sertifikaya güvenmeyi seçin.

**Çıkış** penceresinde **kapsayıcı araçları** seçeneği hangi eylemlerin gerçekleştireceğinizi gösterir.

Menü **araçları**> NuGet Paket Yöneticisi, **Paket Yöneticisi konsolu**' ndan **Paket Yöneticisi konsolu 'nu** (PMC) açın.

Uygulamanın elde edilen Docker görüntüsü *dev*olarak etiketlendi. Görüntü, *Microsoft/DotNet* temel görüntüsünün *2,2-aspnetcore-Runtime* etiketine dayalıdır. Komutunu Paket Yöneticisi Konsolu (PMC) penceresinde çalıştırın. `docker images` Makinedeki görüntüler görüntülenir:

```console
REPOSITORY        TAG                     IMAGE ID      CREATED         SIZE
hellodockertools  dev                     d72ce0f1dfe7  30 seconds ago  255MB
microsoft/dotnet  2.2-aspnetcore-runtime  fcc3887985bb  6 days ago      255MB
```

> [!NOTE]
> **Geliştirme** görüntüsü, uygulama ikililerini ve diğer içerikleri Içermez. **hata ayıklama** yapılandırmalarında, yinelemeli düzenleme ve hata ayıklama deneyimi sağlamak için birim bağlama kullanılır. Tüm içerikleri içeren bir üretim görüntüsü oluşturmak için **yayın** yapılandırmasını kullanın.

`docker ps` Komutu PMC 'de çalıştırın. Uygulamanın, kapsayıcıyı kullanarak çalıştığını unutmayın:

```console
CONTAINER ID        IMAGE                  COMMAND               CREATED             STATUS              PORTS                                           NAMES
cf5d2ef5f19a        hellodockertools:dev   "tail -f /dev/null"   2 minutes ago       Up 2 minutes        0.0.0.0:52036->80/tcp, 0.0.0.0:44342->443/tcp   priceless_cartwright
```

## <a name="publish-docker-images"></a>Docker görüntülerini yayımlama

Uygulamanın geliştirme ve hata ayıklama döngüsünü tamamladıktan sonra uygulamanın üretim görüntüsünü oluşturabilirsiniz.

1. Yapılandırma açılır öğesini değiştirerek uygulamayı **serbest bırakın** ve oluşturun.
1. **Çözüm Gezgini** ' de projenize sağ tıklayın ve **Yayımla**' yı seçin.
1. Hedefi Yayımla iletişim kutusunda **Container Registry** sekmesini seçin.
1. **Yeni Azure Container Registry oluştur** ' u seçin ve **Yayımla**' ya tıklayın.
1. **Yeni Azure Container Registry oluştur ' a**istediğiniz değerleri girin.

    | Ayar      | Önerilen değer  | Açıklama                                |
    | ------------ |  ------- | -------------------------------------------------- |
    | **DNS ön eki** | Genel olarak benzersiz bir ad | Kapsayıcı kayıt defterinizi benzersiz bir şekilde tanımlayan ad. |
    | **Abonelik** | Aboneliğinizi seçin | Kullanılacak Azure aboneliği. |
    | **[Kaynak grubu](/azure/azure-resource-manager/resource-group-overview)** | myResourceGroup |  Kapsayıcı kayıt defterinizin oluşturulacağı kaynak grubunun adı. Yeni bir kaynak grubu oluşturmak için **Yeni** ' yi seçin.|
    | **[ISTEYIN](https://docs.microsoft.com/azure/container-registry/container-registry-skus)** | Standart | Kapsayıcı kayıt defterinin hizmet katmanı  |
    | **Kayıt defteri konumu** | Size yakın bir konum | Size yakın bir [bölgede](https://azure.microsoft.com/regions/) veya kapsayıcı kayıt defterinizi kullanacak diğer hizmetlerin yakınında bir konum seçin. |

    ![Visual Studio 'nun Azure Container Registry oluştur iletişim kutusu][0]

1. **Oluştur**'a tıklayın.

   ![Başarılı yayımlamayı gösteren ekran görüntüsü](../../media/container-tools/publish-succeeded.png)

## <a name="next-steps"></a>Sonraki Adımlar

Artık kapsayıcıyı, kayıt defterinden Docker görüntülerini çalıştırabilen herhangi bir konağa çekebilirsiniz, örneğin [Azure Container Instances](/azure/container-instances/container-instances-tutorial-deploy-app).

[0]:../../media/hosting-web-apps-in-docker/vs-acr-provisioning-dialog-2019.png
