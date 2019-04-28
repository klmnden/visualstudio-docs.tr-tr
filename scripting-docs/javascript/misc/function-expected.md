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
ms.openlocfilehash: 4442143b2766ed3608a852d0f811a6b943fd19df
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63007112"
---
# <a name="function-expected"></a>İşlev bekleniyor
Ya da birini çağırmaya çalıştığınız **işlev prototipi** yöntemleri olmayan bir nesne üzerinde bir `Function` nesne veya işlev çağrı bağlamındaki nesne kullanılan. Örneğin, aşağıdaki kod çünkü bu hatayı üretir **örnek** bir işlev değil.  
  
```JavaScript  
var example = new Object();  // Create a new object called "example".  
var x = example();           // Try and call example as if it were a function.  
```  
  
### <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için  
  
- Yalnızca çağrı **işlev prototipi** yöntemlerde `Function` nesneleri.  
  
- İşlev çağrısı işleci kullandığınızdan emin olun `()` yalnızca işlevleri çağırmak için.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [İşlev nesnesi](../../javascript/reference/function-object-javascript.md)   
 [prototype Özelliği (Nesne)](../../javascript/reference/prototype-property-object-javascript.md)