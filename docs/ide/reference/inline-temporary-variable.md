---
title: Geçici bir değişken değeriyle değiştirin.
ms.date: 01/26/2018
ms.prod: visual-studio-dev15
ms.topic: reference
author: gewarren
ms.author: gewarren
manager: douge
dev_langs:
- CSharp
- VB
ms.workload:
- dotnet
ms.openlocfilehash: aa329dd3fe7d01046c35be9829aed4ca4519c3e1
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53909040"
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