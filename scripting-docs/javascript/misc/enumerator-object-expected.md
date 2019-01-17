---
title: Numaralandırıcı nesne bekleniyor | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-client-threshold
ms.reviewer: ''
ms.suite: ''
ms.technology:
- javascript
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- VS.WebClient.Help.SCRIPT5015
dev_langs:
- JavaScript
- TypeScript
- DHTML
ms.assetid: dc6e32c1-a6e6-4e12-ac99-e3f65f91c8d7
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 002c3a748af8f7fa5c21109adcb279f893b38965
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54347248"
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