---
title: Windows Form Tasarımcısı öğreticisi
ms.date: 08/09/2019
ms.topic: conceptual
helpviewer_keywords:
- Windows Forms Designer, get started
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 64045221ad9200223264632d4bdbd33ff82d631f
ms.sourcegitcommit: b83fefa8177c5554cbe2c59c4d102cbc534f7cc6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/19/2019
ms.locfileid: "69585348"
---
# <a name="walkthrough-get-started-with-windows-forms-designer"></a>İzlenecek yol: Windows Form Tasarımcısı’nı kullanmaya başlama

Windows Form Tasarımcısı, Windows Forms uygulamalar oluşturmak için birçok araç sağlar. Bu makalede, aşağıdaki görevler de dahil olmak üzere tasarımcı tarafından sunulan çeşitli araçları kullanarak bir uygulamanın nasıl oluşturulacağı gösterilmektedir:

- Denetimleri, yama çizgileri kullanarak düzenleyin.
- Akıllı etiketleri kullanarak tasarımcı görevlerini gerçekleştirin.
- Denetimler için kenar boşluklarını ve doldurmayı ayarlayın.
- Denetimleri bir <xref:System.Windows.Forms.TableLayoutPanel> denetim kullanarak düzenleyin.
- Denetim kullanarak <xref:System.Windows.Forms.SplitContainer> denetiminizin yerleşimini bölümleyin.
- Belge Anahattı penceresi ile mizanpajına gidin.
- Boyut ve konum bilgileri görüntüsüne sahip denetimleri konumlandırın.
- Özellikler penceresi kullanarak özellik değerlerini ayarlayın.

İşiniz bittiğinde, Windows Form Tasarımcısı kullanılabilen çeşitli düzen özellikleri kullanılarak birleştirilen özel bir denetiminiz olacaktır. Bu denetim, basit bir Hesaplayıcı için Kullanıcı arabirimini (UI) uygular. Aşağıdaki görüntüde Hesaplayıcı denetiminin genel yerleşimi gösterilmektedir:

![Kılavuzlu Tur Hesaplayıcı Kullanıcı arabirimi](media/calculator-ui.gif)

## <a name="create-the-custom-control-project"></a>Özel denetim projesi oluşturma

İlk adım, Demohesaplayıcı denetim projesini oluşturmaktır.

1. Visual Studio 'Yu açın ve yeni bir **Windows Forms denetim kitaplığı** projesi oluşturun. Projenin **Demohesap Torlib**olarak adlandırın.

   ::: moniker range=">=vs-2019"

   ![Visual Studio 2019 ' de denetim kitaplığı şablonu Windows Forms](media/windows-forms-control-library-template.png)

   ::: moniker-end

2. Dosyayı yeniden adlandırmak için, **Çözüm Gezgini**' de, **UserControl1. vb** veya **UserControl1.cs**öğesine sağ tıklayın, **Yeniden Adlandır**' ı seçin ve dosya adını demohesaplayıcı. vb veya DemoCalculator.cs olarak değiştirin. "UserControl1" kod öğesiyle tüm başvuruları yeniden adlandırmak isteyip istemediğiniz sorulduğunda **Evet** ' i seçin.

Windows Form Tasarımcısı Demohesaplayıcı denetimi için tasarımcı yüzeyini gösterir. Bu görünümde, araç kutusu ' ndan denetimler ve bileşenler ' i seçip tasarımcı yüzeyine yerleştirerek denetimin görünümünü grafiksel olarak tasarlayabilirsiniz. Özel denetimler hakkında daha fazla bilgi için bkz. [Özel denetimlerin değişen özellikleri](/dotnet/framework/winforms/controls/varieties-of-custom-controls).

## <a name="design-the-control-layout"></a>Denetim düzeni tasarlama

Demohesaplayıcı denetimi çeşitli Windows Forms denetimleri içerir. Bu yordamda, Windows Form Tasarımcısı kullanarak denetimleri düzenleyebilirsiniz.

1. Windows Form Tasarımcısı, sağ alt köşedeki boyutlandırma tutamacını seçerek ve sağa sürükleyerek Demohesaplayıcı denetimini daha büyük bir boyutla değiştirin. Visual Studio 'nun sağ alt köşesinde, denetimler için boyut ve konum bilgilerini bulun. Denetimi yeniden boyutlandırırken boyut bilgilerini izleyerek denetimin boyutunu Width 500 ve Height 400 olarak ayarlayın.

2. **Araç kutusu**'nda, açmak için **kapsayıcılar** düğümünü seçin. **SplitContainer** denetimini seçin ve tasarımcı yüzeyine sürükleyin.

   , `SplitContainer` Demohesaplayıcı denetiminin tasarımcı yüzeyine yerleştirilir.

    > [!TIP]
    > `SplitContainer` Denetim, demohesaplayıcı denetiminin boyutunu sığacak şekilde boyutlandırır. `SplitContainer` Denetimin özellik ayarlarını görmek için **Özellikler** penceresine bakın. <xref:System.Windows.Forms.SplitContainer.Dock%2A> Özelliği bulun. Değeri [DockStyle. Fill](xref:System.Windows.Forms.DockStyle.Fill)' dir. Bu, `SplitContainer` denetimin kendisini her zaman demohesaplayıcı denetiminin sınırlarına göre boyutlandıracağı anlamına gelir. Bu davranışı doğrulamak için Demohesaplayıcı denetimini yeniden boyutlandırın.

3. **Özellikler** penceresinde, <xref:System.Windows.Forms.SplitContainer.Dock%2A> özelliğinin değerini olarak `None`değiştirin.

    `SplitContainer` Denetim varsayılan boyutunu küçültür ve artık demohesaplayıcı denetiminin boyutunu takip eder.

4. Denetimin sağ üst köşesinde![](media/smart-tag-glyph.gif)akıllı etiket karakterini (akıllı etiket karakteri) seçin. `SplitContainer` `Dock` Özelliği olarak`Fill`ayarlamak için **üst kapsayıcıda yerleştir '** i seçin.

    `SplitContainer` Denetim noktaları demohesaplayıcı denetiminin sınırlarına göre yapılır.

    > [!NOTE]
    > Birçok denetim, tasarımı kolaylaştırmak için akıllı etiketler sunar. Daha fazla bilgi için bkz [. İzlenecek yol: Windows Forms denetimlerinde](/dotnet/framework/winforms/controls/performing-common-tasks-using-smart-tags-on-wf-controls)akıllı etiketleri kullanarak ortak görevleri gerçekleştirin.

5. Panolar arasındaki dikey kenarlığı seçin ve sol panel tarafından alınan alanın çoğu için sağa sürükleyin.

    Demohesaplayıcı denetimini, taşınabilir bir kenarlık ile iki panele böler.`SplitContainer` Soldaki panel, hesaplayıcı düğmelerini ve görüntülemeyi tutar ve sağdaki panel, Kullanıcı tarafından gerçekleştirilen aritmetik işlemlerin bir kaydını gösterir.

6. **Özellikler** penceresinde, `BorderStyle` özelliğinin değerini olarak `Fixed3D`değiştirin.

7. **Araç kutusu**' nda **ortak denetimler** düğümünü seçerek açın. Denetimi seçin ve `SplitContainer` denetimin sağ paneline sürükleyin. `ListView`

8. `ListView` Denetimin akıllı etiket karakterini seçin. Akıllı etiket panelinde `View` ayarı olarak `Details`değiştirin.

9. Akıllı etiket panelinde **Sütunları Düzenle**' yi seçin.

   **ColumnHeader koleksiyon Düzenleyicisi** iletişim kutusu açılır.

10. **ColumnHeader koleksiyon Düzenleyicisi** iletişim kutusunda, `ListView` denetime sütun eklemek için **Ekle** ' yi seçin. Sütunun `Text` özelliğinin değerini **History**olarak değiştirin. Sütunu oluşturmak için **Tamam ' ı** seçin.

11. Akıllı etiket panelinde, **Ana kapsayıcıda yerleştir**' i seçin ve akıllı etiket panelini kapatmak için akıllı etiket glifi ' nı seçin.

12. **Kapsayıcılar** düğüm **araç kutusundan**denetimin sol paneline `TableLayoutPanel` `SplitContainer` bir denetim sürükleyin.

    `TableLayoutPanel` Denetim, akıllı etiket paneli açık olan tasarımcı yüzeyinde görünür. Denetim `TableLayoutPanel` , alt denetimlerini bir kılavuzda düzenler. `TableLayoutPanel` Denetim, demohesaplayıcı denetiminin görüntüleme ve düğmelerini tutacaktır. Daha fazla bilgi için bkz [. İzlenecek yol: TableLayoutPanel](/dotnet/framework/winforms/controls/walkthrough-arranging-controls-on-windows-forms-using-a-tablelayoutpanel)kullanarak denetimleri düzenleyin.

13. Akıllı etiket panelinde **satırları ve sütunları Düzenle** ' yi seçin.

    **Sütun ve satır stilleri** iletişim kutusu açılır.

14. Beş sütun görüntülenene kadar **Ekle** düğmesini seçin. Beş sütunu da seçin ve ardından **Boyut türü** kutusunda **yüzde** ' yi seçin. **Yüzde** değerini **20**olarak ayarlayın. Bu, her sütunu aynı genişliğe ayarlar.

15. **Göster**altında **Satırlar**' ı seçin.

16. Beş satır görüntülenene kadar **Ekle** ' yi seçin. Beş satırı ve **Boyut türü** kutusunda **yüzde** seçimini seçin. **Yüzde** değerini **20**olarak ayarlayın. Bu, her bir satırı aynı yüksekliğe ayarlar.

17. Değişikliklerinizi kabul etmek için **Tamam** ' ı seçin ve akıllı etiket panelini kapatmak için akıllı etiket glifi ' nı seçin.

18. **Özellikler** penceresinde, `Dock` özelliğinin değerini olarak `Fill`değiştirin.

## <a name="populate-the-control"></a>Denetimi doldur

Artık denetimin düzeni ayarlanmış olduğuna göre, Demohesaplayıcı denetimini düğmeler ve bir ekran ile doldurabilirsiniz.

1. **Araç kutusu**' nda `TextBox` denetim simgesine çift tıklayın.

   Denetim, `TableLayoutPanel` denetimin ilk hücresine yerleştirilir. `TextBox`

2. **Özellikler** penceresinde, `TextBox` denetimin ColumnSpan özelliğinin değerini **5**olarak değiştirin.

   `TextBox` Denetim, satırında ortalanmış bir konuma gider.

3. `TextBox` Denetimin özelliğinin değerini olarak değiştirin`Right`. `Anchor` `Left`

   Denetim `TextBox` , beş sütunun tamamını kapsayacak şekilde yatay olarak genişletilir.

4. `TextBox` Denetimin özelliğinin değerini olarak`Right`değiştirin. `TextAlign`

5. **Özellikler** penceresinde, `Font` Özellik düğümünü genişletin. 14 `Size` olarakayarlayın ve `Bold` Denetim`TextBox` için **true** olarak ayarlayın.

6. `TableLayoutPanel` Denetimi seçin.

7. **Araç kutusu**'nda `Button` simgesine çift tıklayın.

   Denetim `Button` , `TableLayoutPanel` denetimin bir sonraki açık hücresine yerleştirilir.

8. **Araç kutusunda**, `TableLayoutPanel` denetimin ikinci satırını doldurmak `Button` için simgeye dört kez daha çift tıklayın.

9. **Shift** tuşunu basılı `Button` tutarken beş denetimin tamamını seçerek seçin. Denetimleri panoya kopyalamak+ için CTRL C tuşlarına basın. `Button`

10. `Button` Denetimlerin+kopyalarını denetimin`TableLayoutPanel` kalan satırlarına kopyalamak için CTRL**V** ' ye üç kez basın.

11. **Shift** tuşunu basılı `Button` tutarken tüm 20 denetimleri seçerek seçin.

12. **Özellikler** penceresinde, `Dock` özelliğinin değerini olarak `Fill`değiştirin.

    Tüm denetimler `Button` , kapsayan hücrelerini dolduracak şekilde yerleştirme.

13. **Özellikler** penceresinde, `Margin` Özellik düğümünü genişletin. Değerini `All` **5**olarak ayarlayın.

    Tüm denetimler `Button` , aralarında daha büyük bir kenar boşluğu oluşturmak için daha küçük boyutlardır.

14. **Button10** ve **button20**' i seçin ve sonra düzenden kaldırmak için **Sil** ' e basın.

15. **Button5** ve **button15**öğesini seçin ve ardından `RowSpan` özelliğinin değerini **2**olarak değiştirin. Bu, demohesaplayıcı denetimi **=** için **Açık** ve düğmeler olacaktır.

## <a name="use-the-document-outline-window"></a>Belge Anahattı penceresini kullanın

Denetiminiz veya formunuz çeşitli denetimlerle doldurulduğu zaman, belge anahattı penceresi ile mizanpajınızı gezinmeyi daha kolay bulabilirsiniz.

1. Menü çubuğunda,**diğer Windows** > **belge anahattını** **görüntüle** > ' yi seçin.

   Belge Anahattı penceresi, Demohesaplayıcı denetiminin ve onun bileşen denetimlerinin ağaç görünümünü gösterir. İçindeki kapsayıcı denetimleri, `SplitContainer` alt denetimlerini ağaçta alt düğümleri olarak göster. Ayrıca Belge Anahattı penceresini kullanarak yerinde denetimleri yeniden adlandırabilirsiniz.

2. **Belge ana hattı** penceresinde **button1**' i sağ seçin ve ardından **Yeniden Adlandır**' ı seçin. Adını yeti düğmesi olarak değiştirin.

3. **Belge Anahattı** penceresini kullanarak, aşağıdaki listeye göre `Button` tasarımcı tarafından oluşturulan ad içindeki denetimleri üretim adı olarak yeniden adlandırın:

   - Button1- **on yedi düğmesi**

   - Button2 to **Sektbutton**

   - Button3 to **nineButton**

   - Button4 to **divisionButton**

   - Button5 to **clearButton**

   - Button6 to **on düğmesi**

   - button7 to **Fıvebutton**

   - button8 to **Altbutton**

   - Button9 to **multiplicationButton**

   - button11 to **oneButton**

   - button12- **Twobtan**

   - button13 to **threeButton**

   - button14 to **subtractionButton**

   - button15 to **equalsButton**

   - button16 to **Zerobtan**

   - button17 to **changeSignButton**

   - button18 to **decimalButton**

   - button19 to **additionButton**

4. **Belge ana hattını** ve **Özellikler** pencerelerini kullanarak her `Text` `Button` denetim adı için özellik değerini aşağıdaki listeye göre değiştirin:

   - On yedi düğme denetim metni özelliğini **7** olarak değiştirin

   - Sekizinci Tbutton denetim metni özelliğini **8** olarak değiştirme

   - NineButton denetim metni özelliğini **9** olarak değiştirme

   - DivisionButton denetim metni özelliğini (eğik çizgi **/** ) olarak değiştirme

   - ClearButton denetim metni özelliğini **Temizle** olarak değiştirme

   - On Button denetim metni özelliğini **4** olarak değiştirin

   - FiveButton denetim metni özelliğini **5** olarak değiştirin

   - Altbutton denetim metni özelliğini **6** olarak değiştirme

   - MultiplicationButton denetim metni özelliğini (yıldız işareti **\*** ) olarak değiştirme

   - OneButton denetim metni özelliğini **1** olarak değiştirin

   - Twobtan denetim metni özelliğini **2** olarak değiştirme

   - ThreeButton denetim metni özelliğini **3** olarak değiştirme

   - SubtractionButton denetim metni özelliğini (kısa çizgi **-** ) olarak değiştirme

   - EqualsButton denetim metni özelliğini (eşittir işareti **=** ) olarak değiştirme

   - Zerobtan Control Text özelliğini **0** olarak değiştirme

   - ChangeSignButton denetim metni özelliğini şu şekilde değiştirin **+/-**

   - DecimalButton denetim metni özelliğini olarak değiştirin **.** dönemini

   - AdditionButton denetim metni özelliğini (artı işareti **+** ) olarak değiştirme

5. Tasarımcı yüzeyinde, **Shift** tuşunu basılı tutarken tüm `Button` denetimleri seçerek seçin.

6. **Özellikler** penceresinde, `Font` Özellik düğümünü genişletin. 14 `Size` olarakayarlayın ve tüm `Bold` denetimleriçintrueolarak`Button` ayarlayın.

Bu, Demohesaplayıcı denetiminin tasarımını tamamlar. Kalan şey, hesaplayıcı mantığını sağlamaktır.

## <a name="implement-event-handlers"></a>Olay işleyicilerini Uygula

Demohesaplayıcı denetimindeki düğmelerin, hesaplayıcı mantığının çoğunu uygulamak için kullanılabilecek olay işleyicileri vardır. Windows Form Tasarımcısı, tek bir çift tıklama ile tüm düğmelerin tüm olay işleyicilerinin saplamalarını uygulamanıza olanak sağlar.

1. Tasarımcı yüzeyinde, **Shift** tuşunu basılı tutarken tüm `Button` denetimleri seçerek seçin.

2. `Button` Denetimlerden birine çift tıklayın.

   Kod Düzenleyicisi, tasarımcı tarafından oluşturulan olay işleyicileri için açılır.

## <a name="test-the-control"></a>Denetimi test etme

Demohesaplayıcı denetimi <xref:System.Windows.Forms.UserControl> sınıfından devraldığından, onun davranışını **UserControl Test kapsayıcısı**ile test edebilirsiniz. Daha fazla bilgi için [nasıl yapılır: UserControl](/dotnet/framework/winforms/controls/how-to-test-the-run-time-behavior-of-a-usercontrol)'un çalışma zamanı davranışını test edin.

1. **UserControl Test kapsayıcısında**demohesaplayıcı denetimini derlemek ve çalıştırmak için **F5** tuşuna basın.

2. `SplitContainer` Paneller arasındaki kenarlığı seçin ve sola ve sağa sürükleyin. Ve `TableLayoutPanel` tüm alt denetimleri, kullanılabilir alana sığacak şekilde kendilerini yeniden boyutlandırır.

3. Denetimi test etmeyi bitirdiğinizde **Kapat**' ı seçin.

## <a name="use-the-control-on-a-form"></a>Form üzerinde denetimi kullanma

Demohesaplayıcı denetimi, diğer bileşik denetimlerde veya bir formda kullanılabilir. Aşağıdaki yordamda nasıl kullanılacağı açıklanmaktadır.

### <a name="create-the-project"></a>Projeyi oluşturma

İlk adım uygulama projesini oluşturmaktır. Bu projeyi, özel denetiminizi gösteren uygulamayı oluşturmak için kullanacaksınız.

1. Yeni bir **Windows Forms uygulama** projesi oluşturun ve bunu **Demohesaplatortest**olarak adlandırın.

2. **Çözüm Gezgini**, **Demohesaplatortest** projesine sağ tıklayın ve sonra başvuru Ekle Iletişim kutusunu açmak için **Başvuru Ekle** ' yi seçin.

3. **Projeler** sekmesini seçin ve ardından test projesine başvuruyu eklemek Için Demohesaplatorlib projesine çift tıklayın.

4. **Çözüm Gezgini**, **Demohesaplatortest**öğesine sağ tıklayın ve ardından **Başlangıç projesi olarak ayarla**' yı seçin.

5. Windows Form Tasarımcısı, formun boyutunu **700 x 500**hakkında artırın.

### <a name="use-the-control-in-the-forms-layout"></a>Formun düzeninde denetimi kullanın

Bir uygulamada Demohesaplayıcı denetimini kullanmak için, onu bir forma yerleştirmeniz gerekir.

1. **Araç kutusu**'Nda **Demohesaplatorlib bileşenleri** düğümünü genişletin.

2. **Araç kutusu** ' ndan **demohesaplayıcı** denetimini formunuza sürükleyin. Denetimi formun sol üst köşesine taşıyın. Denetim formun kenarlıklarına yakınsa, yama *çizgileri* görüntülenir. Anlık görüntü çizgileri, formun `Padding` özelliğinin ve `Margin` denetimin özelliğinin uzaklığını belirtir. Denetimi, snaplines belirtilen konuma konumlandırın.

   Daha fazla bilgi için bkz [. İzlenecek yol: Denetimleri, yama çizgileri](/dotnet/framework/winforms/controls/walkthrough-arranging-controls-on-windows-forms-using-snaplines)kullanarak düzenleyin.

3. `Button` **Araç kutusu** ' ndan bir denetim sürükleyip form üzerine bırakın.

4. `Button` Denetimi demohesaplayıcı denetiminin çevresinde taşıyın ve anlık görüntü çizgilerinin nerede göründüğünü gözlemleyin. Bu özelliği kullanarak denetimlerinizi tam ve kolay bir şekilde hizalayabilirsiniz. İşiniz bittiğinde `Button` denetimi silin.

5. Demohesaplayıcı denetimini sağ seçin ve ardından **Özellikler**' i seçin.

6. `Dock` Özelliğin değerini olarak `Fill`değiştirin.

7. Formu seçin ve ardından `Padding` Özellik düğümünü genişletin. **All** değerini **20**olarak değiştirin.

   Demohesaplayıcı denetiminin boyutu, formun yeni `Padding` değerine uyum sağlayacak şekilde azaltılır.

8. Çeşitli boyutlandırma tutamaçlarını farklı konumlara sürükleyerek formu yeniden boyutlandırın. Demohesaplayıcı denetiminin sığması için nasıl yeniden boyutlandırıldığını gözlemleyin.

## <a name="next-steps"></a>Sonraki adımlar

Bu makalede, basit bir Hesaplayıcı için Kullanıcı arabiriminin nasıl oluşturulacağı gösterilmiştir. Devam etmek için, hesaplayıcı mantığını uygulayarak ve ardından [uygulamayı ClickOnce kullanarak yayımlayarak](../deployment/how-to-publish-a-clickonce-application-using-the-publish-wizard.md)işlevselliğini genişletebilirsiniz. Ya da [Windows Forms kullanarak bir resim görüntüleyici oluşturduğunuz](../ide/tutorial-1-create-a-picture-viewer.md)farklı bir öğreticiye devam edin.

## <a name="see-also"></a>Ayrıca bkz.

- [Windows Forms denetimleri](/dotnet/framework/winforms/controls/)
- [Windows Forms denetimleri için erişilebilirlik](/dotnet/framework/winforms/controls/providing-accessibility-information-for-controls-on-a-windows-form)
- [ClickOnce kullanarak yayımlama](../deployment/how-to-publish-a-clickonce-application-using-the-publish-wizard.md)