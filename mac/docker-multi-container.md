---
title: Öğretici - oluşturmak çok kapsayıcılı Docker ile uygulama oluşturma
description: Mac için Visual Studio'da aralarında iletişim kurmak ve birden fazla kapsayıcı yönetme hakkında bilgi edinin
author: asb3993
ms.author: amburns
ms.date: 06/17/2019
ms.openlocfilehash: 7570788b50a83d9a74657408d4f38fbce21bd1c3
ms.sourcegitcommit: 7fbfb2a1d43ce72545096c635df2b04496b0be71
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/09/2019
ms.locfileid: "67691715"
---
# <a name="create-a-multi-container-app-with-docker-compose"></a>Oluşturmak çok kapsayıcılı Docker ile uygulama oluşturma

Bu öğreticide, birden fazla kapsayıcı yönetme ve aralarında Mac için Visual Studio kullanarak Docker Compose iletişim hakkında bilgi edineceksiniz

## <a name="prerequisites"></a>Önkoşullar

* [Docker Masaüstü](https://hub.docker.com/editions/community/docker-ce-desktop-mac)
* [2019 Mac için Visual Studio](https://visualstudio.microsoft.com/vs/mac)

## <a name="create-an-aspnet-core-web-application-and-add-docker-support"></a>Bir ASP.NET Core Web uygulaması oluşturma ve Docker desteği Ekle

1. Giderek yeni bir çözüm oluşturmak **Dosya > Yeni Çözüm**.
1. Altında **.NET Core > Uygulama** seçin **Web uygulaması** şablonu: ![Yeni bir ASP.NET uygulaması oluşturma](media/docker-quickstart-1.png)
1. Hedef Framework'ü seçin. Bu örnekte, .NET Core 2.2 kullanacağız: ![Hedef Framework'ü ayarlama](media/docker-quickstart-2.png)
1. Proje Ayrıntıları gibi proje adı girin (_DockerDemoFrontEnd_ Bu örnekte) ve çözüm adı (_DockerDemo_). Oluşturulan projeyi derlemek ve bir ASP.NET Core web sitesini çalıştırmak için gereken tüm temel öğeleri içerir.
1. Çözüm panelinde DockerDemoFrontEnd projeyi sağ tıklatın ve seçin **Ekle > Docker desteği Ekle**: ![Docker desteği Ekle](media/docker-quickstart-3.png)

Mac için Visual Studio otomatik olarak olarak adlandırılan çözümünüze yeni bir proje ekleyecek **docker-compose** ve ekleme bir **Dockerfile** mevcut projenize.

## <a name="create-an-aspnet-core-web-api-and-add-docker-support"></a>Bir ASP.NET Core Web API'si oluşturma ve Docker desteği Ekle

Bizim arka uç API olarak hareket edecek, ikinci bir proje sonraki oluşturacağız. **.NET Core API** kurmamızı RESTful isteklerini işlemek bir denetleyici şablonu içerir.

1. Çözüme sağ tıklayıp seçerek mevcut çözüme yeni bir proje eklemek **Ekle > Yeni Proje Ekle**.
1. Altında **.NET Core > Uygulama** seçin **API** şablonu.
1. Hedef Framework'ü seçin. Bu örnekte, .NET Core 2.2 kullanacağız
1. Proje Ayrıntıları gibi proje adı girin (_DockerDemoAPI_ Bu örnekte).
1. Oluşturulduktan sonra çözüm bölmesi için Git ve DockerDemoAPI projeyi sağ tıklatın ve seçin **Ekle > Docker desteği Ekle**.

**Docker-compose.yml** dosyası **docker-compose** proje otomatik olarak güncelleştirilecek var olan Web uygulaması projesi yanı sıra API projesini dahil et. Ne zaman biz derleme ve çalıştırma **docker-compose** proje, bu projelerin her biri için ayrı bir Docker kapsayıcısı dağıtılacak.

```
version: '3.4'

services:
  dockerdemofrontend:
    image: ${DOCKER_REGISTRY-}dockerdemofrontend
    build:
      context: .
      dockerfile: DockerDemoFrontEnd/Dockerfile

  dockerdemoapi:
    image: ${DOCKER_REGISTRY-}dockerdemoapi
    build:
      context: .
      dockerfile: DockerDemoAPI/Dockerfile
```

## <a name="integrate-the-two-containers"></a>İki kapsayıcı tümleştirin

Bizim çözümde şimdi iki ASP.NET projeleri vardır ve her ikisi de yapılandırılır Docker desteği. Bazı kod eklemek için ihtiyacımız olan sonraki!

1. İçinde `DockerDemoFrontEnd` projesini açarsanız *Index.cshtml.cs* dosyasını bulun ve değiştirin `OnGet` yöntemini aşağıdaki kod ile:

   ```csharp
    public async Task OnGet()
    {
       ViewData["Message"] = "Hello from webfrontend";

       using (var client = new System.Net.Http.HttpClient())
       {
          // Call *mywebapi*, and display its response in the page
          var request = new System.Net.Http.HttpRequestMessage();
          request.RequestUri = new Uri("http://dockerdemoapi/api/values/1");
          var response = await client.SendAsync(request);
          ViewData["Message"] += " and " + await response.Content.ReadAsStringAsync();
       }
    }
   ```

1. İçinde *Index.cshtml* görüntülemek için bir satır ekleyin `ViewData["Message"]` böylece dosyanın şu kod gibi görünür:

      ```cshtml
      @page
      @model IndexModel
      @{
          ViewData["Title"] = "Home page";
      }

      <div class="text-center">
          <h1 class="display-4">Welcome</h1>
          <p>Learn about <a href="https://docs.microsoft.com/aspnet/core">building Web apps with ASP.NET Core</a>.</p>
          <p>@ViewData["Message"]</p>
      </div>
      ```

1. Şimdi Web API projesinde, kod, eklediğiniz arama API'si tarafından döndürülen iletisini özelleştirmek için değerleri denetleyici ekleyin *webfrontend*:

      ```csharp
        // GET api/values/5
        [HttpGet("{id}")]
        public ActionResult<string> Get(int id)
        {
            return "webapi (with value " + id + ")";
        }
      ```

1. Ayarlama `docker-compose` projesini başlangıç projesi olarak ve Git **çalıştırın > hata ayıklamayı Başlat**. Her şeyin doğru şekilde yapılandırıldıysa, "Hello webfrontend ve webapı (1 değeriyle)." iletisini görürsünüz:

![Çalışan docker çoklu kapsayıcı çözümü](media/docker-multicontainer-debug.png)
