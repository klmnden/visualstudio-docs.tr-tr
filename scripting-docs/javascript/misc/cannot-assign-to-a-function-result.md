---
title: İşlev sonucuna atanamaz | Microsoft Docs
ms.date: 01/18/2017
ms.prod: visual-studio-windows
ms.technology: vs-javascript
ms.topic: reference
f1_keywords:
- VS.WebClient.Help.SCRIPT5003
dev_langs:
- JavaScript
- TypeScript
- DHTML
ms.assetid: ee8ffb3a-1451-4cb3-99bf-5e9cf8b77d79
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 226056f139e45f432d757aff8f8774b013742de3
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60076818"
---
# <a name="cannot-assign-to-a-function-result"></a>İşlev sonucuna atanamaz
İşlev sonucuna bir değer atamak çalışıldı. Bir işlevin sonucu bir değişkene atanabilir, ancak bir değişken olarak kullanılamaz. İşlev için yeni bir değer atamak istiyorsanız, parantezler (işlev çağrısı işleci) atlayın. Aşağıdaki örnek bu hata oluşturulduğu bir durumu gösterir.  
  
```js
myFunction() = 42;  // Attempting to assign the value 42 to the result of the function call.  
```  
  
### <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için  
  
- Bir işlev çağrısı sonucunu değerini yapabilecekleriniz bir şey kullanmayın *atama*. İşlev çağrısı sonucunu atayabilirsiniz *bir değişkene* rağmen.  
  
    ```JavaScript  
    myVar = myFunction(42);  
    ```  
  
- Alternatif olarak, işlev kendisi (ve dönüş değeri) bir değişkene atayabilirsiniz.  
  
    ```JavaScript  
    myFunction = new Function("return 42;");  
    ```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [İşlev nesnesi](../../javascript/reference/function-object-javascript.md)   
 [JavaScript kodu yazma](../../javascript/writing-javascript-code.md)   
 [İşlevler](../../javascript/functions-javascript.md)