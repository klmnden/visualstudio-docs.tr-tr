---
title: 'Öğretici: Kullanmaya başlama C# ve ASP.NET Core'
titleSuffix: ''
description: Visual Studio'da C# ile adım adım ASP.NET Core web uygulaması oluşturmayı öğrenin.
ms.custom: seodec18, get-started
ms.date: 03/23/2019
ms.technology: vs-ide-general
ms.prod: visual-studio-windows
ms.topic: tutorial
ms.devlang: CSharp
author: TerryGLee
ms.author: tglee
manager: jillfra
dev_langs:
- CSharp
ms.workload:
- aspnet
- dotnetcore
ms.openlocfilehash: 191be9ea5433351f6f89366cc2240d8b0801e54b
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60111733"
---
# <a name="tutorial-get-started-with-c-and-aspnet-core-in-visual-studio"></a>Öğretici: C# ve Visual Studio'da ASP.NET Core ile çalışmaya başlama

Visual Studio kullanarak ASP.NET Core ile C# geliştirme için Bu öğreticide, bir C# ASP.NET Core web uygulaması oluşturma, değişiklik, bazı IDE özelliklerini ve sonra uygulamayı çalıştırın.

## <a name="before-you-begin"></a>Başlamadan önce

### <a name="install-visual-studio"></a>Visual Studio'yu yükleme

::: moniker range="vs-2017"

Visual Studio henüz yüklemediyseniz, Git [Visual Studio indirmeleri](https://visualstudio.microsoft.com/vs/older-downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=vs+2017+download) ücretsiz yüklemek için sayfa.

::: moniker-end

::: moniker range="vs-2019"

Visual Studio henüz yüklemediyseniz, Git [Visual Studio indirmeleri](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2019) ücretsiz yüklemek için sayfa.

::: moniker-end

### <a name="update-visual-studio"></a>Visual Studio’yu güncelleştirme

Visual Studio'yu önceden yüklediyseniz, en son sürümü çalıştırdığınızdan emin olun. Yüklemenizi güncelleştirme hakkında daha fazla bilgi için bkz. [Visual Studio en son sürüme güncelleştirme](../../install/update-visual-studio.md) sayfası.

### <a name="choose-your-theme-optional"></a>(İsteğe bağlı) temanızı seçin

Bu öğretici, koyu Tema kullanan ekran görüntüleri içerir. Koyu tema kullanmayan ancak öğrenmek istiyorsanız [Düzenleyicisi ve Visual Studio IDE'yi kişiselleştirme](../../ide/quickstart-personalize-the-ide.md) öğrenmek için sayfa nasıl.

## <a name="create-a-project"></a>Proje oluşturma

İlk olarak, bir ASP.NET Core projesi oluşturacaksınız. Proje türü bile herhangi bir şey ekledik önce tam olarak işlevsel bir Web sitesi için ihtiyacınız olacak tüm şablonu dosyalarıyla birlikte gelir!

::: moniker range="vs-2017"

1. Visual Studio 2017'yi açın.

2. Üstteki menü çubuğundan seçin **dosya** > **yeni** > **proje**.

3. İçinde **yeni proje** iletişim kutusunun sol bölmesinde, **Visual C#**, genişletin **Web**ve ardından **.NET Core**. Orta bölmede seçin **ASP.NET Core Web uygulaması**. Dosya adı *MyCoreApp* ve **Tamam**.

   ![Visual Studio IDE'de yeni proje iletişim kutusundaki ASP.NET Core Web uygulaması proje şablonu](media/csharp-aspnet-choose-template-name-razor-mycoreapp-file.png)

### <a name="add-a-workload-optional"></a>(İsteğe bağlı) bir iş yükü Ekle

Görmüyorsanız **ASP.NET Core Web uygulaması** proje şablonu, alabilirsiniz, ekleyerek **ASP.NET ve web geliştirme** iş yükü. Bu iş yükü, makinenizde yüklü Visual Studio 2017 güncelleştirmeleri bağlı olarak iki aşağıdaki yollardan biriyle ekleyebilirsiniz.

#### <a name="option-1-use-the-new-project-dialog-box"></a>1. seçenek: Yeni Proje iletişim kutusunu kullanın

1. Seçin **açık Visual Studio yükleyicisi** sol bölmesinde bağlantıyı **yeni proje** iletişim kutusu. (Görünen ayarlarınıza bağlı olarak, görmek için kaydırmanız gerekebilir.)

   ![Yeni Proje iletişim kutusundan açık Visual Studio yükleyicisi bağlantıyı seçin](../media/open-visual-studio-installer-mycoreapp.png)

1. Visual Studio Yükleyicisi'ni başlatır. Seçin **ASP.NET ve web geliştirme** iş yükü ve ardından **Değiştir**.

   ![.NET core çoklu platform geliştirme iş yükünü Visual Studio yükleyicisi](../media/tutorial-aspnet-workload.png)

   (Yeni iş yükünü yüklemek devam etmeden önce Visual Studio'yu kapatın gerekebilir.)

#### <a name="option-2-use-the-tools-menu-bar"></a>2. seçenek: Araçlar menü çubuğunu kullanın

1. / İptal **yeni proje** iletişim kutusu. Ardından, üstteki menü çubuğundan **Araçları** > **araçları ve özellikleri Al**.

1. Visual Studio Yükleyicisi'ni başlatır. Seçin **ASP.NET ve web geliştirme** iş yükü ve ardından **Değiştir**.

   (Yeni iş yükünü yüklemek devam etmeden önce Visual Studio'yu kapatın gerekebilir.)

### <a name="add-a-project-template"></a>Bir proje şablonu Ekle

1. İçinde **yeni ASP.NET Core Web uygulaması** iletişim kutusunda **Web uygulaması** proje şablonu.

1. Doğrulayın **ASP.NET Core 2.1** üstteki açılan menüde görünür. Ardından, **Tamam**.

   ![Yeni ASP.NET Core Web uygulaması iletişim kutusu](media/new-project-csharp-aspnet-razor-web-app.png)

   > [!NOTE]
   > Görmüyorsanız **ASP.NET Core 2.1** veya daha sonra üstteki açılan menüden Visual Studio'nun en son sürümü çalıştırdığınızdan emin olun. Yüklemenizi güncelleştirme hakkında daha fazla bilgi için bkz. [Visual Studio en son sürüme güncelleştirme](../../install/update-visual-studio.md) sayfası.

::: moniker-end

::: moniker range="vs-2019"

1. Pencerenin başlangıç seçin **yeni bir proje oluşturma**.

   !['Yeni Proje oluştur' penceresini görüntüleyin](../../get-started/media/vs-2019/create-new-project-dark-theme.png)

1. Üzerinde **yeni bir proje oluşturma** penceresinde girin veya yazın *ASP.NET* arama kutusuna. Ardından, **C#** dilden listeleyin ve ardından **Windows** Platform listesinde. 

   Tüm dil ve platform filtreleri uyguladıktan sonra seçin **ASP.NET Core Web uygulaması** şablonu seçip **sonraki**.

   ![Seçin C# ASP.NET Core Web uygulaması şablonu](./media/vs-2019/csharp-create-new-project-search-aspnet-core-filtered.png)

   > [!NOTE]
   > Görmüyorsanız, **ASP.NET Core Web uygulaması** şablon yükleyebileceğiniz buradan **yeni bir proje oluşturma** penceresi. İçinde **aradığınızı bulamadınız?** message öğesini **daha fazla araçları ve özellikleri yükleme** bağlantı.
   >
   > !['Daha fazla araçları ve özellikleri yükleme' bağlantı 'Yeni Proje oluştur' penceresinde 'aradığınızı bulma yok' iletisi](../../get-started/media/vs-2019/not-finding-what-looking-for.png) 
   > 
   > Ardından, Visual Studio yükleyicisinde **ASP.NET ve web geliştirme** iş yükü.
   >
   > ![.NET core çoklu platform geliştirme iş yükünü Visual Studio yükleyicisi](../../get-started/media/aspnet-core-web-dev-workload.png)
   >
   > Bundan sonra seçin **Değiştir** Visual Studio Yükleyicisi'nde düğmesi. Çalışmanızı kaydetmek için istenebilir; Bu durumda, bunu yapın. Ardından, **devam** iş yükünü yüklemek için. Ardından, 2. adım bu dönün "[proje oluşturma](#create-a-project)" yordamı.

1. İçinde **yeni projenizi yapılandırın** penceresinde yazın veya girin *MyCoreApp* içinde **proje adı** kutusu. Ardından, **Oluştur**.

   !['yeni projenizi yapılandırın' penceresinde 'MyCoreApp' projenizi adlandırın](./media/vs-2019/csharp-name-your-aspnet-mycoreapp-project.png)

1. İçinde **yeni bir ASP.NET Core Web uygulaması oluşturma** penceresinde doğrulayın **ASP.NET Core 2.1** veya daha sonra üstteki açılan menüde görünür. Ardından, **Web uygulaması**, örnek Razor sayfaları içerir. Ardından, **Oluştur**.

   !['Yeni bir ASP.NET Core Web uygulaması oluştur' penceresi](./media/vs-2019/csharp-create-aspnet-core-razor-pages-app.png)

   Yeni projeniz Visual Studio açılır.

::: moniker-end

### <a name="about-your-solution"></a>Çözümünüzü hakkında

Bu çözüm aşağıdaki **Razor sayfası** tasarım deseni. Farklı [Model-View-Controller (MVC)](/aspnet/core/tutorials/first-mvc-app/start-mvc?view=aspnetcore-2.1&tabs=aspnetcore2x) tasarım deseni, kolaylaştırılmış kendi kendini Razor sayfası içindeki model ve denetleyici kod eklemek için.

## <a name="tour-your-solution"></a>Çözümünüzü turuna katılın

 1. Proje şablonu, bir çözüm ile adlı bir tek bir ASP.NET Core projesi oluşturur. _MyCoreApp_. Seçin **Çözüm Gezgini** içeriğini görüntülemek için sekmesinde.

    ![MyCoreApp adlı Razor sayfaları çözümü için Visual Studio'da ASP.NET Çözüm Gezgini](media/csharp-aspnet-razor-solution-explorer-mycoreapp.png)

 1. Genişletin **sayfaları** klasörünü ve ardından *About.cshtml*.

     ![Visual Studio'daki Çözüm Gezgini'nde About.cshtml dosyasında](media/csharp-aspnet-razor-solution-explorer-aboutcshtml.png)

 1. Görünüm **About.cshtml** dosyasını Kod düzenleyicisinde.

     ![Visual Studio Kod Düzenleyicisi'nde About.cshtml dosyasını görüntüleyin](media/csharp-aspnet-razor-aboutcshtml-mycoreapp-code.png)

 1. Seçin **About.cshtml.cs** dosya.

     ![Visual Studio Kod Düzenleyicisi'nde About.cshtml.cs dosyayı seçin](media/csharp-aspnet-razor-solution-explorer-aboutcshtmlcs.png)

 1. Görünüm **About.cshtml.cs** dosyasını Kod düzenleyicisinde.

     ![Visual Studio Kod Düzenleyicisi'nde About.cshtml dosyasını görüntüleyin](media/csharp-aspnet-razor-aboutcshtmlcs-mycoreapp-code.png)

 1. Projeyi içeren bir **wwwroot** Web siteniz için kök klasör. İçindekileri görüntülemek için klasörünü genişletin.

     ![Visual Studio'daki Çözüm Gezgini'nde Wwwroot klasörü](media/csharp-aspnet-razor-solution-explorer-wwwroot.png)

    Statik içerik koyabilirsiniz&mdash;CSS, görüntü ve JavaScript kitaplıkları gibi&mdash;doğrudan istediğiniz bunları yollarda.

 1. Proje, ayrıca çalışma zamanında web uygulamasını yönetme, yapılandırma dosyalarını içerir. Varsayılan uygulama [yapılandırma](/aspnet/core/fundamentals/configuration) depolanan *appsettings.json*. Ancak, bu ayarları kullanarak geçersiz kılabilirsiniz *appsettings. Development.JSON*. Genişletin **appsettings.json** görüntülemek için dosya **appsettings. Development.JSON** dosya.

     ![Visual Studio'daki Çözüm Gezgini'nde yapılandırma dosyaları](media/csharp-aspnet-razor-solution-explorer-appsettingsjson.png)

## <a name="run-debug-and-make-changes"></a>Çalıştırma, hata ayıklama ve değişiklik

1. Seçin **IIS Express** oluşturmak ve uygulamayı hata ayıklama modunda çalıştırmak için IDE'de düğmesi. (Alternatif olarak, basın **F5**, ya da seçin **hata ayıklama** > **hata ayıklamayı Başlat** menü çubuğundan.)

     ![Visual Studio'da IIS Express düğmeyi seçin](media/csharp-aspnet-razor-iisexpress.png)

     > [!NOTE]
     > Bildiren bir hata iletisi alırsanız **web sunucusu için 'IIS Express' bağlanılamıyor**, Visual Studio'yu kapatın ve ardından kullanarak açın **yönetici olarak çalıştır** sağ tıklayın veya bağlam menüsünde seçenek. Ardından, uygulamayı yeniden çalıştırın.
     >
     > Ayrıca, bir IIS Express SSL sertifikası kabul etmek isteyip istemediğinizi soran bir ileti alabilirsiniz. Kodu bir web tarayıcısında, görüntülemeyi **Evet**ve ardından **Evet** güvenlik izleme uyarı iletisi alırsanız. 

1. Visual Studio, bir tarayıcı penceresi açar. Ardından görmelisiniz **giriş**, **hakkında**, ve **kişi** menü çubuğundaki sayfaları. (Bunu yapmazsanız, bunları görüntülemek için bir "hamburger" menü öğesini seçin.)

    ![Web uygulamanıza menü çubuğundan "hamburger" menü öğesini seçin.](media/csharp-aspnet-razor-browser-page.png)

     > [!TIP]
     > Projenize bir tarayıcı penceresinde açtığınızda Visual Studio Kod düzenleyicisinde kod düzenlenemiyor. 

1. Seçin **hakkında** menü çubuğundan.

   ![Uygulamanız için tarayıcı penceresinin menü çubuğundaki hakkında seçin](media/csharp-aspnet-razor-browser-page-about-menu.png)

   Başka şeylerin yanında **hakkında** sayfasını tarayıcıda işler ayarlanmış olan metin *About.cshtml* dosya.

   ![Hakkında sayfasında metin görüntüleme](media/csharp-aspnet-razor-browser-page-about.png)

1. Tarayıcı penceresi açın ve geri dönüş için Visual Studio tutun.

1. Visual Studio'da **About.cshtml**. Sonra Sil _ek_ ve bunun yerine, sözcükleri ekleme _dosya ve dizin_.

    ![About.cshtml dosyadaki metni değiştirme](media/csharp-aspnet-razor-aboutcshtml-mycoreapp-code-changed.png)

1. Seçin **About.cshtml.cs**. Ardından, temizleme `using` aşağıdaki kısayolunu kullanarak dosyanın üst kısmındaki yönergeleri:

   Grileştirilmiş birini `using` yönergeleri ve [hızlı Eylemler](../../ide/quick-actions.md) ampul hemen altına giriş işaretinin veya sol kenar boşluğunda görünür. Ampule ve ardından seçin **gereksiz kullanımları Kaldır**.

   ![About.cshtml.cs dosyasında gereksiz kullanımları Kaldır](media/csharp-aspnet-razor-remove-unnecessary-usings.png)

     Visual Studio siler gereksiz `using` dosyasındaki yönergeleri.

1. Ardından `OnGet()` yöntem gövdesi aşağıdaki kodla değiştirin:

     ```csharp
     public void OnGet()
     {
         string directory = Environment.CurrentDirectory;
     Message = String.Format("Your directory is {0}.", directory);
     }
    ```

1. İki dalgalı alt çizgiler altında göründüğünü fark **ortam** ve **dize**. Bu türleri kapsamındaki olmadığından dalgalı alt çizgiler görünür.

   ![Dalgalı alt çizgiler OnGet yöntemi olarak ile işaretlenen hataları](media/csharp-aspnet-razor-add-new-on-get-method.png)

    Açık **hata listesi** aynı hatalar görmeniz için araç çubuğunda listelenen vardır. (Görmüyorsanız **hata listesi** araç seçin **görünümü** > **hata listesi** üst menü çubuğundan.)

   ![Visual Studio hata listesi](media/csharp-aspnet-razor-error-list.png)

1. Şimdi bunu düzeltelim. Kod düzenleyicisinde, imlecinizin hatayı içeren ya da satıra yerleştirin ve hızlı Eylemler ampul sol kenar boşluğunda seçin. Ardından açılan menüden seçin **sistemiyle;** bu yönerge dosyanızın en üstüne ekleyin ve hataları giderin.

   ![Ekleme "Sistem; kullanma" yönergesi](media/csharp-aspnet-razor-add-usings.png)

1. Tuşuna **Ctrl**+**S** yaptığınız değişiklikleri kaydetmek ve web tarayıcısında uygulamanızı yenileyin.

1. Web sitesinin en üstünde **hakkında** yaptığınız değişiklikleri görmek için.

   ![Yaptığınız değişiklikleri içeren sayfasında hakkında güncelleştirilmiş görüntüleyin](media/csharp-aspnet-razor-browser-page-about-changed.png)

1. Kapat tuşuna web tarayıcısı **Shift**+**F5** hata ayıklama modunu durdurmak ve ardından Visual Studio'yu kapatın.

## <a name="quick-answers-faq"></a>Hızlı yanıtlar hakkında SSS

İşte bazı temel kavramları vurgulamak için hızlı bir SSS.

### <a name="what-is-c"></a>C# nedir?

[C#](/dotnet/csharp/getting-started/introduction-to-the-csharp-language-and-the-net-framework) sağlam ve öğrenmesi kolay olacak şekilde tasarlanan bir tür kullanımı uyumlu ve nesne yönelimli programlama dilidir.

### <a name="what-is-aspnet-core"></a>ASP.NET Core nedir?

ASP.NET Core web uygulamaları ve hizmetler gibi İnternet'e bağlı uygulamalar oluşturmaya yönelik açık kaynaklı ve platformlar arası bir çerçevedir. .NET Core veya .NET Framework üzerinde ASP.NET Core uygulamaları çalıştırabilirsiniz. Geliştirin ve Windows, Mac ve Linux'ta ASP.NET Core uygulamaları platformlar arası çalıştırın. ASP.NET Core, açık kaynak konumunda [GitHub](https://github.com/aspnet/home).

### <a name="what-is-visual-studio"></a>Visual Studio nedir?

Visual Studio geliştiricileri için üretkenlik aracından oluşan bir tümleşik geliştirme paketidir. Bunu, programları ve uygulamaları oluşturmak için kullanabileceğiniz bir program olarak düşünün.

## <a name="next-steps"></a>Sonraki adımlar

Bu öğreticiyi tamamlamak Tebrikler! C#, ASP.NET Core ve Visual Studio IDE hakkında biraz öğrenilen umuyoruz. C# ve ASP.NET ile web uygulaması veya Web sitesi oluşturma hakkında daha fazla bilgi edinmek için şu öğretici ile devam edin:

> [!div class="nextstepaction"]
> [ASP.NET Core Razor sayfaları web uygulaması oluşturma](/aspnet/core/tutorials/razor-pages/?view=aspnetcore-2.1)

## <a name="see-also"></a>Ayrıca bkz.

[Visual Studio kullanarak web uygulamanızı Azure App Service'e yayımlama](../../deployment/quickstart-deploy-to-azure.md)
