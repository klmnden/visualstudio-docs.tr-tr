---
title: Fse deyimi
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
ms.openlocfilehash: a6dd0a3ebdb41243734850cea4f4b43604ebb94b
ms.sourcegitcommit: 11337745c1aaef450fd33e150664656d45fe5bc5
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2019
ms.locfileid: "57325278"
---
# <a name="invert-if-statement"></a>Fse deyimi

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

    ![Fse başka kod düzeltmesi](media/invert-if-codefix.png)

3. Seçin **fse**.

    ![Fse başka sonucu](media/invert-if-codefix-result.png)

## <a name="see-also"></a>Ayrıca bkz.

- [Yeniden Düzenleme](../refactoring-in-visual-studio.md)
- [.NET Geliştiricileri için İpuçları](../../ide/visual-studio-2017-for-dotnet-developers.md)
