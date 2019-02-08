---
title: '10. Adım: Ek düğmeler ve onay kutusu için kod yazma'
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 185cf370-ab39-4ac0-b6bc-601d5b95a4a2
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 19c82238a0379e6b94e82bb1e34f20282ff4654f
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55930174"
---
# <a name="step-10-write-code-for-additional-buttons-and-a-check-box"></a>10. Adım: Ek düğmeler ve onay kutusu için kod yazma
Diğer dört yöntemi tamamlamaya artık hazırsınız. Bu kodu kopyalayıp, ancak bilgi almak istiyorsanız bu öğreticiden en iyi kodu yazıp IntelliSense kullanın.

 Bu kod, daha önce eklediğiniz düğmelere işlevsellik ekler. Bu kod olmadan düğmeler hiçbir şey yapmaz. Kodda düğmelerini kendi <xref:System.Windows.Forms.Control.Click> olayları (ve onay kutusu kullandığı <xref:System.Windows.Forms.CheckBox.CheckedChanged> olay) denetimleri etkinleştirdiğinizde değişik şeyler yapmak için. Örneğin, `clearButton_Click` seçtiğinizde olayı, **resmi Temizle** düğmesi, ayarlayarak geçerli görüntüyü siler, **görüntü** özelliğini **null**(veya **hiçbir şey**). Her olay, kodun ne yaptığını açıklayan yorumlar içerir.

 ![video bağlantısı](../data-tools/media/playvideo.gif)bu konunun video sürümü için bkz: [öğretici 1: Visual Basic'te - Video 5 resim görüntüleyici oluşturma](http://go.microsoft.com/fwlink/?LinkId=205216) veya [öğretici 1: İçinde resim görüntüleyici oluşturma C# -Video 5](http://go.microsoft.com/fwlink/?LinkId=205206). Bazı menü komutlarında ve diğer kullanıcı arabirimi öğelerinde küçük farklılıklar olduğundan bu videolarda Visual Studio'nun önceki bir sürümü kullanın. Ancak, kavramlar ve yordamlar benzer şekilde Visual Studio'nun geçerli sürümünde çalışır.

> [!NOTE]
>  En iyi uygulama olarak: Her zaman kodunuza yorum yapın. Yorumlar bir kişinin okuması için için bilgilerdir ve kodunuzu anlaşılır hale getirmek için zaman ayırmanız iyidir. Bir yorum satırındaki her şey program tarafından göz ardı edilir. Visual C# içinde bir satır başına iki eğik yazarak yorum (/ /), ve Visual Basic'te, bir satır tek tırnak işaretiyle (') başlatarak yorum yazabilirsiniz.

## <a name="to-write-code-for-additional-buttons-and-a-check-box"></a>Ek düğmeler ve onay kutusu için kod yazma

-   Aşağıdaki kodu ekleyin, **Form1** kod dosyası (*Form1.cs* veya *Form1.vb*). Seçin **VB** Visual Basic kodunu görüntülemek için sekmesinde.

     [!code-vb[VbExpressTutorial1Step9_10#2](../ide/codesnippet/VisualBasic/step-10-write-code-for-additional-buttons-and-a-check-box_1.vb)]
     [!code-csharp[VbExpressTutorial1Step9_10#2](../ide/codesnippet/CSharp/step-10-write-code-for-additional-buttons-and-a-check-box_1.cs)]

## <a name="to-continue-or-review"></a>Devam etmek veya gözden geçirmek için

-   Sonraki öğretici adımına gitmek için bkz: [11. adım: Programınızı çalıştırmak ve diğer özellikleri deneme](../ide/step-11-run-your-program-and-try-other-features.md).

-   Önceki öğretici adımına dönmek için bkz: [9. adım: Gözden geçirme, açıklama ve kodunuzu test](../ide/step-9-review-comment-and-test-your-code.md).
