---
title: Throw ardından aynı kaynak satırdaki bir ifade tarafından gerekir | Microsoft Docs
ms.date: 01/18/2017
ms.prod: visual-studio-windows
ms.technology: vs-javascript
ms.topic: reference
f1_keywords:
- VS.WebClient.Help.SCRIPT1035
dev_langs:
- JavaScript
- TypeScript
- DHTML
ms.assetid: b03b7747-01a1-40c6-af80-a1dd70bc5781
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 4c8ed951fb30b84f114f8f44a60e94b88f0f1d0f
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60069529"
---
# <a name="throw-must-be-followed-by-an-expression-on-the-same-source-line"></a>Throw ardından aynı kaynak satırdaki bir ifade gelmelidir
Kullanılan `throw` anahtar sözcüğü, bir ifade ile aynı kaynak satırdaki celbi değil ancak. A `throw` deyim iki bölümden oluşur: `throw` oluşturulmasına ifadeyle anahtar sözcüğü. Örneğin:  
  
```JavaScript  
if (denominator == 0) {  
 throw new DivideByZeroException();  
}  
```  
  
 Bu iki bileşenin bölünemiyor.  
  
### <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için  
  
- Emin olun `throw` anahtar sözcüğü ve durum ifade aynı satırda görünür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Hata nesnesi](../../javascript/reference/error-object-javascript.md)   
 [Throw deyimi](../../javascript/reference/throw-statement-javascript.md)   
 [try...catch...finally Deyimi](../../javascript/reference/try-dot-dot-dot-catch-dot-dot-dot-finally-statement-javascript.md)