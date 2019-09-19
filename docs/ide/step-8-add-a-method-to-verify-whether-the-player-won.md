---
title: '8\. Adım: Oyuncunun kazanıp kazanmadığını doğrulamak için yöntem ekleme'
ms.date: 11/04/2016
ms.topic: tutorial
ms.prod: visual-studio-windows
ms.technology: vs-ide-general
dev_langs:
- CSharp
- VB
ms.assetid: 6e317f6e-ba4c-4306-8924-300b0c2f65c6
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: b58cb236f1da88c20e0e96878a7cd5c60052f44f
ms.sourcegitcommit: 6eed0372976c0167b9a6d42ba443f9a474b8bb91
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/19/2019
ms.locfileid: "71118633"
---
# <a name="step-8-add-a-method-to-verify-whether-the-player-won"></a>8\. Adım: Oyuncunun kazanıp kazanmadığını doğrulamak için yöntem ekleme
Eğlenceli bir oyun oluşturdunuz, ancak bitirmek için bir şeye daha ihtiyaç var. Oyuncu, oynatıcı WINS 'e göre sona erdirmek için oyuncunun kazanıp kazanılmadığını doğrulamak `CheckForWinner()` üzere bir yöntem eklemeniz gerekir.

## <a name="to-add-a-method-to-verify-whether-the-player-won"></a>Oyuncunun kazanıp kazanmadığını doğrulamak üzere bir yöntem eklemek için

1. Aşağıdaki kodda `CheckForWinner()` gösterildiği gibi, kodunuzun altına, `timer1_Tick()` olay işleyicisinin altına bir yöntem ekleyin.

     [!code-csharp[VbExpressTutorial4Step8#10](../ide/codesnippet/CSharp/step-8-add-a-method-to-verify-whether-the-player-won_1.cs)]
     [!code-vb[VbExpressTutorial4Step8#10](../ide/codesnippet/VisualBasic/step-8-add-a-method-to-verify-whether-the-player-won_1.vb)]

     `foreach` Yöntemi, C# `For Each` içindeki herbiretikettegezinmekiçingörselveyaVisualBasicdöngüsündebaşkabirdöngükullanır.<xref:System.Windows.Forms.TableLayoutPanel> Her etiketin simge rengini denetlemek için`==` , arka C# planla `=` eşleşip eşleşmediğini doğrulamak üzere eşitlik işlecini (görselde ve Visual Basic) kullanır. Renkler eşleşiyorsa simge görünmez halde kalır ve oyuncu kalan simgelerin tümünü eşleştirmemiştir. Bu durumda program, yöntemin geri kalanını atlamak `return` için bir ifade kullanır. Döngü, `return` ifadeyi yürütmeden tüm etiketleri alırsa, bu, formdaki tüm simgelerin eşleştirildiği anlamına gelir. Program, oyunu kazanmakta olan bir MessageBox gösterir ve ardından oyunun sona erdirmek için formun `Close()` yöntemini çağırır.

2. Sonra, etiketin <xref:System.Windows.Forms.Control.Click> olay işleyicisinin yeni `CheckForWinner()` yöntemi çağırmasını sağlayabilirsiniz. Oyuncunun seçtiği ikinci simgeyi gösterdikten hemen sonra programınızın bir kazanan olup olmadığını denetlediğinden emin olun. İkinci seçili simgenin rengini ayarladığınız çizgiyi bulun ve ardından aşağıdaki kodda gösterildiği gibi `CheckForWinner()` yöntemi hemen sonra çağırın.

     [!code-csharp[VbExpressTutorial4Step8#11](../ide/codesnippet/CSharp/step-8-add-a-method-to-verify-whether-the-player-won_2.cs)]
     [!code-vb[VbExpressTutorial4Step8#11](../ide/codesnippet/VisualBasic/step-8-add-a-method-to-verify-whether-the-player-won_2.vb)]

3. Programı kaydedip çalıştırın. Oyunu oynayın ve tüm simgeleri eşleştirin. Kazandığınızda, program bir kutlama **MessageBox** (aşağıdaki resimde gösterildiği gibi) görüntüler ve kutuyu kapatır.

     ![](../ide/media/express_tut4step8.png)
 **MessageBox** **ile eşleşen bir oyun ile** eşleşen oyun

## <a name="to-continue-or-review"></a>Devam etmek veya gözden geçirmek için

- Sonraki öğretici adımına gitmek için bkz [. Adım 9: Diğer özellikleri](../ide/step-9-try-other-features.md)deneyin.

- Önceki öğretici adımına dönmek için bkz [. 7. Adım: Çiftleri görünür](../ide/step-7-keep-pairs-visible.md)tutun.
