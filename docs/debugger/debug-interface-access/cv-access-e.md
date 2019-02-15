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
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 2b5fa908692167b49c6bb92c892fb143b882d231
ms.sourcegitcommit: 752f03977f45169585e407ef719450dbe219b7fc
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2019
ms.locfileid: "56318582"
---
# <a name="cvaccesse"></a>CV_access_e
Görünürlüğü (erişim düzeyi) üye işlevleri ve değişkenler kapsamını belirtir.

## <a name="syntax"></a>Sözdizimi

```C++
typedef enum CV_access_e {
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
[Enumerations and Structures](../../debugger/debug-interface-access/enumerations-and-structures.md)  
[IDiaSymbol::get_access](../../debugger/debug-interface-access/idiasymbol-get-access.md)  
[IDiaSymbol::get_symTag](../../debugger/debug-interface-access/idiasymbol-get-symtag.md)
