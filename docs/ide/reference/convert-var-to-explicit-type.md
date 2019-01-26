---
title: Var açık bir tür değiştirmek için kodu yeniden düzenleyin
ms.date: 05/15/2018
ms.prod: visual-studio-dev15
ms.topic: reference
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
ms.workload:
- dotnet
ms.openlocfilehash: 4434d5187809a4517161f1239c3adfea193fcd5c
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54980199"
---
# <a name="refactoring-to-replace-var-with-an-explicit-type"></a>Var açık bir tür değiştirmek için yeniden düzenleme

Değiştirmek için bu yeniden düzenleme kullanın [var](/dotnet/csharp/language-reference/keywords/var) açık bir türü olan bir yerel değişken bildiriminde.

Bu yeniden düzenleme için geçerlidir:

- C#

## <a name="why-to-use-an-explicit-type"></a>Neden bir açık tür kullan

Açık bir tür ile bir değişken bildirmek için bazı nedenler şunlardır:

- Kodun okunabilirliğini geliştirmek için.

- Ne zaman bildirimde değişkeni başlatmak istemediğiniz.

Ancak, [var](/dotnet/csharp/language-reference/keywords/var) içeren bir anonim tür bir değişken başlatılır ve sonraki bir noktada nesnenin özelliklerini erişilen kullanılmalıdır. Daha fazla bilgi için [örtülü olarak yazılan yerel değişkenler (C#)](/dotnet/csharp/programming-guide/classes-and-structs/implicitly-typed-local-variables).

## <a name="how-to-use-it"></a>Kullanımı

1. Giriş işaretini yerleştir `var` anahtar sözcüğü.

1. Tuşuna **Ctrl**+**.** veya tornavida ![tornavida simgesi](../media/screwdriver-icon.png) kod dosyasının boşluğundaki simgeye.

   ![Hızlı Eylemler menüsü açık tür kullanma](media/use-explicit-type.png)

1. Seçin **açık tür kullan**. Ya da seçin **değişiklik önizlemesi** açmak için [Değişiklikleri Önizle](../../ide/preview-changes.md) iletişim tıklayın ve ardından **Uygula**.

## <a name="see-also"></a>Ayrıca bkz.

- [Örtülü türdeki değişkenler (C#)](/dotnet/csharp/programming-guide/classes-and-structs/implicitly-typed-local-variables)
- [Yeniden Düzenleme](../refactoring-in-visual-studio.md)
- [Değişiklikleri Önizleme](../../ide/preview-changes.md)