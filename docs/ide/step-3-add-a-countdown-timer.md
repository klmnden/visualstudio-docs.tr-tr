---
title: '3. Adım: Bir geri sayım Zamanlayıcısı ekleme'
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 62670a2b-efdc-45c6-9646-9b17eeb33dcb
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 2a703c7d4e28dd2287dff301727872b64e40b9ce
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60041423"
---
# <a name="step-3-add-a-countdown-timer"></a>3. Adım: Bir geri sayım Zamanlayıcısı ekleme
Bu Eğitimin üçüncü kısmında sınava giren bitirmek kalan saniye sayısını izlemek için bir geri sayım Zamanlayıcısı ekleyeceksiniz.

> [!NOTE]
>  Bu konu, temel kodlama kavramları hakkındaki bir öğretici serisinin bir parçasıdır. Öğreticiye genel bakış için bkz. [öğretici 2: Zamanlı matematik testi oluşturma](../ide/tutorial-2-create-a-timed-math-quiz.md).

## <a name="to-add-a-countdown-timer"></a>Bir geri sayım Zamanlayıcısı ekleme

1. Adlı bir tam sayı değişkeni ekleyin **timeLeft**, önceki yordamda yaptığınız gibi. Kodunuzu aşağıdaki gibi görünmelidir.

     [!code-vb[VbExpressTutorial3Step3#5](../ide/codesnippet/VisualBasic/step-3-add-a-countdown-timer_1.vb)]
     [!code-csharp[VbExpressTutorial3Step3#5](../ide/codesnippet/CSharp/step-3-add-a-countdown-timer_1.cs)]

     Şimdi, aslında bir olay başlatır, belirttiğiniz süre miktarını sonra bir Zamanlayıcı gibi saniye sayan bir yöntem gerekir.

2. Tasarım penceresinde Taşı bir <xref:System.Windows.Forms.Timer> denetimi **bileşenleri** kategorisi **araç kutusu** formunuza.

     Denetim tasarım penceresinin altındaki gri alanda görüntülenir.

3. Form üzerinde seçin **Süreölçer1** yalnızca eklenen ve Ayarla simgesi kendi **aralığı** özelliğini **1000**.

     Aralık değeri milisaniye cinsinden değeri 1000 neden olduğundan <xref:System.Windows.Forms.Timer.Tick> her saniye tetiklenmesine olay.

4. Formda çift **Zamanlayıcı** denetleyen veya bunu seçin ve ardından **Enter** anahtarı.

     Kod Düzenleyicisi görünür ve yeni eklediğiniz Tick olay işleyicisinin yöntemini görüntüler.

5. Aşağıdaki deyimleri yeni olay işleyici yöntemine ekleyin.

     [!code-vb[VbExpressTutorial3Step3#6](../ide/codesnippet/VisualBasic/step-3-add-a-countdown-timer_2.vb)]
     [!code-csharp[VbExpressTutorial3Step3#6](../ide/codesnippet/CSharp/step-3-add-a-countdown-timer_2.cs)]

     Zaman belirleyerek aşımına uğrayıp, eklediğiniz üzerinde bağlı olarak, Zamanlayıcı saniyede denetler olmadığını **timeLeft** tamsayı değişkeninin 0'dan büyük. İse, zaman kalıyor. Zamanlayıcı ilk Timeleft'ten 1 çıkarır ve ardından güncelleştirmeleri **metin** özelliği **timeLabel** sınava kaç saniye kaldığını göstermek için denetim.

     Hiçbir zaman kalırsa, Zamanlayıcıyı durdurur ve metnini değiştirir **timeLabel** , denetiminin **saatin yukarı!** Bir mesaj kutusu sınavın ve yanıt açıklanır sunar; bu durumda addend1 ve addend2 ekleyerek tarafından. **Etkin** özelliği **startButton** denetim ayarı **true** sınavı alanın başka bir test başlayabilmesi.

     Az önce eklediğiniz bir `if else` kararlar programların nasıl size deyimi. Bir `if else` deyimi aşağıdaki gibi görünür.

    > [!NOTE]
    >  Aşağıdaki örnek yalnızca gösterim amaçlıdır-projenize eklemeyin.

    ```vb
    If (something that your program will check) Then
        ' One or more statements that will run
        ' if what the program checked is true.
    Else
        ' One or more statements that will run
        ' if what the program checked is false.
    End If
    ```

    ```csharp
    if (something that your program will check)
    {
        // One or more statements that will run
        // if what the program checked is true.
    }
    else
    {
        // One or more statements that will run
        // if what the program checked is false.
    }
    ```

     Yakından bakın eklediğiniz deyime `else` ek soruya yanıtı göstermek için blok.

     [!code-vb[VbExpressTutorial3Step3#24](../ide/codesnippet/VisualBasic/step-3-add-a-countdown-timer_3.vb)]
     [!code-csharp[VbExpressTutorial3Step3#24](../ide/codesnippet/CSharp/step-3-add-a-countdown-timer_3.cs)]

     Deyim `addend1 + addend2` iki değişkendeki değerleri toplar. İlk Kısım (`sum.Value`) kullanan **değer** özelliğini doğru yanıtı görüntülemek için NumericUpDown denetimi. Aynı özellik daha sonra sınavın yanıtlarını denetlemek için kullanın.

     Sınava girenlerin sayı girebilir, daha kolay kullanarak bir <xref:System.Windows.Forms.NumericUpDown> matematik sorularının yanıtları için kullandığınız neden olan denetim. Olası yanıtların tümü 0 ile 100 arası tamsayılardır. Varsayılan değerlerini bırakarak tarafından **Minimum**, **maksimum**, ve **OndalıkBasamaklar** özellikleri, emin sınava girenlerin ondalık girin olamaz, negatif sayılar, veya çok yüksek sayılar. (Sınava girenlerin 3.141 girmek izin vermek istediyseniz ama 3.1415, ayarladığınız, **OndalıkBasamaklar** özelliğini 3.)

6. Sonuna üç satır ekleyin `StartTheQuiz()` yöntemi, kod aşağıdaki gibi görünür.

     [!code-vb[VbExpressTutorial3Step3#7](../ide/codesnippet/VisualBasic/step-3-add-a-countdown-timer_4.vb)]
     [!code-csharp[VbExpressTutorial3Step3#7](../ide/codesnippet/CSharp/step-3-add-a-countdown-timer_4.cs)]

     Artık sınavınız başladığında, **timeLeft** değişkenini 30 ve **metin** özelliği **timeLabel** denetimi, 30 saniye olarak ayarlanır. Ardından <xref:System.Windows.Forms.Timer.Start> Zamanlayıcı denetimi yöntemi geri sayımı başlatır. (Sınav yanıtı henüz denetlemedi; sonraki gelen.)

7. Programınızı kaydedin, çalıştırın ve ardından **Başlat** formundaki düğmesi.

     Zamanlayıcı saymaya başlar. Zaman zaman sınav sona erer ve yanıtlar görünür. Aşağıdaki çizim sınavı göstermektedir.

     ![Matematik sınavı devam ediyor](../ide/media/express_addcountdown.png) matematik sınavı devam ediyor

## <a name="to-continue-or-review"></a>Devam etmek veya gözden geçirmek için

- Sonraki öğretici adımına gitmek için bkz: [4. adım: CheckTheAnswer() yöntemi ekleme](../ide/step-4-add-the-checktheanswer-parens-method.md).

- Önceki öğretici adımına dönmek için bkz: [2. adım: Rasgele bir toplama problemi oluşturma](../ide/step-2-create-a-random-addition-problem.md).
