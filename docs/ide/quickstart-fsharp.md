---
title: 'Hızlı Başlangıç: İçinde bir ASP.NET Core Web hizmeti oluşturunF#'
description: Visual Studio 'da F#, adım adım ' da bir ASP.NET Core Web hizmeti oluşturmayı öğrenin.
ms.date: 08/24/2018
ms.topic: quickstart
author: cartermp
ms.author: phcart
manager: andrehal
dev_langs:
- FSharp
ms.workload:
- aspnet
- dotnetcore
ms.openlocfilehash: 990106f7f3ca97ae38a20170ca6ed2e1d699d4e4
ms.sourcegitcommit: 44e9b1d9230fcbbd081ee81be9d4be8a485d8502
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/30/2019
ms.locfileid: "70180317"
---
# <a name="quickstart-use-visual-studio-to-create-your-first-aspnet-core-web-service-in-f"></a>Hızlı Başlangıç: İlk ASP.NET Core Web hizmetinizi F 'de oluşturmak için Visual Studio 'Yu kullanma\#

Visual Studio 'da bu 5-10 dakikalık F# bir giriş için bir F# ASP.NET Core Web uygulaması oluşturacaksınız.

::: moniker range="vs-2017"

Visual Studio henüz yüklemediyseniz, Git [Visual Studio indirmeleri](https://visualstudio.microsoft.com/vs/older-downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=vs+2017+download) ücretsiz yüklemek için sayfa.

::: moniker-end

::: moniker range="vs-2019"

Visual Studio henüz yüklemediyseniz, Git [Visual Studio indirmeleri](https://visualstudio.microsoft.com/downloads) ücretsiz yüklemek için sayfa.

::: moniker-end

## <a name="create-a-project"></a>Proje oluşturma

İlk olarak, bir ASP.NET Core Web API projesi oluşturacaksınız. Proje türü, hatta herhangi bir şey eklemeden önce işlevsel bir Web hizmetini oluşturan şablon dosyaları ile birlikte gelir!

::: moniker range="vs-2017"

1. Visual Studio'yu açın.

2. Üstteki menü çubuğundan **Dosya** > **Yeni** > **Proje**' yi seçin.

3. **Yeni proje** iletişim kutusunda, sol bölmede, **görsel F#** ' i genişletin ve ardından **Web**' i seçin. Orta bölmede **ASP.NET Core Web uygulaması**' nı seçin ve ardından **Tamam**' ı seçin.

     Görmüyorsanız **.NET Core** projesinin şablon kategorisi **açık Visual Studio yükleyicisi** sol bölmede bağlantı. Visual Studio Yükleyicisi'ni başlatır. **ASP.net ve Web geliştirme** iş yükünü seçin ve ardından **Değiştir**' i seçin.

     ![ASP.NET iş yükü VS yükleyicisi](../ide/media/quickstart-aspnet-workload.png)

**yeni ASP.NET Core Web uygulaması** iletişim kutusunu 4.ın üst açılan menüden **ASP.NET Core 2,1** ' i seçin. (Listede **ASP.NET Core 2,1** görmüyorsanız, iletişim kutusunun üst kısmına yakın bir sarı çubukta görünmesi gereken **indirme** bağlantısını izleyerek yükleyin.) **Tamam**’ı seçin.

::: moniker-end

::: moniker range=">=vs-2019"

1. Visual Studio'yu açın.

2. Başlangıç penceresinde **Yeni proje oluştur**' u seçin.

3. **Yeni proje oluştur** sayfasında, ara kutusuna **f # Web** yazın ve ardından **ASP.NET Core Web uygulaması** proje şablonu ' nu seçin. Seçin **sonraki**.

4. **Yeni projenizi yapılandırın** sayfasında, bir ad girin ve ardından **Oluştur**' u seçin.

5. **Yeni bir ASP.NET Core Web uygulaması oluştur** sayfasında, üst açılan menüden **ASP.NET Core 2,1** ' i seçin ve ardından **Oluştur**' u seçin.

::: moniker-end

## <a name="explore-the-ide"></a>IDE'yi keşfedin

1. **Çözüm Gezgini** araç çubuğunda, **denetleyiciler** klasörünü genişletin ve ardından, düzenleyicide açmak için **valuescontroller. FS** ' yi seçin.

   ![F# Web API projesinde genişletilmiş denetleyiciler klasörüyle Çözüm Gezgini](../ide/media/hello-world-fs-sln-explorer.png)

2. Sonra, `Get()` üyeyi aşağıdakiler olacak şekilde değiştirin:

   ```fsharp
   [<HttpGet>]
   member this.Get() =
       let values = [|"Hello"; "World"; "First F#/ASP.NET Core web API!"|]
       ActionResult<string[]>(values)
   ```

Kod basittir. Bir F# değerler dizisi `values` ada bağlanır ve sonra ASP.NET Core MVC çerçevesine bir `ActionResult`olarak geçirilir. ASP.NET Core, geri kalanını sizin yerinize gerçekleştirir.

Düzenleyicide şöyle görünmelidir:

![Değiştirilen üye Al](../ide/media/hello-world-fs-get-member.png)

## <a name="run-the-application"></a>Uygulamayı çalıştırma

1. Uygulamayı çalıştırmak ve bir Web tarayıcısında açmak için **CTRL**+**F5** tuşuna basın.

2. Sayfa `/api/values` yola gitmelidir, ancak yoksa tarayıcınıza girin `https://localhost:44396/api/values` .

Web tarayıcısı artık daha önce yazdıklarınız ile eşleşen JSON 'ı görüntüleyecek.

## <a name="next-steps"></a>Sonraki adımlar

Bu hızlı başlangıcı tamamladığınızda Tebrikler! ASP.NET Core, ve Visual Studio IDE hakkında biraz F#bilgi edindiniz. Uygulamayı ortak bir sunucuda çalıştırmayı görmek için aşağıdaki düğmeyi seçin.

> [!div class="nextstepaction"]
> [Uygulamayı Azure App Service'e dağıtma](../deployment/quickstart-deploy-to-azure.md)

Hakkında F#daha fazla bilgi edinmek için resmi [ F# kılavuza](/dotnet/fsharp/index)göz atın.