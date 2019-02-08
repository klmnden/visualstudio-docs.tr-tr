---
title: '7. Adım: Çarpma ve bölme soruları ekleyin'
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: e638959e-f6a4-4eb4-b2e9-f63b7855cf8f
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 6bc9c1e28b86956c611d48d332c3444665a66de4
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55917824"
---
# <a name="step-7-add-multiplication-and-division-problems"></a>7. Adım: Çarpma ve bölme soruları ekleyin
Bu Eğitimin yedinci kısmında çarpma ve bölme soruları ekleyeceksiniz ancak önce bu değişiklik hakkında düşünün. Değerleri depolamayı da içeren ilk adımı düşünün.

## <a name="to-add-multiplication-and-division-problems"></a>Çarpma ve bölme sorunları ekleme

1.  Daha fazla dört tamsayı değişken formuna ekleyin.

     [!code-vb[VbExpressTutorial3Step7#15](../ide/codesnippet/VisualBasic/step-7-add-multiplication-and-division-problems_1.vb)]
     [!code-csharp[VbExpressTutorial3Step7#15](../ide/codesnippet/CSharp/step-7-add-multiplication-and-division-problems_1.cs)]

2.  Daha önce yaptığınız gibi değiştirebilir `StartTheQuiz()` çarpma ve bölme sorularını için rastgele sayılarla dolduracak şekilde yöntemi.

     [!code-vb[VbExpressTutorial3Step7#16](../ide/codesnippet/VisualBasic/step-7-add-multiplication-and-division-problems_2.vb)]
     [!code-csharp[VbExpressTutorial3Step7#16](../ide/codesnippet/CSharp/step-7-add-multiplication-and-division-problems_2.cs)]

3.  Değiştirme `CheckTheAnswer()` BT'nin ayrıca çarpma ve bölme sorularını kontrol edecek şekilde yöntemi.

     [!code-vb[VbExpressTutorial3Step7#17](../ide/codesnippet/VisualBasic/step-7-add-multiplication-and-division-problems_3.vb)]
     [!code-csharp[VbExpressTutorial3Step7#17](../ide/codesnippet/CSharp/step-7-add-multiplication-and-division-problems_3.cs)]

     Çarpı işareti (×) kolayca giremezsiniz ve bölme klavyeyi kullanarak oturum açma (bölü;), böylece Visual C# ve Visual Basic bir yıldız işareti (*) için çarpma ve bölme için bir eğik çizgi işareti (/) kabul edin.

4.  Zamanlayıcının son kısmını değiştirin <xref:System.Windows.Forms.Timer.Tick> Süre dolduğunda BT'nin doğru yanıtı dolduracak şekilde olay işleyicisi.

     [!code-vb[VbExpressTutorial3Step7#23](../ide/codesnippet/VisualBasic/step-7-add-multiplication-and-division-problems_4.vb)]
     [!code-csharp[VbExpressTutorial3Step7#23](../ide/codesnippet/CSharp/step-7-add-multiplication-and-division-problems_4.cs)]

5.  Programınızı kaydedin ve çalıştırın.

     Sınava girenlerin aşağıdaki çizimde gösterildiği gibi sınavı tamamlamak için dört sorusuna yanıt vermeniz gerekir.

     ![Dört Sorulu matematik sınavı](../ide/media/express_finishedquiz.png)
**matematik sınavı** dört Sorulu

## <a name="to-continue-or-review"></a>Devam etmek veya gözden geçirmek için

-   Sonraki öğretici adımına gitmek için bkz: [adım 8: Testi özelleştirme](../ide/step-8-customize-the-quiz.md).

-   Önceki öğretici adımına dönmek için bkz: [adım 6: Çıkarma problemi ekleme](../ide/step-6-add-a-subtraction-problem.md).
