---
title: Türü eşleşen dosya yeniden düzenleme için Taşı
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
ms.openlocfilehash: 31e3b12f6a19ea64e43f7a5e00e3c795cc7358e0
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62540761"
---
# <a name="move-a-type-to-a-matching-file-refactoring"></a>Bir eşleşen dosya yeniden düzenleme için bir tür Taşı

Bu yeniden düzenleme için geçerlidir:

- C#

- Visual Basic

**Ne:** Seçilen tür aynı ada sahip ayrı bir dosyaya taşımanıza olanak tanır.

**ne zaman:** Aynı dosyada, ayırmak istediğiniz birden fazla sınıflar, yapılar, arabirimler, vb. vardır.

**Neden:** Aynı dosyaya birden fazla yerleştirme, bu tür bulmak zorlaştırabilir. Aynı ada sahip dosyaları türleri taşıyarak, kod daha okunabilir ve giderek daha kolay hale gelir.

## <a name="how-to"></a>Nasıl Yapılır Konuları

1. Burada tanımlanan türünün adı imleci yerleştirin. Örneğin:

   ```csharp
   class Person
   ```

   ```vb
   Class Person
   ```

2. Ardından, aşağıdakilerden birini yapın:

   - Tuşuna **Ctrl**+**.**
   - Tür adına sağ tıklayıp **hızlı Eylemler ve yeniden düzenlemeler**

1. Seçin **türüne taşımak için *TypeName*.cs** menüsünden, burada *TypeName* seçtiğiniz türünün adı.

   Yeni bir dosya türü ile aynı ada sahip bir proje türü taşınır.

   - C# İÇİN:

      ![Satır içi sonucu-C#](media/movetype-result-cs.png)

   - Visual Basic:

      ![Satır içi sonucu - Visual Basic](media/movetype-result-vb.png)

## <a name="see-also"></a>Ayrıca bkz.

- [Yeniden Düzenleme](../refactoring-in-visual-studio.md)
