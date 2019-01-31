---
title: 'Öğretici: Windows Presentation Foundation (WPF) ile Merhaba Dünya uygulamasıC#'
description: Basit bir Windows Masaüstü .NET uygulaması oluşturun C# Windows Presentation Foundation (WPF) UI çerçevesi kullanarak Visual Studio ile.
ms.custom: seodec18, get-started
ms.date: 10/03/2017
ms.prod: visual-studio-dev15
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
ms.openlocfilehash: 757ec79e2ae1996c6453fd01b20e71e9a6d62594
ms.sourcegitcommit: 9866740aec05d1a3a5dc3b4b6d2ceaeecbd3fc29
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55424518"
---
# <a name="tutorial-create-a-simple-application-with-c"></a>Öğretici: İle basit uygulama oluşturmaC#

Bu izlenecek yolu tamamlayarak, birçok araçları, iletişim kutuları ve Visual Studio ile uygulamalar geliştirirken kullanabileceğiniz tasarımcıları sahibi olacaksınız. Bir "Hello, World" uygulaması oluşturacak, kullanıcı arabirimini tasarlayacak, kod ekleyin ve tümleşik geliştirme ortamında çalışma hakkında bilgi edinirken, hatalarını ayıklama ([IDE](visual-studio-ide.md)).

Visual Studio henüz yüklemediyseniz, Git [Visual Studio indirmeleri](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2017) ücretsiz yüklemek için sayfa.

## <a name="configure-the-ide"></a>IDE'yi yapılandırma

Visual Studio'yu ilk kez başlattığınızda, oturum açmanız istenir. Bu adım, bu kılavuz için isteğe bağlıdır. Sonraki renk teması ve geliştirme ayarlarınızı seçin isteyen bir iletişim kutusu gösterilebilir. Varsayılan değerleri koruyun ve seçin **Visual Studio Başlangıç**.

![Ayarlarını Seç iletişim kutusu](../media/exploreide-settings.png)

Visual Studio'yu başlattıktan sonra araç pencerelerini, menüleri ve araç çubuklarını ve ana pencere alanını görürsünüz. Araç pencereleri tutturulmuştur ve uygulama penceresinin sol tarafında ile **hızlı başlatma**, menü çubuğu ve en üstte standart araç çubuğu. Uygulama penceresinin ortasında olup **başlangıç sayfası**. Bir çözüm veya projeyi yüklediğinizde, alanda görünür düzenleyiciler ve tasarımcılar burada **başlangıç sayfası** olduğu. Uygulama geliştirirken zamanınızın çoğunu bu Orta alanda geçireceksiniz.

![Genel Ayarları uygulanmış IDE](../media/exploreide-idewithgeneralsettings.png)

## <a name="create-the-project"></a>Projeyi oluşturma

Visual Studio'da bir uygulama oluştururken önce bir proje ve bir çözüm oluşturursunuz. Bu örnekte, bir Windows Presentation Foundation (WPF) projesi oluşturacaksınız.

1. Yeni bir proje oluşturun. Menü çubuğunda, seçin **dosya** > **yeni** > **proje**.

     ![Menü çubuğunda, dosya, yeni proje](../media/exploreide-filenewproject.png)

1. İçinde **yeni proje** iletişim kutusunda **yüklü** > **Visual C#**   >  **Windows Masaüstü**kategori tıklayın ve ardından **WPF uygulaması (.NET Framework)** şablonu. Projeyi adlandırın **HelloWPFApp**.

     ![Visual Studio yeni proje iletişim kutusunda WPF uygulaması şablonu](media/exploreide-newprojectcsharp.png)

1. **Tamam**’ı seçin.

   HelloWPFApp projesi ve çözüm, Visual Studio oluşturur ve **Çözüm Gezgini** çeşitli dosyaları gösterir. **WPF Tasarımcısı** XAML görünümünü ve Tasarım görünümünü gösterir *MainWindow.xaml* bölünmüş görünümdeki. Daha fazla veya daha az gösterilecek bölme kaydırabilirsiniz ya da görünümün. Yalnızca bir görsel görünümünü veya yalnızca XAML görünümü görmek seçebilirsiniz. Aşağıdaki öğeler görünür **Çözüm Gezgini**:

   ![Çözüm Gezgini ile yüklenen HelloWPFApp dosyaları](../media/exploreide-hellowpfappfiles.png)

   > [!NOTE]
   > XAML (Genişletilebilir uygulama biçimlendirme dili) hakkında daha fazla bilgi için bkz: [WPF için XAML genel bakış](/dotnet/framework/wpf/advanced/xaml-overview-wpf) sayfası.

Projeyi oluşturduktan sonra özelleştirebilirsiniz. Kullanarak **özellikleri** penceresi (bulunan **görünümü** menüsü), görüntüleyebilir ve proje öğelerine, denetimleri ve uygulamadaki diğer öğeler için seçeneklerini değiştirin.

### <a name="change-the-name-of-mainwindowxaml"></a>MainWindow.xaml adını değiştirin

Şimdi MainWindow daha belirgin bir ad verin.

1. İçinde **Çözüm Gezgini**seçin *MainWindow.xaml*. Görmeniz gerekir **özellikleri** , seçerseniz yoktur ancak pencere, **görünümü** menüsünü ve ardından **Özellikler penceresi** öğesi.

1. Değişiklik **dosya adı** özelliğini `Greetings.xaml`.

     ![Vurgulanmış dosya adıyla Özellikler penceresi](../media/exploreide-filenameinpropertieswindow.png)

     **Çözüm Gezgini** dosyanın adını artık olmadığını *Greetings.xaml*, ve iç içe geçmiş kodu dosya artık adlı *Greetings.xaml.cs*. Bu kod dosyasının altında iç içe *.xaml* yakından ilişkili oldukları diğer için gösterilecek dosya düğümü.

## <a name="design-the-user-interface-ui"></a>Kullanıcı arabirimini (UI) tasarlama

Bu uygulamaya üç tür denetim ekleyeceğiz: bir <xref:System.Windows.Controls.TextBlock> denetim, iki <xref:System.Windows.Controls.RadioButton> denetimleri ve <xref:System.Windows.Controls.Button> denetimi.

### <a name="add-a-textblock-control"></a>TextBlock denetimi ekleme

1. Açık **araç kutusu** penceresini seçerek **görünümü** menü ve **araç kutusu** öğesi.

2. İçinde **araç kutusu**, genişletme **ortak WPF denetimleri** TextBlock denetimini görmek için düğümü.

     ![Araç kutusu vurgulanmış TextBlock denetimi ile](../media/exploreide-textblocktoolbox.png)

3. TextBlock denetimi tasarım yüzeyine seçerek eklemek **TextBlock** öğesi ve pencereyi tasarım yüzeyine sürükleyerek. Pencerenin üst kısmındaki denetim merkezi.

Pencereniz aşağıdaki gösterime benzemelidir:

![Greetings formdaki TextBlock denetimi](../media/exploreide-greetingswithtextblockonly.png)

XAML işaretleme aşağıdaki örnekteki gibi görünmelidir:

```xaml
<TextBlock HorizontalAlignment="Center" TextWrapping="Wrap" VerticalAlignment="Center" RenderTransformOrigin="4.08,2.312" Margin="237,57,221,238"><Run Text="TextBlock"/><InlineUIContainer><TextBlock TextWrapping="Wrap" Text="TextBlock"/>
```

### <a name="customize-the-text-in-the-text-block"></a>Metin bloğu içindeki metni özelleştirin

1. XAML görünümünde TextBlock için biçimlendirmeyi yerleştirin ve metin özniteliğini değiştirin:

   ```xaml
   Text="Select a message option and then choose the Display button."
   ```

2. TextBlock gerekirse yeniden merkezi ve tuşlarına basarak yaptığınız değişiklikleri kaydetmek **Ctrl**+**S** veya bu adı kullanıyor **dosya** menü öğesi.

Ardından iki ekleyeceksiniz [RadioButton](/dotnet/framework/wpf/controls/radiobutton) formu için denetimler.

### <a name="add-radio-buttons"></a>Radyo düğmeleri ekleme

1. İçinde **araç kutusu**, bulma **RadioButton** denetimi.

     ![Araç penceresi seçili RadioButton denetimi ile](../media/exploreide-radiobuttontoolbox.png)

2. İki RadioButton denetimi tasarım yüzeyine seçerek ekleme **RadioButton** öğesi ve pencereyi tasarım yüzeyine sürükleyerek. (Bunları seçerek ve ok tuşlarını kullanarak) düğmeleri Taşı düğmeleri TextBlock denetiminin altında yan yana görünür.

     Pencerenizin şuna benzemesi gerekir:

     ![Greetings formu textblock ve iki RadioButton'ları](../media/exploreide-greetingswithradiobuttons.png)

3. İçinde **özellikleri** değişiklik sol taraftaki RadioButton denetimi için pencere **adı** özelliği (özellik en üstündeki **özellikleri** penceresi) için `HelloButton`.

     ![RadioButton Özellikler penceresi](../media/exploreide-buttonproperties.png)

4. İçinde **özellikleri** değişiklik sağ taraftaki RadioButton denetimi için pencere **adı** özelliğini `GoodbyeButton`ve ardından değişikliklerinizi kaydedin.

Artık her bir RadioButton denetimi için görüntü metni ekleyebilirsiniz. Aşağıdaki yordam güncelleştirmeleri **içerik** özelliği bir RadioButton denetimi için.

### <a name="add-display-text-for-each-radio-button"></a>Her bir radyo düğmesine görüntü metni Ekle

1. Tasarım yüzeyinde, üzerinde HelloButton sağ fare düğmesine basarak HelloButton için kısayol menüsünü açın, **Metni Düzenle**yazıp enter `Hello`.

2. Açık GoodbyeButton üzerinde sağ fare düğmesine basarak GoodbyeButton kısayol menüsünü seçin **Metni Düzenle**yazıp enter `Goodbye`.

### <a name="set-a-radio-button-to-be-checked-by-default"></a>Varsayılan olarak denetlenmesi için bir radyo düğmesi ayarlayın

Bu adımda, biz, böylece iki radyo düğmelerinden birini seçili her zaman varsayılan olarak denetlenecek HelloButton ayarlarsınız.

XAML görünümünde HelloButton için işaretleme bulun ve ekleme bir **IsChecked** özniteliği:

```xaml
IsChecked="True"
```

Son ekleyeceğiniz UI öğesi bir [düğmesi](/dotnet/framework/wpf/controls/button) denetimi.

### <a name="add-the-button-control"></a>Düğme denetimi ekleyin

1. İçinde **araç kutusu**, bulma **düğmesi** denetlemek ve tasarım yüzeyinde RadioButton denetimlerinin altında Tasarım görünümünde forma sürükleyerek ekleyin.

2. XAML Görünümü'nde değiştirin **içerik** Button denetimi için `Content="Button"` için `Content="Display"`ve değişiklikleri kaydedin.

     İşaretleme şu örneğe benzemelidir:   `<Button Content="Display" HorizontalAlignment="Left" VerticalAlignment="Top" Width="75" Margin="215,204,0,0"/>`

     Pencereniz aşağıdaki gösterime benzemelidir.

     ![Greetings biçimiyle, denetim etiketleri](media/exploreide-greetingswithcontrollabels-cs.png)

### <a name="add-code-to-the-display-button"></a>Görüntüle düğmesine kod ekleme

Bu uygulama çalışırken, bir kullanıcı bir radyo düğmesini seçerse ve sonra seçtiğinde bir ileti kutusu görünür **görünen** düğmesi. Merhaba için bir ileti kutusu ve Güle Güle için bir diğer ileti kutusu görünecektir. Bu davranışı oluşturmak için kod ekleyeceksiniz `Button_Click` olayında *Greetings.xaml.cs*.

1. Tasarım yüzeyinde, çift **görünen** düğmesi.

     *Greetings.xaml.cs* açılır ve imleç `Button_Click` olay.

    ```csharp
    private void Button_Click_1(object sender, RoutedEventArgs e)
    {

    }
    ```

2. Aşağıdaki kodu girin:

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

3. Uygulamayı kaydedin.

## <a name="debug-and-test-the-application"></a>Uygulamanın hatalarını ayıklama ve test etme

Ardından, hatalara bakmak ve her iki ileti kutusunun da doğru görünüp görünmediğini test etmek için uygulamanın hatasını ayıklama. Aşağıdaki yönergeler size nasıl oluşturacağınızı ve hata ayıklayıcıyı başlatma, ancak daha sonra okuyabilir [bir WPF uygulaması (WPF) derleme](/dotnet/framework/wpf/app-development/building-a-wpf-application-wpf) ve [hata ayıklama WPF](../../debugger/debugging-wpf.md) daha fazla bilgi için.

### <a name="find-and-fix-errors"></a>Hataları bulma ve düzeltme

Bu adımda, önceki adını değiştirerek neden olan hata bulabilirsiniz *MainWindow.xaml* dosya.

#### <a name="start-debugging-and-find-the-error"></a>Hata ayıklamayı başlatmak ve hatayı Bul

1. Hata ayıklayıcı seçerek başlayın **hata ayıklama**, ardından **hata ayıklamayı Başlat**.

     ![Hata ayıklama komutu hata ayıklama menüsünden başlayın.](../media/exploreide-startdebugging.png)

     A **kesme modu** penceresi görüntülenir ve **çıkış** penceresini gösteren bir Ioexception oluştu: 'Mainwindow.xaml' kaynağının yeri belirlenemiyor.

2. Seçerek hata ayıklayıcıyı **hata ayıklama** > **hata ayıklamayı Durdur**.

     ![Hata ayıklamayı Debug menüsünden Durdur komutu](../media/exploreide-stopdebugging.png)

Biz yeniden adlandırıldı *MainWindow.xaml* için *Greetings.xaml* başvurduğu yine de bu izlenecek yol, ancak kod başlangıcında *MainWindow.xaml* uygulamaya ilişkin başlangıç URI olarak , proje başlatamazsınız.

#### <a name="specify-greetingsxaml-as-the-startup-uri"></a>Başlangıç URI'si olarak Greetings.XAML belirtin

1. İçinde **Çözüm Gezgini**açın *App.xaml* dosya.

2. Değişiklik `StartupUri="MainWindow.xaml"` için `StartupUri="Greetings.xaml"`ve değişiklikleri kaydedin.

Hata ayıklayıcıyı yeniden başlatın (basın **F5**). Görmelisiniz **Greetings** uygulama penceresi. Artık hata ayıklamayı durdurmak için uygulama penceresini kapatın.

### <a name="debug-with-breakpoints"></a>Kesme noktaları ile hata ayıklama

Bazı kesme noktası ekleyerek hata ayıklama sırasında kodu test edebilirsiniz. Kesme noktaları belirleyerek ekleyebileceğiniz **hata ayıklama** > **iki durumlu kesme noktası**, kesmenin istediğiniz yere sol kenar düzenleyicinin kod satırının yanındaki tıklayarak veya basarak  **F9**.

#### <a name="add-breakpoints"></a>Kesme Noktası Ekle

1. Açık *Greetings.xaml.cs*, aşağıdaki satırı seçin: `MessageBox.Show("Hello.")`

2. Bir kesme noktası menüden seçerek ekleyin **hata ayıklama**, ardından **iki durumlu kesme noktası**.

     ![Hata ayıklama menüsünden kesim noktasını Değiştir komutu](../media/exploreide-togglebreakpoint.png)

     Düzenleyici penceresinin en sol kenar boşluğunda, kod satırının yanında kırmızı bir daire görünür.

3. Aşağıdaki satırı seçin: `MessageBox.Show("Goodbye.")`.

4. Basın **F9** bir kesme noktası eklemek için anahtar ve tuşuna **F5** hata ayıklama başlatılamıyor.

5. İçinde **Greetings** penceresinde seçin **Hello** radyo düğmesini ve ardından **görünen** düğmesi.

     Satır `MessageBox.Show("Hello.")` sarı renkle vurgulanır. IDE, Otolar, Yereller ve İzle altındaki windows birlikte sol tarafa yerleşir ve çağrı yığını, kesme noktaları, komut, anlık ve çıkış pencereleri birlikte sağ tarafta yerleşir.

6. Menü çubuğunda, **hata ayıklama** > **Step Out**.

     Uygulama yürütmeyi devam ettirir ve "Hello" sözcüğünü içeren bir ileti kutusu görünür.

7. Seçin **Tamam** ileti kutusunu kapatmak için düğme.

8. İçinde **Greetings** penceresinde seçin **güle güle** radyo düğmesini ve ardından **görünen** düğmesi.

     Satır `MessageBox.Show("Goodbye.")` sarı renkle vurgulanır.

9. Seçin **F5** hata ayıklamaya devam etmek için anahtarı. İleti kutusu göründüğünde **Tamam** ileti kutusunu kapatmak için düğme.

10. Hata ayıklamayı durdurmak için uygulama penceresini kapatın.

11. Menü çubuğunda, **hata ayıklama** > **tüm kesme noktalarını devre dışı**.

### <a name="build-a-release-version-of-the-application"></a>Uygulamanın yayın sürümünü oluşturma

Her şeyin çalıştığını doğruladığınıza göre uygulamanın bir yayın derlemesini hazırlayabilirsiniz.

1. Ana menüden **derleme** > **temiz çözümü** Ara dosyaları ve önceki derlemeler sırasında oluşturulan çıktı dosyalarını silmek için. Bu gerekli değildir, ancak hata ayıklama derleme çıktılarını ' temizler.

     ![Derle menüsünde çözümü Temizle komutu](../media/exploreide-cleansolution.png)

2. HelloWPFApp için yapı yapılandırmasını değiştirme **hata ayıklama** için **yayın** (yazacaktır "Debug" şu anda) araç çubuğundaki aşağı açılır denetimden kullanarak.

     ![Standart araç çubuğunda seçilen sürüm](../media/exploreide-releaseversion.png)

3. Çözüm seçerek yapı **derleme** > **Çözümü Derle**.

     ![Yapı menüsünde derleme çözümü komutu](../media/exploreide-buildsolution.png)

Bu öğreticiyi tamamlamak Tebrikler! Bulabilirsiniz *.exe* çözüm ve proje dizininiz altında oluşturulan (*...\HelloWPFApp\HelloWPFApp\bin\Release*).

## <a name="see-also"></a>Ayrıca bkz.

- [Üretkenlik ipuçları](../../ide/productivity-tips-for-visual-studio.md)