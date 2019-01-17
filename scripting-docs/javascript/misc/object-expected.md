---
title: Nesne bekleniyor | Microsoft Docs
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
- VS.WebClient.Help.SCRIPT5007
dev_langs:
- JavaScript
- TypeScript
- DHTML
ms.assetid: 5d88c93d-e5b5-4b11-9bb5-bf1a5e41ccc3
caps.latest.revision: 9
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 49d66c82081af06bf23a43922629a579a6d6f590
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54345792"
---
# <a name="object-expected"></a>Nesne bekleniyor
Dışında bir yöntem veya özellik türü bir nesne üzerinde çağırma girişiminde `Object`, veya başka bir türde bir bağımsız değişken geçirilen `Object` olduğunda bir `Object` gerekiyordu.  
  
### <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için  
  
-   Yalnızca nesne türü özelliği ve yöntemi Çağır `Object`.  
  
-   Türünde bir nesne için bir nesne olmayan bağımsız değişken hatası meydana gelirse, geçmesi `Object`.  
  
-   Tanımlanmamışsa veya null bir başvuru türünde bir nesne yerine çağrılan olup olmadığını denetleyin `Object`.  
  
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