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
ms.openlocfilehash: e1e34be9f8eab5171af0e2553d5777b0958bf3c2
ms.sourcegitcommit: 23feea519c47e77b5685fec86c4bbd00d22054e3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/26/2019
ms.locfileid: "56840876"
---
# <a name="exception-thrown-and-not-caught"></a>Oluşan özel durum yakalanmadı
Dahil edilen bir `throw` kodunuzu, ancak deyiminde çevrilmeyen içinde bir **deneyin** bloğu veya oluştu Hayır ilişkili **catch** bloğunun Hata. Özel durumlar içinden **deneyin** kullanarak block **throw** deyimi ve yakalanan dışında **deneyin** ile engelleyecek bir **catch** deyimi.  
  
### <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için  
  
-   Bir özel durum oluşturabilecek kod içine bir **deneyin** engellemek ve buna karşılık gelen bulunduğundan emin olun **catch** blok.  
  
-   Catch deyimi özel durumu doğru biçimde bekliyor emin olun.  
  
-   Özel durum yeniden oluşur, ilgili başka bir catch deyimi olduğundan emin olun.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Hata nesnesi](../../javascript/reference/error-object-javascript.md)   
 [Throw deyimi](../../javascript/reference/throw-statement-javascript.md)   
 [try...catch...finally Deyimi](../../javascript/reference/try-dot-dot-dot-catch-dot-dot-dot-finally-statement-javascript.md)