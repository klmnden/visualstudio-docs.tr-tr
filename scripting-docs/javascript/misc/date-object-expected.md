---
title: Tarih nesnesi bekleniyor | Microsoft Docs
ms.date: 01/18/2017
ms.prod: visual-studio-windows
ms.technology: vs-javascript
ms.topic: reference
f1_keywords:
- VS.WebClient.Help.SCRIPT5006
dev_langs:
- JavaScript
- TypeScript
- DHTML
ms.assetid: d6ab82e6-ca64-46b4-a06c-5c6b0aa057cb
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: a53ff758622cf719c2b10ea47fc516ac8684eb6a
ms.sourcegitcommit: 23feea519c47e77b5685fec86c4bbd00d22054e3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/26/2019
ms.locfileid: "56842253"
---
# <a name="date-object-expected"></a>Tarih nesnesi bekleniyor
Çağırmaya çalıştığınız **Date.prototype.toString** veya **Date.prototype.valueOf** yöntemi dışında bir türde bir nesne üzerinde `Date`. Bu tür çağrısının nesne türünde olmalıdır `Date`. Örneğin:  
  
```JavaScript  
var o = new Object;  
o.f = Date.prototype.toString;  
o.f();  
```  
  
### <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için  
  
-   Yalnızca çağırma **Date.prototype.toString** veya **Date.prototype.valueOf** türünden nesnelerin yöntemleri `Date`.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Tarih nesnesi](../../javascript/reference/date-object-javascript.md)   
 [getDate metodu (tarih)](../../javascript/reference/getdate-method-date-javascript.md)   
 [İç Nesneler](../../javascript/intrinsic-objects-javascript.md)