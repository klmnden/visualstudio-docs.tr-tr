---
title: Yerel bir Docker kapsayıcısı uygulamalarında hata ayıklama | Microsoft Docs
description: Yerel bir Docker kapsayıcısı içinde çalışan bir uygulamayı değiştirmek öğrenin, kapsayıcı düzenleme ve yenileme aracılığıyla yenileyin ve kesme noktaları hata ayıklama ayarlayın
services: container-service
author: ghogen
manager: jillfra
ms.assetid: 480e3062-aae7-48ef-9701-e4f9ea041382
ms.topic: conceptual
ms.workload: multiple
ms.date: 03/01/2019
ms.author: ghogen
ms.openlocfilehash: 7f80681d4aa307675f73eac24d0fbe17c7c7b9a9
ms.sourcegitcommit: 11337745c1aaef450fd33e150664656d45fe5bc5
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2019
ms.locfileid: "57323769"
---
# <a name="debugging-apps-in-a-local-docker-container"></a>Yerel Docker kapsayıcısındaki uygulamalarda hata ayıklama

## <a name="overview"></a>Genel Bakış

Visual Studio 2017, bir Docker kapsayıcısı içinde geliştirin ve uygulamanızı yerel olarak doğrulamak için tutarlı bir yol sağlar.
Kapsayıcı bir kod değişikliği yaptığınızda her zaman yeniden başlatmanız gerekmez.
Bu makalede, yerel bir Docker kapsayıcısında ASP.NET Core Web uygulaması başlatın, gerekli değişiklikleri yapın ve ardından bu değişiklikleri görmek için tarayıcıyı yenilemek için "Düzenle ve Yenile" özelliğini kullanmayı göstermektedir.
Bu makalede ayrıca hata ayıklama için kesme noktaları ayarlama işlemini gösterir.

## <a name="prerequisites"></a>Önkoşullar

Aşağıdaki araçlar yüklü olması gerekir.

::: moniker range="vs-2017"

* [Visual Studio 2017](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2017) yüklü Web geliştirme iş yüküyle birlikte sağlanır.

::: moniker-end

::: moniker range="vs-2019"

* [Visual Studio 2019](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2019+rc) yüklü Web geliştirme iş yüküyle birlikte sağlanır.

::: moniker-end

Yerel olarak Docker kapsayıcıları çalıştırmak için bir yerel docker istemcisi gerekir.
Kullanabileceğiniz [Docker araç kutusu](https://www.docker.com/products/docker-toolbox), Hyper-V devre dışı bırakılmasını gerektiren veya kullanabilirsiniz [için Docker Windows](https://www.docker.com/get-docker), Hyper-V kullanır ve Windows 10 gerektirir.

Docker araç kutusu kullanıyorsanız gerekecektir [Docker istemciyi Yapılandırma](vs-azure-tools-docker-setup.md)

## <a name="1-create-a-web-app"></a>1. Web uygulaması oluşturma

[!INCLUDE [create-aspnet5-app](../azure/includes/create-aspnet5-app.md)]

## <a name="2-edit-your-code-and-refresh"></a>2. Kodunuz ve yenileme Düzenle

Değişikliklerini hızlıca yinelemek için bir kapsayıcı içindeki uygulamanızı başlatın ve değişiklik yapmak, IIS Express ile olduğu gibi bunları görüntüleme devam edebilirsiniz.

1. Çözüm yapılandırması ayarlanmış `Debug` basın  **&lt;CTRL + F5 tuşlarına basarak >** , docker görüntüsünü derleyin ve yerel olarak çalıştırın.

    Kapsayıcı görüntüsü oluşturuldu ve bir Docker kapsayıcısı içinde çalışırken sonra Visual Studio Web uygulamasını varsayılan tarayıcınızda başlatır.
    Aksi takdirde hatalar var veya Microsoft Edge tarayıcı kullanıyorsanız, bkz. [sorun giderme](vs-azure-tools-docker-troubleshooting-docker-errors.md) bölümü.
2. Bizim değişiklik yapmak için burada ekleyeceğiz olan hakkında sayfasına gidin.
3. Visual Studio'ya geri dönün ve açık `Views\Home\About.cshtml`.
4. Aşağıdaki HTML içeriği dosyanın sonuna ekleyin ve değişiklikleri kaydedin.

    ```html
    <h1>Hello from a Docker Container!</h1>
    ```

5. Çıkış penceresi, .NET derleme tamamlandığında ve şu satırları görmeniz görüntüleme, tarayıcınızın geri geçiş ve hakkında sayfayı yenileyin.

   ```output
   Now listening on: http://*:80
   Application started. Press Ctrl+C to shut down
   ```

6. Yaptığınız değişiklikleri uygulanmış!

## <a name="3-debug-with-breakpoints"></a>3. Kesme noktaları ile hata ayıklama

Genellikle, değişiklikleri daha fazla inceleme, Visual Studio hata ayıklama özelliklerinin yararlanarak gerekir.

1. Visual Studio'ya geri dönün ve açın `About.cshtml.cs`
2. Öğesinin içeriğini değiştirin `OnGet` aşağıdaki yöntemi:

   ```cs
       Message = "Your application description page from within a Container";
   ```

3. Kod satırının sola bir kesme noktası ayarlayın.
4. Hata ayıklamayı başlatmak için F5'e basın.
5. Kesme noktasına isabet hakkında sayfasına gidin.
6. Kesme noktası görüntülemek için Visual Studio'ya geçiş yapın ve ileti değerini denetleyin.

   ![Kesme noktası](media/vs-azure-tools-docker-edit-and-refresh/breakpoint.png)

## <a name="summary"></a>Özet

Visual Studio 2017'de Docker desteği sayesinde, yerel olarak geliştirme konusunda bir Docker kapsayıcısı içinde üretim gerçekçilik çalışma verimliliği elde edebilirsiniz.

## <a name="troubleshooting"></a>Sorun giderme

[Visual Studio Docker geliştirme sorunlarını giderme](vs-azure-tools-docker-troubleshooting-docker-errors.md)

## <a name="more-about-docker-with-visual-studio-windows-and-azure"></a>Visual Studio, Windows ve Azure ile Docker hakkında daha fazla bilgi

* [Visual Studio ile kapsayıcı geliştirme](/visualstudio/containers) -kapsayıcı geliştirme hub sayfası
* [Azure işlem hatları için docker tümleştirmesi](https://aka.ms/dockertoolsforvsts) - derleme ve docker kapsayıcıları dağıtma
* [Visual Studio Code için docker Araçları](https://aka.ms/dockertoolsforvscode) -yakında daha fazla e2e senaryoları ile docker dosyalarını düzenlemek için dil Hizmetleri
* [Windows kapsayıcı bilgileri](https://aka.ms/containers)-Windows Server ve Nano sunucu bilgileri
* [Azure Kubernetes hizmeti](https://azure.microsoft.com/services/kubernetes-service/) - [Azure Kubernetes Service belgeleri](/azure/aks)
