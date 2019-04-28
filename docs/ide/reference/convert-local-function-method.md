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
ms.openlocfilehash: a580077528c87e62f81e840ed6dee76ff1eac57f
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62968307"
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
- [.NET Geliştiricileri için İpuçları](../../ide/visual-studio-2017-for-dotnet-developers.md)
