---
title: Değer iletişim kutusu değiştiremezsiniz | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- vs.debug.variables.failededit
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- Cannot Change Value dialog box
- variables [debugger], editing
ms.assetid: 19e930c2-5fbf-4c83-aae8-a1dc3f8fcae8
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 2f8f9dafe8ada8914591426dea9abc867de2236f
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56628279"
---
# <a name="cannot-change-value-dialog-box"></a>Değer Değiştirilemez İletişim Kutusu
## <a name="error"></a>Hata
 `The value of this variable cannot be changed` &#124;`The name` *adı* `does not exist in the current context` &#124; *çeşitli başka iletiler*

 Hata ayıklayıcı penceresindeki (Otomatikler, izleme veya yerel öğeler windows) veya QuickWatch iletişim kutusundaki geçersiz bir değer için bir değişken içeriğini değiştirmeye çalıştığınızda bu ileti kutusu görünür. Örneğin, bir karakter dizesindeki bir tamsayı değişkeninin değeri ayarlamaya çalışırsanız, bu ileti kutusu görünür.

## <a name="solution"></a>Çözüm
 Hata ayıklayıcı pencereye yazın giriş olduğundan emin olun veya QuickWatch iletişim kutusu ayarlamaya çalıştığınız değişken için geçerli bir değeri temsil eder.

## <a name="see-also"></a>Ayrıca Bkz.

- [Hata Ayıklayıcısındaki İfadeler](../debugger/expressions-in-the-debugger.md)