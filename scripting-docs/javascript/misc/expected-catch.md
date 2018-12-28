---
title: "'Catch' bekleniyor. | Microsoft Docs"
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
- VS.WebClient.Help.SCRIPT1033
dev_langs:
- JavaScript
- TypeScript
- DHTML
ms.assetid: f1cd947f-eba2-411e-8e84-8ca86f608643
caps.latest.revision: 6
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 244635605abafc5c0bd22c5203b105aa6e7dc669
ms.sourcegitcommit: f6dd17b0864419083d0a1bf54910023045526437
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/27/2018
ms.locfileid: "53801989"
---
# <a name="expected-catch"></a>'catch' bekleniyor.
Özel durum işleme kullanılan **deneyin** engellemek, ancak ilişkili yazmadı **catch** deyimi. Özel durum işleme mekanizmasını, bir özel durum oluşursa, yürütülecek değil kod ile birlikte başarısız olabilir kodu içinde sarmalamak gerektiren bir **deneyin** blok. Özel durumlar içinden **deneyin** kullanarak block **throw** deyimi ve yakalanan dışında **deneyin** bir veya daha fazla blok **catch**deyimleri.  
  
### <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için  
  
-   İlişkili ekleme **catch** blok.  
  
-   Kullanmayı deneyin bir **son** bloğu yerine bir **catch** blok.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [try... catch... finally deyimi](../../javascript/reference/try-dot-dot-dot-catch-dot-dot-dot-finally-statement-javascript.md)   
 [Hata Nesnesi](../../javascript/reference/error-object-javascript.md)