---
title: Switch deyimini switch ifadesine dönüştürme
ms.date: 06/19/2019
ms.topic: reference
author: mikadumont
ms.author: midumont
manager: jillfra
dev_langs:
- CSharp
ms.workload:
- dotnet
ms.openlocfilehash: cc13cffe8352d9fb57f5bb991c3af615eddb2a14
ms.sourcegitcommit: b56dc6fadc6c924beed36bb4c2ccc16cf6bcfa1c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/02/2019
ms.locfileid: "68740051"
---
# <a name="convert-switch-statement-to-switch-expression"></a>Switch deyimini switch ifadesine dönüştürme

Bu yeniden düzenleme için geçerlidir:

- C#

**Yazdırılacak** [Switch deyimini](/dotnet/csharp/language-reference/keywords/switch) C# 8,0 [anahtar ifadesine](/dotnet/csharp/whats-new/csharp-8#switch-expressions)Dönüştür.

**Oluşturulurken** Bir `switch` deyimi`switch` ifadeye dönüştürmek istiyorsunuz, tersi de geçerlidir. 

**Kaydol** Yalnızca ifadeler kullanıyorsanız, bu yeniden düzenleme geleneksel `switch` deyimlerden kolay bir geçişe izin vermez.

## <a name="how-to"></a>Nasıl Yapılır Konuları

1. Proje dosyanızda, `switch` ifadeler yeni C# bir 8,0 özelliği olduğundan [dil sürümünü önizleme olarak ayarlayın](/dotnet/csharp/language-reference/configure-language-version#edit-the-project-file) .
2. İmlecinizi `switch` anahtar sözcüğe yerleştirip **CTRL**+tuşuna basın **.** Tetikleyici için **hızlı Eylemler ve yeniden düzenlemeler** menüsü.
3. **Switch deyimini Ifadeye Dönüştür**' ü seçin.

   ![Switch deyimini switch ifadesine dönüştürme](media/convert-switch-statement-to-switch-expression.png) 

## <a name="see-also"></a>Ayrıca bkz.

- [Yeniden Düzenleme](../refactoring-in-visual-studio.md)
