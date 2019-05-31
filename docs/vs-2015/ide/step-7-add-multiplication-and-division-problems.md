---
title: '7. Adım: Çarpma ve bölme problemleri ekleme | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: conceptual
ms.assetid: e638959e-f6a4-4eb4-b2e9-f63b7855cf8f
caps.latest.revision: 19
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 47623d7a65de85b50ad1910425052288a261e49d
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60109588"
---
# <a name="step-7-add-multiplication-and-division-problems"></a>7. Adım: Çarpma ve Bölme Problemleri Ekleme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bu Eğitimin yedinci kısmında çarpma ve bölme soruları ekleyeceksiniz ancak önce bu değişiklik hakkında düşünün. Değerleri depolamayı da içeren ilk adımı düşünün.  
  
### <a name="to-add-multiplication-and-division-problems"></a>Çarpma ve bölme sorunları ekleme  
  
1. Daha fazla dört tamsayı değişken formuna ekleyin.  
  
     [!code-csharp[VbExpressTutorial3Step7#15](../snippets/csharp/VS_Snippets_VBCSharp/vbexpresstutorial3step7/cs/form1.cs#15)]
     [!code-vb[VbExpressTutorial3Step7#15](../snippets/visualbasic/VS_Snippets_VBCSharp/vbexpresstutorial3step7/vb/form1.vb#15)]  
  
2. Daha önce yaptığınız gibi değiştirebilir `StartTheQuiz()` çarpma ve bölme sorularını için rastgele sayılarla dolduracak şekilde yöntemi.  
  
     [!code-csharp[VbExpressTutorial3Step7#16](../snippets/csharp/VS_Snippets_VBCSharp/vbexpresstutorial3step7/cs/form1.cs#16)]
     [!code-vb[VbExpressTutorial3Step7#16](../snippets/visualbasic/VS_Snippets_VBCSharp/vbexpresstutorial3step7/vb/form1.vb#16)]  
  
3. Değiştirme `CheckTheAnswer()` BT'nin ayrıca çarpma ve bölme sorularını kontrol edecek şekilde yöntemi.  
  
     [!code-csharp[VbExpressTutorial3Step7#17](../snippets/csharp/VS_Snippets_VBCSharp/vbexpresstutorial3step7/cs/form1.cs#17)]
     [!code-vb[VbExpressTutorial3Step7#17](../snippets/visualbasic/VS_Snippets_VBCSharp/vbexpresstutorial3step7/vb/form1.vb#17)]  
  
     Çarpı işareti (×) kolayca giremezsiniz ve bölme klavyeyi kullanarak oturum açma (bölü;), böylece Visual C# ve Visual Basic bir yıldız işareti (*) için çarpma ve bölme için bir eğik çizgi işareti (/) kabul edin.  
  
4. Zaman aşımı halinde doğru yanıtı doldurur. böylece, Zamanlayıcının Tick olay işleyicisinin son kısmını değiştirin.  
  
     [!code-csharp[VbExpressTutorial3Step7#23](../snippets/csharp/VS_Snippets_VBCSharp/vbexpresstutorial3step7/cs/form1.cs#23)]
     [!code-vb[VbExpressTutorial3Step7#23](../snippets/visualbasic/VS_Snippets_VBCSharp/vbexpresstutorial3step7/vb/form1.vb#23)]  
  
5. Programınızı kaydedin ve çalıştırın.  
  
     Sınava girenlerin aşağıdaki çizimde gösterildiği gibi sınavı tamamlamak için dört sorusuna yanıt vermeniz gerekir.  
  
     ![Dört Sorulu matematik sınavı](../ide/media/express-finishedquiz.png "Express_FinishedQuiz")  
Dört Sorulu matematik sınavı  
  
### <a name="to-continue-or-review"></a>Devam etmek veya gözden geçirmek için  
  
- Sonraki öğretici adımına gitmek için bkz: [adım 8: Testi özelleştirme](../ide/step-8-customize-the-quiz.md).  
  
- Önceki öğretici adımına dönmek için bkz: [adım 6: Çıkarma problemi ekleme](../ide/step-6-add-a-subtraction-problem.md).
