---
title: CV_access_e | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- CV_access_e enumeration
ms.assetid: 33c05d65-abb4-4800-a382-54a3805ea7b0
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 373149884078b58926493fd7f37756ddb4eb8829
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53838761"
---
# <a name="cvaccesse"></a>CV_access_e
Görünürlüğü (erişim düzeyi) üye işlevleri ve değişkenler kapsamını belirtir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
typedef enum CV_access_e {   
   CV_private   = 1,  
   CV_protected = 2,  
   CV_public    = 3  
} CV_access_e;  
```  
  
## <a name="elements"></a>Öğeleri  
 CV_private  
 Üye, özel erişimi vardır.  
  
 CV_protected  
 Üye erişimi ile korumaya aldı.  
  
 CV_public  
 Üye erişimine sahiptir.  
  
## <a name="remarks"></a>Açıklamalar  
 `friend` Erişim belirticisi değil dahil burada çünkü genellikle sınıfın özel ve korumalı öğelerine erişimi olmayan üye işlevleri tarafından kullanılıyor. Kullanım [Idiasymbol::get_symtag](../../debugger/debug-interface-access/idiasymbol-get-symtag.md) ile simgeleri bulmak için yöntem `SymTagFriend` erişim.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: cvconst.h  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Sabit listeleri ve yapıları](../../debugger/debug-interface-access/enumerations-and-structures.md)   
 [Idiasymbol::get_access](../../debugger/debug-interface-access/idiasymbol-get-access.md)   
 [IDiaSymbol::get_symTag](../../debugger/debug-interface-access/idiasymbol-get-symtag.md)