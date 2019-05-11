---
title: Yerel bir işlev bir yönteme Dönüştür
ms.date: 02/19/2019
ms.topic: reference
author: kendrahavens
ms.author: kehavens
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- dotnet
ms.openlocfilehash: ccddc3aef24ba14245dc568ca5f369e38ce8eba0
ms.sourcegitcommit: 614d5b99576ea27a41957cd94062dc95cbd29c1c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2019
ms.locfileid: "65531645"
---
# <a name="convert-a-local-function-to-a-method"></a>Yerel bir işlev bir yönteme Dönüştür

Bu yeniden düzenleme için geçerlidir:

- C#
- Visual Basic

**Ne:** Yerel bir işlev bir yönteme dönüştürün.

**ne zaman:** Geçerli yerel bağlamı dışında tanımlamak istediğiniz yerel bir işlev var.

**Neden:** Yerel, bağlamı dışında çağırabilirsiniz yerel bir işlev bir yönteme dönüştürmek istediğiniz. Yerel işlevinizi çok uzun alırken bir yönteme dönüştürmek isteyebilirsiniz. Ayrı bir yöntem işlevi tanımladığınızda, kodunuzu daha kolay.

## <a name="convert-local-function-to-method-refactoring"></a>Yerel işlev yöntemi yeniden düzenlemesi için Dönüştür

1. İmlecinizi yerel işlevde yerleştirin.

    ![Yerel bir işlev yöntemi kod örneğine Dönüştür](media/convert-local-function-to-method.png)

2. Tuşuna **Ctrl**+**.** Tetikleyici için **hızlı Eylemler ve yeniden düzenlemeler** menüsü.

    ![Yerel işlev yöntemi kod düzeltme örneğine Dönüştür](media/convert-local-function-to-method-codefix.png)

2. Yeniden düzenleme kabul etmek için Enter tuşuna basın.

    ![Yerel işlev yöntemi sonucu örneğine Dönüştür](media/convert-local-function-to-method-result.png)

## <a name="see-also"></a>Ayrıca bkz.

- [Yeniden Düzenleme](../refactoring-in-visual-studio.md)
- [.NET Geliştiricileri için İpuçları](../csharp-developer-productivity.md)
