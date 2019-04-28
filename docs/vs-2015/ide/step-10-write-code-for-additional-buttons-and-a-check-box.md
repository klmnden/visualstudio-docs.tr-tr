---
title: '10. Adım: Ek düğmeler ve onay kutusu için kod yazma | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: conceptual
ms.assetid: 185cf370-ab39-4ac0-b6bc-601d5b95a4a2
caps.latest.revision: 23
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 87c441271e72ef2aa67e0908e19473279f26ec53
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63441944"
---
# <a name="step-10-write-code-for-additional-buttons-and-a-check-box"></a>10. Adım: Ek Düğmeler ve Onay Kutusu için Kod Yazma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Diğer dört yöntemi tamamlamaya artık hazırsınız. Bu kodu kopyalayıp, ancak bilgi almak istiyorsanız bu öğreticiden en iyi kodu yazıp IntelliSense kullanın.  
  
 Bu kod, daha önce eklediğiniz düğmelere işlevsellik ekler. Bu kod olmadan düğmeler hiçbir şey yapmaz. Kodda düğmelerini kendi `Click` olayları (ve onay kutusu kullandığı `CheckChanged` olay) denetimleri etkinleştirdiğinizde değişik şeyler yapmak için. Örneğin, `clearButton_Click` seçtiğinizde olayı, **resmi Temizle** düğmesi, ayarlayarak geçerli görüntüyü siler, `Image` özelliğini `null` (veya `nothing`). Her olay, kodun ne yaptığını açıklayan yorumlar içerir.  
  
 ![video bağlantısı](../data-tools/media/playvideo.gif "PlayVideo")bu konunun video sürümü için bkz: [öğretici 1: Visual Basic'te - Video 5 resim görüntüleyici oluşturma](http://go.microsoft.com/fwlink/?LinkId=205216) veya [öğretici 1: İçinde resim görüntüleyici oluşturma C# -Video 5](http://go.microsoft.com/fwlink/?LinkId=205206). Bazı menü komutlarında ve diğer kullanıcı arabirimi öğelerinde küçük farklılıklar olduğundan bu videolarda Visual Studio'nun önceki bir sürümü kullanın. Ancak, kavramlar ve yordamlar benzer şekilde Visual Studio'nun geçerli sürümünde çalışır.  
  
> [!NOTE]
> En iyi uygulama olarak: Her zaman kodunuza yorum yapın. Yorumlar bir kişinin okuması için için bilgilerdir ve kodunuzu anlaşılır hale getirmek için zaman ayırmanız iyidir. Bir yorum satırındaki her şey program tarafından göz ardı edilir. Visual C# içinde bir satır başına iki eğik yazarak yorum (/ /), ve Visual Basic'te, bir satır tek tırnak işaretiyle (') başlatarak yorum yazabilirsiniz.  
  
### <a name="to-write-code-for-additional-buttons-and-a-check-box"></a>Ek düğmeler ve onay kutusu için kod yazma  
  
- Form1 kod dosyanıza (Form1.cs veya Form1.vb) aşağıdaki kodu ekleyin. Seçin **VB** Visual Basic kodunu görüntülemek için sekmesinde.  
  
     [!code-csharp[VbExpressTutorial1Step9_10#2](../snippets/csharp/VS_Snippets_VBCSharp/vbexpresstutorial1step9_10/cs/form1.cs#2)]
     [!code-vb[VbExpressTutorial1Step9_10#2](../snippets/visualbasic/VS_Snippets_VBCSharp/vbexpresstutorial1step9_10/vb/form1.vb#2)]  
  
### <a name="to-continue-or-review"></a>Devam etmek veya gözden geçirmek için  
  
- Sonraki öğretici adımına gitmek için bkz: [11. adım: Programınızı çalıştırmak ve diğer özellikleri deneme](../ide/step-11-run-your-program-and-try-other-features.md).  
  
- Önceki öğretici adımına dönmek için bkz: [9. adım: Gözden geçirme, açıklama ve kodunuzu Test](../ide/step-9-review-comment-and-test-your-code.md).
