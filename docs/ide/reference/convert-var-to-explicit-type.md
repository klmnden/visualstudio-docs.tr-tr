---
title: Var açık bir tür değiştirmek için kodu yeniden düzenleyin
ms.date: 05/15/2018
ms.prod: visual-studio-dev15
ms.topic: reference
author: gewarren
ms.author: gewarren
manager: douge
dev_langs:
- CSharp
ms.workload:
- dotnet
ms.openlocfilehash: 893fc2f989dab579690cdac37edae3ba0fad606a
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53869144"
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