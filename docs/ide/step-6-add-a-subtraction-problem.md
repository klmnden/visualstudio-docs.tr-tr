---
title: '6\. Adım: Çıkarma problemi ekleme'
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- csharp
- vb
ms.assetid: 59204ef9-24bd-4f81-b85f-e3168e518a3e
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: d429d2921f252e97bfe7c233a9fe963f7f91299b
ms.sourcegitcommit: 59e5758036223ee866f3de5e3c0ab2b6dbae97b6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/23/2019
ms.locfileid: "68416555"
---
# <a name="step-6-add-a-subtraction-problem"></a>6\. Adım: Çıkarma problemi ekleme
Bu öğreticinin altıncı bölümünde, bir çıkarma sorunu ekleyecek ve aşağıdaki görevlerin nasıl gerçekleştirileceğini öğreneceksiniz:

- Çıkarma değerlerini saklayın.

- Sorun için rastgele sayılar oluşturun (ve yanıtın 0 ile 100 arasında olduğundan emin olun).

- Yanıtları denetleyen yöntemi, yeni çıkarma sorununu da denetleyecek şekilde güncelleştirin.

- Zamanlayıcının <xref:System.Windows.Forms.Timer.Tick> olay işleyicisini, zaman aşımına uğrar sonra olay işleyicisinin doğru yanıtı doldurması için güncelleştirin.

## <a name="to-add-a-subtraction-problem"></a>Çıkarma sorunu eklemek için

1. Ekleme sorunu ve Zamanlayıcı için tamsayı değişkenleri arasına, çıkarma sorunu için iki tamsayı değişkeni ekleyin. Kod aşağıdaki gibi görünmelidir.

     [!code-vb[VbExpressTutorial3Step5_6#12](../ide/codesnippet/VisualBasic/step-6-add-a-subtraction-problem_1.vb)]
     [!code-csharp[VbExpressTutorial3Step5_6#12](../ide/codesnippet/CSharp/step-6-add-a-subtraction-problem_1.cs)]

     Yeni tamsayı değişkenlerinin adları —**eksilen** ve **çıkarılan**— programlama terimleridir. Çıkarılan numara için aritmetik olarak geleneksel adlara sahiptir (çıkarılan) ve çıkarılan çıkarılan sayı (minuend). Aradaki fark, çıkarılan 'in eksi. Programınız değişkenler, denetimler, bileşenler veya yöntemler için özel adlar gerektirmediğinden diğer adları kullanabilirsiniz. Adları basamakla başlatma gibi kuralları izlemeniz gerekir, ancak genellikle x1, X2, X3 ve x4 gibi adları kullanabilirsiniz. Ancak, genel adlar kodun okunmasını zorlaştırabilir ve sorunları neredeyse olanaksız hale getirir. Değişken adlarını benzersiz ve yararlı tutmak için, bu öğreticide daha sonra çarpma (çoğullıve × çarpanı = ürün) ve bölüm (bölünen ÷ bölen = bölüm) için geleneksel adları kullanacaksınız.

     Daha sonra, çıkarma sorunu için `StartTheQuiz()` rastgele değerler sağlamak üzere metodunu değiştirirsiniz.

2. "Çıkarma sorununu doldur" açıklamasında sonra aşağıdaki kodu ekleyin.

     [!code-vb[VbExpressTutorial3Step5_6#13](../ide/codesnippet/VisualBasic/step-6-add-a-subtraction-problem_2.vb)]
     [!code-csharp[VbExpressTutorial3Step5_6#13](../ide/codesnippet/CSharp/step-6-add-a-subtraction-problem_2.cs)]

     Çıkarma sorununa yönelik olumsuz yanıtları engellemek için, bu kod, ek sorunun <xref:System.Random.Next> nasıl yaptığından farklı <xref:System.Random> olarak sınıfının yöntemini kullanır. `Next()` Yönteme iki değer verdiğinizde, ilk değerden büyük veya buna eşit ve ikinciden küçük bir rastgele sayı seçer. Aşağıdaki kod, 1 ile 100 arasında rastgele bir sayı seçer ve eksilen değişkeninde depolar.

     [!code-vb[VbExpressTutorial3Step5_6#21](../ide/codesnippet/VisualBasic/step-6-add-a-subtraction-problem_3.vb)]
     [!code-csharp[VbExpressTutorial3Step5_6#21](../ide/codesnippet/CSharp/step-6-add-a-subtraction-problem_3.cs)]

     Bu öğreticide daha `Next()` önce "rasgeleizer" olarak adlandırdığınız Random sınıfının yöntemini birden çok şekilde çağırabilirsiniz. Birden fazla yoldan çağırabileceğiniz Yöntemler aşırı yüklenmiş olarak adlandırılır ve IntelliSense 'i kullanarak bunları keşfedebilirsiniz. `Next()` Yöntemi için IntelliSense penceresinin araç ipucunda bir daha göz atın.

     ![IntelliSense penceresi araç](../ide/media/express_overloads.png)
İpucu**IntelliSense** penceresi araç ipucu

     Araç İpucu **(+ 2 aşırı yükleme**) gösterir. Bu, `Next()` yöntemi iki farklı şekilde çağırabilmeniz anlamına gelir. Aşırı yüklemeler farklı sayılar veya bağımsız değişken türleri içerir, böylece bir diğerinden biraz farklı çalışırlar. Örneğin, bir yöntem tek bir tamsayı bağımsız değişkeni alabilir ve aşırı yüklerinden biri tamsayı ve dize alabilir. Ne yapmak istediğinize bağlı olarak doğru aşırı yüklemeyi seçersiniz. Kodu `StartTheQuiz()` yöntemine eklediğinizde, girdiğiniz `randomizer.Next(`anda IntelliSense penceresinde daha fazla bilgi görüntülenir. Aşırı yüklemeler arasında geçiş yapmak için, aşağıdaki çizimde gösterildiği gibi **yukarı ok** ve **aşağı ok** tuşlarını seçin:

     ![IntelliSense&#40; &#41; 'de **Next ()** yöntemi](../ide/media/express_nextoverload.png) için IntelliSense aşırı yüklemesi içinde Next yöntemi  için aşırı yükleme

     Bu durumda, en düşük ve en yüksek değerleri belirtebileceğiniz için son aşırı yüklemeyi seçmek istersiniz.

3. Doğru çıkarma yanıtını denetlemek için yönteminideğiştirin.`CheckTheAnswer()`

     [!code-vb[VbExpressTutorial3Step5_6#14](../ide/codesnippet/VisualBasic/step-6-add-a-subtraction-problem_4.vb)]
     [!code-csharp[VbExpressTutorial3Step5_6#14](../ide/codesnippet/CSharp/step-6-add-a-subtraction-problem_4.cs)]

     Görselde C# `&&` , `logical and` işleçtir. Visual Basic ' de, eşdeğer işleç ' `AndAlso`dir. Bu işleçler, "addend1 ve addend2 toplamının Sum NumericUpDown değerine eşit olup olmadığını ve eksilen eksi çıkarılan değerinin fark NumericUpDown değerine eşit olup olmadığını gösterir. Yöntemi `CheckTheAnswer()` , yalnızca `true` toplama ve çıkarma sorunlarına verilen yanıtların ikisi de doğru olduğunda döndürülür.

4. Zamanlayıcının Tick olay işleyicisinin son bölümünü aşağıdaki kodla değiştirin, böylece zaman aşımı olduğunda doğru yanıtı dolduracaktır.

     [!code-vb[VbExpressTutorial3Step5_6#22](../ide/codesnippet/VisualBasic/step-6-add-a-subtraction-problem_5.vb)]
     [!code-csharp[VbExpressTutorial3Step5_6#22](../ide/codesnippet/CSharp/step-6-add-a-subtraction-problem_5.cs)]

5. Kodunuzu kaydedin ve çalıştırın.

     Aşağıdaki çizimde gösterildiği gibi programınız bir çıkarma sorunu içerir:

     ![Çıkarma sorunu ile matematik sınavından çıkarma sorunu ](../ide/media/express_addsubtract.png)


## <a name="to-continue-or-review"></a>Devam etmek veya gözden geçirmek için

- Sonraki öğretici adımına gitmek için bkz [. 7. Adım: Çarpma ve bölme sorunları](../ide/step-7-add-multiplication-and-division-problems.md)ekleyin.

- Önceki öğretici adımına dönmek için bkz [. 5. Adım: NumericUpDown denetimleri](../ide/step-5-add-enter-event-handlers-for-the-numericupdown-controls.md)için Enter Olay işleyicileri ekleyin.
