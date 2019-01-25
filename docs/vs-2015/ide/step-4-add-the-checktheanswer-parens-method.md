---
title: '4. Adım: CheckTheAnswer() yöntemi ekleme | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: conceptual
ms.assetid: c66f3831-b4a0-40bc-a109-8f46f4db35ed
caps.latest.revision: 21
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 8ce0a3f35001c468f887c1a595cd37231b38cb72
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54802509"
---
# <a name="step-4-add-the-checktheanswer-method"></a>4. Adım: CheckTheAnswer() Yöntemi Ekleme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bu Eğitimin dördüncü kısmında bir yöntem yazacaksınız `CheckTheAnswer()`, matematik sorularının yanıtlarını doğru olup olmadığını belirler. Bu konu, temel kodlama kavramları hakkındaki bir öğretici serisinin bir parçasıdır. Öğreticiye genel bakış için bkz. [öğretici 2: Zamanlı matematik testi oluşturma](../ide/tutorial-2-create-a-timed-math-quiz.md).  
  
> [!NOTE]
>  Visual Basic'te izliyorsanız, kullanacağınız `Function` anahtar sözcüğü yerine `Sub` anahtar sözcüğü çünkü bu yöntem bir değer döndürür. Bu gerçekten bu kadar kolaydır: bir alt bir değer döndürmez ama bir işlev.  
  
### <a name="to-verify-whether-the-answers-are-correct"></a>Yanıtların doğru olup olmadığını doğrulamak için  
  
1.  Ekleme `CheckTheAnswer()` yöntemi.  
  
     Bu yöntem çağrıldığında, addend1 ve addend2 değerleri toplar ve sonucu toplama karşılaştırır `NumericUpDown` denetimi. Değerler eşitse yöntem değerini döndürür. `true`. Aksi takdirde yöntem bir değeri döndürür `false`. Kodunuzu aşağıdaki gibi görünmelidir.  
  
     [!code-csharp[VbExpressTutorial3Step4#8](../snippets/csharp/VS_Snippets_VBCSharp/vbexpresstutorial3step4/cs/form1.cs#8)]
     [!code-vb[VbExpressTutorial3Step4#8](../snippets/visualbasic/VS_Snippets_VBCSharp/vbexpresstutorial3step4/vb/form1.vb#8)]  
  
     Ardından, yeni çağırmak Zamanlayıcının Tick olay işleyicisinin yöntemini kodu güncelleştirerek yanıtı kontrol edeceğiz `CheckTheAnswer()` yöntemi.  
  
2.  Aşağıdaki kodu ekleyin `if else` deyimi.  
  
     [!code-csharp[VbExpressTutorial3Step4#10](../snippets/csharp/VS_Snippets_VBCSharp/vbexpresstutorial3step4/cs/form1.cs#10)]
     [!code-vb[VbExpressTutorial3Step4#10](../snippets/visualbasic/VS_Snippets_VBCSharp/vbexpresstutorial3step4/vb/form1.vb#10)]  
  
     Yanıt doğru ise, `CheckTheAnswer()` döndürür `true`. Olay işleyicisi Zamanlayıcıyı durdurur, bir kutlama iletisini gösterir ve sonra yapar **Başlat** düğmesini tekrar kullanılabilir. Aksi halde sınav devam eder.  
  
3.  Programınızı kaydedin, çalıştırın, bir sınav başlatın ve ek soruya doğru yanıtı sağlayın.  
  
    > [!NOTE]
    >  Yanıtınızı girerken, varsayılan değeri Seçmeli başlangıç veya sıfırı el ile silmelisiniz önce ya da seçmeniz gerekir. Bu öğreticinin ilerleyen bölümlerinde bu davranışı düzelteceksiniz.  
  
     Doğru yanıtı verdiğinizde bir ileti kutusu açılır, **Başlat** düğmesi kullanılabilir olur ve Zamanlayıcı durur.  
  
### <a name="to-continue-or-review"></a>Devam etmek veya gözden geçirmek için  
  
-   Sonraki öğretici adımına gitmek için bkz: [5. adım: Ekleme NumericUpDown denetimleri için giriş olay işleyicileri girin](../ide/step-5-add-enter-event-handlers-for-the-numericupdown-controls.md).  
  
-   Önceki öğretici adımına dönmek için bkz: [3. adım: Bir geri sayım Zamanlayıcısı ekleme](../ide/step-3-add-a-countdown-timer.md).
