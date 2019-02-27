---
title: İşlev bekleniyor | Microsoft Docs
ms.date: 01/18/2017
ms.prod: visual-studio-windows
ms.technology: vs-javascript
ms.topic: reference
f1_keywords:
- VS.WebClient.Help.SCRIPT5002
dev_langs:
- JavaScript
- TypeScript
- DHTML
ms.assetid: f62ade94-9f6f-4832-9b9b-49a06a385bbe
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 41d1ecc982dcdc4d494fc167e4784e9121bec15e
ms.sourcegitcommit: 23feea519c47e77b5685fec86c4bbd00d22054e3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/26/2019
ms.locfileid: "56843941"
---
# <a name="function-expected"></a>İşlev bekleniyor
Ya da birini çağırmaya çalıştığınız **işlev prototipi** yöntemleri olmayan bir nesne üzerinde bir `Function` nesne veya işlev çağrı bağlamındaki nesne kullanılan. Örneğin, aşağıdaki kod çünkü bu hatayı üretir **örnek** bir işlev değil.  
  
```JavaScript  
var example = new Object();  // Create a new object called "example".  
var x = example();           // Try and call example as if it were a function.  
```  
  
### <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için  
  
-   Yalnızca çağrı **işlev prototipi** yöntemlerde `Function` nesneleri.  
  
-   İşlev çağrısı işleci kullandığınızdan emin olun `()` yalnızca işlevleri çağırmak için.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [İşlev nesnesi](../../javascript/reference/function-object-javascript.md)   
 [prototype Özelliği (Nesne)](../../javascript/reference/prototype-property-object-javascript.md)