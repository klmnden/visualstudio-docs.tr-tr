---
title: Koşullu ifadeleri ve mantıksal işlemleri tersine çevirme
ms.date: 02/19/2019
ms.topic: reference
author: kendrahavens
ms.author: kendrahavens
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- dotnet
ms.openlocfilehash: a35f5949bee6cb3c4fbcbf9ba6a9b501d54b2014
ms.sourcegitcommit: 11337745c1aaef450fd33e150664656d45fe5bc5
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2019
ms.locfileid: "57325257"
---
# <a name="invert-conditional-expressions-and-conditional-andor-operators"></a>Koşullu ifadeleri ve koşullu ters çevir ve/veya işleçler

Bu yeniden düzenleme için geçerlidir:

- C#
- Visual Basic

**Ne:** Bir koşullu ifade veya koşullu ters olanak tanır ve/veya işleci.

**ne zaman:** Bir koşullu ifade veya koşullu ve/veya ters işleci, daha iyi anlaşılması.

**Neden:** Bir ifade veya koşullu ters çevirme ve/veya el ile operatör daha uzun sürer ve büyük olasılıkla hatalara. Bu kod düzeltmesi bu otomatik olarak yeniden düzenleme yapmanıza yardımcı olur.

## <a name="invert-conditional-expressions-and-conditional-andor-operators-refactoring"></a>Koşullu ifadeleri ve koşullu ters çevir ve/veya çıkarma işleçleri

1. Bir koşullu ifade veya koşullu imleci yerleştirin ve/veya işleci.
2. Tuşuna **Ctrl**+**.** Tetikleyici için **hızlı Eylemler ve yeniden düzenlemeler** menüsü.
3. Seçin **renkleri ters çevirme koşullu** veya **Değiştir ' & &' ile ' ||'**

    ![Koşullu ters çevir](media/invert-conditional.png)

    ![Koşullu ters çevir](media/invert-logical-operator.png)

## <a name="see-also"></a>Ayrıca bkz.

- [Yeniden Düzenleme](../refactoring-in-visual-studio.md)
- [.NET Geliştiricileri için İpuçları](../../ide/visual-studio-2017-for-dotnet-developers.md)
