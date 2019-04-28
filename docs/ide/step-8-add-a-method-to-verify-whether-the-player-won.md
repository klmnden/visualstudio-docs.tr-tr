---
title: '8. Adım: Oyuncunun kazanıp kazanmadığını doğrulamak için yöntem ekleme'
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 6e317f6e-ba4c-4306-8924-300b0c2f65c6
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: e21caa6b73d6cf23a41bd7691fa19b1f7ff8e2f2
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62996552"
---
# <a name="step-8-add-a-method-to-verify-whether-the-player-won"></a>8. Adım: Oyuncunun kazanıp kazanmadığını doğrulamak için yöntem ekleme
Eğlenceli bir oyun oluşturdunuz, ancak bitirmek için bir şeye daha ihtiyaç var. Oyuncu eklemeniz gerekir. Bu nedenle oyun bitmeli; bu bir `CheckForWinner()` oyuncunun kazanıp kazanmadığını doğrulamak için yöntem.

## <a name="to-add-a-method-to-verify-whether-the-player-won"></a>Oyuncunun kazanıp kazanmadığını doğrulamak üzere bir yöntem eklemek için

1. Ekleme bir `CheckForWinner()` kodunuz alt kısmına yöntemi aşağıda `timer1_Tick()` olay işleyicisi, aşağıdaki kodda gösterildiği gibi.

     [!code-csharp[VbExpressTutorial4Step8#10](../ide/codesnippet/CSharp/step-8-add-a-method-to-verify-whether-the-player-won_1.cs)]
     [!code-vb[VbExpressTutorial4Step8#10](../ide/codesnippet/VisualBasic/step-8-add-a-method-to-verify-whether-the-player-won_1.vb)]

     Başka bir yöntem kullanır `foreach` Visual döngüde C# veya `For Each` döngüsü içinde her bir etiketi Git, Visual Basic'te <xref:System.Windows.Forms.TableLayoutPanel>. Eşitlik işlecini kullanır (`==` Visual C# ve `=` Visual Basic'te) arka plan ile eşleşip eşlemediğini doğrulamak için her bir etiketin simge rengini denetlemek için. Renkler eşleşiyorsa simge görünmez halde kalır ve oyuncu kalan simgelerin tümünü eşleştirmemiştir. Bu durumda, programın kullandığı bir `return` deyimi yöntemin geri kalanını atlayın. Döngü tüm etiketleri çalıştırmadan alır, `return` anlamına gelen form üzerindeki simgelerin tümü eşleştirilmiş olan ifade. Program oyuncunun galibiyetini kutlayan bir MessageBox gösterir ve ardından formun çağırır `Close()` da oyunu sonlandırmak için yöntemi.

2. Ardından, etiketin sahip <xref:System.Windows.Forms.Control.Click> olay işleyicisi çağırma yeni `CheckForWinner()` yöntemi. Oyuncunun seçtiği ikinci simgeyi gösterdikten hemen sonra programınızın bir kazanan olup olmadığını denetlediğinden emin olun. Seçilen ikinci simgenin rengini ayarladığınız satırı arayın ve sonra çağrı `CheckForWinner()` aşağıdaki kodda gösterildiği gibi hemen yöntemi.

     [!code-csharp[VbExpressTutorial4Step8#11](../ide/codesnippet/CSharp/step-8-add-a-method-to-verify-whether-the-player-won_2.cs)]
     [!code-vb[VbExpressTutorial4Step8#11](../ide/codesnippet/VisualBasic/step-8-add-a-method-to-verify-whether-the-player-won_2.vb)]

3. Programı kaydedip çalıştırın. Oyunu oynayın ve tüm simgeleri eşleştirin. Kazandığınızda program kutlama amaçlı bir görüntüler **MessageBox** (olarak gösterilen aşağıdaki resimde) ve sonra da kutuyu kapatır.

     ![MessageBox ile eşleştirme oyunu](../ide/media/express_tut4step8.png)
**eşleştirme oyunu** ile **MessageBox**

## <a name="to-continue-or-review"></a>Devam etmek veya gözden geçirmek için

- Sonraki öğretici adımına gitmek için bkz: [9. adım: Diğer özellikleri deneme](../ide/step-9-try-other-features.md).

- Önceki öğretici adımına dönmek için bkz: [adım 7: Çiftleri görünür kılma](../ide/step-7-keep-pairs-visible.md).
