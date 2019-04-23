---
title: Nesne bekleniyor | Microsoft Docs
ms.date: 01/18/2017
ms.prod: visual-studio-windows
ms.technology: vs-javascript
ms.topic: reference
f1_keywords:
- VS.WebClient.Help.SCRIPT5007
dev_langs:
- JavaScript
- TypeScript
- DHTML
ms.assetid: 5d88c93d-e5b5-4b11-9bb5-bf1a5e41ccc3
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 501496c4f1bb929308ffbb75c6572de3d3f5b33b
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60115100"
---
# <a name="object-expected"></a>Nesne bekleniyor
Dışında bir yöntem veya özellik türü bir nesne üzerinde çağırma girişiminde `Object`, veya başka bir türde bir bağımsız değişken geçirilen `Object` olduğunda bir `Object` gerekiyordu.  
  
### <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için  
  
- Yalnızca nesne türü özelliği ve yöntemi Çağır `Object`.  
  
- Türünde bir nesne için bir nesne olmayan bağımsız değişken hatası meydana gelirse, geçmesi `Object`.  
  
- Tanımlanmamışsa veya null bir başvuru türünde bir nesne yerine çağrılan olup olmadığını denetleyin `Object`.  
  
     Örneğin, aşağıdaki kodda myVar bu hatayı alırsanız:  
  
    ```JavaScript  
    var str = myVar.toString();  
    ```  
  
     Bunun yerine bu kodu kullanabilirsiniz:  
  
    ```JavaScript  
    if (myVar) {  
        var str = myVar.toString();  
    }  
    ```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Nesne nesnesi](../../javascript/reference/object-object-javascript.md)   
 [Nesneler ve Diziler](../../javascript/objects-and-arrays-javascript.md)