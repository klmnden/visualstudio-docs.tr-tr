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
ms.openlocfilehash: 90230bd95e1dbcd3e4c186257c6c36faad6ba1f7
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62555136"
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
CV_private üyesi özel erişimi var.

CV_protected üye erişimi ile korumaya aldı.

CV_public üye erişimine sahiptir.

## <a name="remarks"></a>Açıklamalar
`friend` Erişim belirticisi değil dahil burada çünkü genellikle sınıfın özel ve korumalı öğelerine erişimi olmayan üye işlevleri tarafından kullanılıyor. Kullanım [Idiasymbol::get_symtag](../../debugger/debug-interface-access/idiasymbol-get-symtag.md) ile simgeleri bulmak için yöntem `SymTagFriend` erişim.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: cvconst.h

## <a name="see-also"></a>Ayrıca Bkz.
- [Enumerations and Structures](../../debugger/debug-interface-access/enumerations-and-structures.md)
- [IDiaSymbol::get_access](../../debugger/debug-interface-access/idiasymbol-get-access.md)
- [IDiaSymbol::get_symTag](../../debugger/debug-interface-access/idiasymbol-get-symtag.md)
