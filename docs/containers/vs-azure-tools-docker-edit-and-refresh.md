---
title: Yerel bir Docker kapsayıcısı uygulamalarında hata ayıklama | Microsoft Docs
description: Yerel bir Docker kapsayıcısı içinde çalışan bir uygulamayı değiştirmek öğrenin, kapsayıcı düzenleme ve yenileme aracılığıyla yenileyin ve kesme noktaları hata ayıklama ayarlayın
author: ghogen
manager: jillfra
ms.assetid: 480e3062-aae7-48ef-9701-e4f9ea041382
ms.topic: conceptual
ms.workload: multiple
ms.date: 03/05/2019
ms.author: ghogen
ms.technology: vs-azure
ms.openlocfilehash: 76de7613afbed91d746bcfb2c851d1e3fe9cf992
ms.sourcegitcommit: 509fc3a324b7748f96a072d0023572f8a645bffc
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58856362"
---
# <a name="debugging-apps-in-a-local-docker-container"></a>Yerel Docker kapsayıcısındaki uygulamalarda hata ayıklama

## <a name="overview"></a>Genel Bakış

Visual Studio, bir Docker kapsayıcısı içinde geliştirin ve uygulamanızı yerel olarak doğrulamak için tutarlı bir yol sağlar.
Kapsayıcı bir kod değişikliği yaptığınızda her zaman yeniden başlatmanız gerekmez.
Bu makalede, yerel bir Docker kapsayıcısında ASP.NET Core Web uygulaması başlatın, gerekli değişiklikleri yapın ve ardından bu değişiklikleri görmek için tarayıcıyı yenilemek için "Düzenle ve Yenile" özelliğini kullanmayı göstermektedir.
Bu makalede ayrıca hata ayıklama için kesme noktaları ayarlama işlemini gösterir.

## <a name="prerequisites"></a>Önkoşullar

Aşağıdaki araçlar yüklü olması gerekir.

::: moniker range="vs-2017"

* [Visual Studio 2017](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2017) yüklü Web geliştirme iş yüküyle birlikte sağlanır.

::: moniker-end

::: moniker range="vs-2019"

* [Visual Studio 2019](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2019) yüklü Web geliştirme iş yüküyle birlikte sağlanır.

::: moniker-end

Yerel olarak Docker kapsayıcıları çalıştırmak için bir yerel docker istemcisi gerekir.
Kullanabileceğiniz [Docker araç kutusu](https://www.docker.com/products/docker-toolbox), Hyper-V devre dışı bırakılmasını gerektiren veya kullanabilirsiniz [için Docker Windows](https://www.docker.com/get-docker), Hyper-V kullanır ve Windows 10 gerektirir.

Docker araç kutusunu kullanarak, Docker istemciyi yapılandırmak gerekir.

## <a name="1-create-a-web-app"></a>1. Web uygulaması oluşturma

::: moniker range="vs-2017"
[!INCLUDE [create-aspnet5-app](../azure/includes/create-aspnet5-app.md)]
::: moniker-end
::: moniker range=">= vs-2019"
[! DAHİL [oluşturma-aspnet5-app-2019](../azure/includes/vs-2019/create-aspnet5-app-2019.md)
::: moniker-end

## <a name="2-edit-your-code-and-refresh"></a>2. Kodunuz ve yenileme Düzenle

Değişikliklerini hızlıca yinelemek için bir kapsayıcı içindeki uygulamanızı başlatın ve değişiklik yapmak, IIS Express ile olduğu gibi bunları görüntüleme devam edebilirsiniz.

1. Çözüm yapılandırması ayarlanmış `Debug` ve docker görüntünüzü derlemek ve yerel olarak çalıştırmak için Ctrl + F5 tuşlarına basın.

    Kapsayıcı görüntüsü oluşturuldu ve bir Docker kapsayıcısı içinde çalışırken sonra Visual Studio web uygulamasını varsayılan tarayıcınızda başlatır.

2. Bizim değişiklik yapmak için burada ekleyeceğiz olan dizin sayfasına gidin.
3. Visual Studio'ya geri dönün ve açık `Index.cshtml`.
4. Aşağıdaki HTML içeriği dosyanın sonuna ekleyin ve değişiklikleri kaydedin.

    ```html
    <h1>Hello from a Docker Container!</h1>
    ```

5. Çıkış penceresi, .NET derleme tamamlandığında ve şu satırları görmeniz görüntüleme, tarayıcınızın geri geçiş ve sayfayı yenileyin.

   ```output
   Now listening on: http://*:80
   Application started. Press Ctrl+C to shut down
   ```

6. Yaptığınız değişiklikleri uygulanmış!

## <a name="3-debug-with-breakpoints"></a>3. Kesme noktaları ile hata ayıklama

Genellikle, değişiklikleri daha fazla inceleme, Visual Studio hata ayıklama özelliklerinin yararlanarak gerekir.

1. Visual Studio'ya geri dönün ve açın `Index.cshtml.cs`
2. Öğesinin içeriğini değiştirin `OnGet` aşağıdaki yöntemi:

   ```csharp
       ViewData["Message"] = "Your application description page from within a Container";
   ```

3. Kod satırının sola bir kesme noktası ayarlayın.
4. Kesme noktasına isabet ve hata ayıklamayı başlatmak için F5'e basın.
5. Kesme noktası görüntüleme, değerleri inceleyin ve benzeri için Visual Studio'ya geçiş yapın.

   ![Kesme noktası](media/vs-azure-tools-docker-edit-and-refresh/breakpoint.png)

## <a name="summary"></a>Özet

Visual Studio'da Docker desteği sayesinde, yerel olarak geliştirme konusunda bir Docker kapsayıcısı içinde üretim gerçekçilik çalışma verimliliği elde edebilirsiniz.

## <a name="troubleshooting"></a>Sorun giderme

[Visual Studio Docker geliştirme sorunlarını giderme](vs-azure-tools-docker-troubleshooting-docker-errors.md)

## <a name="more-about-docker-with-visual-studio-windows-and-azure"></a>Visual Studio, Windows ve Azure ile Docker hakkında daha fazla bilgi

* [Visual Studio ile kapsayıcı geliştirme](/visualstudio/containers) - giriş sayfası bir kapsayıcı geliştirme
* [Azure işlem hatları için docker tümleştirmesi](https://aka.ms/dockertoolsforvsts) - derleme ve docker kapsayıcıları dağıtma
* [Windows kapsayıcı bilgileri](https://aka.ms/containers)-Windows Server ve Nano sunucu bilgileri
* [Azure Kubernetes hizmeti](https://azure.microsoft.com/services/kubernetes-service/) - [Azure Kubernetes Service belgeleri](/azure/aks)
