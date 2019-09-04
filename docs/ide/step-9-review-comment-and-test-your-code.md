---
title: '9\. Adım: Kodunuzu gözden geçirme, açıklama ve test etme'
ms.date: 08/30/2019
ms.assetid: f26f79ba-c91b-4164-b87f-679a1b231c09
ms.topic: tutorial
ms.prod: visual-studio-windows
ms.technology: vs-ide-general
ms.devlang:
- csharp
- vb
dev_langs:
- csharp
- vb
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 6f9f5c6f3aff6338feb0de16a44d3b7d02d0c3b9
ms.sourcegitcommit: 9c07ae6fb18204ea080c8248994a683fa12e5c82
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/04/2019
ms.locfileid: "70293644"
---
# <a name="step-9-review-comment-and-test-your-code"></a>9\. Adım: Kodunuzu gözden geçirme, açıklama ve test etme

Daha sonra kodunuza bir açıklama eklersiniz. Yorum, programın davranış biçimini değiştirmeyen bir notdur. Kodunuzu okuyan birisinin ne yaptığını öğrenmesini kolaylaştırır. Kodunuza açıklama eklemek için iyi bir önleminizi alarak vardır.

İçinde C#, iki eğik çizgi (//) bir satırı açıklama olarak işaretler. Visual Basic, bir satırı açıklama olarak işaretlemek için tek tırnak işareti (') kullanılır. Bir açıklama ekledikten sonra, programınızı test edersiniz. Projeniz üzerinde çalışırken kodunuzu sık çalıştırmak ve test etmek iyi bir uygulamadır. bu sayede, kod daha karmaşık hale gelmeden önce sorunları önceden yakalayabilir ve çözebilirsiniz. Buna *yinelemeli test*denir.

Yalnızca bir şey oluşturmuş olabilirsiniz ve henüz yapılmasa da, bir resmi yükleyebilir. Kodunuza bir açıklama eklemeden ve test etmeden önce, bu kavramları sık kullandığınız için kod kavramlarını gözden geçirmek için zaman alın:

- **Windows form tasarımcısı** **resim göster** DÜĞMESINE çift tıkladığınızda, IDE programınızın koduna otomatik olarak bir *Yöntem* ekledi.

- Yöntemler, kodunuzu nasıl düzenleirsiniz: Kodunuz birlikte gruplandırılır.

- Çoğu zaman, `showButton_Click()` (veya `ShowButton_Click()`) yönteminizin bir iletişim kutusu gösterdiği ve sonra bir resmi yükleyen gibi belirli bir sırada çok sayıda şey yapmaz.

- Yöntem kod *deyimlerinden*veya kod satırlarından oluşur. Bir yöntemi kod deyimlerini birlikte paketetmenin bir yolu olarak düşünün.

- Bir yöntem yürütüldüğünde veya *çağrıldığında*, yöntem içindeki deyimler sırayla yürütülür ve ilki birinci bir ile başlar.

   Aşağıda bir deyimin örneği verilmiştir.

  ```csharp
  PictureBox1.Load(openFileDialog1.FileName);
  ```

  ```vb
  pictureBox1.Load(openFileDialog1.FileName)
  ```

   Deyimler, programlarınızın şeyleri yapabilecekleri şeydir. İçinde C#, bir ifade her zaman noktalı virgül ile biter. Visual Basic, satırın sonu deyimin sonu olur. (Visual Basic noktalı virgül gerekmez.) Yukarıdaki ifade, denetiinizde <xref:System.Windows.Forms.PictureBox> **OpenFileDialog** bileşeni ile kullanıcının seçtiği dosyayı yüklemesini söyler.

## <a name="to-add-comments"></a>Açıklama eklemek için

1. Aşağıdaki yorumu kodunuza ekleyin.

    > [!IMPORTANT]
    > C# Kod parçacığını veya Visual Basic kod parçacığını görüntülemek için bu sayfanın sağ üst kısmındaki programlama dili denetimini kullanın.<br><br>![Docs.Microsoft.com için programlama dili denetimi](../ide/media/docs-programming-language-control.png)

     [!code-csharp[VbExpressTutorial1Step9_10#1](../ide/codesnippet/CSharp/step-9-review-comment-and-test-your-code_1.cs)]
     
     [!code-vb[VbExpressTutorial1Step9_10#1](../ide/codesnippet/VisualBasic/step-9-review-comment-and-test-your-code_1.vb)]

    **ShowButton** düğinizin <xref:System.Windows.Forms.Control.Click> olay işleyicisi artık tamamlandı ve çalışıyor. Bir `if` deyimden başlayarak kod yazmaya başladıysanız. Bir `if` ifade, programınıza "Bu şeyi denetle ve doğru ise, bu eylemleri yapın." Bu durumda, programınıza **Dosya Aç** iletişim kutusunu açmasını söylersiniz ve Kullanıcı bir dosya seçip **Tamam** düğmesini seçerse, bu dosyayı **PictureBox**'a yükleyin.

    > [!TIP]
    > IDE, kod yazmanızı kolaylaştıracak şekilde oluşturulmuştur ve *kod parçacıkları* bunu yapmanın bir yoludur. Kod parçacığı, küçük bir kod bloğuna genişletilmiş bir kısayoldur.
    >
    >  Kullanılabilir tüm parçacıkları görebilirsiniz. Menü çubuğunda **Araçlar** > **kod parçacıkları Yöneticisi**' ni seçin. İçin C#, `if` kod parçacığı **görseldir C#**  . Visual Basic için, `if` kod parçacıkları **conditionals ve döngü** > **kodu desenlerinde**yer alır. Bu yöneticiyi, mevcut parçacıkları taramak veya kendi kod parçacıklarınızı eklemek için kullanabilirsiniz.
    >
    >  Kodu yazarken bir kod parçacığını etkinleştirmek için yazın ve **sekme** tuşunu seçin. Birçok parçacık, **IntelliSense** penceresinde görünür. bu **nedenle,** **IntelliSense** PENCERESINDE kod parçacığını seçmek ve sonra IDE 'nin kod parçacığını kullanmasını söylemek için. (IntelliSense parçacığı destekler `if` , ancak `ifelse` kod parçacığını destekler.)

1. Programınızı çalıştırmadan önce, aşağıdaki ekran görüntüsüne benzer şekilde görünmesi gereken, **Tümünü Kaydet** araç çubuğu düğmesini seçerek programınızı kaydedin.

     ![Tümünü Kaydet araç çubuğu düğmesi](../ide/media/express_iconsaveall.png)<br>
***Tümünü Kaydet*** *düğme*

     Alternatif olarak, programınızı kaydetmek için, **Dosya** > **Tümünü** menü çubuğundan Kaydet ' i seçin (veya **CTRL**+ **+ Shift**+**S**tuşlarına basın). Bu, erken ve sık tasarrufu sağlamak için en iyi uygulamadır.

     Çalıştığında, programınız aşağıdaki görüntüye benzer şekilde görünmelidir.

     ![Resim görüntüleyici](../ide/media/express_pictureviewerdonerun.png)<br>***Resim görüntüleyici***

## <a name="to-test-your-program"></a>Programınızı test etmek için

1. **F5** tuşunu seçin veya **hata ayıklamayı Başlat** araç çubuğu düğmesini seçin.

1. Yeni yazdığınız kodu çalıştırmak için **bir resim göster** düğmesini seçin. İlk olarak, program açık bir **Dosya** iletişim kutusu açar. Filtrelerinizin, iletişim kutusunun alt kısmındaki **dosya türü** açılan listesinde göründüğünü doğrulayın. Ardından bir resme gidin ve açın. Genellikle *Belgelerim klasörünüzdeki Windows* işletim sistemiyle birlikte gelen örnek resimleri, *Resimlerim \ örnek resimler* klasörü içinde bulabilirsiniz.

    > [!TIP]
    > **Resim dosyası seç** iletişim kutusunda herhangi bir görüntü görmüyorsanız, iletişim kutusunun sağ alt tarafındaki aşağı açılan listede **tüm dosyalar (\**.)** filtresinin seçili olduğundan emin olun.

1. Bir resim yükleyin ve PictureBox 'da görünür. Ardından, kenarlıklarını sürükleyerek formunuzu yeniden boyutlandırmayı deneyin. PictureBox 'ın, kendisini formun içine yerleştirilmiş bir TableLayoutPanel içinde yerleştiğinden, resim alanı kendini form kadar geniş olacak şekilde yeniden boyutlandırır ve formun en üstteki% 90 ' unu dolduracaktır. <xref:System.Windows.Forms.TableLayoutPanel> Ve<xref:System.Windows.Forms.FlowLayoutPanel> kapsayıcılarını şu şekilde kullandınız: Kullanıcı onu yeniden boyutlandırdığında formunuzu doğru boyutlandırırlar.

     Şimdi, daha büyük resimler resim görüntüleyicinizin kenarlıklarının ötesine geçer. Sonraki adımda, resimlerin pencereye sığması için kod ekleyeceksiniz.

## <a name="to-continue-or-review"></a>Devam etmek veya gözden geçirmek için

- Sonraki öğretici adımına gitmek için bkz [. adım 10: Ek düğmeler ve onay kutusu](../ide/step-10-write-code-for-additional-buttons-and-a-check-box.md)için kod yazın.

- Önceki öğretici adımına dönmek için bkz [. 8. Adım: Resim göster düğmesi olay işleyicisi](../ide/step-8-write-code-for-the-show-a-picture-button-event-handler.md)için kod yazın.

## <a name="see-also"></a>Ayrıca bkz.

* [Öğretici 2: Süreli matematik testi oluşturma](tutorial-2-create-a-timed-math-quiz.md)
* [Öğretici 3: Eşleşen bir oyun oluşturun](tutorial-3-create-a-matching-game.md)
