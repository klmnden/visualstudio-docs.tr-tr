---
title: Geçersiz karakter aralığı ayarlayın (JavaScript) | Microsoft Docs
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
- VS.WebClient.Help.SCRIPT5021
dev_langs:
- JavaScript
- TypeScript
- DHTML
ms.assetid: 971e9d5a-f88a-47a8-af94-f3c7c4aed5ab
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: e4cc8feb9a33c2995e592f8031beb2e03605891d
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54346091"
---
# <a name="invalid-range-in-character-set-javascript"></a>Geçersiz karakter kümesi aralığı (JavaScript)
Normal bir ifade bir geçersiz karakter kümesi aralığı ile oluşturulmaya çalışıldı. Karakter kümesi, a-z veya 0-9 gibi yalnızca tek karakterleri aralığında olması gerekir; bir karakter kümesindeki karakter sınıfları \w gibi içeremez. Aralıktaki ilk karakteri de ikinci karakter aralığı önce gelmelidir. Örneğin:  
  
```JavaScript  
var good = /[a-z]/;     // A valid character range - a comes before z.  
var notGood = /[z-a]/;  // An invalid character range - z does not come before a.  
```  
  
### <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için  
  
-   Yalnızca tek bir karakter, normal ifade karakter kümesi oluşturun ve doğru sırada olduklarından emin olmak için kullanın.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Normal ifade nesnesi](../../javascript/reference/regular-expression-object-javascript.md)   
 [Normal ifade söz dizimi (JavaScript)](https://msdn.microsoft.com/library/1400241x)