---
title: Yerel işlevi metoda dönüştürme
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
ms.openlocfilehash: 96064b16e53081e0456ed43275acd5edf7ead468
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58152960"
---
# <a name="convert-local-function-to-method"></a>Yerel işlevi metoda dönüştürme

Bu yeniden düzenleme için geçerlidir:

- C#
- Visual Basic

**Ne:** Yerel bir işlev bir yönteme Dönüştür

**ne zaman:** Geçerli yerel bağlamı dışında tanımlamak istediğiniz yerel bir işlev var.

**Neden:** Yerel Bağlamınızı dışında çağırabilmek yerel bir işlev bir yönteme dönüştürmek isteyebilirsiniz. Yerel işlevinizi çok uzun alırken bir yönteme dönüştürmek isteyebilirsiniz. Ayrı bir yöntem tanımlama kodunuzu daha kolay okunabilir hale getirir.

## <a name="convert-local-function-to-method-refactoring"></a>Yerel işlev yöntemi yeniden düzenlemesi için Dönüştür

1. İmlecinizi bir yerel işlevde yerleştirin.

    ![Yerel işlevi metoda dönüştürme](media/convert-local-function-to-method.png)

2. Tuşuna **Ctrl**+**.** Tetikleyici için **hızlı Eylemler ve yeniden düzenlemeler** menüsü.

    ![Yerel işlev yöntemi kod düzeltme Dönüştür](media/convert-local-function-to-method-codefix.png)

2. Tuşuna **Enter** yeniden düzenleme kabul etmek için.

    ![Yerel işlev yöntemi sonucu Dönüştür](media/convert-local-function-to-method-result.png)

## <a name="see-also"></a>Ayrıca bkz.

- [Yeniden Düzenleme](../refactoring-in-visual-studio.md)
- [.NET Geliştiricileri için İpuçları](../../ide/visual-studio-2017-for-dotnet-developers.md)
