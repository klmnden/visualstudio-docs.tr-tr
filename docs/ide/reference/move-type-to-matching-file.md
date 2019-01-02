---
title: Türü eşleşen dosya yeniden düzenleme için Taşı
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
ms.openlocfilehash: 793ae8f86bf4c4641a3170cde011a3912d0d38ef
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53870553"
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
