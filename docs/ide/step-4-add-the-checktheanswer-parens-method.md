---
title: '4. Adım: CheckTheAnswer() yöntemi ekleme'
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: c66f3831-b4a0-40bc-a109-8f46f4db35ed
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 0890a153569f8a07c27cb56f4bade7ae89d706ac
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60048014"
---
# <a name="step-4-add-the-checktheanswer-method"></a>4. Adım: CheckTheAnswer() yöntemi ekleme
Bu Eğitimin dördüncü kısmında bir yöntem yazacaksınız `CheckTheAnswer()`, matematik sorularının yanıtlarını doğru olup olmadığını belirler. Bu konu, temel kodlama kavramları hakkındaki bir öğretici serisinin bir parçasıdır. Öğreticiye genel bakış için bkz. [öğretici 2: Zamanlı matematik testi oluşturma](../ide/tutorial-2-create-a-timed-math-quiz.md).

> [!NOTE]
>  Visual Basic'te izliyorsanız, kullanacağınız `Function` anahtar sözcüğü yerine `Sub` anahtar sözcüğü çünkü bu yöntem bir değer döndürür. Bu gerçekten bu kadar kolaydır: bir alt bir değer döndürmez ama bir işlev.

## <a name="to-verify-whether-the-answers-are-correct"></a>Yanıtların doğru olup olmadığını doğrulamak için

1. Ekleme `CheckTheAnswer()` yöntemi.

     Bu yöntem çağrıldığında, addend1 ve addend2 değerleri toplar ve sonucu toplama karşılaştırır <xref:System.Windows.Forms.NumericUpDown> denetimi. Değerler eşitse yöntem değerini döndürür. `true`. Aksi takdirde yöntem bir değeri döndürür `false`. Kodunuzu aşağıdaki gibi görünmelidir.

     [!code-vb[VbExpressTutorial3Step4#8](../ide/codesnippet/VisualBasic/step-4-add-the-checktheanswer-parens-method_1.vb)]
     [!code-csharp[VbExpressTutorial3Step4#8](../ide/codesnippet/CSharp/step-4-add-the-checktheanswer-parens-method_1.cs)]

     Ardından, Zamanlayıcının için yöntemindeki kodu güncelleştirerek yanıtı kontrol edeceğiz <xref:System.Windows.Forms.Timer.Tick> yeni çağrılacak olay işleyicisi `CheckTheAnswer()` yöntemi.

2. Aşağıdaki kodu ekleyin `if else` deyimi.

     [!code-vb[VbExpressTutorial3Step4#10](../ide/codesnippet/VisualBasic/step-4-add-the-checktheanswer-parens-method_2.vb)]
     [!code-csharp[VbExpressTutorial3Step4#10](../ide/codesnippet/CSharp/step-4-add-the-checktheanswer-parens-method_2.cs)]

     Yanıt doğru ise, `CheckTheAnswer()` döndürür `true`. Olay işleyicisi Zamanlayıcıyı durdurur, bir kutlama iletisini gösterir ve sonra yapar **Başlat** düğmesini tekrar kullanılabilir. Aksi halde sınav devam eder.

3. Programınızı kaydedin, çalıştırın, bir sınav başlatın ve ek soruya doğru yanıtı sağlayın.

    > [!NOTE]
    >  Yanıtınızı girerken, varsayılan değeri Seçmeli başlangıç veya sıfırı el ile silmelisiniz önce ya da seçmeniz gerekir. Bu öğreticinin ilerleyen bölümlerinde bu davranışı düzelteceksiniz.

     Doğru yanıtı verdiğinizde bir ileti kutusu açılır, **Başlat** düğmesi kullanılabilir olur ve Zamanlayıcı durur.

## <a name="to-continue-or-review"></a>Devam etmek veya gözden geçirmek için

- Sonraki öğretici adımına gitmek için bkz: [5. adım: NumericUpDown denetimleri için gir olayı işleyicilerini ekleme](../ide/step-5-add-enter-event-handlers-for-the-numericupdown-controls.md).

- Önceki öğretici adımına dönmek için bkz: [3. adım: Bir geri sayım Zamanlayıcısı ekleme](../ide/step-3-add-a-countdown-timer.md).
