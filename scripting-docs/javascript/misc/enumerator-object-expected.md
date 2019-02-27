---
title: Numaralandırıcı nesne bekleniyor | Microsoft Docs
ms.date: 01/18/2017
ms.prod: visual-studio-windows
ms.technology: vs-javascript
ms.topic: reference
f1_keywords:
- VS.WebClient.Help.SCRIPT5015
dev_langs:
- JavaScript
- TypeScript
- DHTML
ms.assetid: dc6e32c1-a6e6-4e12-ac99-e3f65f91c8d7
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 14fcb4d990b03a8e7b896014403eb8dceac66b80
ms.sourcegitcommit: 23feea519c47e77b5685fec86c4bbd00d22054e3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/26/2019
ms.locfileid: "56841837"
---
# <a name="enumerator-object-expected"></a>Numaralandırıcı nesne bekleniyor
Çağırmaya çalıştığınız **Enumerator.prototype.atEnd, Enumerator.prototype.item Enumerator.prototype.moveFirst,** veya **Enumerator.prototype.moveNext** başka bir türde bir nesne üzerinde yöntemi daha `Enumerator`. Bu tür çağrısının nesne türünde olmalıdır `Enumerator`. Bu kural koduna ilişkin bir örnek aşağıda verilmiştir:  
  
```JavaScript  
var o = new Object;  
o.f = Enumerator.prototype.atEnd;  
o.f();  
```  
  
### <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için  
  
-   Yalnızca çağırma **Enumerator.prototype.atEnd**, **Enumerator.prototype.item**, **Enumerator.prototype.moveFirst**, veya  **Enumerator.prototype.moveNext** türünden nesnelerin yöntemleri `Enumerator`. Nesnenizin kaydolmadığı için bir `Enumerator` nesne, kullanın:  
  
    ```js
    if(x instanceof Enumerator)  
    ```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Numaralandırıcı Nesnesi](../../javascript/reference/enumerator-object-javascript.md)