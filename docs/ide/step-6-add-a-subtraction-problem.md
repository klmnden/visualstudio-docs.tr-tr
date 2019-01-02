---
title: '6. Adım: Çıkarma problemi ekleme'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: conceptual
ms.assetid: 59204ef9-24bd-4f81-b85f-e3168e518a3e
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: f42d2b414e79c1138f699964808ff13a375ec4fe
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53948173"
---
# <a name="step-6-add-a-subtraction-problem"></a>6. Adım: Çıkarma problemi ekleme
Bu Eğitimin altıncı kısmında bir çıkarma sorusu ekleyin ve aşağıdaki görevleri nasıl gerçekleştireceğinizi öğrenin:

-   Çıkarma değerlerini Store.

-   Sorun için rastgele sayılar üretin (ve yanıtın 0 ile 100 arasında olduğundan emin olun).

-   Yanıtları denetler ve böylece çok yeni bir çıkarma sorusu denetler yöntemi güncelleştirin.

-   Zamanlayıcınızın güncelleştirme <xref:System.Windows.Forms.Timer.Tick> olay işleyicisi böylece Süre dolduğunda olay işleyicisi doğru yanıtı doldurur.

## <a name="to-add-a-subtraction-problem"></a>Çıkartma problemi ekleme

1.  Formunuza tamsayı değişkenleri ek sorunun ve Zamanlayıcının arasında çıkartma sorusu için iki tamsayı değişkeni ekleyin. Kod aşağıdaki gibi görünmelidir.

     [!code-vb[VbExpressTutorial3Step5_6#12](../ide/codesnippet/VisualBasic/step-6-add-a-subtraction-problem_1.vb)]
     [!code-csharp[VbExpressTutorial3Step5_6#12](../ide/codesnippet/CSharp/step-6-add-a-subtraction-problem_1.cs)]

     Yeni tamsayı değişkenlerinin adları —**Eksilen** ve **çıkarılan**— programlama terimleri değildir. Bunlar, çıkarılmakta olan sayı (çıkarılan) ile içinden çıkartıldığı sayı (Eksilen) çıkartılır için aritmetikte kullanılan geleneksel adlardır hedeflenmiştir. Fark, Eksilen eksi çıkarılandır vardır. Programınızı değişkenler, denetimler, bileşenler veya yöntemleri için belirli adlar verilmesini gerektirmediği diğer adlar kullanabilirsiniz. Adları basamak ile başlamıyor gibi kurallara uymanız gerekir, ancak genellikle x1, x2 x3 ve x4 gibi adlar kullanabilirsiniz. Ancak genel adlar kodun zor okunmasına ve sorunların neredeyse çözülemez hale. Değişken adları benzersiz ve yararlı tutmak için çarpma geleneksel adlarını kullanmanız gerekir (çarpan × çarpan ürün =) ve bölme (bölü; bölen bölünen sayının =) Bu öğreticinin sonraki bölümlerinde.

     Ardından, değiştireceksiniz `StartTheQuiz()` yöntemini çıkarma sorusu için rastgele değerler sağlayacak.

2.  Aşağıdaki kodu "çıkartma sorusundaki dolgu" yorumundan sonra ekleyin.

     [!code-vb[VbExpressTutorial3Step5_6#13](../ide/codesnippet/VisualBasic/step-6-add-a-subtraction-problem_2.vb)]
     [!code-csharp[VbExpressTutorial3Step5_6#13](../ide/codesnippet/CSharp/step-6-add-a-subtraction-problem_2.cs)]

     Çıkartma sorusu için negatif yanıtları önlemek için bu kodu kullanan <xref:System.Random.Next> yöntemi <xref:System.Random> biraz farklı ek sorunun nasıl yaptığını sınıfı. Size zaman `Next()` yöntemine iki değer değerinden büyük veya eşit ilk değer ve daha az rastgele bir sayı seçer ve ikinci değerden. Aşağıdaki kod, 1 ile 100 arasında rastgele bir sayı seçer ve bunu Eksilen değişkeninde depolar.

     [!code-vb[VbExpressTutorial3Step5_6#21](../ide/codesnippet/VisualBasic/step-6-add-a-subtraction-problem_3.vb)]
     [!code-csharp[VbExpressTutorial3Step5_6#21](../ide/codesnippet/CSharp/step-6-add-a-subtraction-problem_3.cs)]

     Çağırabilirsiniz `Next()` birden çok yolla bu öğreticinin önceki kısımlarındaki "randomizer" adlı rastgele sınıfının yöntemi. Birden fazla şekilde çağırabileceğiniz yöntemler için aşırı yüklü olarak başvurulur ve bunlarda gezinmek için IntelliSense'i kullanabilirsiniz. Konum yeniden için IntelliSense penceresini araç ipucuna `Next()` yöntemi.

     ![IntelliSense pencere araç ipucu](../ide/media/express_overloads.png)
**IntelliSense** pencere araç ipucu

     Araç İpucu gösterilmektedir **(+ 2 çağırabileceğiniz**, çağırabileceğiniz anlamına gelen `Next()` iki yolla yöntemi. Böylece birbirinden biraz farklı çalıştığını farklı sayılarda ya da türlerde bağımsız değişkenleri, aşırı yüklemeleri içerir. Örneğin, bir yöntem tek bir bağımsız değişken alabilir ve bunun aşırı yüklerinden biri bir tam sayı ve bir dize alabilir. Ne, bunu yapmak için istediğinize bağlı olarak doğru aşırı yüklemesi'ı seçin. Koda eklediğinizde `StartTheQuiz()` yöntemi, daha fazla bilgi IntelliSense penceresinde görünür, girer girmez `randomizer.Next(`. Aşırı yüklemeler arasında geçiş yapmak için seçin **yukarı ok** ve **aşağı ok** anahtarları aşağıdaki çizimde gösterildiği gibi:

     ![Sonraki için aşırı yükleme&#40; &#41; IntelliSense yönteminde](../ide/media/express_nextoverload.png) için aşırı yükleme **Next()** yönteminde **IntelliSense**

     Bu durumda, minimum ve maksimum değerleri belirttiğinden, son aşırı yükü seçmek istersiniz.

3.  Değiştirme `CheckTheAnswer()` yöntemini doğru çıkarma yanıtını kontrol edecek şekilde.

     [!code-vb[VbExpressTutorial3Step5_6#14](../ide/codesnippet/VisualBasic/step-6-add-a-subtraction-problem_4.vb)]
     [!code-csharp[VbExpressTutorial3Step5_6#14](../ide/codesnippet/CSharp/step-6-add-a-subtraction-problem_4.cs)]

     Visual C# içinde `&&` olduğu `logical and` işleci. Visual Basic'te, eşdeğer işlecidir `AndAlso`. Bu işleçler "addend1 ve addend2 Toplamı toplam NumericUpDown değeri eşitse göstermeye yardımcı olur ve Eksilen eksi çıkarılan fark NumericUpDown'ının değerine eşitse." `CheckTheAnswer()` Yöntemi döndürür `true` yalnızca toplama ve çıkarma yanıtlar doğru hem de olması gerekir.

4.  Zaman aşımı halinde doğru yanıtı doldurur. böylece, Zamanlayıcının Tick olay işleyicisinin son kısmını aşağıdaki kodla değiştirin.

     [!code-vb[VbExpressTutorial3Step5_6#22](../ide/codesnippet/VisualBasic/step-6-add-a-subtraction-problem_5.vb)]
     [!code-csharp[VbExpressTutorial3Step5_6#22](../ide/codesnippet/CSharp/step-6-add-a-subtraction-problem_5.cs)]

5.  Kaydet ve kodunuzu çalıştırın.

     Programınız aşağıdaki çizimde gösterildiği gibi bir çıkarma sorusu içerir:

     ![Çıkarma Sorulu matematik sınavı](../ide/media/express_addsubtract.png)
**matematik sınavı** çıkarma Sorulu

## <a name="to-continue-or-review"></a>Devam etmek veya gözden geçirmek için

-   Sonraki öğretici adımına gitmek için bkz: [adım 7: Çarpma ve bölme soruları ekleyin](../ide/step-7-add-multiplication-and-division-problems.md).

-   Önceki öğretici adımına dönmek için bkz: [5. adım: NumericUpDown denetimleri için gir olayı işleyicilerini ekleme](../ide/step-5-add-enter-event-handlers-for-the-numericupdown-controls.md).
