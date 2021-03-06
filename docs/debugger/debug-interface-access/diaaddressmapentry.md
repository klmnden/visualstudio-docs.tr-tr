---
title: DiaAddressMapEntry | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- DiaAddressMapEntry enumeration
ms.assetid: 5d0ae226-981d-4541-a801-fc4993fe663b
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 311762f4eafc8dad63da5854870f2836ee68b3ee
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62554902"
---
# <a name="diaaddressmapentry"></a>DiaAddressMapEntry
Bir adres eşlemesi bir girişe açıklar.

## <a name="syntax"></a>Sözdizimi

```C++
struct DiaAddressMapEntry {
    DWORD rva,
    DWORD rvaTo
};
```

## <a name="elements"></a>Öğeleri
`rva` A. görüntüdeki göreli sanal adres (RVA)

`rvaTo` Göreli sanal adres `rva` görüntüde b eşlenir

## <a name="remarks"></a>Açıklamalar
Bir adres eşlemesi tek bir görüntü düzeninden bir çeviri (A) için başka bir (B) sağlar. Bir dizi `DiaAddressMapEntry` ölçütü yapıları `rva` adres Haritası tanımlar.

Bir adresi çevrilecek `addrA`, bir adrese bir görüntüdeki `addrB`, görüntü B, aşağıdaki adımları gerçekleştirin:

1. Eşleme girişi için arama `e`, en büyük ile `rva` ya da eşit `addrA`.

2. Ayarlama `delta = addrA - e.rva`.

3. Ayarlama `addrB = e.rvaTo + delta`.

    Bir dizi `DiaAddressMapEntry` yapıları geçirildiğinde [Idiaaddressmap::set_addressmap](../../debugger/debug-interface-access/idiaaddressmap-set-addressmap.md) yöntemi.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: dia2.h

## <a name="see-also"></a>Ayrıca Bkz.
- [Enumerations and Structures](../../debugger/debug-interface-access/enumerations-and-structures.md)
- [IDiaAddressMap::set_addressMap](../../debugger/debug-interface-access/idiaaddressmap-set-addressmap.md)
