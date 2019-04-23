---
title: Beklenmeyen niceleyici (JavaScript) | Microsoft Docs
ms.date: 01/18/2017
ms.prod: visual-studio-windows
ms.technology: vs-javascript
ms.topic: reference
f1_keywords:
- VS.WebClient.Help.SCRIPT5018
dev_langs:
- JavaScript
- TypeScript
- DHTML
ms.assetid: ba6d34f9-2d6f-486c-a929-6cd9818be322
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 52b98875b560e4863a93849cf99c2f8756cd438a
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60117154"
---
# <a name="unexpected-quantifier-javascript"></a>Beklenmeyen niceleyici (JavaScript)
Normal ifade arama kriterinizi oluştururken bir geçersiz yineleme faktörü ile bir desen öğesi oluşturuldu. Örneğin, deseni  
  
```js
/^+/  
```  
  
 Geçersiz çünkü öğenin ^ (giriş başlangıcına), bir yineleme faktörü sahip olamaz. Aşağıdaki tabloda, yineleme Etkenler olamaz öğeleri listeler.  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|^|Giriş başına|  
|$|Konec vstupu|  
|\b|Sözcük sınırı|  
|\B|Sözcük olmayan sınır|  
|*|Sıfır veya daha fazla yinelemeleri|  
|+|Bir veya daha fazla yinelemeleri|  
|?|Sıfır veya bir yinelemeleri|  
|{n}|n yinelemeleri|  
|{n}|n ya da daha fazla yinelemeleri|  
|{n, m}|Bir n-m repetitions, kapsamlı|  
  
### <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için  
  
- Arama deseni öğeniz yalnızca geçerli yinelemeyi faktörleri içeren emin olun.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Normal ifade nesnesi](../../javascript/reference/regular-expression-object-javascript.md)   
 [Normal ifade söz dizimi (JavaScript)](https://msdn.microsoft.com/library/1400241x)