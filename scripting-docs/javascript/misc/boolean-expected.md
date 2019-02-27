---
title: Boolean bekleniyor | Microsoft Docs
ms.date: 01/18/2017
ms.prod: visual-studio-windows
ms.technology: javascript
ms.topic: reference
f1_keywords:
- VS.WebClient.Help.SCRIPT5010
dev_langs:
- JavaScript
- TypeScript
- DHTML
ms.assetid: 35d71b7f-53fd-44c4-a7c7-b1550c65cfd4
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 82123fe2a38b3de1d6e6c015f47bc5f7edd02791
ms.sourcegitcommit: 23feea519c47e77b5685fec86c4bbd00d22054e3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/26/2019
ms.locfileid: "56840530"
---
# <a name="boolean-expected"></a>Boolean bekleniyor
Çağırmaya çalıştığınız **Boolean.prototype.toString** veya **Boolean.prototype.valueOf** yöntemi dışında bir türde bir nesne üzerinde `Boolean`. Bu tür çağrısının nesne türünde olmalıdır `Boolean`. Örneğin:

```JavaScript
var o = new Object;
o.f = Boolean.prototype.toString;
o.f();
```

## <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için

- Yalnızca çağırma **Boolean.prototype.toString** veya **Boolean.prototype.valueOf** türünden nesnelerin yöntemleri **Boolean.**

## <a name="see-also"></a>Ayrıca Bkz.

- [Boole Nesnesi](../../javascript/reference/boolean-object-javascript.md)
- [Veri Türleri](../../javascript/data-types-javascript.md)
- [Program Akışı Denetimi](../../javascript/controlling-program-flow-javascript.md)
- [Verileri Kopyalama, Geçirme ve Karşılaştırma](../../javascript/advanced/copying-passing-and-comparing-data-javascript.md)