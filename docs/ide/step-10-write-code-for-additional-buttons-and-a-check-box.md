---
title: '10. Adım: Ek düğmeler ve onay kutusu için kod yazma'
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- csharp
- vb
ms.assetid: 185cf370-ab39-4ac0-b6bc-601d5b95a4a2
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 5db017ac20c84b8d06832a9b40f98c6519842361
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68918871"
---
# <a name="step-10-write-code-for-additional-buttons-and-a-check-box"></a>10. Adım: Ek düğmeler ve onay kutusu için kod yazma
Artık diğer dört yöntemi tamamlamaya hazırsınız. Bu kodu kopyalayabilir ve yapıştırabilirsiniz, ancak bu öğreticiden en iyi şekilde bilgi edinmek istiyorsanız kodu yazın ve IntelliSense kullanın.

Bu kod, daha önce eklediğiniz düğmelere işlevsellik ekler. Bu kod olmadan düğmeler hiçbir şey yapmaz. Düğmeler, denetimleri etkinleştirdiğinizde farklı şeyler <xref:System.Windows.Forms.Control.Click> yapmak için olaylarında kod kullanır (ve onay <xref:System.Windows.Forms.CheckBox.CheckedChanged> kutusu olayı kullanır). Örneğin `clearButton_Click` , **Resmi Temizle** düğmesini seçtiğinizde etkinleştiren olay, **Image** özelliğini **null** (veya **Nothing**) olarak ayarlayarak geçerli görüntüyü siler. Koddaki her olay kodun ne yaptığını açıklayan yorumlar içerir.

![video](../data-tools/media/playvideo.gif)bağlantısı bu konunun video sürümü için bkz [. öğretici 1: Visual Basic-video 5](http://go.microsoft.com/fwlink/?LinkId=205216) veya [öğretici 1 ' de bir resim Görüntüleyicisi oluşturun: Video 5 C# ](http://go.microsoft.com/fwlink/?LinkId=205206)' te bir resim görüntüleyici oluşturun. Bu videolar, Visual Studio 'nun önceki bir sürümünü kullanır, bu nedenle bazı menü komutlarında ve diğer kullanıcı arabirimi öğelerinde küçük farklılıklar vardır. Ancak, kavramlar ve yordamlar Visual Studio 'nun geçerli sürümünde benzer şekilde çalışır.

> [!NOTE]
> En iyi uygulama olarak: Kodunuzda her zaman yorum yapın. Yorumlar, bir kişinin okuması ve kodunuzun daha anlaşılır olması için gereken zamana değecektir. Yorum satırındaki her şey program tarafından yok sayılır. Görselde C#bir satırı, başlangıca iki eğik çizgi (//) yazarak yorum yapın ve Visual Basic tek tırnak işaretiyle (') başlayarak bir satırı açıklama olarak görürsünüz.

## <a name="to-write-code-for-additional-buttons-and-a-check-box"></a>Ek düğmeler ve onay kutusu için kod yazmak için

- Aşağıdaki kodu **Form1** kod dosyanıza ekleyin (*Form1.cs* veya *Form1. vb*). Visual Basic kodu görüntülemek için **vb** sekmesini seçin.

     [!code-vb[VbExpressTutorial1Step9_10#2](../ide/codesnippet/VisualBasic/step-10-write-code-for-additional-buttons-and-a-check-box_1.vb)]
     [!code-csharp[VbExpressTutorial1Step9_10#2](../ide/codesnippet/CSharp/step-10-write-code-for-additional-buttons-and-a-check-box_1.cs)]

## <a name="to-continue-or-review"></a>Devam etmek veya gözden geçirmek için

- Sonraki öğretici adımına gitmek için bkz [. adım 11: Programınızı çalıştırın ve diğer özellikleri](../ide/step-11-run-your-program-and-try-other-features.md)deneyin.

- Önceki öğretici adımına dönmek için bkz [. Adım 9: Kodunuzu](../ide/step-9-review-comment-and-test-your-code.md)gözden geçirin, yorum yapın ve test edin.
