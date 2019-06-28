---
title: ASP.NET Core ile Visual Studio kapsayıcı araçları
author: ghogen
description: Visual Studio kapsayıcı araçları ve Docker için Windows kullanmayı öğrenin
ms.author: ghogen
ms.date: 06/06/2019
ms.technology: vs-azure
ms.topic: quickstart
ms.openlocfilehash: 09209393ea32b4eb9b86a8c0c4263103ee5de344
ms.sourcegitcommit: 0cd282a7584b9bfd4df7882f8fdf3ad8a270e219
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/28/2019
ms.locfileid: "67465097"
---
# <a name="quickstart-use-docker-with-a-react-single-page-app-in-visual-studio"></a>Hızlı Başlangıç: Visual Studio'da React tek sayfalı uygulama ile Docker'ı kullanma

Visual Studio ile kolayca oluşturun, hata ayıklama ve kapsayıcılı ASP.NET Core uygulamaları React.js tek sayfalı uygulama gibi istemci tarafı JavaScript olanlar da dahil olmak üzere, çalıştırabilir ve Azure Container Registry (ACR), Docker Hub, Azure App Service, yayımlarsınız veya kendi kapsayıcı kayıt defteri. Bu makalede, biz ACR'ye yayınlayacaksınız.

## <a name="prerequisites"></a>Önkoşullar

::: moniker range="vs-2017"
* [Docker Masaüstü](https://hub.docker.com/editions/community/docker-ce-desktop-windows)
* [Visual Studio 2017](https://visualstudio.microsoft.com/vs/older-downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=vs+2017+download) ile **Web geliştirme**, **Azure Araçları** iş yükünü ve/veya **.NET Core çoklu platform geliştirme** iş yükü yüklenmiş
* Azure Container Registry, Azure aboneliğinin yayınlamak için. [Ücretsiz deneme için kaydolun](https://azure.microsoft.com/offers/ms-azr-0044p/).
::: moniker-end
::: moniker range=">=vs-2019"
* [Docker Masaüstü](https://hub.docker.com/editions/community/docker-ce-desktop-windows)
* [Visual Studio 2019](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2019) ile **Web geliştirme**, **Azure Araçları** iş yükünü ve/veya **.NET Core çoklu platform geliştirme** iş yükü yüklenmiş
* [.NET core 2.2 geliştirme araçları](https://dotnet.microsoft.com/download/dotnet-core/2.2) geliştirme ile .NET Core 2.2
* Azure Container Registry, Azure aboneliğinin yayınlamak için. [Ücretsiz deneme için kaydolun](https://azure.microsoft.com/offers/ms-azr-0044p/).
::: moniker-end

## <a name="installation-and-setup"></a>Yükleme ve Kurulum

Docker yükleme için bölümündeki bilgileri gözden geçirin [için Docker Masaüstü Windows: Yüklemeden önce bilinmesi gerekenler](https://docs.docker.com/docker-for-windows/install/#what-to-know-before-you-install). Ardından, yükleme [Docker Masaüstü](https://hub.docker.com/editions/community/docker-ce-desktop-windows).

## <a name="create-a-project-and-add-docker-support"></a>Proje oluşturma ve Docker desteği Ekle

::: moniker range="vs-2017"
1. Kullanarak yeni bir proje oluşturma **ASP.NET Core Web uygulaması** şablonu.
1. Seçin **React.js**. Seçemezsiniz **Docker desteği etkinleştirme**, ancak endişelenmeyin, projeyi oluşturduktan sonra destek ekleyebilirsiniz.

   ![Yeni React.js projesinin ekran görüntüsü](media/container-tools-react/vs2017/new-react-project.png)

1. Proje düğümünü sağ tıklatın ve seçin **Ekle** > **Docker desteği** bir Dockerfile projenize eklenecek.

   ![Docker desteği Ekle](media/container-tools-react/vs2017/add-docker-support.png)

1. Linux kapsayıcı türü seçin ve tıklayın **Tamam**.
::: moniker-end
::: moniker range=">=vs-2019"
1. Kullanarak yeni bir proje oluşturma **ASP.NET Core Web uygulaması** şablonu.
1. Seçin **React.js**, tıklatıp **Oluştur**. Seçemezsiniz **Docker desteği etkinleştirme**, ancak endişelenmeyin, bu destek daha sonra ekleyebilirsiniz.

   ![Yeni React.js projesinin ekran görüntüsü](media/container-tools-react/vs2019/new-react-project.png)

1. Proje düğümünü sağ tıklatın ve seçin **Ekle** > **Docker desteği** bir Dockerfile projenize eklenecek.

   ![Docker desteği Ekle](media/container-tools-react/vs2017/add-docker-support.png)

1. Linux kapsayıcı türü olarak'ni seçin.
::: moniker-end

## <a name="dockerfile-overview"></a>Dockerfile genel bakış

A *Dockerfile*, son bir Docker görüntüsü oluşturmak için tarif projede oluşturulur. Başvurmak [Dockerfile başvurusunu](https://docs.docker.com/engine/reference/builder/) içindeki komutları anlaşılması için.

Açık *Dockerfile* projesinde ve node.js'yi yüklemek için aşağıdaki satırları ekleyin kapsayıcıdaki 10.x. Bu satırlar, Node package manager yüklemesini eklemek için ilk bölümünde eklediğinizden emin olun *npm.exe* temel görüntüye sonraki adımlarda kullanılır.

```
RUN curl -sL https://deb.nodesource.com/setup_10.x |  bash -
RUN apt-get install -y nodejs
```

*Dockerfile* şunun gibi görünmelidir:

```
FROM microsoft/dotnet:2.2-aspnetcore-runtime-stretch-slim AS base
WORKDIR /app
EXPOSE 80 
EXPOSE 443
RUN curl -sL https://deb.nodesource.com/setup_10.x |  bash -
RUN apt-get install -y nodejs

FROM microsoft/dotnet:2.2-sdk-stretch AS build
WORKDIR /src
COPY ["WebApplication37/WebApplication37.csproj", "WebApplication37/"]
RUN dotnet restore "WebApplication37/WebApplication37.csproj"
COPY . .
WORKDIR "/src/WebApplication37"
RUN dotnet build "WebApplication37.csproj" -c Release -o /app

FROM build AS publish
RUN dotnet publish "WebApplication37.csproj" -c Release -o /app

FROM base AS final
WORKDIR /app
COPY --from=publish /app .
ENTRYPOINT ["dotnet", "WebApplication37.dll"]
```

Önceki *Dockerfile* dayanır [microsoft/aspnetcore](https://hub.docker.com/r/microsoft/aspnetcore/) görüntü ve projenizi oluşturma ve kapsayıcıya ekleyerek temel görüntü değiştirmek için yönergeler içerir.

Yeni Proje iletişim kutusunun **HTTPS için Yapılandır** onay kutusunu işaretli *Dockerfile* iki bağlantı noktalarını kullanıma sunar. Bir bağlantı noktası, HTTP trafiği için kullanılır. diğer bağlantı noktasını, HTTPS için kullanılır. Onay kutusu işaretli değilse, HTTP trafiği için tek bir bağlantı noktası (80) sunulur.

## <a name="debug"></a>Hata ayıklama

Seçin **Docker** gelen hata ayıklama açılır araç ve uygulama hata ayıklamayı başlatın. Bir sertifikaya güvenme hakkında bir istem içeren bir ileti görebilirsiniz; devam etmek için bu sertifikaya güvenmek seçin.

**Kapsayıcı Araçları** seçeneğini **çıkış** penceresi, hangi eylemlerin gerçekleşen gösterir. İle ilişkili yükleme adımlarını görmelisiniz *npm.exe*.

Tarayıcıda uygulama giriş sayfası gösterilir.

::: moniker range="vs-2017"
   ![Uygulama çalışan işleminin ekran görüntüsü](media/container-tools-react/vs2017/running-app.png)
::: moniker-end
::: moniker range=">=vs-2019"
   ![Uygulama çalışan işleminin ekran görüntüsü](media/container-tools-react/vs2019/running-app.png)
::: moniker-end

Gezinme deneyin *sayacı* sayfasında ve istemci tarafı kod sayacı tıklayarak test **artışı** düğmesi.

Açık **Paket Yöneticisi Konsolu** (PMC) menüsünde **Araçları**> NuGet Paket Yöneticisi **Paket Yöneticisi Konsolu**.

Uygulamasının elde edilen Docker görüntüsü olarak etiketlenmiş *geliştirme*. Görüntü dayanır *aspnetcore-2.2-çalışma zamanı* etiketi *microsoft/dotnet* temel görüntü. Çalıştırma `docker images` komutunu **Paket Yöneticisi Konsolu** (PMC) penceresi. Makine görüntülerinde görüntülenir:

```console
REPOSITORY        TAG                     IMAGE ID      CREATED         SIZE
webapplication37  dev                     d72ce0f1dfe7  30 seconds ago  255MB
microsoft/dotnet  2.2-aspnetcore-runtime  fcc3887985bb  6 days ago      255MB
```

> [!NOTE]
> **Geliştirme** görüntü içermiyor uygulama ikili dosyalarını ve diğer içerik olarak **hata ayıklama** yapılandırmaları yinelemeli düzenleme ve hata ayıklama deneyimi sağlamak için birim bağlama kullanın. Tüm içeriği içeren bir üretim görüntüsü oluşturmak için kullanmak **yayın** yapılandırma.

Çalıştırma `docker ps` PMC komutunu. Uygulamayı kullanarak kapsayıcı çalıştırma dikkat edin:

```console
CONTAINER ID        IMAGE                  COMMAND               CREATED             STATUS              PORTS                                           NAMES
cf5d2ef5f19a        webapplication37:dev   "tail -f /dev/null"   2 minutes ago       Up 2 minutes        0.0.0.0:52036->80/tcp, 0.0.0.0:44342->443/tcp   priceless_cartwright
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

1. **Oluştur**'u tıklatın.

   ![Yayımlama başarılı gösteren ekran görüntüsü](media/container-tools/publish-succeeded.png)

## <a name="next-steps"></a>Sonraki adımlar

Artık kapsayıcı kayıt defterinden herhangi bir konağa Docker görüntüleri, örneğin çalıştırma yeteneğine çekebilirsiniz [Azure Container Instances](/azure/container-instances/container-instances-tutorial-deploy-app).

## <a name="additional-resources"></a>Ek kaynaklar

* [Visual Studio ile kapsayıcı geliştirme](/visualstudio/containers)
* [Visual Studio geliştirme Docker ile ilgili sorunları giderme](troubleshooting-docker-errors.md)
* [Visual Studio kapsayıcı araçları GitHub deposu](https://github.com/Microsoft/DockerTools)

::: moniker range="vs-2017"
[0]:media/hosting-web-apps-in-docker/vs-acr-provisioning-dialog.png
::: moniker-end
::: moniker range=">=vs-2019"
[0]:media/hosting-web-apps-in-docker/vs-acr-provisioning-dialog-2019.png
::: moniker-end