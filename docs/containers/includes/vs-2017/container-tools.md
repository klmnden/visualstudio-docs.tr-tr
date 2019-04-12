---
title: ASP.NET Core ile Visual Studio kapsayıcı araçları
author: ghogen
description: Visual Studio 2017 araçları ve Docker için Windows kullanmayı öğrenin
ms.author: ghogen
ms.date: 02/01/2019
ms.technology: vs-azure
ms.topic: include
ms.openlocfilehash: 5f309813c64bdb8009623847ca66721c63e7ba91
ms.sourcegitcommit: cd91a8a4f6086cda9ba6948be25864fc7d6b8e44
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/12/2019
ms.locfileid: "59537957"
---
Visual Studio ile kolayca oluşturun, hata ayıklama ve kapsayıcılı ASP.NET Core uygulamaları çalıştırın ve Azure Container Registry (ACR), Docker Hub, Azure App Service veya kendi kapsayıcı kayıt defteri yayımlarsınız. Bu makalede, biz ACR'ye yayınlayacaksınız.

## <a name="prerequisites"></a>Önkoşullar

* [Docker Masaüstü](https://hub.docker.com/editions/community/docker-ce-desktop-windows)
* [Visual Studio 2017](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2017) ile **Web geliştirme**, **Azure Araçları** iş yükünü ve/veya **.NET Core çoklu platform geliştirme** iş yükü yüklenmiş
* Azure Container Registry, Azure aboneliğinin yayınlamak için. [Ücretsiz deneme için kaydolun](https://azure.microsoft.com/offers/ms-azr-0044p/).

## <a name="installation-and-setup"></a>Yükleme ve Kurulum

Docker yükleme için bölümündeki bilgileri gözden geçirin [için Docker Masaüstü Windows: Yüklemeden önce bilinmesi gerekenler](https://docs.docker.com/docker-for-windows/install/#what-to-know-before-you-install). Ardından, yükleme [Docker Masaüstü](https://hub.docker.com/editions/community/docker-ce-desktop-windows).

## <a name="add-a-project-to-a-docker-container"></a>Bir Docker kapsayıcısı için bir proje ekleyin

1. Visual Studio menüden **Dosya > Yeni > Proje**.
1. Altında **şablonları** bölümünü **yeni proje** iletişim kutusunda **Visual C# > Web**.
1. Seçin **ASP.NET Core Web uygulaması**.
1. Uygulamanızı yeni bir ad verin (veya varsayılan olması) seçip **Tamam**.
1. Seçin **Web uygulaması**.
1. Denetleme **Docker desteğini etkinleştir** onay kutusu.

   ![Docker desteği onay kutusunu etkinleştirin](../../media/container-tools/enable-docker-support.PNG)

1. (Windows veya Linux) istediğiniz kapsayıcı türü seçin **Tamam**.

## <a name="dockerfile-overview"></a>Dockerfile genel bakış

A *Dockerfile*, son bir Docker görüntüsü oluşturmak için tarif projede oluşturulur. Başvurmak [Dockerfile başvurusunu](https://docs.docker.com/engine/reference/builder/) içindeki komutları anlaşılması için.:

```
FROM microsoft/dotnet:2.1-aspnetcore-runtime AS base
WORKDIR /app
EXPOSE 59518
EXPOSE 44364

FROM microsoft/dotnet:2.1-sdk AS build
WORKDIR /src
COPY HelloDockerTools/HelloDockerTools.csproj HelloDockerTools/
RUN dotnet restore HelloDockerTools/HelloDockerTools.csproj
COPY . .
WORKDIR /src/HelloDockerTools
RUN dotnet build HelloDockerTools.csproj -c Release -o /app

FROM build AS publish
RUN dotnet publish HelloDockerTools.csproj -c Release -o /app

FROM base AS final
WORKDIR /app
COPY --from=publish /app .
ENTRYPOINT ["dotnet", "HelloDockerTools.dll"]
```

Önceki *Dockerfile* dayanır [microsoft/aspnetcore](https://hub.docker.com/r/microsoft/aspnetcore/) görüntü ve projenizi oluşturma ve kapsayıcıya ekleyerek temel görüntü değiştirmek için yönergeler içerir.

Yeni Proje iletişim kutusunun **HTTPS için Yapılandır** onay kutusunu işaretli *Dockerfile* iki bağlantı noktalarını kullanıma sunar. Bir bağlantı noktası, HTTP trafiği için kullanılır. diğer bağlantı noktasını, HTTPS için kullanılır. Onay kutusu işaretli değilse, HTTP trafiği için tek bir bağlantı noktası (80) sunulur.

## <a name="debug"></a>Hata ayıklama

Seçin **Docker** gelen hata ayıklama açılır araç ve uygulama hata ayıklamayı başlatın. Bir sertifikaya güvenme hakkında bir istem içeren bir ileti görebilirsiniz; devam etmek için bu sertifikaya güvenmek seçin.

**Çıkış** penceresi, hangi eylemlerin gerçekleşen gösterir.

Açık **Paket Yöneticisi Konsolu** (PMC) menüsünde **Araçları**> NuGet Paket Yöneticisi **Paket Yöneticisi Konsolu**.

Uygulamasının elde edilen Docker görüntüsü olarak etiketlenmiş *geliştirme*. Görüntü dayanır *2.1 aspnetcore runtime* etiketi *microsoft/dotnet* temel görüntü. Çalıştırma `docker images` komutunu **Paket Yöneticisi Konsolu** (PMC) penceresi. Makine görüntülerinde görüntülenir:

```console
REPOSITORY        TAG                     IMAGE ID      CREATED         SIZE
hellodockertools  dev                     d72ce0f1dfe7  30 seconds ago  255MB
microsoft/dotnet  2.1-aspnetcore-runtime  fcc3887985bb  6 days ago      255MB
```

> [!NOTE]
> **Geliştirme** görüntü içermiyor uygulama ikili dosyalarını ve diğer içerik olarak **hata ayıklama** yapılandırmaları yinelemeli düzenleme ve hata ayıklama deneyimi sağlamak için birim bağlama kullanın. Tüm içeriği içeren bir üretim görüntüsü oluşturmak için kullanmak **yayın** yapılandırma.

Çalıştırma `docker ps` PMC komutunu. Uygulamayı kullanarak kapsayıcı çalıştırma dikkat edin:

```console
CONTAINER ID        IMAGE                  COMMAND                   CREATED             STATUS              PORTS                   NAMES
baf9a678c88d        hellodockertools:dev   "C:\\remote_debugge..."   21 seconds ago      Up 19 seconds       0.0.0.0:37630->80/tcp   dockercompose4642749010770307127_hellodockertools_1
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

## <a name="next-steps"></a>Sonraki adımlar

Artık kapsayıcı kayıt defterinden herhangi bir konağa Docker görüntüleri, örneğin çalıştırma yeteneğine çekebilirsiniz [Azure Container Instances](/azure/container-instances/container-instances-tutorial-deploy-app).

[0]:../../media/hosting-web-apps-in-docker/vs-acr-provisioning-dialog.png
