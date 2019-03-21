---
title: 'Hızlı Başlangıç: Bir ASP.NET Core web hizmetini oluşturunF#'
description: Visual Studio ile bir ASP.NET Core web hizmeti oluşturmayı öğrenin F#, adım adım.
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
ms.openlocfilehash: f0fab988185efef6baf7e39c0b4250ada88b5fbd
ms.sourcegitcommit: 3d37c2460584f6c61769be70ef29c1a67397cf14
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/21/2019
ms.locfileid: "58322251"
---
# <a name="quickstart-use-visual-studio-to-create-your-first-aspnet-core-web-service-in-f"></a>Hızlı Başlangıç: F içinde ilk ASP.NET Core web hizmetinizi oluşturmak için Visual Studio\#

5-10 dakika giriş bölümünde F# Visual Studio'da oluşturacağınız bir F# ASP.NET Core web uygulaması.

Visual Studio henüz yüklemediyseniz, Git [Visual Studio indirmeleri](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2017) ücretsiz yüklemek için sayfa.

## <a name="create-a-project"></a>Proje oluşturma

İlk olarak, bir ASP.NET Core Web API projesi oluşturacaksınız. Proje türü şablonu dosyalarıyla bile herhangi bir şey ekledik önce işlevsel bir web hizmeti olarak oluşturan gelir!

::: moniker range="vs-2017"

1. Visual Studio'yu açın.

2. Üstteki menü çubuğundan seçin **dosya** > **yeni** > **proje**.

3. İçinde **yeni proje** iletişim kutusunda, sol bölmede, **Visual F#** , ardından **Web**. Orta bölmede seçin **ASP.NET Core Web uygulaması**, ardından **Tamam**.

     Görmüyorsanız **.NET Core** projesinin şablon kategorisi **açık Visual Studio yükleyicisi** sol bölmede bağlantı. Visual Studio Yükleyicisi'ni başlatır. Seçin **ASP.NET ve web geliştirme** iş yükü, ardından **Değiştir**.

     ![ASP.NET iş yükü VS yükleyicisi](../ide/media/quickstart-aspnet-workload.png)

4. buna **yeni ASP.NET Core Web uygulaması** iletişim kutusunda **ASP.NET Core 2.1** üstteki açılan menüden. (Görmüyorsanız **ASP.NET Core 2.1** listesinde izleyerek yükleyin **indirme** iletişim kutusunun üst kısmındaki sarı çubuk gözükeceğini bağlantıyı.) Seçin **Tamam**.

::: moniker-end

::: moniker range=">=vs-2019"

1. Visual Studio'yu açın.

2. Pencerenin başlangıç seçin **yeni bir proje oluşturma**.

3. Üzerinde **yeni bir proje oluşturma** sayfasında **f # web** Ara kutusuna ve ardından **ASP.NET Core Web uygulaması** proje şablonu. Seçin **sonraki**.

4. Üzerinde **yeni projenizi yapılandırın** sayfasında, bir ad girin ve ardından **Oluştur**.

5. Üzerinde **yeni bir ASP.NET Core Web uygulaması oluşturma** sayfasında **ASP.NET Core 2.1** üstteki açılan menüden seçin **Oluştur**.

::: moniker-end

## <a name="explore-the-ide"></a>IDE'yi keşfedin

1. İçinde **Çözüm Gezgini** araç genişletin **denetleyicileri** klasörü seçin **ValuesController.fs** Düzenleyicisi'nde açın.

   ![Çözüm Gezgini denetleyicileri klasörle genişletilmiş içinde F# Web API projesi](../ide/media/hello-world-fs-sln-explorer.png)

2. Ardından, değişiklik `Get()` aşağıdaki üyesinin:

   ```fsharp
   [<HttpGet>]
   member this.Get() =
       let values = [|"Hello"; "World"; "First F#/ASP.NET Core web API!"|]
       ActionResult<string[]>(values)
   ```

Kod basittir. Bir F# değerleri dizisi bağlı `values` adlandırın ve ardından ASP.NET Core MVC çerçevesi geçirilen bir `ActionResult`. ASP.NET Core REST sizin için üstlenir.

Şu şekilde düzenleyicide görünmelidir:

![Değiştirilen Get member](../ide/media/hello-world-fs-get-member.png)

## <a name="run-the-application"></a>Uygulamayı çalıştırma

1. Tuşuna **Ctrl**+**F5** uygulamayı çalıştırın ve bir web tarayıcısında açın.

2. Sayfaya gitmek `/api/values` route, ancak kullanmıyorsa, girin `https://localhost:44396/api/values` tarayıcınıza.

Web tarayıcısı artık daha önce yazdığınız eşleşen JSON görüntüler.

## <a name="next-steps"></a>Sonraki adımlar

Bu hızlı başlangıcı tamamladığınızda Tebrikler! Hakkında biraz öğrendiğiniz umuyoruz F#, ASP.NET Core ve Visual Studio IDE. Ortak bir sunucu üzerinde çalışan uygulamayı görmek için aşağıdaki düğmeyi seçin.

> [!div class="nextstepaction"]
> [Uygulamayı Azure App Service'e dağıtma](../deployment/quickstart-deploy-to-azure.md)

Hakkında daha fazla bilgi edinmek için F#, resmi denetleyin [ F# Kılavuzu](/dotnet/fsharp/index).