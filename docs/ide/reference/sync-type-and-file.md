---
title: Bir dosya adı bir türüyle eşleşecek şekilde yeniden adlandırın
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
ms.openlocfilehash: 90783dcd609094659517d994c3a4d4e0610b7735
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62945199"
---
# <a name="sync-a-type-to-a-filename-or-a-filename-to-a-type-refactoring"></a>Bir dosya adı veya türü bir yeniden düzenleme için bir dosya adı için bir tür eşitleme

Bu yeniden düzenleme için geçerlidir:

- C#

- Visual Basic

**Ne:** Bir tür dosya adı eşleşecek şekilde yeniden adlandırın veya bir dosya adı içerdiği türüyle eşleşecek şekilde yeniden adlandırmak imkan tanır.

**ne zaman:** Bir dosya veya türü yeniden adlandırmış ve karşılık gelen dosya ya da türü eşleşecek şekilde güncelleştirildi henüz yapmadıysanız.

**Neden:** Farklı bir ad veya tam tersi, aradığınızı bulmak zor, bir dosyadaki türü yapılıyor. Türü veya dosya adı yeniden adlandırarak kodu daha okunabilir ve giderek daha kolay hale gelir.

> [!NOTE]
> Bu yeniden düzenleme henüz .NET Standard ve .NET Core projeleri için kullanılabilir değil.

## <a name="how-to"></a>Nasıl Yapılır Konuları

1. Vurgulama veya eşitlenecek türü adını metin imleci yerleştirin:

   - C# İÇİN:

       ![Vurgulanan kodu:C#](media/synctype-highlight-cs.png)

   - Visual Basic:

       ![Vurgulanmış kodu - Visual Basic](media/synctype-highlight-vb.png)

2. Ardından, aşağıdakilerden birini yapın:

   - **Klavye**
      - Tuşuna **Ctrl**+**.** Tetikleyici için **hızlı Eylemler ve yeniden düzenlemeler** menü ve select **için dosyayı yeniden adlandır *TypeName*.cs** önizleme penceresi açılan menüsü'nden burada *TypeName* seçtiğiniz türünün adı.
      - Tuşuna **Ctrl**+**.** Tetikleyici için **hızlı Eylemler ve yeniden düzenlemeler** menü ve seçin **yeniden adlandırmak için türü _Filename_**  önizleme penceresi açılan menüsü'nden burada *Filename* geçerli dosya adıdır.
   - **Fare**
      - Kod sağ tıklayın, **hızlı Eylemler ve yeniden düzenlemeler** seçin ve menü **için dosyayı yeniden adlandır *TypeName*.cs** önizleme penceresi açılan menüsü'nden burada *TypeName* seçtiğiniz türünün adı.
      - Kod sağ tıklayın, **hızlı Eylemler ve yeniden düzenlemeler** menü ve seçin **yeniden adlandırma türü _Filename_**  önizleme penceresi açılan menüsü'nden burada  *Filename* geçerli dosya adıdır.

   Türe veya dosya yeniden adlandırılır.

   - C#: Dosya aşağıdaki örnekte **MyClass.cs** adlandırıldı **MyNewClass.cs** tür adıyla eşleşecek şekilde.

       ![Satır içi sonucuC#](media/synctype-result-cs.png)

   - Visual Basic: Dosya aşağıdaki örnekte **Employee.vb** adlandırıldı **Person.vb** tür adıyla eşleşecek şekilde.

       ![Satır içi sonucu Visual Basic](media/synctype-result-vb.png)

## <a name="see-also"></a>Ayrıca bkz.

- [Yeniden Düzenleme](../refactoring-in-visual-studio.md)
