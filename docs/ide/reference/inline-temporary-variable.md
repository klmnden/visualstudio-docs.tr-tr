---
title: Geçici bir değişken değeriyle değiştirin.
ms.date: 01/26/2018
ms.topic: reference
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- dotnet
ms.openlocfilehash: a7c691efcc507212aa0649b6c4b4179fb8288f06
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55946112"
---
# <a name="inline-a-temporary-variable-refactoring"></a>Satır içi bir geçici değişken yeniden düzenleme

Bu yeniden düzenleme için geçerlidir:

- C#

- Visual Basic

**Ne:** Geçici bir değişkene kaldırın ve bunun yerine değeriyle değiştirin olanak sağlar.

**ne zaman:** Geçici değişkene kullanımını anlamak kod zorlaştırır.

**Neden:** Geçici bir değişkene kaldırmak kod kolay okunur hale getirebilir.

## <a name="how-to"></a>Nasıl Yapılır Konuları

1. Vurgulama veya satır içine alınmayacak kadar geçici değişken metin imleci yerleştirin:

   - C# İÇİN:

       ![Vurgulanan kodu:C#](media/inline-highlight-cs.png)

   - Visual Basic:

       ![Vurgulanan kod - Visual Basic](media/inline-highlight-vb.png)

2. Ardından, aşağıdakilerden birini yapın:

   - **Klavye**
      - Tuşuna **Ctrl**+**.** Tetikleyici için **hızlı Eylemler ve yeniden düzenlemeler** menüsü.
   - **Fare**
      - Kod sağ tıklayıp **hızlı Eylemler ve yeniden düzenlemeler** menüsü.

3. Seçin **satır içi geçici değişken** gelen önizleme penceresi açılır.

   Değişken kaldırılır ve kendi kullanımları değişkenin değeriyle değiştirilir.

   - C# İÇİN:

      ![Satır içi sonucu-C#](media/inline-result-cs.png)

   - Visual Basic:

      ![Satır içi sonucu - Visual Basic](media/inline-result-vb.png)

## <a name="see-also"></a>Ayrıca bkz.

- [Yeniden Düzenleme](../refactoring-in-visual-studio.md)