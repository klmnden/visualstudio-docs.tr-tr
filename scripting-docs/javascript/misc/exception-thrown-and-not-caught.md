---
title: Oluşturulan özel durum yakalanmadı | Microsoft Docs
ms.date: 01/18/2017
ms.prod: visual-studio-windows
ms.technology: vs-javascript
ms.topic: reference
f1_keywords:
- VS.WebClient.Help.SCRIPT5022
dev_langs:
- JavaScript
- TypeScript
- DHTML
ms.assetid: b5235490-a8e7-42e3-804e-d85235bc6f05
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: bae4ed0a335a9c12d16cb46208f77c4b66f12547
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60050517"
---
# <a name="exception-thrown-and-not-caught"></a>Oluşan özel durum yakalanmadı
Dahil edilen bir `throw` kodunuzu, ancak deyiminde çevrilmeyen içinde bir **deneyin** bloğu veya oluştu Hayır ilişkili **catch** bloğunun Hata. Özel durumlar içinden **deneyin** kullanarak block **throw** deyimi ve yakalanan dışında **deneyin** ile engelleyecek bir **catch** deyimi.  
  
### <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için  
  
- Bir özel durum oluşturabilecek kod içine bir **deneyin** engellemek ve buna karşılık gelen bulunduğundan emin olun **catch** blok.  
  
- Catch deyimi özel durumu doğru biçimde bekliyor emin olun.  
  
- Özel durum yeniden oluşur, ilgili başka bir catch deyimi olduğundan emin olun.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Hata nesnesi](../../javascript/reference/error-object-javascript.md)   
 [Throw deyimi](../../javascript/reference/throw-statement-javascript.md)   
 [try...catch...finally Deyimi](../../javascript/reference/try-dot-dot-dot-catch-dot-dot-dot-finally-statement-javascript.md)