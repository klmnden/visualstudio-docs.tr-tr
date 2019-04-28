---
title: "'return' deyimi işlev dışı | Microsoft Docs"
ms.date: 01/18/2017
ms.prod: visual-studio-windows
ms.technology: vs-javascript
ms.topic: reference
f1_keywords:
- VS.WebClient.Help.SCRIPT1018
dev_langs:
- JavaScript
- TypeScript
- DHTML
ms.assetid: 03568f9f-5f4f-4a10-a738-9a73f3832b9e
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 01ef96385d5fe3dccf14a7491e67983d39913280
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63006412"
---
# <a name="return-statement-outside-of-function"></a>'return' deyimi işlev dışı
Kullanılan bir `return` kodunuzun genel kapsamda deyimi. `return` Deyimi yalnızca bir işlev gövdesinin içinde görünmelidir.  
  
 Bir işlev ile çağırma `()` işleci bir ifadedir. Tüm ifadeler değerlere sahip; `return` deyimi, işlev tarafından döndürülen değer belirtmek için kullanılır. Genel formu şöyledir:  
  
```js
  
return [ expression ];  
```  
  
 Zaman `return` deyimi yürütüldüğünde, *ifade* değerlendirilir ve işlev değeri olarak döndürdü. Herhangi bir ifade ise **tanımlanmamış** döndürülür.  
  
 Bir işlevin yürütülmesini durdurur `return` deyimi yürütüldüğünde, işlev gövdesinde yine de kalan diğer deyimler olsa bile. Bu kuralın istisnası, **dönüş** ifade oluştuğu yer bir **deneyin** bloğu ve karşılık gelen **son** engellenmesi, kod  **Son olarak** blok işlevi döndürmeden önce yürütülecek.  
  
 Bir işlev verir, çünkü çalıştırmadan işlev gövdesinin sonuna ulaştığında, bir `return` açıklamadır, döndürülen değer **tanımlanmamış** değeri (yani işlev sonucu daha büyük bir ifadenin bir parçası olarak kullanılamaz ).  
  
### <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için  
  
- Kaldırma `return` deyimi ana gövdesinden kodunuzun (genel kapsamlı).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [return deyimi](../../javascript/reference/return-statement-javascript.md)   
 [İşlev nesnesi](../../javascript/reference/function-object-javascript.md)   
 [caller Özelliği (İşlev)](../../javascript/reference/caller-property-function-javascript.md)