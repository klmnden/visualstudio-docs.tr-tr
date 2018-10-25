---
title: Visual Studio'da bir yöntemi geçersiz kılma oluşturma
ms.date: 01/26/2018
ms.prod: visual-studio-dev15
ms.technology: vs-ide-general
ms.topic: reference
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- dotnet
ms.openlocfilehash: 5d51139d2e5197607de2255b267c24bf2a9db2b3
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49919071"
---
# <a name="generate-an-override-in-visual-studio"></a>Visual Studio'da bir geçersiz kılma oluşturma

Bu kod oluşturma için geçerlidir:

- C#

- Visual Basic

**Ne:** geçersiz kılınabilir bir yöntemi için kod bir taban sınıftan hemen oluşturmanıza olanak tanır.

**Ne zaman:** bir temel sınıf yöntemini geçersiz kılın ve imza otomatik olarak oluşturmak istiyorsunuz.

**Neden:** ancak bu özellik imzası otomatik olarak oluşturur, yöntem imzası kendiniz yazabilirsiniz.

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