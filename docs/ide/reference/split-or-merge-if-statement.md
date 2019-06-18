---
title: Birleştir veya ayır if deyimleri
ms.date: 06/12/2019
ms.topic: reference
author: mikadumont
ms.author: midumont
manager: jillfra
dev_langs:
- CSharp
ms.workload:
- dotnet
ms.openlocfilehash: 405ccd4bc0197ce06aa14982a16dc02f6d13a537
ms.sourcegitcommit: d4920babfc3d24a3fe1d4bf446ed3fe73b344467
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/17/2019
ms.locfileid: "67160722"
---
# <a name="split-or-merge-if-statements"></a>Birleştir veya ayır if deyimleri

Bu yeniden düzenleme için geçerlidir:

- C#

**Ne:** **Ne:** Bölme ve birleştirme [varsa](/dotnet/csharp/language-reference/keywords/if-else) deyimleri.

**ne zaman:** Bölmek istediğiniz bir `if` kullanan deyimi `&&` veya `||` işleçleri iç içe bir `if` deyimi veya birleştirme bir `if` deyimi bir dış `if` deyimi.

**Neden:** Stil tercih bir konudur.  

## <a name="how-to"></a>Nasıl Yapılır Konuları

Bölmek istiyorsanız `if` deyimi:

1. İmlecinizi, `if` deyimi tarafından `&&` veya `||` işleci.

2. Tuşuna **Ctrl**+ **.** Tetikleyici için **hızlı Eylemler ve yeniden düzenlemeler** menüsü.

    ![Bölünmüş If deyimi](../media/split-if-statement.png)

3. Seçin **iç içe geçmiş if bölme deyimleri**.

    ![Bölünmüş If deyimi tamamlandı](../media/split-if-statement-complete.png)

İç birleştirmek istiyorsanız `if` dış deyimiyle `if` deyimi: 

1. İmlecinizi iç `if` anahtar sözcüğü.

2. Tuşuna **Ctrl**+ **.** Tetikleyici için **hızlı Eylemler ve yeniden düzenlemeler** menüsü.

    ![Merge deyimi](../media/merge-if-statement.png)

3. Seçin **birleştirme ile dış if deyimi**.

    ![Varsa birleştirme tamamlandı deyimi](../media/merge-if-statement-complete.png)

## <a name="see-also"></a>Ayrıca bkz.

- [Yeniden Düzenleme](../refactoring-in-visual-studio.md)