---
title: Geçersiz değiştirici bağımsız değişken | Microsoft Docs
ms.date: 01/18/2017
ms.prod: visual-studio-windows
ms.technology: vs-javascript
ms.topic: reference
f1_keywords:
- VS.WebClient.Help.SCRIPT5035
dev_langs:
- JavaScript
- TypeScript
- DHTML
ms.assetid: 4727186f-facd-4aa6-9447-bbefbae83f07
caps.latest.revision: 12
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 46e01a4e6bb989fad2da6f979c79b7aba13df63a
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63007320"
---
# <a name="invalid-replacer-argument"></a>Geçersiz değiştirici bağımsız değişken
Çağırmak için bir girişimde bulunuldu `JSON.stringify` bağımsız değişkeni geçerli değil. `replacer` Bağımsız değişkeni bir işlev veya dizi olması gerekir.  
  
### <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için  
  
- Değişiklik `replacer` bağımsız değişkeni bir işlev veya dizi.  
  
## <a name="example"></a>Örnek  
 Bu örnekteki kod bir çalışma zamanı hatasına neden olur `memberfilter` bir işlev veya dizi yerine bir nesnedir.  
  
```JavaScript  
var contact = new Object();  
contact.firstname = "Jesper";  
contact.surname = "Aaberg";  
contact.phone = ["555-0100", "555-0120"];  
  
var memberfilter = new Object();  
  
// This line will cause a runtime error.  
var jsontext = JSON.stringify(contact, memberfilter, "\t");  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [JSON nesnesi](../../javascript/reference/json-object-javascript.md)   
 [JSON.parse işlevi](../../javascript/reference/json-parse-function-javascript.md)   
 [JavaScript Çalışma zamanı Hataları](../../javascript/reference/javascript-run-time-errors.md)