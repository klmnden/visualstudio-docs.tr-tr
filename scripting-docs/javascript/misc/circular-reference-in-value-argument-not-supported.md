---
title: Desteklenmeyen değer bağımsız değişkeninde döngüsel başvuru | Microsoft Docs
ms.date: 01/18/2017
ms.prod: visual-studio-windows
ms.technology: vs-javascript
ms.topic: reference
f1_keywords:
- VS.WebClient.Help.SCRIPT5034
dev_langs:
- JavaScript
- TypeScript
- DHTML
ms.assetid: 5d06f0fa-86f5-49d1-8d50-af1759990f43
caps.latest.revision: 13
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: a31b56b4b2d568b3bc3fd59f876f5052b9f6faff
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60064004"
---
# <a name="circular-reference-in-value-argument-not-supported"></a>Değer bağımsız değişkeninde döngüsel başvuru desteklenmez
Çağırmak için bir girişimde bulunuldu `JSON.stringify` , geçerli olmayan bir değere sahip. `value` Bağımsız değişkeni, bir dizi veya nesne, döngüsel başvuru içeriyor.  
  
### <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için  
  
- Döngüsel başvuru bağımsız değişkende kaldırın.  
  
## <a name="example"></a>Örnek  
 Bu örnekteki kod bir çalışma zamanı hatasına neden olur `john` bir başvuru içeriyor `mary` ve `mary` bir başvuru içeriyor `john`. Döngüsel başvuru kaldırmak için ya da kaldırın veya ayarlama özelliği `brother` gelen `mary` nesne veya `sister` özelliğinden `john` nesne.  
  
```JavaScript  
var john = new Object();  
var mary = new Object();  
john.sister = mary;  
mary.brother = john;  
  
// This line causes a runtime error.  
var error = JSON.stringify(john);  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [JSON nesnesi](../../javascript/reference/json-object-javascript.md)   
 [JSON.parse işlevi](../../javascript/reference/json-parse-function-javascript.md)   
 [JavaScript Çalışma zamanı Hataları](../../javascript/reference/javascript-run-time-errors.md)