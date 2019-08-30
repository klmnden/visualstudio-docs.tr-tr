---
title: İçinde WPF ile uygulama Merhaba DünyaC#
description: Windows Presentation Foundation (WPF) Kullanıcı arabirimi çerçevesini kullanarak C# Visual Studio ile basit bir Windows Masaüstü .NET uygulaması oluşturun.
ms.custom: seodec18, get-started
ms.date: 08/09/2019
ms.prod: visual-studio-windows
ms.technology: vs-ide-general
ms.topic: conceptual
dev_langs:
- CSharp
ms.assetid: f84339c7-d617-4f56-bfcd-af2215c347ba
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- dotnet
ms.openlocfilehash: d146416190924c8f1835ef17bc0fb622fcc53e03
ms.sourcegitcommit: 44e9b1d9230fcbbd081ee81be9d4be8a485d8502
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/30/2019
ms.locfileid: "70180221"
---
# <a name="tutorial-create-a-simple-application-with-c"></a>Öğretici: C ile basit bir uygulama oluşturma\#

Bu öğreticiyi tamamlayarak, Visual Studio ile uygulama geliştirirken kullanabileceğiniz birçok araç, iletişim kutusu ve tasarımcı hakkında bilgi sahibi olacaksınız. Tümleşik geliştirme ortamında ([IDE](visual-studio-ide.md)) çalışmayı öğrenirken, "Merhaba, Dünya" uygulaması, Kullanıcı arabirimini tasarlayacağınız, kod ekleyerek ve hata ayıkladığınızda bir "Hello, World" uygulaması oluşturacaksınız.

::: moniker range="vs-2017"
Visual Studio henüz yüklemediyseniz, Git [Visual Studio indirmeleri](https://visualstudio.microsoft.com/vs/older-downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=vs+2017+download) ücretsiz yüklemek için sayfa.
::: moniker-end
::: moniker range=">=vs-2019"
Visual Studio henüz yüklemediyseniz, Git [Visual Studio indirmeleri](https://visualstudio.microsoft.com/downloads) ücretsiz yüklemek için sayfa.
::: moniker-end

## <a name="configure-the-ide"></a>IDE'yi yapılandırma

::: moniker range="vs-2017"

Visual Studio 'Yu ilk kez açtığınızda, oturum açmanız istenir. Bu adım, bu öğretici için isteğe bağlıdır. Ardından, geliştirme ayarlarınızı ve renk temasını seçmenizi isteyen bir iletişim kutusu görüntülenebilir. Varsayılanları koruyun ve **Visual Studio 'Yu Başlat**' ı seçin.

![Ayarları Seç iletişim kutusu](../media/exploreide-settings.png)

Visual Studio başlatıldıktan sonra araç pencerelerini, menüleri ve araç çubuklarını ve ana pencere alanını görürsünüz. Araç pencereleri, **Hızlı Başlat**, menü çubuğu ve en üstteki Standart araç çubuğu ile uygulama penceresinin sol ve sağ taraflarına yerleştirilir. Uygulama penceresinin merkezinde **Başlangıç sayfası**bulunur. Bir çözüm veya proje yüklediğinizde, düzenleyiciler ve tasarımcılar **Başlangıç sayfasının** bulunduğu alanda görüntülenir. Bir uygulama geliştirirken, bu merkezi alanda zamanınızın çoğunu harcarcaksınız.

![Genel ayarlar uygulanmış şekilde Visual Studio 2017 IDE](../media/exploreide-idewithgeneralsettings.png "Genel ayarların uygulanmış olduğu Visual Studio 2017 IDE ekran görüntüsü")

::: moniker-end

::: moniker range=">=vs-2019"

Visual Studio 'Yu başlattığınızda ilk olarak başlangıç penceresi açılır. Geliştirme ortamını açmak için **kod olmadan devam et** ' i seçin. Araç pencerelerini, menüleri ve araç çubuklarını ve ana pencere alanını görürsünüz. Araç pencereleri, uygulama penceresinin sol ve sağ taraflarından, bir arama kutusuyla, menü çubuğundan ve en üstteki Standart araç çubuğundan yerleştirildi. Bir çözüm veya proje yüklediğinizde, düzenleyiciler ve tasarımcılar uygulama penceresinin orta alanında görüntülenir. Bir uygulama geliştirirken, bu merkezi alanda zamanınızın çoğunu harcarcaksınız.

::: moniker-end

## <a name="create-the-project"></a>Projeyi oluşturma

Visual Studio'da bir uygulama oluştururken önce bir proje ve bir çözüm oluşturursunuz. Bu örnekte, bir Windows Presentation Foundation (WPF) projesi oluşturacaksınız.

::: moniker range="vs-2017"

1. Yeni bir proje oluşturun. Menü çubuğunda **Dosya** > **Yeni** > **Proje**' yi seçin.

     ![Menü çubuğunda dosya, yeni, proje ' yi seçin.](../media/exploreide-filenewproject.png "Dosya, yeni, proje ' yi seçtiğiniz menü çubuğunun ekran görüntüsü")

1. **Yeni proje** iletişim kutusunda, **yüklü** > olan  > **Visual C#**  **Windows Masaüstü** kategorisini seçin ve ardından **WPF uygulaması (.NET Framework)** şablonunu seçin. Projeyi **HelloWPFApp**olarak adlandırın ve **Tamam**' ı seçin.

     ![Visual Studio 'Da WPF uygulama şablonu yeni proje iletişim kutusu](media/exploreide-newprojectcsharp.png "Yeni proje iletişim kutusunda WPF uygulama şablonunun ekran görüntüsü")

::: moniker-end

::: moniker range="vs-2019"

1. Visual Studio 2019 ' i açın.

1. Başlangıç penceresinde **Yeni proje oluştur**' u seçin.

   ![' Yeni proje oluştur ' penceresini görüntüleyin](../../get-started/media/vs-2019/start-window-create-new-project.png "' Yeni proje oluştur ' penceresinin ekran görüntüsü")

1. **Yeni proje oluştur** ekranında, "WPF" araması yapın **wpf uygulaması (.NET Framework)** öğesini seçin ve ardından **İleri**' yi seçin.

   ![' Yeni proje oluştur ' iletişim kutusunda WPF uygulama şablonu](media/vs-2019/exploreide-newprojectcsharp-vs2019.png "' Yeni proje oluştur ' iletişim kutusunda WPF uygulama şablonunun ekran görüntüsü")

1. Sonraki ekranda, projeye **HelloWPFApp**adını verin ve **Oluştur**' u seçin.

   ![Projenizin ' HelloWPFApp ' olarak adlandırın](./media/vs-2019/exploreide-nameproject.png "Projenizin adını girdiğiniz pencerenin ekran görüntüsü")

::: moniker-end

Visual Studio HelloWPFApp projesini ve çözümünü oluşturur ve **Çözüm Gezgini** çeşitli dosyaları gösterir. **WPF Tasarımcısı** , bölünmüş bir görünümde *MainWindow. xaml* ' in BIR Tasarım görünümünü ve XAML görünümünü gösterir. Herhangi bir görünümden daha fazla veya daha az görünmesi için Bölümlendirici slaytı gösterebilirsiniz. Yalnızca görsel görünümü veya yalnızca XAML görünümünü görmeyi seçebilirsiniz.

![IDE 'de WPF projesi ve çözümü](media/exploreide-wpfproject-cs.png "IDE 'DEKI WPF projesi ve çözümünün ekran görüntüsü")

> [!NOTE]
> XAML (Genişletilebilir uygulama biçimlendirme dili) hakkında daha fazla bilgi için bkz. [WPF Için xaml genel bakış](/dotnet/framework/wpf/advanced/xaml-overview-wpf) sayfası.

Projeyi oluşturduktan sonra özelleştirebilirsiniz. Bunu yapmak için, **Görünüm** menüsünden **Özellikler penceresi** ' ni seçin veya **F4**tuşuna basın. Daha sonra, bir uygulamadaki proje öğeleri, denetimler ve diğer öğeler için seçenekleri görüntüleyebilir ve değiştirebilirsiniz.

   ![Özellikler penceresi](../media/exploreide-hellowpfappfiles.png "WPF dosya uygulama adlarıyla Özellikler penceresi ekran görüntüsü")   

### <a name="change-the-name-of-mainwindowxaml"></a>MainWindow. xaml adını değiştirme

Şimdi, MainWindow 'e daha özel bir ad verelim.

1. **Çözüm Gezgini**, *MainWindow. xaml*' i seçin. **Özellikler** penceresini görmeniz gerekir, ancak bunu yapmazsanız, **Görünüm** menüsünü ve ardından **Özellikler penceresi** öğesini seçin. (Veya **F4**tuşuna basın.)

1. **Dosya adı** özelliğini olarak `Greetings.xaml`değiştirin.

     ![Dosya adı vurgulanmış Özellikler penceresi](../media/exploreide-filenameinpropertieswindow.png "Dosya adı vurgulanmış Özellikler penceresi ekran görüntüsü")

     **Çözüm Gezgini** , dosyanın adının artık *Greetings. xaml*olduğunu ve iç içe geçmiş kod dosyasının artık *Greetings.xaml.cs*olarak adlandırıldığını gösterir. Bu kod dosyası, birbirleriyle yakından ilişkili olduğunu göstermek için *. xaml* dosya düğümünün altına yuvalanmıştır.

     ![Greetings dosya adı ile Özellikler penceresi ve Çözüm Gezgini pencere](../media/exploreide-greetingsfilename.png "Greetings dosya adı ile Özellikler penceresi ve Çözüm Gezgini penceresinin ekran görüntüsü")     

## <a name="design-the-user-interface-ui"></a>Kullanıcı arabirimini (UI) tasarlama

Bu uygulamaya üç tür denetim ekleyeceğiz: <xref:System.Windows.Controls.TextBlock> denetim, iki <xref:System.Windows.Controls.RadioButton> denetim ve bir <xref:System.Windows.Controls.Button> denetim.

### <a name="add-a-textblock-control"></a>TextBlock denetimi ekleme

1. Arama kutusunu etkinleştirmek ve **araç kutusu**yazın için **CTRL**+**Q** tuşlarına girin. Sonuçlar listesinden **> araç kutusunu görüntüle** ' yi seçin.

1. **Araç kutusunda**, TextBlock denetimini görmek IÇIN **ortak WPF denetimleri** düğümünü genişletin.

     ![TextBlock denetimi vurgulanmış olan araç kutusu](../media/exploreide-textblocktoolbox.png "TextBlock denetimi vurgulanmış şekilde araç kutusu penceresinin ekran görüntüsü")

1. **TextBlock** öğesini seçerek ve tasarım yüzeyinde pencereye sürükleyerek tasarım yüzeyine bir TextBlock denetimi ekleyin. Pencerenin üst kısmına yakın olan denetimi ortalayın.

    Pencereniz aşağıdaki gösterime benzemelidir:

    ![Greetings formundaki TextBlock denetimi](../media/exploreide-greetingswithtextblockonly.png "Tebrikler formundaki TextBlock denetiminin ekran görüntüsü")

   XAML işaretlemesi aşağıdaki örnekteki gibi görünmelidir:

    ```xaml
    <Grid>
        <TextBlock HorizontalAlignment="Left" Margin="387,60,0,0" TextWrapping="Wrap" Text="TextBlock" VerticalAlignment="Top"/>
    </Grid>
    ```

### <a name="customize-the-text-in-the-text-block"></a>Metin bloğundaki metni özelleştirme

1. XAML görünümünde **TextBlock** için biçimlendirmeyi bulun ve **metin** özniteliğini ' den `TextBox` ' a değiştirin.`Select a message option and then choose the Display button.`

   XAML işaretlemesi aşağıdaki örnekteki gibi görünmelidir:

   ```xaml
   <Grid>
       <TextBlock HorizontalAlignment="Left" Margin="387,60,0,0" TextWrapping="Wrap" Text="Select a message option and then choose the Display button." VerticalAlignment="Top"/>
   </Grid>
   ```

1. Gerekirse, daha sonra **CTRL + S** tuşlarına basarak veya **Dosya** menü öğesini kullanarak değişikliklerinizi yeniden ortalayın.

Ardından, forma iki [RadioButton](/dotnet/framework/wpf/controls/radiobutton) denetimi ekleyeceksiniz.

### <a name="add-radio-buttons"></a>Radyo düğmeleri ekleme

1. **Araç kutusunda** **RadioButton** denetimini bulun.

     ![RadioButton denetimi seçiliyken araç kutusu penceresi](../media/exploreide-radiobuttontoolbox.png "RadioButton denetimi seçiliyken araç kutusu penceresinin ekran görüntüsü")

1. **RadioButton** öğesini seçerek ve tasarım yüzeyinde pencereye sürükleyerek tasarım yüzeyine iki RadioButton denetimi ekleyin. Düğmeleri TextBlock denetimi altında yan yana görünecek şekilde düğmeleri (onları seçerek ve ok tuşlarını kullanarak) taşıyın.

   Pencerenizin şuna benzemesi gerekir:

   ![TextBlock ve iki radyo düğmesi Içeren Tebrikler formu](../media/exploreide-greetingswithradiobuttons.png "TextBlock ve iki radyo düğmesi Ile Greetings formunun ekran görüntüsü")

1. Sol RadioButton denetimi için **Özellikler** penceresinde, **ad** özelliğini ( **Özellikler** penceresinin üst kısmındaki özellik) olarak `HelloButton`değiştirin.

    ![RadioButton Özellikler penceresi](../media/exploreide-buttonproperties.png "RadioButton Özellikleri penceresinin ekran görüntüsü")

1. Sağ RadioButton denetimi için **Özellikler** penceresinde, **ad** özelliğini olarak `GoodbyeButton`değiştirin ve ardından değişikliklerinizi kaydedin.

Ardından, her RadioButton denetimi için görüntü metni ekleyeceksiniz. Aşağıdaki yordam bir RadioButton denetimi için **içerik** özelliğini güncelleştirir.

### <a name="add-display-text-for-each-radio-button"></a>Her radyo düğmesi için görüntü metni Ekle

1. Tasarım yüzeyinde, Merhaba düğmesine sağ fare düğmesine basarak Merhaba düğme kısayol menüsünü açın, **Metni Düzenle**' yi seçin ve ardından girin `Hello`.

1. GoodbyeButton üzerinde sağ fare düğmesine basarak GoodbyeButton için kısayol menüsünü açın, **Metni Düzenle**' yi seçin ve ENTER `Goodbye`tuşuna basın.

   XAML işaretlemesi artık aşağıdaki örneğe benzer şekilde görünmelidir:

   ```xaml
   <Grid>
        <TextBlock HorizontalAlignment="Left" Margin="252,47,0,0" TextWrapping="Wrap" Text="Select a message option and then choose the Display button." VerticalAlignment="Top"/>
        <RadioButton x:Name="HelloButton" Content="Hello" HorizontalAlignment="Left" Margin="297,161,0,0" VerticalAlignment="Top"/>
        <RadioButton x:Name="GoodbyeButton" Content="Goodbye" HorizontalAlignment="Left" Margin="488,161,0,0" VerticalAlignment="Top"/>
   </Grid>
   ```

### <a name="set-a-radio-button-to-be-checked-by-default"></a>Radyo düğmesini varsayılan olarak denetlenecek şekilde ayarla

Bu adımda, her zaman iki radyo düğmelerinden biri seçili olacak şekilde, Merhaba düğmesini varsayılan olarak denetlenecek şekilde ayarlayacağız.

1. XAML görünümünde, Merhaba düğmesine yönelik biçimlendirmeyi bulun.

1. Bir **IsChecked** özniteliği ekleyin ve bunu **true**olarak ayarlayın. Özellikle, ekleyin `IsChecked="True"`.

   XAML işaretlemesi artık aşağıdaki örneğe benzer şekilde görünmelidir:

   ```xaml
   <Grid>
        <TextBlock HorizontalAlignment="Left" Margin="252,47,0,0" TextWrapping="Wrap" Text="Select a message option and then choose the Display button." VerticalAlignment="Top"/>
        <RadioButton x:Name="HelloButton" Content="Hello" IsChecked="True" HorizontalAlignment="Left" Margin="297,161,0,0" VerticalAlignment="Top"/>
        <RadioButton x:Name="GoodbyeButton" Content="Goodbye" HorizontalAlignment="Left" Margin="488,161,0,0" VerticalAlignment="Top"/>
   </Grid>
   ```

Ekleyeceğiniz son UI öğesi bir [düğme](/dotnet/framework/wpf/controls/button) denetimidir.

### <a name="add-the-button-control"></a>Düğme denetimini ekleme

1. **Araç kutusunda** **düğme** denetimini bulun ve ardından Tasarım görünümündeki forma sürükleyerek RadioButton denetimlerinin altındaki tasarım yüzeyine ekleyin.

1. XAML görünümünde düğme denetimi `Content="Button"` için **içerik** değerini olarak `Content="Display"`değiştirin ve ardından değişiklikleri kaydedin.

     Pencereniz aşağıdaki gösterime benzemelidir.

     ![Denetim etiketleriyle Greetings formu](media/exploreide-greetingswithcontrollabels-cs.png "Denetim etiketleriyle Greetings formunun ekran görüntüsü")

   XAML işaretlemesi artık aşağıdaki örneğe benzer şekilde görünmelidir:

   ```xaml
   <Grid>
        <TextBlock HorizontalAlignment="Left" Margin="252,47,0,0" TextWrapping="Wrap" Text="Select a message option and then choose the Display button." VerticalAlignment="Top"/>
        <RadioButton x:Name="HelloButton" Content="Hello" IsChecked="True" HorizontalAlignment="Left" Margin="297,161,0,0" VerticalAlignment="Top"/>
        <RadioButton x:Name="GoodbyeButton" Content="Goodbye" HorizontalAlignment="Left" Margin="488,161,0,0" VerticalAlignment="Top"/>
        <Button Content="Display" HorizontalAlignment="Left" Margin="377,270,0,0" VerticalAlignment="Top" Width="75"/>
   </Grid>
   ```

### <a name="add-code-to-the-display-button"></a>Görüntü düğmesine kod ekleme

Bu uygulama çalıştığında, bir Kullanıcı radyo düğmesini seçtikten sonra **görüntüle** düğmesini seçtiğinde bir ileti kutusu görünür. Merhaba için bir ileti kutusu ve Güle Güle için bir diğer ileti kutusu görünecektir. Bu davranışı oluşturmak için `Button_Click` *Greetings.xaml.cs*içindeki olaya kod ekleyeceksiniz.

1. Tasarım yüzeyinde **görüntüle** düğmesine çift tıklayın.

     *Greetings.xaml.cs* , imleç `Button_Click` olayda açılır.

    ```csharp
    private void Button_Click_1(object sender, RoutedEventArgs e)
    {

    }
    ```

1. Aşağıdaki kodu girin:

    ```csharp
    if (HelloButton.IsChecked == true)
    {
         MessageBox.Show("Hello.");
    }
    else if (GoodbyeButton.IsChecked == true)
    {
        MessageBox.Show("Goodbye.");
    }
    ```

1. Uygulamayı kaydedin.

## <a name="debug-and-test-the-application"></a>Uygulamanın hatalarını ayıklama ve test etme

Sonra, hataları bulmak ve her iki ileti kutusunun doğru şekilde göründüğünü sınamak için uygulamada hata ayıklaması yapacaksınız. Aşağıdaki yönergelerde hata ayıklayıcıyı nasıl derleyip başlatacağınız, ancak daha sonra daha fazla bilgi için WPF [uygulaması (WPF) oluşturma](/dotnet/framework/wpf/app-development/building-a-wpf-application-wpf) ve [WPF hata ayıklama](../../debugger/debugging-wpf.md) işlemlerini okuyabilirsiniz.

### <a name="find-and-fix-errors"></a>Hataları bulma ve düzeltme

Bu adımda, daha önce *MainWindow. xaml* dosyasının adını değiştirerek neden olduğumuz hatayı bulacaksınız.

#### <a name="start-debugging-and-find-the-error"></a>Hata ayıklamayı başlatma ve hatayı bulma

1. **F5** tuşuna basarak veya **Hata Ayıkla**' yı seçerek hata ayıklayıcıyı başlatın ve ardından **hata ayıklamayı başlatın**.

   **Kesme modu** penceresi görünür ve **Çıkış** penceresi bir IOException oluştuğunu belirtir: ' MainWindow. xaml ' kaynağı bulunamıyor.

   ![IOException iletisi](../media/exploreide-ioexception.png "IOException Iletisinin ekran görüntüsü")

1. Hata ayıklamayı Durdur hata > **ayıklamayı**Durdur seçeneğini belirleyerek durdurun.

Bu öğreticinin başlangıcında *MainWindow. xaml* ' i *Greetings. xaml* olarak yeniden adlandırdık, ancak kod yine de uygulama için başlangıç URI 'si olarak *MainWindow. xaml* 'e başvuruyor, bu nedenle proje başlatılamıyor.

#### <a name="specify-greetingsxaml-as-the-startup-uri"></a>Başlangıç URI 'SI olarak Greetings. xaml belirtin

1. **Çözüm Gezgini**' de *app. xaml* dosyasını açın.

1. `StartupUri="MainWindow.xaml"` Olarak`StartupUri="Greetings.xaml"`değiştirin ve değişiklikleri kaydedin.

Hata ayıklayıcıyı yeniden başlatın ( **F5**tuşuna basın). Uygulamanın **Greetings** penceresini görmeniz gerekir. Hata ayıklamayı durdurmak için şimdi uygulama penceresini kapatın.

### <a name="debug-with-breakpoints"></a>Kesme noktalarıyla hata ayıkla

Hata ayıklama sırasında bazı kesme noktaları ekleyerek kodu test edebilirsiniz. Kesme**noktası geçiş noktasını**seçerek > , kesmenin gerçekleşmesini istediğiniz kod satırının yanındaki düzenleyicinin sol kenar boşluğuna tıklayarak veya **F9**tuşuna basarak kesme noktaları ekleyebilirsiniz.

#### <a name="add-breakpoints"></a>Kesme noktaları Ekle

1. *Greetings.xaml.cs*açın ve aşağıdaki satırı seçin:`MessageBox.Show("Hello.")`

1. Menüden **Hata Ayıkla**' yı ve ardından **kesme noktasını aç**' ı seçerek bir kesme noktası ekleyin.

     Düzenleyici penceresinin en sol kenar boşluğunda, kod satırının yanında kırmızı bir daire görünür.

1. Aşağıdaki satırı seçin: `MessageBox.Show("Goodbye.")`.

1. Bir kesme noktası eklemek için **F9** tuşuna basın ve sonra hata ayıklamayı başlatmak için **F5** 'e basın.

1. **Tebrikler** penceresinde, **Merhaba** radyo düğmesini seçin ve ardından **görüntüle** düğmesini seçin.

    Çizgi `MessageBox.Show("Hello.")` sarı renkle vurgulanır. IDE 'nin en altında, oto, Yereller ve Watch pencereleri, sol tarafa birlikte yerleştirilir ve çağrı yığını, kesme noktaları, özel durum ayarları, komut, anlık ve çıkış pencereleri sağ tarafta birlikte yerleştirilir.

    ![Hata ayıklayıcıda kesme noktası](media/exploreide-debugbreakpoint.png "Hata ayıklayıcıda kesme noktası ekran görüntüsü")

1. Menü çubuğunda **Hata Ayıkla** > **Step Out**' ı seçin.

     Uygulama yürütmeyi sürdürür ve "Hello" sözcüğünü içeren bir ileti kutusu görünür.

1. İletiyi kapatmak için ileti kutusunda **Tamam** düğmesini seçin.

1. **Tebrikler** penceresinde, **güle** radyo düğmesini seçin ve ardından **görüntüle** düğmesini seçin.

     Çizgi `MessageBox.Show("Goodbye.")` sarı renkle vurgulanır.

1. Hata ayıklamaya devam etmek için **F5** tuşunu seçin. İleti kutusu göründüğünde kapatmak için ileti kutusunda **Tamam** düğmesini seçin.

1. Hata ayıklamayı durdurmak için uygulama penceresini kapatın.

1. Menü çubuğunda, **Hata Ayıkla** > **tüm kesme noktalarını devre dışı bırak**' ı seçin.

### <a name="build-a-release-version-of-the-application"></a>Uygulamanın yayın sürümünü oluşturma

Her şeyin çalıştığını doğruladığınıza göre uygulamanın bir yayın derlemesini hazırlayabilirsiniz.

1. Ana menüde, önceki derlemeler sırasında oluşturulan ara dosyaları ve çıktı dosyalarını silmek için**temiz çözüm** **Oluştur** > ' u seçin. Bu gerekli değildir, ancak hata ayıklama oluşturma çıkışlarını temizler.

1. Araç çubuğundaki DropDown denetimini kullanarak HelloWPFApp için derleme yapılandırmasını **hata ayıklamadan** **Yayınla** değiştirin (Şu anda "hata ayıkla" ifadesini alır).

1. Build**Build Solution**öğesini seçerek > çözümü oluşturun.

Bu öğreticiyi tamamlamak Tebrikler! Çözümünüz ve proje dizininiz ( *. ..\Hellowpfapp\hellowpfapp\bin\release*) altında oluşturduğunuz *. exe dosyasını* bulabilirsiniz.

## <a name="next-steps"></a>Sonraki adımlar

Bu öğreticiyi tamamlamak Tebrikler! Daha da fazla bilgi edinmek için aşağıdaki öğreticilerle devam edin.

> [!div class="nextstepaction"]
> [Daha fazla WPF öğreticiyle devam edin](/dotnet/framework/wpf/getting-started/wpf-walkthroughs/)

## <a name="see-also"></a>Ayrıca bkz.

- [Üretkenlik ipuçları](../../ide/productivity-features.md)
