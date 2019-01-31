---
description: XAML ile Visual Studio'da bir UWP uygulaması oluşturma veC#
titleSuffix: ''
ms.custom: seodec18, get-started
ms.date: 04/04/2018
ms.prod: visual-studio-dev15
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
ms.openlocfilehash: 63ef768b0279d1859972bd3a5b49242fe549cea7
ms.sourcegitcommit: 9866740aec05d1a3a5dc3b4b6d2ceaeecbd3fc29
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55424440"
---
# <a name="tutorial-create-your-first-universal-windows-platform-application-in-visual-studio-with-xaml-and-c35"></a>Öğretici: Visual Studio'da XAML ve C ile Evrensel Windows platformu ilk uygulamanızı oluşturma&#35;

Bu 5-10 dakikalık bir giriş Visual Studio tümleşik geliştirme ortamı (IDE), tüm Windows 10 cihazlarda çalışan bir "Hello World" uygulaması oluşturacaksınız. Evrensel Windows Platformu (UWP) proje şablonu, Extensible Application Markup Language (XAML) kullanacaksınız. Bunu yapmayı ve C# programlama dilidir.

Visual Studio henüz yüklemediyseniz, Git [Visual Studio indirmeleri](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2017) ücretsiz yüklemek için sayfa.

## <a name="create-a-project"></a>Proje oluşturma

İlk olarak, bir evrensel Windows platformu projesi oluşturun. Proje türü bile herhangi bir şey ekledik önce gereken tüm şablonu dosyalarıyla birlikte gelir!

1. Visual Studio 2017'yi açın.

2. Üstteki menü çubuğundan seçin **dosya** > **yeni** > **proje**.

3. Sol bölmesinde **yeni proje** iletişim kutusunda **Visual C#** ve ardından **Windows Evrensel**. Orta bölmede seçin **boş uygulama (Evrensel Windows)**. Ardından, projeyi adlandırın *HelloWorld* ve **Tamam**.

   ![Visual Studio IDE'de yeni proje iletişim kutusunda Windows Evrensel bir proje şablonu](media/new-project-csharp-uwp-helloworld.png)

   > [!NOTE]
   > Görmüyorsanız **boş uygulama (Evrensel Windows)** proje şablonu, tıklayın **açık Visual Studio yükleyicisi** sol bölmesinde bağlantıyı **yeni proje** iletişim kutusu.<br><br>![Yeni Proje iletişim kutusundan açık Visual Studio yükleyicisi bağlantısına tıklayın](../../ide/media/vb-open-visual-studio-installer-hello-world.png)<br><br>Visual Studio Yükleyicisi'ni başlatır. Seçin **Evrensel Windows platformu geliştirme** iş yükü ve ardından **Değiştir**.<br><br>![Visual Studio Yükleyicisi'nde Evrensel Windows platformu geliştirme iş yükü](media/uwp-dev-workload.png)

4. Zaman **yeni evrensel Windows platformu projesi** iletişim kutusu görüntülenirse, seçin **Tamam**.

   ![Varsayılan hedef sürümünü ve yeni evrensel Windows platformu projesi iletişim kutusunda en düşük sürüm ayarlarını kabul edin](media/new-uwp-project-target-minver-dialog.png)

   > [!NOTE]
   > Bu ilk kez ise bir UWP uygulaması oluşturmak için Visual Studio'yu kullandınız bir **ayarları** iletişim kutusu görünebilir. Seçin **Geliştirici modu**ve ardından **Evet**.<br><br>
   ![UWP Ayarları iletişim kutusunda geliştirici modunu etkinleştir](media/enable-developer-mode.png)<br><br>Visual Studio sizin için ek bir geliştirici modu paketi yükler. Paket yüklemesi tamamlandıktan sonra kapatın **ayarları** iletişim kutusu.

## <a name="create-the-application"></a>Uygulama oluşturma

Geliştirmeye başlamak için zaman var. Düğme denetimi ekleyin, düğme için eylem ekleme ve nasıl göründüğünü görmek için "Hello World" uygulamayı başlatın.

### <a name="add-a-button-to-the-design-canvas"></a>Bir düğme ekleyin tasarım tuvali

1. İçinde **Çözüm Gezgini**, çift *MainPage.xaml* bölünmüş bir görünüm açmak için.

   ![Çözüm Gezgini'nden mainpage.XAML dosyasını açın ](media/uwp-solution-explorer-MainPage-xaml.png)

   İki bölme vardır: **XAML Tasarımcısı**, bir tasarım tuvali içerir ve **XAML Düzenleyicisi**, burada ekleyebilir veya kodu değiştirin.

   ![XAML Düzenleyicisi'nde XAML Tasarımcısı bölmesi](media/uwp-xaml-editor.png)

2. Seçin **araç kutusu** araç kutusu çıkış penceresini açmak için.

   ![Araç kutusu araç kutusu çıkış penceresini açmak için tıklayın](media/uwp-toolbox.png)

   (Görmüyorsanız **araç kutusu** seçeneği açabilirsiniz, menü çubuğundan. Bunu yapmak için **görünümü** > **araç**. Veya basın **Ctrl**+**Alt**+**X**.)

3. Tıklayın **PIN** araç kutusu penceresini sabitlemek için simge.

   ![Araç kutusu penceresini sabitlemek için Raptiye simgesine tıklayın](media/uwp-toolbox-autohide.png)

4. Tıklayın **düğmesi** denetlemek ve tasarım tuvale sürükleyin.

   ![Düğme denetimini tıklatın ve tasarım tuvale sürükleyin](media/uwp-toolbox-add-button-control.png)

   Kodda bakarsanız **XAML Düzenleyicisi**, düğmeyi, çok eklendiğini görürsünüz:

   ![Düğme denetimini tıklatın ve tasarım tuvale sürükleyin](media/uwp-xaml-control-code-window.png)

### <a name="add-a-label-to-the-button"></a>Düğme için bir etiket ekleyin

1. İçinde **XAML Düzenleyicisi**, düğme içerik değeri "Button" "Merhaba Dünya!" değiştirin.

   ![Değiştirme düğmesi içerik değeri Hello World](media/uwp-change-button-text-in-xaml-code-window.png)

2. Dikkat edin düğmede **XAML Tasarımcısı** çok değiştirir.

   ![Hello World tasarım Tuvali üzerindeki düğme değişiklikler](media/uwp-button-text-change-in-design-canvas.png)

### <a name="add-an-event-handler"></a>Bir olay işleyicisi ekleme

"Olay işleyicisi" sesleri karmaşık ancak bir olay meydana geldiğinde çağrılan kodu için başka bir ad değil. Bu durumda, "Hello World!" için bir eylem ekler düğmesi.

1. Tasarım Tuvali üzerindeki düğme denetimini çift tıklayın.

2. Olay işleyici kodu düzenleme *MainPage.xaml.cs*, arka plan kod sayfası.

   Burada ilginç işlerinizi budur. Varsayılan olay işleyicisini şöyle görünür:

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

1. Seçin **yerel makine** uygulamayı başlatmak için.

   ![Yerel makineye başlatmak ve UWP uygulamanızın hatalarını ayıklama için tıklayın](media/uwp-start-or-debug.png)

   (Alternatif olarak, seçebileceğiniz **hata ayıklama** > **hata ayıklamayı Başlat** basın ya da menü çubuğu **F5** uygulamanızı başlatmak için.)

2. Giriş ekranı yakında kaybolur sonra görüntülenen uygulamanızı görüntüleyin. Uygulama şuna benzer görünmelidir:

   ![Bir UWP uygulaması "Merhaba Dünya"](media/uwp-hello-world-app.png)

3. Tıklayın **Hello World** düğmesi.

   Windows 10 cihaz kilit ekranında tam anlamıyla, "Hello, World!"

4. Uygulamayı kapatmak için tıklayın **hata ayıklamayı Durdur** araç çubuğu düğmesi. (Alternatif olarak, seçin **hata ayıklama** > **hata ayıklamayı durdurmak** tuşuna basın veya menü çubuğu **Shift**+**F5**.)

## <a name="next-steps"></a>Sonraki adımlar

Bu hızlı başlangıcı tamamladığınızda Tebrikler! UWP ve Visual Studio IDE ile ilgili bazı temel konuları öğrendiğinize göre umuyoruz. Daha fazla bilgi edinmek için aşağıdaki öğreticiyle devam edin:

> [!div class="nextstepaction"]
> [Bir kullanıcı arabirimi oluşturma](/windows/uwp/design/basics/xaml-basics-ui)
