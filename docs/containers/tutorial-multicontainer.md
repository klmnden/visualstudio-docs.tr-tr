---
title: Docker Compose ve ASP.NET Core ile Visual Studio kapsayıcı araçları çok kapsayıcılı Öğreticisi
author: ghogen
description: Docker Compose ile birden çok kapsayıcı kullanmayı öğrenin
ms.author: ghogen
ms.date: 02/21/2019
ms.technology: vs-azure
ms.topic: include
ms.openlocfilehash: e6087b5ca7682ce03291b34907e2f6d119110858
ms.sourcegitcommit: cd91a8a4f6086cda9ba6948be25864fc7d6b8e44
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/12/2019
ms.locfileid: "59537552"
---
# <a name="tutorial-create-a-multi-container-app-with-docker-compose"></a>Öğretici: Docker Compose ile çok kapsayıcılı uygulama oluşturma

Bu öğreticide, birden fazla kapsayıcı yönetmek ve bunları Visual Studio kapsayıcı araçları kullanırken arasında iletişim kurmak öğreneceksiniz.  Birden çok kapsayıcı yönetme gerektirir *kapsayıcı düzenleme* ve Docker Compose, Kubernetes veya Service Fabric gibi bir orchestrator gerektirir. Docker Compose burayı kullanacağız. Docker Compose, yerel hata ayıklama ve test sırasında geliştirme döngüsü için harika bir yoldur.

## <a name="prerequisites"></a>Önkoşullar

::: moniker range="vs-2017"
* [Docker Masaüstü](https://hub.docker.com/editions/community/docker-ce-desktop-windows)
* [Visual Studio 2017](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2017) ile **Web geliştirme**, **Azure Araçları** iş yükü veya **.NET Core çoklu platform geliştirme** iş yükü yüklenmiş
::: moniker-end

::: moniker range=">= vs-2019"
* [Docker Masaüstü](https://hub.docker.com/editions/community/docker-ce-desktop-windows)
* [Visual Studio 2019](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2019) ile **Web geliştirme**, **Azure Araçları** iş yükünü ve/veya **.NET Core çoklu platform geliştirme** iş yükü yüklenmiş
* [.NET core 2.2 geliştirme araçları](https://dotnet.microsoft.com/download/dotnet-core/2.2) geliştirme ile .NET Core 2.2
::: moniker-end

## <a name="create-a-web-application-project"></a>Bir Web uygulaması projesi oluşturma

Visual Studio'da oluşturma bir **ASP.NET Core Web uygulaması** adlı proje `WebFrontEnd`. Seçin **Web uygulaması** ile Razor sayfaları web uygulaması oluşturmak için. 
  
::: moniker range="vs-2017"

Seçmeyin **Docker desteğini etkinleştir**. Docker desteği daha sonra ekleyeceksiniz.

![Web projesi oluşturma işleminin ekran görüntüsü](./media/tutorial-multicontainer/docker-tutorial-enable-docker-support.png)

::: moniker-end

::: moniker range="vs-2019"

![Web projesi oluşturma işleminin ekran görüntüsü](./media/tutorial-multicontainer/vs-2019/new-aspnet-core-project1.png)

Seçmeyin **Docker desteğini etkinleştir**. Docker desteği daha sonra ekleyeceksiniz.

![Web projesi oluşturma işleminin ekran görüntüsü](./media/tutorial-multicontainer/vs-2019/new-aspnet-core-project.png)

::: moniker-end

## <a name="create-a-web-api-project"></a>Bir Web API projesi oluşturma

Aynı çözüme bir proje ekleyin ve onu çağırmak *MyWebAPI*. Seçin **API** projesi olarak girin ve onay kutusunu temizleyin **HTTPS için Yapılandır**. Bu tasarımda, yalnızca SSL kullanıyoruz aynı web uygulamasındaki kapsayıcılar arasındaki iletişim için değil, istemci iletişimi için. Yalnızca `WebFrontEnd` HTTPS gerekir.

::: moniker range="vs-2017"
   ![Web API projesi oluşturma işleminin ekran görüntüsü](./media/tutorial-multicontainer/docker-tutorial-mywebapi.png)
::: moniker-end
::: moniker range="vs-2019"
   ![Web API projesi oluşturma işleminin ekran görüntüsü](./media/tutorial-multicontainer/vs-2019/web-api-project.png)
::: moniker-end

## <a name="add-code-to-call-the-web-api"></a>Web API'sini çağırmak için kod ekleyin

1. İçinde `WebFrontEnd` projesini açarsanız *Index.cshtml.cs* dosyasını bulun ve değiştirin `OnGet` yöntemini aşağıdaki kod ile.

   ```csharp
    public async Task OnGet()
    {
       ViewData["Message"] = "Hello from webfrontend";

       using (var client = new System.Net.Http.HttpClient())
       {
          // Call *mywebapi*, and display its response in the page
          var request = new System.Net.Http.HttpRequestMessage();
          request.RequestUri = new Uri("http://mywebapi/api/values/1");
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

1. Şimdi Web API projesinde, kod, eklediğiniz arama API'si tarafından döndürülen iletisini özelleştirmek için değerleri denetleyici ekleyin *webfrontend*.
    
      ```csharp
        // GET api/values/5
        [HttpGet("{id}")]
        public ActionResult<string> Get(int id)
        {
            return "webapi (with value " + id + ")";
        }
      ```

1. İçinde `WebFrontEnd` projesinin **Ekle > kapsayıcı Düzenleyicisi desteği**. **Docker destek seçenekleri** iletişim kutusu görüntülenir.

1. Seçin **Docker Compose**.

1. Örneğin, Linux, hedef işletim sistemi seçin.

   ![Hedef işletim sistemi seçme işleminin ekran görüntüsü](media/tutorial-multicontainer/docker-tutorial-docker-support-options.PNG)

   Visual Studio oluşturur bir *docker-compose.yml* dosyası ve bir *.dockerignore* dosyası **docker-compose** çözüm ve proje düğümünü gösteren kalın yazı tipinde başlangıç projesi olduğunu gösterir.

   ![Eklenen docker-compose proje ile çözüm Gezgini'nin ekran](media/tutorial-multicontainer/multicontainer-solution-explorer.png)

   *Docker-compose.yml* aşağıdaki gibi görünür:

   ```yaml
   version: '3.4'

    services:
      webfrontend:
        image: ${DOCKER_REGISTRY-}webfrontend
        build:
          context: .
          dockerfile: WebFrontEnd/Dockerfile
   ```

   *.Dockerignore* dosyası, dosya türleri ve Docker kapsayıcısında dahil etmek istemediğiniz uzantıları içerir. Bu dosyalar genellikle parçası değil uygulama veya hizmet, geliştirmekte olduğunuz kaynak denetimi ve geliştirme ortamı ile ilişkilidir.

   Bakmak **kapsayıcı Araçları** çalıştırılan komutlar hakkında ayrıntılar için çıkış bölmesine bölümü.  Docker-compose komut satırı aracı gördüğünüz yapılandırmak ve çalışma zamanı kapsayıcılarındaki oluşturmak için kullanılır.

1. Web API projesinde, proje düğümünü yeniden sağ tıklatın ve seçin **Ekle** > **kapsayıcı Düzenleyicisi desteği**. Seçin **Docker Compose**ve ardından aynı hedef işletim sistemi seçin.  

    > [!NOTE]
    > Bu adımda, bir Dockerfile oluşturmak Visual Studio sunar. Docker desteği olan bir proje üzerinde bunu yaparsanız, mevcut Dockerfile üzerine yazmak isteyip istemediğinizi istenir. Tutmak istediğiniz Dockerfile içindeki değişiklikler yaptıysanız, Hayır'ı seçin.

    Visual Studio, docker compose YML dosya bazı değişiklikler yapar. Artık her iki hizmet de dahil edilir.

    ```yaml
    version: '3.4'
    
    services:
      webfrontend:
        image: ${DOCKER_REGISTRY-}webfrontend
        build:
          context: .
          dockerfile: WebFrontEnd/Dockerfile
    
      mywebapi:
        image: ${DOCKER_REGISTRY-}mywebapi
        build:
          context: .
          dockerfile: MyWebAPI/Dockerfile
    ```

1. Yerel olarak (F5 veya Ctrl + F5) olarak çalışır durumda olduğunu doğrulamak için beklenen artık site çalıştırın. Her şeyin doğru şekilde yapılandırıldıysa, "Hello webfrontend ve webapı (1 değeriyle)." iletisini görürsünüz

   Kapsayıcı düzenleme eklediğinizde, kullandığınız ilk proje çalıştırdığınızda veya hata ayıklama başlatılacak şekilde ayarlanır. Başlatma eylemi yapılandırabileceğiniz **proje özellikleri** docker-compose projesi için.  Docker-compose proje düğümü bağlam menüsünü açmak için sağ tıklayın ve ardından **özellikleri**, ya da Alt + Enter tuşlarını kullanın.  Aşağıdaki ekran görüntüsünde, burada kullanılan çözüm için istediğiniz özellikleri gösterir.  Örneğin, özelleştirerek yüklenen sayfanın değiştirebilirsiniz **hizmet URL'si** özelliği.

   ![Docker-compose proje özellikleri ekran görüntüsü](media/tutorial-multicontainer/launch-action.png)

   Başlatıldığında gördüğünüz aşağıda verilmiştir:

   ![Çalışan bir web uygulamasının ekran görüntüsü](media/tutorial-multicontainer/webfrontend.png)

## <a name="next-steps"></a>Sonraki adımlar

Konum dağıtmayla seçeneklerinin, [Azure kapsayıcıları](/azure/containers).

## <a name="see-also"></a>Ayrıca bkz.
  
[Docker Compose](https://docs.docker.com/compose/)  
[Kapsayıcı Araçları](/visualstudio/containers/)
