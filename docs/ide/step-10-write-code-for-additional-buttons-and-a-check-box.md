---
title: '10. Adım: Ek düğmeler ve onay kutusu için kod yazma'
ms.date: 08/30/2019
ms.assetid: 185cf370-ab39-4ac0-b6bc-601d5b95a4a2
ms.topic: tutorial
ms.prod: visual-studio-windows
ms.technology: vs-ide-general
ms.devlang:
- csharp
- vb
dev_langs:
- CSharp
- VB
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 2d2e77b3bfd62bf1dfdf15ff083b07459bd3bf77
ms.sourcegitcommit: 2db01751deeee7b2bdb1db25419ea6706e6fcdf8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/17/2019
ms.locfileid: "71062666"
---
# <a name="step-10-write-code-for-additional-buttons-and-a-check-box"></a>10. Adım: Ek düğmeler ve onay kutusu için kod yazma

Artık diğer dört yöntemi tamamlamaya hazırsınız. Bu kodu kopyalayabilir ve yapıştırabilirsiniz, ancak bu öğreticiden en iyi şekilde bilgi edinmek istiyorsanız kodu yazın ve IntelliSense kullanın.

Bu kod, daha önce eklediğiniz düğmelere işlevsellik ekler. Bu kod olmadan düğmeler hiçbir şey yapmaz. Düğmeler, denetimleri etkinleştirdiğinizde farklı şeyler <xref:System.Windows.Forms.Control.Click> yapmak için olaylarında kod kullanır (ve onay <xref:System.Windows.Forms.CheckBox.CheckedChanged> kutusu olayı kullanır). Örneğin, `clearButton_Click` **Resmi Temizle** düğmesini seçtiğinizde `ClearButton_Click`etkinleştiren (veya) olay, **Image** özelliğini **null** (veya **Nothing**) olarak ayarlayarak geçerli görüntüyü siler. Koddaki her olay kodun ne yaptığını açıklayan yorumlar içerir.

> [!TIP]
> En iyi uygulama olarak: Kodunuzda her zaman yorum yapın. Yorumlar, bir kişinin okuması ve kodunuzun daha anlaşılır olması için gereken zamana değecektir. Açıklama satırındaki her şey uygulama tarafından yok sayılır. İçinde C#, başlangıca iki eğik çizgi (//) yazarak bir satır yorum yapın ve Visual Basic tek tırnak işaretiyle (') başlayarak bir satırı açıklama olarak görürsünüz.

## <a name="how-to-write-code-for-additional-buttons-and-a-check-box"></a>Ek düğmeler ve onay kutusu için kod yazma

Aşağıdaki kodu **Form1** kod dosyanıza ekleyin (*Form1.cs* veya *Form1. vb*).
> [!IMPORTANT]
> C# Kod parçacığını veya Visual Basic kod parçacığını görüntülemek için bu sayfanın sağ üst kısmındaki programlama dili denetimini kullanın.<br><br>![Docs.Microsoft.com için programlama dili denetimi](../ide/media/docs-programming-language-control.png)

  [!code-csharp[VbExpressTutorial1Step9_10#2](../ide/codesnippet/CSharp/step-10-write-code-for-additional-buttons-and-a-check-box_1.cs)]

  [!code-vb[VbExpressTutorial1Step9_10#2](../ide/codesnippet/VisualBasic/step-10-write-code-for-additional-buttons-and-a-check-box_1.vb)]

> [!NOTE]
> Kodunuz "camelCase" harflerini görüntülenmeyebilir.

## <a name="next-steps"></a>Sonraki adımlar

* Sonraki öğretici adımına gitmek için bkz  **[. adım 11: Uygulamanızı çalıştırın ve diğer özellikleri](../ide/step-11-run-your-program-and-try-other-features.md)** deneyin.

* Önceki öğretici adımına dönmek için bkz [. Adım 9: Kodunuzu](../ide/step-9-review-comment-and-test-your-code.md)gözden geçirin, yorum yapın ve test edin.

## <a name="see-also"></a>Ayrıca bkz.

* [Öğretici 2: Süreli matematik testi oluşturma](tutorial-2-create-a-timed-math-quiz.md)
* [Öğretici 3: Eşleşen bir oyun oluşturun](tutorial-3-create-a-matching-game.md)
