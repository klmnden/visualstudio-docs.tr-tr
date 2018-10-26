---
title: Visual Studio'da değişken bildirimi başvurunun yanına taşıma
ms.date: 01/26/2018
ms.prod: visual-studio-dev15
ms.technology: vs-ide-general
ms.topic: reference
author: gewarren
ms.author: gewarren
manager: douge
dev_langs:
- csharp
ms.workload:
- dotnet
ms.openlocfilehash: e8587b7bd94f85f40371a211af82661030e3f288
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49908193"
---
# <a name="move-declaration-near-reference-refactoring"></a>Başvuru yeniden düzenleme yakın bildirimi taşıma

Bu yeniden düzenleme için geçerlidir:

- C#

**Ne:** yakın değişken bildirimlerini kullanımları için geçiş yapmanıza izin veren.

**Ne zaman:** daha dar bir kapsamda olan değişken bildirimleri sahip.

**Neden:** olduğu, ancak okunabilirlik sorunları veya bilgi gizleme neden olabilir bırakabilir. Okunabilirliği artırmak için yeniden düzenleme için bir fırsat budur.

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