---
title: Geçersiz karakter aralığı ayarlayın (JavaScript) | Microsoft Docs
ms.date: 01/18/2017
ms.prod: visual-studio-windows
ms.technology: vs-javascript
ms.topic: reference
f1_keywords:
- VS.WebClient.Help.SCRIPT5021
dev_langs:
- JavaScript
- TypeScript
- DHTML
ms.assetid: 971e9d5a-f88a-47a8-af94-f3c7c4aed5ab
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 1cbfa4de401c2a1dc0626f8f00dbb0bd1bf24408
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63007054"
---
# <a name="invalid-range-in-character-set-javascript"></a>Geçersiz karakter kümesi aralığı (JavaScript)
Normal bir ifade bir geçersiz karakter kümesi aralığı ile oluşturulmaya çalışıldı. Karakter kümesi, a-z veya 0-9 gibi yalnızca tek karakterleri aralığında olması gerekir; bir karakter kümesindeki karakter sınıfları \w gibi içeremez. Aralıktaki ilk karakteri de ikinci karakter aralığı önce gelmelidir. Örneğin:  
  
```JavaScript  
var good = /[a-z]/;     // A valid character range - a comes before z.  
var notGood = /[z-a]/;  // An invalid character range - z does not come before a.  
```  
  
### <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için  
  
- Yalnızca tek bir karakter, normal ifade karakter kümesi oluşturun ve doğru sırada olduklarından emin olmak için kullanın.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Normal ifade nesnesi](../../javascript/reference/regular-expression-object-javascript.md)   
 [Normal ifade söz dizimi (JavaScript)](https://msdn.microsoft.com/library/1400241x)