---
title: Oluşturulan özel durum yakalanmadı | Microsoft Docs
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
- VS.WebClient.Help.SCRIPT5022
dev_langs:
- JavaScript
- TypeScript
- DHTML
ms.assetid: b5235490-a8e7-42e3-804e-d85235bc6f05
caps.latest.revision: 6
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 839ff08da4d26406b508a206c809b0813d2b32e1
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54349042"
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