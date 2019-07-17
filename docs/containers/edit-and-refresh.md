---
title: Yerel bir Docker kapsayıcısında uygulama hatalarını ayıklama | Microsoft Docs
description: Yerel bir Docker kapsayıcısı içinde çalışan bir uygulamayı değiştirmek öğrenin, kapsayıcı düzenleme ve yenileme aracılığıyla yenileyin ve ardından kesme noktaları hata ayıklama ayarlayın.
author: ghogen
manager: jillfra
ms.assetid: 480e3062-aae7-48ef-9701-e4f9ea041382
ms.topic: conceptual
ms.workload: multiple
ms.date: 03/05/2019
ms.author: ghogen
ms.technology: vs-azure
ms.openlocfilehash: 70f78f1e7ed05f771e188fe922fef769a38799f9
ms.sourcegitcommit: f369ff7e84b0216f01570a486c7be80ca6d0e61a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/16/2019
ms.locfileid: "68250441"
---
# <a name="debug-apps-in-a-local-docker-container"></a>Yerel bir Docker kapsayıcısında uygulama hatalarını ayıklama

Visual Studio, bir Docker kapsayıcısı içinde geliştirin ve uygulamanızı yerel olarak doğrulamak için tutarlı bir yol sağlar. Kapsayıcı bir kod değişikliği yaptığınızda her zaman yeniden başlatmanız gerekmez.

Bu makalede, yerel bir Docker kapsayıcısında ASP.NET Core web uygulaması başlatın, değişiklikleri yapın ve ardından değişiklikleri görmek için tarayıcıyı yenileyin Visual Studio'da Düzenle ve yenileme özelliğini kullanmayı göstermektedir. Bu makalede ayrıca hata ayıklama için kesme noktaları ayarlama işlemini gösterir.

## <a name="prerequisites"></a>Önkoşullar

Yerel bir Docker kapsayıcısı uygulamalarında hata ayıklamak için aşağıdaki araçları yüklenmelidir:

::: moniker range="vs-2017"

* [Visual Studio 2017](https://visualstudio.microsoft.com/vs/older-downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=vs+2017+download) yüklü Web geliştirme iş yüküyle birlikte sağlanır

::: moniker-end

::: moniker range="vs-2019"

* [Visual Studio 2019](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2019) yüklü Web geliştirme iş yüküyle birlikte sağlanır

::: moniker-end

Yerel olarak çalışan Docker kapsayıcıları için yerel bir Docker istemcisinin olması gerekir. Kullanabileceğiniz [Docker araç kutusu](https://www.docker.com/products/docker-toolbox), Hyper-V devre dışı bırakılmasını gerektirir. Ayrıca [için Docker Windows](https://www.docker.com/get-docker), Hyper-V kullanır ve Windows 10 gerektirir. Docker araç kutusu kullanırsanız, Docker istemcisi yapılandırmanız gerekir.

Docker kapsayıcıları, .NET Framework ve .NET Core projeleri için kullanılabilir. İki örneklere göz atalım. İlk olarak, bir .NET Core web uygulaması bakın. Ardından bir .NET Framework konsol uygulamasını arayın.

## <a name="create-a-web-app"></a>Web uygulaması oluşturma

::: moniker range="vs-2017"
[!INCLUDE [create-aspnet5-app](../azure/includes/create-aspnet5-app.md)]
::: moniker-end
::: moniker range=">= vs-2019"
[! DAHİL [oluşturma-aspnet5-app-2019](../azure/includes/vs-2019/create-aspnet5-app-2019.md)
::: moniker-end

### <a name="edit-your-code-and-refresh"></a>Kodunuz ve yenileme Düzenle

Değişikliklerini hızlıca yinelemek için uygulamanızın bir kapsayıcıda başlatabilirsiniz. Ardından, IIS Express ile olduğu gibi bunları görüntüleme değişiklik yapmak devam edin.

1. Ayarlama **çözüm yapılandırması** için **hata ayıklama**. Ardından, Docker görüntünüzü derlemek ve yerel olarak çalıştırmak için Ctrl + F5 tuşuna basın.

    Ne zaman kapsayıcı görüntüsü oluşturdunuz ve bir Docker kapsayıcısı içinde çalışırken, Visual Studio web uygulamasını varsayılan tarayıcınızda başlatır.

2. Git *dizin* sayfası. Bu sayfada değişiklikler oluşturacağız.
3. Visual Studio'ya geri dönün ve açık *Index.cshtml*.
4. Aşağıdaki HTML içeriği dosyanın sonuna ekleyin ve değişiklikleri kaydedin.

    ```html
    <h1>Hello from a Docker container!</h1>
    ```

5. Çıktı penceresinde, .NET derleme tamamlandıktan ve aşağıdaki satırları görmeniz, tarayıcınızın geri geçin ve sayfayı yenileyin:

   ```output
   Now listening on: http://*:80
   Application started. Press Ctrl+C to shut down.
   ```

Yaptığınız değişiklikleri uygulanmış!

### <a name="debug-with-breakpoints"></a>Kesme noktaları ile hata ayıklama

Genellikle, değişiklikler daha fazla inceleme yapılması gerekir. Bu görev için Visual Studio hata ayıklama özelliklerini kullanabilirsiniz.

1. Visual Studio'da açın *Index.cshtml.cs*.
2. Öğesinin içeriğini değiştirin `OnGet` yöntemini aşağıdaki kod ile:

   ```csharp
       ViewData["Message"] = "Your application description page from within a container";
   ```

3. Kod satırının solunda bir kesme noktası ayarlayın.
4. Kesme noktasına isabet ve hata ayıklamayı başlatmak için F5 tuşuna basın.
5. Kesme noktası görüntülemek için Visual Studio'ya geçiş yapın. Değerleri inceleyin.

   ![Kesme noktası](media/edit-and-refresh/breakpoint.png)

## <a name="create-a-net-framework-console-app"></a>.NET Framework konsol uygulaması oluşturma

.NET Framework konsol uygulamasını projeleri kullandığınızda, Docker desteği düzenleme olmadan ekleme seçeneği desteklenmez. Yalnızca tek bir Docker projesi kullanmıyor olsanız bile aşağıdaki yordamda kullanmaya devam edebilirsiniz.

1. Yeni bir .NET Framework konsol uygulama projesi oluşturun.
1. Çözüm Gezgini'nde proje düğümüne sağ tıklayın ve ardından **Ekle** > **kapsayıcı düzenleme desteği**.  Görüntülenen iletişim kutusunda seçin **Docker Compose**. Bir Dockerfile projenize eklenir ve ilgili destek dosyalarını içeren bir Docker Compose proje eklenir.

### <a name="debug-with-breakpoints"></a>Kesme noktaları ile hata ayıklama

1. Çözüm Gezgini'nde açın *Program.cs*.
2. Öğesinin içeriğini değiştirin `Main` yöntemini aşağıdaki kod ile:

   ```csharp
       System.Console.WriteLine("Hello, world!");
   ```

3. Kod satırının sola bir kesme noktası ayarlayın.
4. Hata ayıklamayı başlatmak için F5 tuşuna basın ve kesme noktasına ulaşırsınız.
5. Kesme noktasını görüntüleyin ve değerleri incelemek için Visual Studio'ya geçiş yapın.

   ![Kesme noktası](media/edit-and-refresh/breakpoint-console.png)

## <a name="container-reuse"></a>Kapsayıcı yeniden kullanma

Dockerfile değiştirdiğinizde geliştirme döngüsü sırasında Visual Studio yalnızca, kapsayıcı görüntülerine ve kapsayıcı oluşturur. Dockerfile değiştirmezseniz, Visual Studio'nun bir önceki çalıştırma kapsayıcısından kullanır.

Kapsayıcı ve temiz bir kapsayıcı görüntüsü ile yeniden başlatmak istediğiniz el ile değiştirdiyseniz, kullanın **derleme** > **temiz** komutu Visual Studio ve daha sonra normal şekilde oluşturabilirsiniz.

## <a name="troubleshoot"></a>Sorun giderme

Bilgi edinmek için nasıl [Visual Studio Docker geliştirme sorunlarını giderme](troubleshooting-docker-errors.md).

## <a name="more-about-docker-with-visual-studio-windows-and-azure"></a>Visual Studio, Windows ve Azure ile Docker hakkında daha fazla bilgi

* Daha fazla bilgi edinin [Visual Studio ile kapsayıcı geliştirme](/visualstudio/containers).
* Derleme ve bir Docker kapsayıcısı dağıtma hakkında bilgi için bkz: [Azure işlem hatları için Docker tümleştirmesi](https://aka.ms/dockertoolsforvsts).
* Windows Server ve Nano Server makaleleri bir dizin için bkz: [Windows kapsayıcı bilgileri](https://aka.ms/containers).
* Hakkında bilgi edinin [Azure Kubernetes hizmeti](https://azure.microsoft.com/services/kubernetes-service/) ve gözden geçirme [Azure Kubernetes Service belgelerinde](/azure/aks).
