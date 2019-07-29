---
title: Yerel bir Docker kapsayıcısında uygulamalarda hata ayıklama | Microsoft Docs
description: Yerel bir Docker kapsayıcısında çalışan bir uygulamayı değiştirmeyi, Düzenle ve Yenile aracılığıyla kapsayıcıyı yenilemeyi ve sonra hata ayıklama kesme noktalarını ayarlamayı öğrenin.
author: ghogen
manager: jillfra
ms.assetid: 480e3062-aae7-48ef-9701-e4f9ea041382
ms.topic: conceptual
ms.workload: multiple
ms.date: 07/25/2019
ms.author: ghogen
ms.technology: vs-azure
ms.openlocfilehash: 1b80fa9316c4db5a51fdb20150a9adae5a378682
ms.sourcegitcommit: ce1ab8a25c66a83e60eab80ed8e1596fe66dd85c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/29/2019
ms.locfileid: "68604762"
---
# <a name="debug-apps-in-a-local-docker-container"></a>Yerel bir Docker kapsayıcısında uygulamalarda hata ayıklama

Visual Studio, bir Docker kapsayıcısında geliştirme ve uygulamanızı yerel olarak doğrulama için tutarlı bir yol sağlar. Her kod değişikliği yaptığınızda kapsayıcıyı yeniden başlatmanız gerekmez.

Bu makalede, Visual Studio 'Nun yerel bir Docker kapsayıcısında bir ASP.NET Core Web uygulaması başlatmak, değişiklikler yapmak ve sonra değişiklikleri görmek için tarayıcıyı yenilemek üzere nasıl kullanılacağı gösterilmektedir. Bu makalede ayrıca, Kapsayıcılı ASP.NET Core Web uygulamaları ve .NET Framework konsol uygulamaları için hata ayıklama için kesme noktalarının nasıl ayarlanacağı gösterilmektedir.

## <a name="prerequisites"></a>Önkoşullar

Yerel bir Docker kapsayıcısında uygulamalarda hata ayıklamak için aşağıdaki araçların yüklü olması gerekir:

::: moniker range="vs-2017"

* Web geliştirme iş yükünün yüklü olduğu [Visual Studio 2017](https://visualstudio.microsoft.com/vs/older-downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=vs+2017+download)

::: moniker-end

::: moniker range="vs-2019"

* Web geliştirme iş yükünün yüklü olduğu [Visual Studio 2019](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2019)

::: moniker-end

Docker kapsayıcılarını yerel olarak çalıştırmak için yerel bir Docker istemciniz olmalıdır. Hyper-V ' d e devre dışı olması gereken [Docker araç kutusunu](https://www.docker.com/products/docker-toolbox)kullanabilirsiniz. Ayrıca, Hyper-V kullanan ve Windows 10 gerektiren [Docker for Windows](https://www.docker.com/get-docker)de kullanabilirsiniz. 

Docker kapsayıcıları .NET Framework ve .NET Core projeleri için kullanılabilir. İki örneğe bakalım. İlk olarak, bir .NET Core Web uygulamasına göz atacağız. Daha sonra, bir .NET Framework konsol uygulamasına göz atacağız.

## <a name="create-a-web-app"></a>Web uygulaması oluşturma

::: moniker range="vs-2017"
[!INCLUDE [create-aspnet5-app](../azure/includes/create-aspnet5-app.md)]
::: moniker-end
::: moniker range=">= vs-2019"
[! [Create-aspnet5-App-2019](../azure/includes/vs-2019/create-aspnet5-app-2019.md) dahil
::: moniker-end

### <a name="edit-your-code-and-refresh"></a>Kodunuzu düzenleyin ve yenileyin

Değişiklikleri hızlıca yinelemek için, uygulamanızı bir kapsayıcıda başlatabilirsiniz. Daha sonra, IIS Express istediğiniz gibi görüntüleyerek değişiklik yapmaya devam edin.

1. **Çözüm yapılandırmasını** **hata ayıklama**olarak ayarlayın. Ardından, Docker görüntünüzü derlemek ve yerel olarak çalıştırmak için CTRL + F5 tuşlarına basın.

    Kapsayıcı görüntüsü bir Docker kapsayıcısında oluşturulup çalıştırıldığında, Visual Studio varsayılan tarayıcınızda Web uygulamasını başlatır.

2. *Dizin* sayfasına gidin. Bu sayfada değişiklik yapacağız.
3. Visual Studio 'ya dönün ve *Index. cshtml*dosyasını açın.
4. Aşağıdaki HTML içeriğini dosyanın sonuna ekleyin ve değişiklikleri kaydedin.

    ```html
    <h1>Hello from a Docker container!</h1>
    ```

5. Çıkış penceresinde, .NET Build tamamlandığında ve aşağıdaki satırları görürseniz, tarayıcınıza geri dönün ve sayfayı yenileyin:

   ```output
   Now listening on: http://*:80
   Application started. Press Ctrl+C to shut down.
   ```

Değişiklikleriniz uygulandı!

### <a name="debug-with-breakpoints"></a>Kesme noktalarıyla hata ayıkla

Genellikle, değişiklikler daha fazla inceleme gerektirir. Bu görev için Visual Studio 'nun hata ayıklama özelliklerini kullanabilirsiniz.

1. Visual Studio 'da *Index.cshtml.cs*' yi açın.
2. `OnGet` Yönteminin içeriğini aşağıdaki kodla değiştirin:

   ```csharp
       ViewData["Message"] = "Your application description page from within a container";
   ```

3. Kod satırının solunda bir kesme noktası ayarlayın.
4. Hata ayıklamayı başlatmak ve kesme noktasına isabet etmek için F5 'e basın.
5. Kesme noktasını görüntülemek için Visual Studio 'ya geçin. Değerleri inceleyin.

   ![Ilı](media/edit-and-refresh/breakpoint.png)

## <a name="create-a-net-framework-console-app"></a>.NET Framework konsol uygulaması oluşturma

.NET Framework konsol uygulaması projelerini kullandığınızda, düzenleme olmadan Docker desteği ekleme seçeneği desteklenmez. Yalnızca tek bir Docker projesi kullanıyor olsanız bile aşağıdaki yordamı kullanabilirsiniz.

1. Yeni bir .NET Framework konsol uygulaması projesi oluşturun.
1. Çözüm Gezgini, proje düğümüne sağ tıklayın ve ardından**kapsayıcı düzenleme desteği** **Ekle** > ' yi seçin.  Görüntülenen iletişim kutusunda **Docker Compose**' yi seçin. Projenize bir Dockerfile eklenir ve ilişkili destek dosyalarına sahip bir Docker Compose projesi eklenir.

### <a name="debug-with-breakpoints"></a>Kesme noktalarıyla hata ayıkla

1. Çözüm Gezgini ' de, *program.cs*' yi açın.
2. `Main` Yönteminin içeriğini aşağıdaki kodla değiştirin:

   ```csharp
       System.Console.WriteLine("Hello, world!");
   ```

3. Kod satırının soluna bir kesme noktası ayarlayın.
4. Hata ayıklamayı başlatmak için F5 tuşuna basın ve kesme noktasına gidin.
5. Kesme noktası ve İnceleme değerlerini görüntülemek için Visual Studio 'ya geçin.

   ![Ilı](media/edit-and-refresh/breakpoint-console.png)

## <a name="container-reuse"></a>Kapsayıcı yeniden kullanımı

Geliştirme çevrimi sırasında, Visual Studio Dockerfile 'ı değiştirdiğinizde yalnızca kapsayıcı görüntülerinizi ve kapsayıcının kendisini yeniden oluşturur. Dockerfile 'ı değiştirmezseniz, Visual Studio önceki bir çalıştırağından kapsayıcıyı yeniden kullanır.

Kapsayıcınızı el ile değiştirdiyseniz ve temiz bir kapsayıcı görüntüsü ile yeniden başlatmak istiyorsanız, Visual Studio 'daki **derleme** > **temiz** komutunu kullanın ve normal olarak oluşturun.

## <a name="troubleshoot"></a>Sorun giderme

[Visual Studio Docker geliştirmede sorun gidermeyi](troubleshooting-docker-errors.md)öğrenin.

## <a name="more-about-docker-with-visual-studio-windows-and-azure"></a>Visual Studio, Windows ve Azure ile Docker hakkında daha fazla bilgi

* [Visual Studio ile kapsayıcı geliştirme](/visualstudio/containers)hakkında daha fazla bilgi edinin.
* Bir Docker kapsayıcısı derlemek ve dağıtmak için bkz. [Azure Pipelines Için Docker tümleştirmesi](https://aka.ms/dockertoolsforvsts).
* Windows Server ve nano sunucu makalelerinin bir dizini için bkz. [Windows kapsayıcı bilgileri](https://aka.ms/containers).
* [Azure Kubernetes hizmeti](https://azure.microsoft.com/services/kubernetes-service/) hakkında bilgi edinin ve [Azure Kubernetes hizmeti belgelerini](/azure/aks)gözden geçirin.
