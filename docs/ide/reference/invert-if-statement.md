---
title: if deyimini tersine çevirme
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
ms.openlocfilehash: 5a809eee1eb5460e245f64156385f759870adbd3
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58159107"
---
# <a name="invert-if-statement"></a>if deyimini tersine çevirme

Bu yeniden düzenleme için geçerlidir:

- C#
- Visual Basic

**Ne:** Ters sayesinde bir `if` veya `if else` kodun anlamı değiştirmeden deyimi.

**ne zaman:** Olduğunda bir `if` veya `if else` ters olduğunda daha iyi olacağını görecektir deyimi anladım.

**Neden:** Ters çevirme bir `if` veya `if else` deyimi el ile daha uzun sürer ve büyük olasılıkla hatalara. Bu kod düzeltmesi bu otomatik olarak yeniden düzenleme yapmanıza yardımcı olur.

## <a name="invert-if-statement-refactoring"></a>Fse deyimi yeniden düzenleme

1. İmlecinizi, bir `if` veya `if else` deyimi.

    ![Fse else](media/invert-if.png)

2. Tuşuna **Ctrl**+**.** Tetikleyici için **hızlı Eylemler ve yeniden düzenlemeler** menüsü.

    ![Başka bir kod düzeltmesi fse](media/invert-if-codefix.png)

3. Seçin **fse**.

    ![Fse başka sonucu](media/invert-if-codefix-result.png)

## <a name="see-also"></a>Ayrıca bkz.

- [Yeniden Düzenleme](../refactoring-in-visual-studio.md)
- [.NET Geliştiricileri için İpuçları](../../ide/visual-studio-2017-for-dotnet-developers.md)
