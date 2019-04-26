---
title: Bir yöntemi geçersiz kılma oluşturma
ms.date: 01/26/2018
ms.topic: reference
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- dotnet
ms.openlocfilehash: afb32a7ddb9a53ac6585cc690a3ba8fd1098b080
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62790514"
---
# <a name="generate-an-override-in-visual-studio"></a>Visual Studio'da bir geçersiz kılma oluşturma

Bu kod oluşturma için geçerlidir:

- C#

- Visual Basic

**Ne:** Geçersiz kılınabilir bir yöntemi için kod bir taban sınıftan hemen oluşturmanıza olanak sağlar.

**ne zaman:** Bir temel sınıf yöntemini geçersiz kılın ve imza otomatik olarak oluşturmak istiyorsunuz.

**Neden:** Bu özellik imzası otomatik olarak oluşturur, ancak yöntem imzası kendiniz yazabilirsiniz.

## <a name="how-to"></a>Nasıl Yapılır Konuları

1. Tür `override` içinde C# veya `Overrides` Visual Basic'te, ardından bir boşluk istediğiniz bir geçersiz kılma yöntemi eklemek için.

   - C# İÇİN:

      ![IntelliSense geçersiz kılC#](media/override-intellisense-cs.png)

   - Visual Basic:

      ![IntelliSense VB geçersiz kıl](media/override-intellisense-vb.png)

2. Taban sınıfından geçersiz kılmak istediğiniz yöntemi seçin.

   > [!TIP]
   > - Özellik simgesi kullanın ![Özellik simgesi](media/override-property-cs.png) Özellikler listesinde gizlemek veya göstermek için.
   > - Yöntem simgesi kullanın ![Yöntem simgesi](media/override-method-cs.png) yöntemleri listesindeki gizlemek veya göstermek için.

   Seçili yöntemi veya özelliği geçersiz kılma uygulanması hazır sınıfa eklenir.

   - C# İÇİN:

       ![Sonucu geçersiz kılC#](media/override-result-cs.png)

   - Visual Basic:

       ![VB sonucu geçersiz kıl](media/override-result-vb.png)

## <a name="see-also"></a>Ayrıca bkz.

- [Kod Oluşturma](../code-generation-in-visual-studio.md)