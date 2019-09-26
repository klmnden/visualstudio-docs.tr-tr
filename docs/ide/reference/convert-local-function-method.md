---
title: Yerel bir işlevi bir yönteme Dönüştür
ms.date: 02/19/2019
ms.topic: reference
author: kendrahavens
ms.author: kehavens
manager: jillfra
ms.workload:
- dotnet
ms.openlocfilehash: 3572682fe68d9b0b1bc4adee537de5cd056a8906
ms.sourcegitcommit: 9a3972eb85de5443ac2bc03964c5a251c39b2921
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/26/2019
ms.locfileid: "71301687"
---
# <a name="convert-a-local-function-to-a-method"></a>Yerel bir işlevi bir yönteme Dönüştür

Bu yeniden düzenleme için geçerlidir:

- C#

**Yazdırılacak** Yerel bir işlevi bir yönteme dönüştürün.

**Oluşturulurken** Geçerli yerel bağlamınızın dışında tanımlamak istediğiniz bir yerel işleviniz var.

**Kaydol** Yerel bir işlevi bir yönteme dönüştürmek istiyorsunuz, böylece bunu yerel içeriğiniz dışında çağırabilirsiniz. Yerel işleviniz çok uzun süren bir yönteme dönüştürmek isteyebilirsiniz. İşlevi ayrı bir yöntemde tanımladığınızda, kodunuzun okunması daha kolay olur.

## <a name="convert-local-function-to-method-refactoring"></a>Yerel işlevi yeniden düzenleme yöntemine Dönüştür

1. İmlecinizi yerel işleve yerleştirin.

    ![Yerel bir işlevi bir yöntem kodu örneğine Dönüştür](media/convert-local-function-to-method.png)

2. Tuşuna **Ctrl**+ **.** Tetikleyici için **hızlı Eylemler ve yeniden düzenlemeler** menüsü.

    ![Yerel işlevi Yöntem kodu düzeltmesini örnekle Dönüştür](media/convert-local-function-to-method-codefix.png)

2. Yeniden düzenlemeyi kabul etmek için ENTER tuşuna basın.

    ![Yerel işlevi Yöntem sonucu örneğine Dönüştür](media/convert-local-function-to-method-result.png)

## <a name="see-also"></a>Ayrıca bkz.

- [Yeniden Düzenleme](../refactoring-in-visual-studio.md)
- [.NET Geliştiricileri için İpuçları](../csharp-developer-productivity.md)
