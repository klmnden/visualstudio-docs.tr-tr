---
title: Switch deyimi'switch ifadesiyle için Dönüştür
ms.date: 06/19/2019
ms.topic: reference
author: mikadumont
ms.author: midumont
manager: jillfra
dev_langs:
- CSharp
ms.workload:
- dotnet
ms.openlocfilehash: ecb7750301101a2607c17e68b5e919623a03caba
ms.sourcegitcommit: 7eb2fb21805d92f085126f3a820ac274f2216b4e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/22/2019
ms.locfileid: "67329104"
---
# <a name="convert-switch-statement-to-switch-expression"></a>Switch deyimi'switch ifadesiyle için Dönüştür

Bu yeniden düzenleme için geçerlidir:

- C#

**Ne:** Dönüştürme bir [geçiş deyimi](/dotnet/csharp/language-reference/keywords/switch) için bir C# 8.0 [geçiş ifadesi](/dotnet/csharp/whats-new/csharp-8#switch-expressions).

**ne zaman:** Dönüştürmek istediğiniz bir `switch` deyimi bir `switch` ifade geçme veya tam tersi. 

**Neden:** İfadeleri yalnızca kullanıyorsanız, geleneksel bir kolayca durumundan bu yeniden düzenleme sağlar `switch` deyimleri.

## <a name="how-to"></a>Nasıl Yapılır Konuları

1. Proje dosyanızda [önizlemek için dil sürümünü ayarlama](/dotnet/csharp/language-reference/configure-language-version#set-the-language-version-in-visual-studio) beri `switch` ifadelerdir yeni C# 8.0 özelliği.
2. İmlecinizi, `switch` anahtar sözcüğü ve ENTER tuşuna **Ctrl**+ **.** Tetikleyici için **hızlı Eylemler ve yeniden düzenlemeler** menüsü.
3. Seçin **dönüştürme switch ifadesi ifade**.

   ![Switch deyimi'switch ifadesiyle için Dönüştür](media/convert-switch-statement-to-switch-expression.png) 

## <a name="see-also"></a>Ayrıca bkz.

- [Yeniden Düzenleme](../refactoring-in-visual-studio.md)
