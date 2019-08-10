---
title: '9\. Adım: Kodunuzu gözden geçirme, açıklama ve test etme'
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- csharp
- vb
ms.assetid: f26f79ba-c91b-4164-b87f-679a1b231c09
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 15c5cfbd419cc34f4d26cdb90da03f38e28a26c4
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68925894"
---
# <a name="step-9-review-comment-and-test-your-code"></a>9\. Adım: Kodunuzu gözden geçirme, açıklama ve test etme
Daha sonra kodunuza bir açıklama eklersiniz. Yorum, programın davranış biçimini değiştirmeyen bir notdur. Kodunuzu okuyan birisinin ne yaptığını öğrenmesini kolaylaştırır. Kodunuza açıklama eklemek için iyi bir önleminizi alarak vardır. Görselde C#iki eğik çizgi (//) bir satırı açıklama olarak işaretleyin. Visual Basic, bir satırı açıklama olarak işaretlemek için tek tırnak işareti (') kullanılır. Bir açıklama ekledikten sonra, programınızı test edersiniz. Projeniz üzerinde çalışırken kodunuzu sık çalıştırmak ve test etmek iyi bir uygulamadır. bu sayede, kod daha karmaşık hale gelmeden önce sorunları önceden yakalayabilir ve çözebilirsiniz. Buna *yinelemeli test*denir.

Yalnızca bir şey oluşturmuş olabilirsiniz ve henüz yapılmasa da, bir resmi yükleyebilir. Kodunuza bir açıklama eklemeden ve test etmeden önce, bu kavramları sık kullandığınız için kod kavramlarını gözden geçirmek için zaman alın:

- **Windows form tasarımcısı** **resim göster** DÜĞMESINE çift tıkladığınızda, IDE programınızın koduna otomatik olarak bir *Yöntem* ekledi.

- Yöntemler, kodunuzu nasıl düzenleirsiniz: Kodunuz birlikte gruplandırılır.

- Çoğu zaman, yöntemin bir iletişim kutusu gösterdiği ve sonra bir resmi yükleyen gibi `showButton_Click()` belirli bir sırada çok sayıda şey yapar.

- Yöntem kod *deyimlerinden*veya kod satırlarından oluşur. Bir yöntemi kod deyimlerini birlikte paketetmenin bir yolu olarak düşünün.

- Bir yöntem yürütüldüğünde veya *çağrıldığında*, yöntem içindeki deyimler sırayla yürütülür ve ilki birinci bir ile başlar.

   Aşağıda bir deyimin örneği verilmiştir.

  ```csharp
  pictureBox1.Load(openFileDialog1.FileName);
  ```

  ```vb
  pictureBox1.Load(openFileDialog1.FileName)
  ```

   Deyimler, programlarınızın şeyleri yapabilecekleri şeydir. Görsel C#içinde, bir ifade her zaman noktalı virgül ile biter. Visual Basic, satırın sonu deyimin sonu olur. (Visual Basic noktalı virgül gerekmez.) Yukarıdaki ifade, denetiinizde <xref:System.Windows.Forms.PictureBox> **OpenFileDialog** bileşeni ile kullanıcının seçtiği dosyayı yüklemesini söyler.

  ![video](../data-tools/media/playvideo.gif)bağlantısı bu konunun video sürümü için bkz [. öğretici 1: Visual Basic-video 5](http://go.microsoft.com/fwlink/?LinkId=205216) veya [öğretici 1 ' de bir resim Görüntüleyicisi oluşturun: Video 5 C# ](http://go.microsoft.com/fwlink/?LinkId=205206)' te bir resim görüntüleyici oluşturun. Bu videolar, Visual Studio 'nun önceki bir sürümünü kullanır, bu nedenle bazı menü komutlarında ve diğer kullanıcı arabirimi öğelerinde küçük farklılıklar vardır. Ancak, kavramlar ve yordamlar Visual Studio 'nun geçerli sürümünde benzer şekilde çalışır.

## <a name="to-add-comments"></a>Açıklama eklemek için

1. Aşağıdaki yorumu kodunuza ekleyin.

     [!code-vb[VbExpressTutorial1Step9_10#1](../ide/codesnippet/VisualBasic/step-9-review-comment-and-test-your-code_1.vb)]
     [!code-csharp[VbExpressTutorial1Step9_10#1](../ide/codesnippet/CSharp/step-9-review-comment-and-test-your-code_1.cs)]

    > [!NOTE]
    > **ShowButton** düğinizin <xref:System.Windows.Forms.Control.Click> olay işleyicisi artık tamamlandı ve çalışıyor. Bir `if` deyimden başlayarak kod yazmaya başladıysanız. Bir `if` ifade, programınıza "Bu şeyi denetle ve doğru ise, bu eylemleri yapın." Bu durumda, programınıza **Dosya Aç** iletişim kutusunu açmasını söylersiniz ve Kullanıcı bir dosya seçip **Tamam** düğmesini seçerse, bu dosyayı **PictureBox**'a yükleyin.

    > [!TIP]
    > IDE, kod yazmanızı kolaylaştıracak şekilde oluşturulmuştur ve *kod parçacıkları* bunu yapmanın bir yoludur. Kod parçacığı, küçük bir kod bloğuna genişletilmiş bir kısayoldur.
    >
    >  Kullanılabilir tüm parçacıkları görebilirsiniz. Menü çubuğunda **Araçlar** > **kod parçacıkları Yöneticisi**' ni seçin. C# Görsel`if` için kod parçacığı görseldir. **C#** Visual Basic için, `if` kod parçacıkları **conditionals ve döngü** > **kodu desenlerinde**yer alır. Bu yöneticiyi, mevcut parçacıkları taramak veya kendi kod parçacıklarınızı eklemek için kullanabilirsiniz.
    >
    >  Kodu yazarken bir kod parçacığını etkinleştirmek için yazın ve **sekme** tuşunu seçin. Birçok parçacık, **IntelliSense** penceresinde görünür. bu nedenle, **IntelliSense** penceresinde kod PARÇACıĞıNı seçmek ve sonra IDE 'nin kod parçacığını kullanmasını söylemek için. (IntelliSense parçacığı destekler `if` , ancak `ifelse` kod parçacığını destekler.)

2. Programınızı çalıştırmadan önce, aşağıdaki gibi görünen **Tümünü Kaydet** araç çubuğu düğmesini seçerek programınızı kaydedin.

     ![Tümünü Kaydet araç çubuğu](../ide/media/express_iconsaveall.png)
düğmesi**Tümünü Kaydet** düğmesi

     Alternatif olarak, programınızı kaydetmek için menü çubuğunda **Dosya** > **Tümünü Kaydet**' i seçin. Bu, erken ve sık tasarrufu sağlamak için en iyi uygulamadır.

     Çalıştığında, programınız aşağıdaki resim gibi görünmelidir.

     ![Resim görüntüleyici](../ide/media/express_pictureviewerdonerun.png)
**Resim Görüntüleyicisi**

## <a name="to-test-your-program"></a>Programınızı test etmek için

1. **F5** tuşunu seçin veya **hata ayıklamayı Başlat** araç çubuğu düğmesini seçin.

2. Yeni yazdığınız kodu çalıştırmak için **bir resim göster** düğmesini seçin. İlk olarak, program açık bir **Dosya** iletişim kutusu açar. Filtrelerinizin, iletişim kutusunun alt kısmındaki **dosya türü** açılan listesinde göründüğünü doğrulayın. Ardından bir resme gidin ve açın. Genellikle Belgelerim klasörünüzdeki Windows işletim sistemiyle birlikte gelen örnek resimleri, *Resimlerim \ örnek resimler* klasörü içinde bulabilirsiniz.

    > [!NOTE]
    > **Resim dosyası seç** iletişim kutusunda herhangi bir görüntü görmüyorsanız, iletişim kutusunun sağ alt tarafındaki aşağı açılan listede **tüm dosyalar (\**.)** filtresinin seçili olduğundan emin olun.

3. Bir resim yükleyin ve PictureBox 'da görünür. Ardından, kenarlıklarını sürükleyerek formunuzu yeniden boyutlandırmayı deneyin. PictureBox 'ın, kendisini formun içine yerleştirilmiş bir TableLayoutPanel içinde yerleştiğinden, resim alanı kendini form kadar geniş olacak şekilde yeniden boyutlandırır ve formun en üstteki% 90 ' unu dolduracaktır. <xref:System.Windows.Forms.TableLayoutPanel> Ve<xref:System.Windows.Forms.FlowLayoutPanel> kapsayıcılarını şu şekilde kullandınız: Kullanıcı onu yeniden boyutlandırdığında formunuzu doğru boyutlandırırlar.

     Şimdi, daha büyük resimler resim görüntüleyicinizin kenarlıklarının ötesine geçer. Sonraki adımda, resimlerin pencereye sığması için kod ekleyeceksiniz.

## <a name="to-continue-or-review"></a>Devam etmek veya gözden geçirmek için

- Sonraki öğretici adımına gitmek için bkz [. adım 10: Ek düğmeler ve onay kutusu](../ide/step-10-write-code-for-additional-buttons-and-a-check-box.md)için kod yazın.

- Önceki öğretici adımına dönmek için bkz [. 8. Adım: Resim göster düğmesi olay işleyicisi](../ide/step-8-write-code-for-the-show-a-picture-button-event-handler.md)için kod yazın.
