---
title: '4\. Adım: CheckTheAnswer() yöntemi ekleme'
ms.date: 11/04/2016
ms.topic: tutorial
ms.prod: visual-studio-windows
ms.technology: vs-ide-general
ms.devlang:
- csharp
- vb
dev_langs:
- CSharp
- VB
ms.assetid: c66f3831-b4a0-40bc-a109-8f46f4db35ed
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 4c940893f74697bdbf51c5910e08e925fedf26db
ms.sourcegitcommit: 541a0556958201ad6626bc8638406ad02640f764
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/18/2019
ms.locfileid: "71079412"
---
# <a name="step-4-add-the-checktheanswer-method"></a>4\. Adım: CheckTheAnswer() yöntemi ekleme

Bu öğreticinin dördüncü bölümünde, matematik sorunlarına verilen yanıtların doğru olup olmadığını belirleyen `CheckTheAnswer()`bir yöntemi yazacaksınız. Bu konu, temel kodlama kavramlarıyla ilgili bir öğretici serisinin bir parçasıdır. Öğreticiye genel bakış için bkz [. öğretici 2: Süreli bir matematik testi](../ide/tutorial-2-create-a-timed-math-quiz.md)oluşturun.

> [!NOTE]
> Bu konu, temel kodlama kavramlarıyla ilgili bir öğretici serisinin bir parçasıdır.
> - Öğreticiye genel bakış için bkz [. öğretici 2: Süreli bir matematik testi](../ide/tutorial-2-create-a-timed-math-quiz.md)oluşturun.
> - Kodun tamamlanmış bir sürümünü indirmek için bkz. [tüm matematik testi öğreticisi örneği](https://code.msdn.microsoft.com/Complete-Math-Quiz-8581813c).

## <a name="to-verify-whether-the-answers-are-correct"></a>Yanıtların doğru olup olmadığını doğrulamak için

> [!NOTE]
> Visual Basic ' de takip ediyorsanız, bu yöntem bir değer döndürdüğünden, `Function` her zamanki `Sub` anahtar sözcüğü yerine anahtar sözcüğünü kullanırsınız. Oldukça basittir: Sub bir değer döndürmez, ancak bir işlev yapar.

1. `CheckTheAnswer()` Yöntemini ekleyin.

     Bu yöntem çağrıldığında, addend1 ve addend2 değerlerini ekler ve sonucu, Sum <xref:System.Windows.Forms.NumericUpDown> denetimindeki değer ile karşılaştırır. Değerler eşitse, yöntemi bir değeri `true`döndürür. Aksi takdirde, yöntemi bir değeri `false`döndürür. Kodunuzun aşağıdaki gibi görünmesi gerekir.

     [!code-vb[VbExpressTutorial3Step4#8](../ide/codesnippet/VisualBasic/step-4-add-the-checktheanswer-parens-method_1.vb)]
     [!code-csharp[VbExpressTutorial3Step4#8](../ide/codesnippet/CSharp/step-4-add-the-checktheanswer-parens-method_1.cs)]

     > [!IMPORTANT]
     > C# Kod parçacığını veya Visual Basic kod parçacığını görüntülemek için bu sayfanın sağ üst kısmındaki programlama dili denetimini kullanın.<br><br>![Docs.Microsoft.com için programlama dili denetimi](../ide/media/docs-programming-language-control.png)

     Daha sonra, yeni <xref:System.Windows.Forms.Timer.Tick> `CheckTheAnswer()` yöntemi çağırmak için zamanlayıcının olay işleyicisine yönelik yöntemdeki kodu güncelleştirerek yanıtı kontrol edersiniz.

2. Aşağıdaki kodu `if else` ifadeye ekleyin.

     [!code-vb[VbExpressTutorial3Step4#10](../ide/codesnippet/VisualBasic/step-4-add-the-checktheanswer-parens-method_2.vb)]
     [!code-csharp[VbExpressTutorial3Step4#10](../ide/codesnippet/CSharp/step-4-add-the-checktheanswer-parens-method_2.cs)]

     Yanıt doğruysa, `CheckTheAnswer()` döndürür `true`. Olay işleyicisi zamanlayıcıyı durduruyor, kutlama iletisini gösterir ve sonra **Başlat** düğmesini tekrar kullanılabilir yapar. Aksi takdirde, test devam eder.

3. Programınızı kaydedin, çalıştırın, bir test başlatın ve ek sorun için doğru bir yanıt sağlayın.

    > [!NOTE]
    > Yanıtınızı girerken, yanıtınızı girmeden önce varsayılan değeri seçmeniz ya da sıfırı el ile silmeniz gerekir. Bu davranışı daha sonra bu öğreticide düzelteceksiniz.

     Doğru bir yanıt sağladığınızda, bir ileti kutusu açılır, **Başlat** düğmesi kullanılabilir hale gelir ve Zamanlayıcı durduruluyor.

## <a name="to-continue-or-review"></a>Devam etmek veya gözden geçirmek için

- Sonraki öğretici adımına gitmek için bkz  **[. 5. Adım: NumericUpDown denetimleri](../ide/step-5-add-enter-event-handlers-for-the-numericupdown-controls.md)** için Enter Olay işleyicileri ekleyin.

- Önceki öğretici adımına dönmek için bkz [. Adım 3: Geri sayım Zamanlayıcısı](../ide/step-3-add-a-countdown-timer.md)ekleyin.
