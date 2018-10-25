---
title: Bir dosya adı, Visual Studio'da bir türüyle eşleşecek şekilde yeniden adlandırın
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
ms.openlocfilehash: 8407e89d9e28c501358877df9c244175ca8155c8
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49942328"
---
# <a name="sync-a-type-to-a-filename-or-a-filename-to-a-type-refactoring"></a>Bir dosya adı veya türü bir yeniden düzenleme için bir dosya adı için bir tür eşitleme

Bu yeniden düzenleme için geçerlidir:

- C#

- Visual Basic

**Ne:** bir tür dosya adı eşleşecek şekilde yeniden adlandırın ya da bir dosya adı içerdiği türüyle eşleşecek şekilde yeniden adlandırmak sağlar.

**Ne zaman:** bir dosya veya türü yeniden adlandırmış ve karşılık gelen dosya ya da türü eşleşecek şekilde güncelleştirildi henüz yapmadıysanız.

**Neden:** farklı bir ad veya tam tersi, aradığınızı bulmak zor, bir dosya türü verme. Türü veya dosya adı yeniden adlandırarak kodu daha okunabilir ve giderek daha kolay hale gelir.

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

   - C#: Aşağıdaki örnekte, dosyanın **MyClass.cs** adlandırıldı **MyNewClass.cs** tür adıyla eşleşecek şekilde.

       ![Satır içi sonucuC#](media/synctype-result-cs.png)

   - Visual Basic: Aşağıdaki örnekte, dosyanın **Employee.vb** adlandırıldı **Person.vb** tür adıyla eşleşecek şekilde.

       ![Satır içi sonucu Visual Basic](media/synctype-result-vb.png)

> ! [NOT] Bu yeniden düzenleme henüz .NET Standard ve .NET Core projeleri için kullanılabilir değil.

## <a name="see-also"></a>Ayrıca bkz.

- [Yeniden Düzenleme](../refactoring-in-visual-studio.md)
