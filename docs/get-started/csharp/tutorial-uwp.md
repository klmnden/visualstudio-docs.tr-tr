---
title: Visual Studio ile bir evrensel Windows Platformu (UWP) uygulaması oluşturma veC#
description: XAML ile Visual Studio'da bir UWP uygulaması oluşturma veC#
titleSuffix: ''
ms.custom: seodec18, get-started
ms.date: 03/23/2019
ms.technology: vs-ide-general
ms.topic: tutorial
ms.devlang: CSharp
author: TerryGLee
ms.author: tglee
manager: jillfra
dev_langs:
- CSharp
ms.workload:
- multiple
ms.openlocfilehash: cbb5eeaaa69852b43d2189c4ca9d308cff75ba98
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/17/2019
ms.locfileid: "59656166"
---
# <a name="tutorial-create-your-first-universal-windows-platform-application-in-visual-studio-with-xaml-and-c35"></a>Öğretici: Visual Studio'da XAML ve C ile Evrensel Windows platformu ilk uygulamanızı oluşturma&#35;

Visual Studio tümleşik geliştirme ortamı (IDE) bu giriş tüm Windows 10 cihazlarda çalışan bir "Hello World" uygulaması oluşturacaksınız. Evrensel Windows Platformu (UWP) proje şablonu, Extensible Application Markup Language (XAML) kullanacaksınız. Bunu yapmayı ve C# programlama dilidir.

::: moniker range="vs-2017"
Visual Studio henüz yüklemediyseniz, Git [Visual Studio indirmeleri](https://visualstudio.microsoft.com/vs/older-downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=vs+2017+download) ücretsiz yüklemek için sayfa.
::: moniker-end
::: moniker range="vs-2019"
Visual Studio henüz yüklemediyseniz, Git [Visual Studio indirmeleri](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2019) ücretsiz yüklemek için sayfa.
::: moniker-end

## <a name="create-a-project"></a>Proje oluşturma

İlk olarak, bir evrensel Windows platformu projesi oluşturun. Proje türü bile herhangi bir şey ekledik önce gereken tüm şablonu dosyalarıyla birlikte gelir!

::: moniker range="vs-2017"
1. Visual Studio'yu açın.

1. Üstteki menü çubuğundan seçin **dosya** > **yeni** > **proje**.

1. Sol bölmesinde **yeni proje** iletişim kutusunda **Visual C#** ve ardından **Windows Evrensel**. Orta bölmede seçin **boş uygulama (Evrensel Windows)**. Ardından, projeyi adlandırın *HelloWorld* ve **Tamam**.

   ![Visual Studio IDE'de yeni proje iletişim kutusunda Windows Evrensel bir proje şablonu](media/new-project-csharp-uwp-helloworld.png)

   > [!NOTE]
   > Görmüyorsanız **boş uygulama (Evrensel Windows)** proje şablonu, tıklayın **açık Visual Studio yükleyicisi** sol bölmesinde bağlantıyı **yeni proje** iletişim kutusu.<br><br>![Yeni Proje iletişim kutusundan açık Visual Studio yükleyicisi bağlantısına tıklayın](../../ide/media/vb-open-visual-studio-installer-hello-world.png)<br><br>Visual Studio Yükleyicisi'ni başlatır. Seçin **Evrensel Windows platformu geliştirme** iş yükü ve ardından **Değiştir**.<br><br>![Visual Studio Yükleyicisi'nde Evrensel Windows platformu geliştirme iş yükü](media/uwp-dev-workload.png)

1. Varsayılan değerleri kabul **hedef sürümü** ve **en düşük sürüm** ayarlarında **yeni evrensel Windows platformu projesi** iletişim kutusu.

   ![Varsayılan hedef sürümünü ve yeni evrensel Windows platformu projesi iletişim kutusunda en düşük sürüm ayarlarını kabul edin](media/new-uwp-project-target-minver-dialog.png)
::: moniker-end

::: moniker range=">=vs-2019"
1. Visual Studio'yu açın ve pencerenin başlangıç **yeni bir proje oluşturma**.

1. Üzerinde **yeni bir proje oluşturun** ekranında, girin *Evrensel Windows* arama kutusunda seçtiğiniz C# şablonu **boş uygulama (Evrensel Windows)** seçin **Sonraki**.

   ![Oluştur yeni bir proje ekran görüntüsü](media/vs-2019/uwp-create-new-project.png)

   > [!NOTE]
   > Görmüyorsanız **boş uygulama (Evrensel Windows)** proje şablonu, tıklayın **daha fazla araçları ve özellikleri yükleme** bağlantı.<br><br>![Daha fazla araçlarına ve özelliklerine bağlantı Yükle'ye tıklayın](media/vs-2019/uwp-not-finding.png)<br><br>Visual Studio Yükleyicisi'ni başlatır. Seçin **Evrensel Windows platformu geliştirme** iş yükü ve ardından **Değiştir**.<br><br>![Visual Studio Yükleyicisi'nde Evrensel Windows platformu geliştirme iş yükü](media/uwp-dev-workload.png)

1. Varsayılan değerleri kabul **hedef sürümü** ve **en düşük sürüm** ayarlarında **yeni evrensel Windows platformu projesi** iletişim kutusu.

   ![Varsayılan hedef sürümünü ve yeni evrensel Windows platformu projesi iletişim kutusunda en düşük sürüm ayarlarını kabul edin](media/vs-2019/new-uwp-project-target-minver-dialog.png)
::: moniker-end

   > [!NOTE]
   > Bu ilk kez ise bir UWP uygulaması oluşturmak için Visual Studio'yu kullandınız bir **ayarları** iletişim kutusu görünebilir. Seçin **Geliştirici modu**ve ardından **Evet**.<br><br>
   ![UWP Ayarları iletişim kutusunda geliştirici modunu etkinleştir](media/enable-developer-mode.png)<br><br>Visual Studio sizin için ek bir geliştirici modu paketi yükler. Paket yüklemesi tamamlandıktan sonra kapatın **ayarları** iletişim kutusu.

## <a name="create-the-application"></a>Uygulama oluşturma

Geliştirmeye başlamak için zaman var. Düğme denetimi ekleyin, düğme için eylem ekleme ve nasıl göründüğünü görmek için "Hello World" uygulamayı başlatın.

### <a name="add-a-button-to-the-design-canvas"></a>Bir düğme ekleyin tasarım tuvali

1. İçinde **Çözüm Gezgini**, çift *MainPage.xaml* bölünmüş bir görünüm açmak için.

   ::: moniker range="vs-2017"
   ![Çözüm Gezgini'nden mainpage.XAML dosyasını açın ](media/uwp-solution-explorer-MainPage-xaml.png)
   ::: moniker-end
   ::: moniker range=">=vs-2019"
   ![Çözüm Gezgini'nden mainpage.XAML dosyasını açın](media/vs-2019/uwp-solution-explorer-mainpage-xaml.png)
   ::: moniker-end

   İki bölme vardır: **XAML Tasarımcısı**, bir tasarım tuvali içerir ve **XAML Düzenleyicisi**, burada ekleyebilir veya kodu değiştirin.

   ![XAML Düzenleyicisi'nde XAML Tasarımcısı bölmesi](media/uwp-xaml-editor.png)

1. Seçin **araç kutusu** araç kutusu çıkış penceresini açmak için.

   ![Araç kutusu araç kutusu çıkış penceresini açmak için tıklayın](media/uwp-toolbox.png)

   (Görmüyorsanız **araç kutusu** seçeneği açabilirsiniz, menü çubuğundan. Bunu yapmak için **görünümü** > **araç**. Veya basın **Ctrl**+**Alt**+**X**.)

1. Tıklayın **PIN** araç kutusu penceresini sabitlemek için simge.

   ![Araç kutusu penceresini sabitlemek için Raptiye simgesine tıklayın](media/uwp-toolbox-autohide.png)

1. Tıklayın **düğmesi** denetlemek ve tasarım tuvale sürükleyin.

   ![Düğme denetimini tıklatın ve tasarım tuvale sürükleyin](media/uwp-toolbox-add-button-control.png)

   Kodda bakarsanız **XAML Düzenleyicisi**, düğmeyi, çok eklendiğini görürsünüz:

   ![Düğme denetimini tıklatın ve tasarım tuvale sürükleyin](media/uwp-xaml-control-code-window.png)

### <a name="add-a-label-to-the-button"></a>Düğme için bir etiket ekleyin

1. İçinde **XAML Düzenleyicisi**, düğme içerik değeri "Button" "Merhaba Dünya!" değiştirin.

   ![Değiştirme düğmesi içerik değeri Hello World](media/uwp-change-button-text-in-xaml-code-window.png)

1. Dikkat edin düğmede **XAML Tasarımcısı** çok değiştirir.

   ![Hello World tasarım Tuvali üzerindeki düğme değişiklikler](media/uwp-button-text-change-in-design-canvas.png)

### <a name="add-an-event-handler"></a>Bir olay işleyicisi ekleme

"Olay işleyicisi" sesleri karmaşık ancak bir olay meydana geldiğinde çağrılan kodu için başka bir ad değil. Bu durumda, "Hello World!" için bir eylem ekler düğmesi.

1. Tasarım Tuvali üzerindeki düğme denetimini çift tıklayın.

1. Olay işleyici kodu düzenleme *MainPage.xaml.cs*, arka plan kod sayfası.

   Burada ilginç işlerinizi aşağıda verilmiştir. Varsayılan olay işleyicisini şöyle görünür:

   ![Varsayılan Button_Click olay işleyicisi ](media/uwp-button-click-code.png)

   Şimdi şuna benzer şekilde, değiştirin:

   ![Yeni zaman uyumsuz Button_Click olay işleyicisi ](media/uwp-add-hello-world-async-code.png)

   Kopyalama ve yapıştırma için kod aşağıdaki gibidir:

   ```C#
   private async void Button_Click(object sender, RoutedEventArgs e)
         {
             MediaElement mediaElement = new MediaElement();
             var synth = new Windows.Media.SpeechSynthesis.SpeechSynthesizer();
             Windows.Media.SpeechSynthesis.SpeechSynthesisStream stream = await synth.SynthesizeTextToStreamAsync("Hello, World!");
             mediaElement.SetSource(stream, stream.ContentType);
             mediaElement.Play();
         }
   ```

#### <a name="what-did-we-just-do"></a>Hangi yalnızca işlemleri yaptık?

Kod bir konuşma sentezi nesnesi oluşturmak için bazı Windows API'leri kullanır ve ardından söylemek metin sağlar. (Daha fazla bilgi için `SpeechSynthesis`, bkz: <xref:System.Speech.Synthesis>.)

## <a name="run-the-application"></a>Uygulamayı çalıştırma

Bunu oluşturmanızı, dağıtmanızı ve ne göründüğünü ve benzer görmek için "Hello World" UWP uygulaması başlatma zamanı geldi. İşte nasıl.

1. Oynat düğmesini kullanın (metni içeren **yerel makine**) yerel makine üzerinde uygulamayı başlatmak için.

   ![Yerel makineye başlatmak ve UWP uygulamanızın hatalarını ayıklama için tıklayın](media/uwp-start-or-debug.png)

   (Alternatif olarak, seçebileceğiniz **hata ayıklama** > **hata ayıklamayı Başlat** menü çubuğu veya uygulamanızı başlatmak için F5 tuşuna basın.)

1. Giriş ekranı yakında kaybolur sonra görüntülenen uygulamanızı görüntüleyin. Uygulama şuna benzer görünmelidir:

   ![Bir UWP uygulaması "Merhaba Dünya"](media/uwp-hello-world-app.png)

1. Tıklayın **Hello World** düğmesi.

   Windows 10 cihaz kilit ekranında tam anlamıyla, "Hello, World!"

1. Uygulamayı kapatmak için tıklayın **hata ayıklamayı Durdur** araç çubuğu düğmesi. (Alternatif olarak, seçin **hata ayıklama** > **hata ayıklamayı durdurmak** menü çubuğu veya Shift + F5 tuşuna basın.)

## <a name="next-steps"></a>Sonraki adımlar

Bu öğreticiyi tamamlamak Tebrikler! UWP ve Visual Studio IDE ile ilgili bazı temel konuları öğrendiğinize göre umuyoruz. Daha fazla bilgi edinmek için aşağıdaki öğreticiyle devam edin:

> [!div class="nextstepaction"]
> [Bir kullanıcı arabirimi oluşturma](/windows/uwp/design/basics/xaml-basics-ui)