---
title: '7. Adım: Çarpma ve bölme soruları ekleyin'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: conceptual
ms.assetid: e638959e-f6a4-4eb4-b2e9-f63b7855cf8f
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 359f4e5035c564a3f7f4b117994ab4d84d1f6eff
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53889007"
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
