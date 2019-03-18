---
title: Koşullu ifadeleri ve mantıksal işlemleri tersine çevirme
ms.date: 02/19/2019
ms.topic: reference
author: kendrahavens
ms.author: kehavens
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- dotnet
ms.openlocfilehash: 7d59b61cff622a9ba305ebfa86f7c0ebe3c00fe3
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58157366"
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
