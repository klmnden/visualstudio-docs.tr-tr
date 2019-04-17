---
title: Bir ASP.NET Core web uygulaması oluşturunC#
description: Visual Studio'da C# ve ASP.NET Core, adım adım ile basit bir Hello World web uygulaması oluşturmayı öğrenin.
ms.custom: mvc,seodec18
ms.date: 03/23/2019
ms.technology: vs-ide-general
ms.prod: visual-studio-windows
ms.topic: quickstart
author: TerryGLee
ms.author: tglee
manager: jillfra
dev_langs:
- CSharp
ms.workload:
- aspnet
- dotnetcore
ms.openlocfilehash: ea01ff2671212c8dfeb023d145cfd224a5feb2f8
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/17/2019
ms.locfileid: "59665504"
---
# <a name="quickstart-use-visual-studio-to-create-your-first-aspnet-core-web-app"></a>Hızlı Başlangıç: İlk ASP.NET Core web uygulamanızı oluşturmak için Visual Studio

Bu 5-10 dakikalık bir giriş Visual Studio'nun nasıl kullanılacağını, bir ASP.NET projesi şablonunu ve C# programlama dilini kullanarak basit bir "Hello World" web uygulaması oluşturacaksınız.

## <a name="before-you-begin"></a>Başlamadan önce

### <a name="install-visual-studio"></a>Visual Studio'yu yükleme

::: moniker range="vs-2017"

Visual Studio henüz yüklemediyseniz, Git [Visual Studio indirmeleri](https://visualstudio.microsoft.com/vs/older-downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=vs+2017+download) ücretsiz yüklemek için sayfa.

::: moniker-end

::: moniker range="vs-2019"

Visual Studio henüz yüklemediyseniz, Git [Visual Studio indirmeleri](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2019) ücretsiz yüklemek için sayfa.

::: moniker-end

### <a name="choose-your-theme-optional"></a>(İsteğe bağlı) temanızı seçin

Bu hızlı başlangıç öğreticisinde, koyu Tema kullanan ekran görüntüleri içerir. Koyu tema kullanmayan ancak öğrenmek istiyorsanız [Düzenleyicisi ve Visual Studio IDE'yi kişiselleştirme](quickstart-personalize-the-ide.md) öğrenmek için sayfa nasıl.

## <a name="create-a-project"></a>Proje oluşturma

Başlamak için bir ASP.NET Core web uygulaması projesi oluşturacaksınız. Proje türü bile herhangi bir şey ekledik önce bir web uygulaması oluşturmak için şablonu dosyalarıyla birlikte gelir!

::: moniker range="vs-2017"

1. Visual Studio 2017'yi açın.

1. Üstteki menü çubuğundan seçin **dosya** > **yeni** > **proje**.

1. Sol bölmesinde **yeni proje** iletişim kutusunda **Visual C#** ve ardından **.NET Core**. Orta bölmede seçin **ASP.NET Core Web uygulaması**. <br/><br/>Ardından dosyanızı adlandırın `HelloWorld` ve **Tamam**.

   ![Yeni ASP.NET Core Web uygulaması projesi oluşturmak için C#](../ide/media/csharp-aspnet-choose-template-name-file.png)

   > [!NOTE]
   > Görmüyorsanız **.NET Core** projesinin şablon kategorisi **açık Visual Studio yükleyicisi** sol bölmede bağlantı. (Görünen ayarlarınıza bağlı olarak, görmek için kaydırmanız gerekebilir.)
   >
   > ![Visual Studio yükleyicisi yeni proje iletişim kutusundan açın](../ide/media/open-visual-studio-installer.png)
   >
   > Visual Studio Yükleyicisi'ni başlatır. Seçin **ASP.NET ve web geliştirme** iş yükü ve ardından **Değiştir**.
   >
   > ![ASP.NET iş yükü VS yükleyicisi](../ide/media/quickstart-aspnet-workload.png)
   >
   > (Yeni iş yükünü yüklemek devam etmeden önce Visual Studio'yu kapatın gerekebilir.)

1. İçinde **yeni ASP.NET Core Web uygulaması** iletişim kutusunda **ASP.NET Core 2.1** üstteki açılan menüden. Ardından, **Web uygulaması**ve ardından **Tamam**.

   ![Yeni ASP.NET Core Web uygulaması iletişim kutusu](../ide/media/aspnet-core-2dot1.png)

   > [!NOTE]
   > Görmüyorsanız **ASP.NET Core 2.1** veya daha sonra Visual Studio'nun en son sürümü çalıştırdığınızdan emin olun. Yüklemenizi güncelleştirme hakkında daha fazla bilgi için bkz. [Visual Studio en son sürüme güncelleştirme](../install/update-visual-studio.md) sayfası.

Hemen sonra Visual Studio proje dosyanızı açar.

::: moniker-end

::: moniker range="vs-2019"

1. Visual Studio'yu açın.

1. Pencerenin başlangıç seçin **yeni bir proje oluşturma**.

   !['Yeni Proje oluştur' penceresini görüntüleyin](../get-started/media/vs-2019/create-new-project-dark-theme.png)

1. Üzerinde **yeni bir proje oluşturma** penceresinde girin veya yazın *ASP.NET* arama kutusuna. Ardından, **C#** dilden listeleyin ve ardından **Windows** Platform listesinde.

   Tüm dil ve platform filtreleri uyguladıktan sonra seçin **ASP.NET Core Web uygulaması** şablonu seçip **sonraki**.

   ![Seçin C# ASP.NET Core Web uygulaması şablonu](../get-started/csharp/media/vs-2019/csharp-create-new-project-search-aspnet-core-filtered.png)

   > [!NOTE]
   > Görmüyorsanız, **ASP.NET Core Web uygulaması** şablon yükleyebileceğiniz buradan **yeni bir proje oluşturma** penceresi. İçinde **aradığınızı bulamadınız?** message öğesini **daha fazla araçları ve özellikleri yükleme** bağlantı.
   >
   > !['Daha fazla araçları ve özellikleri yükleme' bağlantı 'Yeni Proje oluştur' penceresinde 'aradığınızı bulma yok' iletisi](../get-started/media/vs-2019/not-finding-what-looking-for.png)
   >
   > Ardından, Visual Studio yükleyicisinde **ASP.NET ve web geliştirme** iş yükü.
   >
   > ![ASP.NET Core Web uygulaması iş yükü Visual Studio yükleyicisi](../get-started/media/aspnet-core-web-dev-workload.png)
   >
   > Bundan sonra seçin **Değiştir** Visual Studio Yükleyicisi'nde düğmesi. Çalışmanızı kaydetmek için istenebilir; Bu durumda, bunu yapın. Ardından, **devam** iş yükünü yüklemek için. Ardından, 2. adım bu dönün "[proje oluşturma](#create-a-project)" yordamı.

1. İçinde **yeni projenizi yapılandırın** penceresinde yazın veya girin *HelloWorld* içinde **proje adı** kutusu. Ardından, **Oluştur**.

   !['yeni projenizi yapılandırın' penceresinde 'HelloWorld' projenizi adlandırın](../get-started/csharp/media/vs-2019/csharp-name-your-aspnet-helloworld-project.png)

1. İçinde **yeni bir ASP.NET Core Web uygulaması oluşturma** penceresinde doğrulayın **ASP.NET Core 2.1** veya daha sonra üstteki açılan menüde görünür. Ardından, **Web uygulaması**, örnek Razor sayfaları içerir. Ardından, **Oluştur**.

   !['Yeni bir ASP.NET Core Web uygulaması oluştur' penceresi](../get-started/csharp/media/vs-2019/csharp-create-aspnet-core-razor-pages-app.png)

   Yeni projeniz Visual Studio açılır.

::: moniker-end

## <a name="create-and-run-the-app"></a>Oluşturma ve uygulama çalıştırma

1. İçinde **Çözüm Gezgini**, genişletme **sayfaları** klasörünü ve ardından **About.cshtml**.

   ![Çözüm Gezgini'nden About.cshtml dosyayı seçin](../ide/media/csharp-aspnet-about-page-html-file.png)

   Bu dosya adında bir sayfaya karşılık gelen **hakkında** web uygulamasında, bir web tarayıcısında çalışan.

   ![Web uygulaması hakkında sayfası](../ide/media/csharp-aspnet-about-page.png)

   Düzenleyicide HTML görürsünüz "ek bilgileri" alanı için kod **hakkında** sayfası.

   ![Visual Studio düzenleyicisinde ek bilgi alanının HTML kodu](../ide/media/csharp-aspnet-about-cshtml-page.png)

1. Okunacak "ek bilgileri" metni değiştirme "**Merhaba Dünya!**".

   ![Visual Studio Düzenleyicisi ek bilgi alanında varsayılan HTML kodunu değiştirme](../ide/media/csharp-aspnet-about-cshtml-page-hello-world.png)

1. İçinde **Çözüm Gezgini**, genişletme **About.cshtml**ve ardından **About.cshtml.cs**. (Bu dosya ayrıca karşılık **hakkında** bir web tarayıcısında sayfasına.)

   ![Çözüm Gezgini'nden About.cshtml dosyayı seçin](../ide/media/csharp-aspnet-about-page-code-file.png)

   Düzenleyici'de C# göreceğiniz "uygulama açıklaması" alanı için metin içeren kod **hakkında** sayfası.

   ![Visual Studio Düzenleyicisi uygulama açıklama alanında için C# kodu](../ide/media/csharp-aspnet-about-cshtml-cs-code.png)

1. Okunacak "uygulama açıklaması" ileti metni değiştirme "**iletime nedir?**".

   ![Visual Studio Düzenleyicisi'nde uygulama açıklama alanı için varsayılan ileti metni değiştirme](../ide/media/csharp-aspnet-about-cshtml-cs-message.png)

1. Seçin **IIS Express** veya basın **Ctrl**+**F5** uygulamayı çalıştırın ve bir web tarayıcısında açın.

   ![Visual Studio'da IIS Express düğmeyi seçin](../ide/media/csharp-aspnet-helloworld-iisbutton.png)

   > [!NOTE]
   > Yazan bir hata iletisi alırsanız **web sunucusu için 'IIS Express' bağlanılamıyor**, veya bir SSL sertifikası ilgili bir hata iletisi Visual Studio'yu kapatın. Ardından, Visual Studio kullanarak açma **yönetici olarak çalıştır** sağ tıklatın ve bağlam menüsünden seçeneği. Ardından, uygulamayı yeniden çalıştırın.

1. Web tarayıcısında doğrulayın **hakkında** sayfa güncelleştirilmiş metni içerir.

   ![Yaptığınız değişiklikleri içeren sayfasında hakkında güncelleştirilmiş görüntüleyin](../ide/media/csharp-aspnet-about-page-hello-world.png)

1. Web tarayıcısını kapatın.

### <a name="review-your-work"></a>Çalışmanızı gözden geçirin

Önceki bölümde tamamlanan iş denetlemek için aşağıdaki animasyon görüntüleyin.

  ![Oluşturma ve basit bir çalıştırma işlemi gösterilmektedir animasyonlu .gif dosyayı görüntülemek C# Visual Studio'da ASP.NET Core web uygulaması](../ide/media/csharp-aspnet-animated-hello-world.gif)

Bu hızlı başlangıcı tamamladığınızda Tebrikler! C#, ASP.NET Core ve Visual Studio IDE (tümleşik geliştirme ortamı) hakkında biraz öğrenilen umuyoruz.

## <a name="next-steps"></a>Sonraki adımlar

Daha fazla bilgi için şu öğreticiyle devam edin:

> [!div class="nextstepaction"]
> [C# ve Visual Studio'da ASP.NET kullanmaya başlama](../get-started/csharp/tutorial-aspnet-core.md)

## <a name="see-also"></a>Ayrıca bkz.

[Visual Studio kullanarak web uygulamanızı Azure App Service'e yayımlama](../deployment/quickstart-deploy-to-azure.md)
