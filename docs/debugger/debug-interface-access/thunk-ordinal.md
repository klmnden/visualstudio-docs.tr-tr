---
title: THUNK_ORDINAL | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- Thunk_Ordinal enumeration
ms.assetid: 026f98a9-36b8-41ef-8a72-12d7cbc2d362
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 776ee35e57b62463d47fc6f7fa26133f507f16f9
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62854441"
---
# <a name="thunkordinal"></a>THUNK_ORDINAL
Dönüştürücü türlerini belirtir.

## <a name="syntax"></a>Sözdizimi

```C++
typedef enum THUNK_ORDINAL {
    THUNK_ORDINAL_NOTYPE,
    THUNK_ORDINAL_ADJUSTOR,
    THUNK_ORDINAL_VCALL,
    THUNK_ORDINAL_PCODE,
    THUNK_ORDINAL_LOAD

    // trampoline thunk ordinals - only for use in Trampoline thunk symbols
    THUNK_ORDINAL_TRAMP_INCREMENTAL,
    THUNK_ORDINAL_TRAMP_BRANCHISLAND,
} THUNK_ORDINAL;
```

## <a name="elements"></a>Öğeleri
THUNK_ORDINAL_NOTYPE standart dönüştürücü.

THUNK_ORDINAL_ADJUSTOR A `this` adjustor dönüştürücü.

THUNK_ORDINAL_VCALL sanal çağrı dönüştürücü.

THUNK_ORDINAL_PCODE P-code dönüştürücü.

THUNK_ORDINAL_LOAD gecikme yükü dönüştürücü.

THUNK_ORDINAL_TRAMP_INCREMENTAL artımlı trampoline dönüştürücü (trampoline dönüştürücü çağrıları bir bellek alanından Sıçrama için kullanılır).

THUNK_ORDINAL_TRAMP_BRANCHISLAND dal noktası trampoline dönüştürücü.

## <a name="remarks"></a>Açıklamalar
Bu sabit listesi değerleri çağrısından döndürülen [Idiasymbol::get_thunkordinal](../../debugger/debug-interface-access/idiasymbol-get-thunkordinal.md) yöntemi.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: cvconst.h

## <a name="see-also"></a>Ayrıca Bkz.
- [Enumerations and Structures](../../debugger/debug-interface-access/enumerations-and-structures.md)
- [IDiaSymbol::get_thunkOrdinal](../../debugger/debug-interface-access/idiasymbol-get-thunkordinal.md)
