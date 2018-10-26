---
title: Visual Studio'da değeriyle geçici bir değişkenle değiştirin.
ms.date: 01/26/2018
ms.prod: visual-studio-dev15
ms.technology: vs-ide-general
ms.topic: reference
author: gewarren
ms.author: gewarren
manager: douge
dev_langs:
- CSharp
- VB
ms.workload:
- dotnet
ms.openlocfilehash: fb6fc6888e33b2cc0d210e9cb1e1aababe304f2a
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49916770"
---
# <a name="inline-a-temporary-variable-refactoring"></a>Satır içi bir geçici değişken yeniden düzenleme

Bu yeniden düzenleme için geçerlidir:

- C#

- Visual Basic

**Ne:** geçici değişken kaldırın ve bunun yerine değeriyle değiştirme olanak tanır.

**Ne zaman:** geçici değişken kullanımı kodu anlamak zorlaştırır.

**Neden:** geçici değişken kaldırılması duruma kodu daha kolay okunabilir.

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