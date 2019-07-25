---
title: '7\. Adım: Çarpma ve bölme problemleri ekleme'
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- csharp
- vb
ms.assetid: e638959e-f6a4-4eb4-b2e9-f63b7855cf8f
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 887af3a439e1f6e0f21d5ca68061d2f9977dfac7
ms.sourcegitcommit: 59e5758036223ee866f3de5e3c0ab2b6dbae97b6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/23/2019
ms.locfileid: "68416542"
---
# <a name="step-7-add-multiplication-and-division-problems"></a>7\. Adım: Çarpma ve bölme problemleri ekleme
Bu öğreticinin yedinci kısmında çarpma ve bölme sorunları ekleyeceksiniz, ancak önce bu değişikliği nasıl yapacağınızı düşünün. Değerlerin depolanmasını içeren ilk adımı göz önünde bulundurun.

## <a name="to-add-multiplication-and-division-problems"></a>Çarpma ve bölme sorunları eklemek için

1. Forma dört tamsayı değişken ekleyin.

     [!code-vb[VbExpressTutorial3Step7#15](../ide/codesnippet/VisualBasic/step-7-add-multiplication-and-division-problems_1.vb)]
     [!code-csharp[VbExpressTutorial3Step7#15](../ide/codesnippet/CSharp/step-7-add-multiplication-and-division-problems_1.cs)]

2. Daha önce yaptığınız gibi, çarpma ve `StartTheQuiz()` bölme sorunları için yöntemi rastgele sayıları dolduracak şekilde değiştirin.

     [!code-vb[VbExpressTutorial3Step7#16](../ide/codesnippet/VisualBasic/step-7-add-multiplication-and-division-problems_2.vb)]
     [!code-csharp[VbExpressTutorial3Step7#16](../ide/codesnippet/CSharp/step-7-add-multiplication-and-division-problems_2.cs)]

3. `CheckTheAnswer()` Yöntemi, çarpma ve bölme sorunlarını da denetleyecek şekilde değiştirin.

     [!code-vb[VbExpressTutorial3Step7#17](../ide/codesnippet/VisualBasic/step-7-add-multiplication-and-division-problems_3.vb)]
     [!code-csharp[VbExpressTutorial3Step7#17](../ide/codesnippet/CSharp/step-7-add-multiplication-and-division-problems_3.cs)]

     Klavye kullanarak çarpma işaretini (×) ve bölme işaretini (÷) kolayca giremezsiniz, böylece görsel C# ve Visual Basic bölme için bir yıldız işareti (*) ve bölme için bir eğik çizgi (/) kabul eder.

4. Zamanlayıcının <xref:System.Windows.Forms.Timer.Tick> olay işleyicisinin son bölümünü, zaman dolduğunda doğru yanıtı dolduracak şekilde değiştirin.

     [!code-vb[VbExpressTutorial3Step7#23](../ide/codesnippet/VisualBasic/step-7-add-multiplication-and-division-problems_4.vb)]
     [!code-csharp[VbExpressTutorial3Step7#23](../ide/codesnippet/CSharp/step-7-add-multiplication-and-division-problems_4.cs)]

5. Programınızı kaydedin ve çalıştırın.

     Aşağıdaki çizimde gösterildiği gibi, test takiciler, testi tamamlamaya yönelik dört sorunu yanıtmalıdır.

     ![Dört problemi olan matematik sınavından](../ide/media/express_finishedquiz.png)
dört sorunla karşılaşırsanız

## <a name="to-continue-or-review"></a>Devam etmek veya gözden geçirmek için

- Sonraki öğretici adımına gitmek için bkz [. 8. Adım: Testi](../ide/step-8-customize-the-quiz.md)özelleştirin.

- Önceki öğretici adımına dönmek için bkz [. 6. Adım: Çıkarma sorunu](../ide/step-6-add-a-subtraction-problem.md)ekleyin.
