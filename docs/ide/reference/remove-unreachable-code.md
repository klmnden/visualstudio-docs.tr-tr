---
title: Erişilemeyen kodları yeniden düzenleme Kaldır
ms.date: 01/26/2018
ms.prod: visual-studio-dev15
ms.topic: reference
author: gewarren
ms.author: gewarren
manager: douge
dev_langs:
- CSharp
ms.workload:
- dotnet
ms.openlocfilehash: 481c0d116eb2aee2c4f931f1ca4cb2de7927c62e
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53842544"
---
# <a name="remove-unreachable-code-refactoring"></a>Erişilemeyen kodları yeniden düzenleme Kaldır

Bu yeniden düzenleme için geçerlidir:

- C#

**Ne:** Hiçbir zaman yürütülecek kodu kaldırır.

**ne zaman:** Programınızın Bu kod parçacığı gereksiz yapmadan bir kod parçacığı, hiçbir yolu vardır.

**Neden:** Okunabilirlik ve sürdürülebilirliği gereksiz olan ve hiçbir zaman yürütülecek kodu kaldırarak geliştirin.

## <a name="how-to"></a>Nasıl Yapılır Konuları

1. İmlecinizi, erişilemeyen soluk çıkış kodu herhangi bir yere yerleştirebilirsiniz:

![Soluk erişilemeyen kod](media/unreachablecode-faded-cs.png)

1. Ardından, aşağıdakilerden birini yapın:

   - **Klavye**
      - Tuşuna **Ctrl**+**.** Tetikleyici için **hızlı Eylemler ve yeniden düzenlemeler** menü ve select **erişilemeyen kodları kaldırma** gelen önizleme penceresi açılır.
   - **Fare**
      - Kod sağ tıklayın, **hızlı Eylemler ve yeniden düzenlemeler** menü ve select **erişilemeyen kodları kaldırma** gelen önizleme penceresi açılır.

1. Değişiklik ile tamamladığınızda basın **Enter** veya düzeltmeyi menüsünde tıklatın ve değişiklikler uygulanır.

Örnek:

```csharp
// Before
private void Method()
{
    throw new Exception(nameof(Method));
    Console.WriteLine($"Exception for method {nameof(Method)}");
}

// Remove unreachable code

// After
private void Method()
{
    throw new Exception(nameof(Method));
}
```

## <a name="see-also"></a>Ayrıca bkz.

- [Yeniden Düzenleme](../refactoring-in-visual-studio.md)
- [Değişiklikleri Önizleme](../../ide/preview-changes.md)