---
title: Bir ASP.NET Core web uygulaması oluşturunC#
description: Visual Studio'da C# ve ASP.NET Core, adım adım ile basit bir Hello World web uygulaması oluşturmayı öğrenin.
ms.custom: mvc,seodec18
ms.date: 06/06/2019
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
ms.openlocfilehash: 28994e7f3a4f31a9e3ee8c292a08df1132cf20df
ms.sourcegitcommit: 44e9b1d9230fcbbd081ee81be9d4be8a485d8502
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/30/2019
ms.locfileid: "70180390"
---
# <a name="quickstart-use-visual-studio-to-create-your-first-aspnet-core-web-app"></a>Hızlı Başlangıç: İlk ASP.NET Core Web uygulamanızı oluşturmak için Visual Studio 'Yu kullanma

Bu 5-10 dakikalık bir giriş Visual Studio'nun nasıl kullanılacağını, bir ASP.NET projesi şablonunu ve C# programlama dilini kullanarak basit bir "Hello World" web uygulaması oluşturacaksınız.

## <a name="before-you-begin"></a>Başlamadan önce

### <a name="install-visual-studio"></a>Visual Studio'yu yükleme

::: moniker range="vs-2017"

Visual Studio henüz yüklemediyseniz, Git [Visual Studio indirmeleri](https://visualstudio.microsoft.com/vs/older-downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=vs+2017+download) ücretsiz yüklemek için sayfa.

::: moniker-end

::: moniker range="vs-2019"

Visual Studio henüz yüklemediyseniz, Git [Visual Studio indirmeleri](https://visualstudio.microsoft.com/downloads) ücretsiz yüklemek için sayfa.

::: moniker-end

### <a name="choose-your-theme-optional"></a>(İsteğe bağlı) temanızı seçin

Bu hızlı başlangıç öğreticisinde, koyu Tema kullanan ekran görüntüleri içerir. Koyu tema kullanmayan ancak öğrenmek istiyorsanız [Düzenleyicisi ve Visual Studio IDE'yi kişiselleştirme](quickstart-personalize-the-ide.md) öğrenmek için sayfa nasıl.

## <a name="create-a-project"></a>Proje oluşturma

Başlamak için bir ASP.NET Core web uygulaması projesi oluşturacaksınız. Proje türü, bir Web uygulaması oluşturmak için tüm şablon dosyalarıyla birlikte gelir, hatta herhangi bir şey eklemeden önce!

::: moniker range="vs-2017"

1. Visual Studio 2017'yi açın.

1. Üstteki menü çubuğundan **Dosya** > **Yeni** > **Proje**' yi seçin.

1. Sol bölmesinde **yeni proje** iletişim kutusunda **Visual C#** ve ardından **.NET Core**. Orta bölmede seçin **ASP.NET Core Web uygulaması**. <br/><br/>Ardından dosyanızı adlandırın `HelloWorld` ve **Tamam**.

   ![İçin yeni ASP.NET Core Web uygulaması projesi oluşturunC#](../ide/media/csharp-aspnet-choose-template-name-file.png)

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

1. **Yeni ASP.NET Core Web uygulaması** iletişim kutusunda üst açılan menüden **ASP.NET Core 2,1** ' ı seçin. Sonra, **Web uygulaması**' nı ve ardından **Tamam**' ı seçin.

   ![Yeni ASP.NET Core Web uygulaması iletişim kutusu](../ide/media/aspnet-core-2dot1.png)

   > [!NOTE]
   > **ASP.NET Core 2,1**görmüyorsanız, Visual Studio 'nun en son sürümünü çalıştırdığınızdan emin olun. Yüklemenizi güncelleştirme hakkında daha fazla bilgi için bkz. [Visual Studio 'yu en son sürüm sayfasına güncelleştirme](../install/update-visual-studio.md) .

Hemen sonra Visual Studio proje dosyanızı açar.

::: moniker-end

::: moniker range="vs-2019"

1. Visual Studio'yu açın.

1. Başlangıç penceresinde **Yeni proje oluştur**' u seçin.

   ![' Yeni proje oluştur ' penceresini görüntüleyin](../get-started/media/vs-2019/create-new-project-dark-theme.png)

1. **Yeni proje oluştur** penceresinde, arama kutusuna *ASP.net* girin veya yazın. Ardından, dil **C#** listesinden seçin ve ardından platform listesinden **Windows** ' u seçin.

   Dil ve platform filtrelerini uyguladıktan sonra, **ASP.NET Core Web uygulaması** şablonunu seçin ve ardından **İleri**' yi seçin.

   ![ASP.NET Core Web C# uygulaması için şablonu seçin](../get-started/csharp/media/vs-2019/csharp-create-new-project-search-aspnet-core-filtered.png)

   > [!NOTE]
   > **ASP.NET Core Web uygulaması** şablonunu görmüyorsanız, **Yeni proje oluştur** penceresinden yükleyebilirsiniz. **Aradığınızı bulamıyor musunuz?** iletisi için **daha fazla araç ve özellik yüklemeyi** seçin bağlantısına tıklayın.
   >
   > ![' Yeni proje oluştur ' penceresindeki ' daha fazla araç ve özellik yüklemesi ' ' ne aradığınızı bulma ' iletisi bağlantısı](../get-started/media/vs-2019/not-finding-what-looking-for.png)
   >
   > Ardından Visual Studio Yükleyicisi, **ASP.net ve Web geliştirme** iş yükünü seçin.
   >
   > ![Visual Studio Yükleyicisi Web uygulaması iş yükünü ASP.NET Core](../get-started/media/aspnet-core-web-dev-workload.png)
   >
   > Bundan sonra Visual Studio Yükleyicisi **Değiştir** düğmesini seçin. İşinizi kaydetmeniz istenebilir; Öyleyse, bunu yapın. Sonra, iş yükünü yüklemek için **devam** ' ı seçin. Ardından, bu "[Proje oluşturma](#create-a-project)" yordamında 2. adıma geri dönün.

1. **Yeni projeyi yapılandırın** penceresinde, **Proje adı** kutusuna *HelloWorld* yazın veya girin. Ardından **Oluştur**' u seçin.

   ![' yeni projenizi yapılandırın ' penceresinde, projenizi ' HelloWorld ' olarak adlandırın](../get-started/csharp/media/vs-2019/csharp-name-your-aspnet-helloworld-project.png)

1. **Yeni ASP.NET Core Web uygulaması oluştur** penceresinde, **ASP.NET Core 2,1** ' ın üst açılan menüde göründüğünü doğrulayın. Ardından, örnek Razor Pages içeren **Web uygulaması**' nı seçin. Sonra **Oluştur**' u seçin.

   ![' Yeni ASP.NET Core Web uygulaması oluşturma ' penceresi](../get-started/csharp/media/vs-2019/csharp-create-aspnet-core-razor-pages-app.png)

   Visual Studio yeni projenizi açar.

::: moniker-end

## <a name="create-and-run-the-app"></a>Oluşturma ve uygulama çalıştırma

1. **Çözüm Gezgini**, **Sayfalar** klasörünü genişletin ve ardından **. cshtml**' yi seçin.

   ![Çözüm Gezgini'nden About.cshtml dosyayı seçin](../ide/media/csharp-aspnet-about-page-html-file.png)

   Bu dosya adında bir sayfaya karşılık gelen **hakkında** web uygulamasında, bir web tarayıcısında çalışan.

   ![Web uygulaması hakkında sayfası](../ide/media/csharp-aspnet-about-page.png)

   Düzenleyicide, **hakkında** sayfasının "ek bilgiler" alanı için HTML kodu görürsünüz.

   ![Visual Studio düzenleyicisinde ek bilgi alanı için HTML kodu](../ide/media/csharp-aspnet-about-cshtml-page.png)

1. "Ek bilgiler" metnini "**Merhaba Dünya!** " okumak için değiştirin.

   ![Visual Studio Düzenleyicisi 'nde ek bilgi alanı için varsayılan HTML kodunu değiştirme](../ide/media/csharp-aspnet-about-cshtml-page-hello-world.png)

1. İçinde **Çözüm Gezgini**, genişletme **About.cshtml**ve ardından **About.cshtml.cs**. (Bu dosya Ayrıca, bir Web tarayıcısında **hakkında hakkında** sayfasına karşılık gelir.)

   ![Çözüm Gezgini'nden About.cshtml dosyayı seçin](../ide/media/csharp-aspnet-about-page-code-file.png)

   Düzenleyicide, **hakkında** sayfasının "uygulama açıklaması C# " alanı için metin içeren kodu görürsünüz.

   ![Visual C# Studio düzenleyicisinde uygulama açıklaması alanı için kod](../ide/media/csharp-aspnet-about-cshtml-cs-code.png)

1. Okunacak "uygulama açıklaması" ileti metni değiştirme "**iletime nedir?** ".

   ![Visual Studio Düzenleyicisi 'nde uygulama açıklaması alanı için varsayılan ileti metnini değiştirme](../ide/media/csharp-aspnet-about-cshtml-cs-message.png)

1. Seçin **IIS Express** veya basın **Ctrl**+**F5** uygulamayı çalıştırın ve bir web tarayıcısında açın.

   ![Visual Studio 'da IIS Express düğmesini seçin](../ide/media/csharp-aspnet-helloworld-iisbutton.png)

   > [!NOTE]
   > Yazan bir hata iletisi alırsanız **web sunucusu için 'IIS Express' bağlanılamıyor**, veya bir SSL sertifikası ilgili bir hata iletisi Visual Studio'yu kapatın. Ardından, sağ tıklama bağlam menüsünde **yönetici olarak çalıştır** seçeneğini kullanarak Visual Studio 'yu açın. Ardından, uygulamayı yeniden çalıştırın.

1. Web tarayıcısında doğrulayın **hakkında** sayfa güncelleştirilmiş metni içerir.

   ![Yaptığınız değişiklikleri içeren güncelleştirilmiş hakkında sayfasını görüntüleyin](../ide/media/csharp-aspnet-about-page-hello-world.png)

1. Web tarayıcısını kapatın.

### <a name="review-your-work"></a>Çalışmanızı gözden geçirin

Önceki bölümde tamamladığınız işi denetlemek için aşağıdaki animasyonu görüntüleyin.

  ![Visual Studio 'da basit C# bir ASP.NET Core Web uygulaması oluşturmayı ve çalıştırmayı gösteren animasyonlu. gif dosyasını görüntüleme](../ide/media/csharp-aspnet-animated-hello-world.gif)

Bu hızlı başlangıcı tamamladığınızda Tebrikler! C#, ASP.NET Core ve Visual Studio IDE (tümleşik geliştirme ortamı) hakkında biraz öğrenilen umuyoruz.

## <a name="next-steps"></a>Sonraki adımlar

Daha fazla bilgi için şu öğreticiyle devam edin:

> [!div class="nextstepaction"]
> [C# ve Visual Studio'da ASP.NET kullanmaya başlama](../get-started/csharp/tutorial-aspnet-core.md)

## <a name="see-also"></a>Ayrıca bkz.

[Visual Studio kullanarak web uygulamanızı Azure App Service'e yayımlama](../deployment/quickstart-deploy-to-azure.md)
