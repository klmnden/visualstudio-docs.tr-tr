---
title: Değişken bildirimi başvurunun yanına taşıma
ms.date: 01/26/2018
ms.topic: reference
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
ms.workload:
- dotnet
ms.openlocfilehash: e23c5c8d6ea0895f9e5a78e726bb7a7cede071bb
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62540602"
---
# <a name="move-declaration-near-reference-refactoring"></a>Başvuru yeniden düzenleme yakın bildirimi taşıma

Bu yeniden düzenleme için geçerlidir:

- C#

**Ne:** Kendi kullanımı için değişken bildirimlerini yakın taşımanıza olanak tanır.

**ne zaman:** Dar bir kapsamda olabilir değişken bildirimleri var.

**Neden:** Bu, ancak okunabilirlik sorunları veya bilgi gizleme neden olabilecek bırakabilir. Okunabilirliği artırmak için yeniden düzenleme için bir fırsat budur.

## <a name="how-to"></a>Nasıl Yapılır Konuları

1. İmlecinizi Değişken bildiriminde yerleştirin.

1. Ardından, aşağıdakilerden birini yapın:

   - **Klavye**
      - Tuşuna **Ctrl**+**.** Tetikleyici için **hızlı Eylemler ve yeniden düzenlemeler** menü ve select **bildirimi başvurunun yanına taşıma** gelen önizleme penceresi açılır.
   - **Fare**
      - Kod sağ tıklayın, **hızlı Eylemler ve yeniden düzenlemeler** menü ve select **bildirimi başvurunun yanına taşıma** gelen önizleme penceresi açılır.

1. Değişiklik ile tamamladığınızda basın **Enter** veya düzeltmeyi menüsünde tıklatın ve değişiklikler uygulanır.

Örnek:

```csharp
// Before
int x;
if (condition)
{
    x = 1;
    Console.WriteLine(x);
}

// Move declaration near reference

// After
if (condition)
{
    int x = 1;
    Console.WriteLine(x);
}
```

## <a name="see-also"></a>Ayrıca bkz.

- [Yeniden Düzenleme](../refactoring-in-visual-studio.md)
- [Değişiklikleri Önizleme](../../ide/preview-changes.md)