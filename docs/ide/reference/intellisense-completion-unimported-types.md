---
title: Önemsiz türler için IntelliSense tamamlanması
description: IntelliSense tamamlanma ile henüz içeri aktarmadığınızı türlerini kullanmak üzere nasıl bir `using` yönergesi.
ms.date: 06/20/2019
ms.topic: reference
author: mikadumont
ms.author: midumont
manager: jillfra
dev_langs:
- CSharp
ms.workload:
- dotnet
ms.openlocfilehash: f313cfa8520e4c13b310be0f9223466c529ca18f
ms.sourcegitcommit: 16bcaca215de75479695738d3c2d703c78c3500e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/21/2019
ms.locfileid: "67313208"
---
# <a name="intellisense-completion-for-unimported-types"></a>Önemsiz türler için IntelliSense tamamlanması

Bu yeniden düzenleme için geçerlidir:

- C#

**Ne:** Önemsiz türler için tamamlama IntelliSense sağlar.

**ne zaman:** Bir bağımlılık projenizde zaten olan bir türü eklemek istediğiniz, ancak içeri aktarma deyimi dosyanıza henüz eklenmedi. 

**Neden:** El ile içeri aktarma deyimi dosyanıza eklemeniz gerekmez.

## <a name="how-to"></a>Nasıl Yapılır Konuları

1. Projenizde bir bağımlılık olan bir türü kullanarak başladığınızda IntelliSense önerileri verin.
2. Tuşuna **sekmesini**. 

   Dosyanıza import deyimini eklenir.

   ![Önemsiz türler için IntelliSense tamamlanması](media/intellisense-completion-unimported-types.png)

## <a name="see-also"></a>Ayrıca bkz.

- [Yeniden Düzenleme](../refactoring-in-visual-studio.md)
