---
title: Sonlandırılmamış açıklama | Microsoft Docs
ms.date: 01/18/2017
ms.prod: visual-studio-windows
ms.technology: vs-javascript
ms.topic: reference
f1_keywords:
- VS.WebClient.Help.SCRIPT1016
dev_langs:
- JavaScript
- TypeScript
- DHTML
ms.assetid: d4286315-814b-4966-b4c4-1ee19d796eff
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: f2b21c585bb48b55929a78554d686477e0fa5649
ms.sourcegitcommit: 23feea519c47e77b5685fec86c4bbd00d22054e3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/26/2019
ms.locfileid: "56842455"
---
# <a name="unterminated-comment"></a>Sonlandırılmayan açıklama
Çok satırlı açıklama bloğu başladı, ancak düzgün bir şekilde, sona ermedi değil. Çok satırlı açıklamalar başlar ile bir "/\*" birleşimi ve geriye doğru ile biten "\*/" birleşimi. Bir örnek verilmiştir:  
  
```JavaScript  
/* This is a comment  
This is another part of the same comment.*/  
```  
  
### <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için  
  
-   Çok satırlı yorumlarla sonlandırmak mutlaka "*/".  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Açıklama Deyimleri](../../javascript/reference/comment-statements-javascript.md)