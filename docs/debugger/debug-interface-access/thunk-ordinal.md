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
ms.openlocfilehash: 482c5f7bd0565c3b6ece124c88bd5e225b4cc7dd
ms.sourcegitcommit: 752f03977f45169585e407ef719450dbe219b7fc
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2019
ms.locfileid: "56318530"
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
THUNK_ORDINAL_NOTYPE  
Standart dönüştürücü.

THUNK_ORDINAL_ADJUSTOR  
A `this` adjustor dönüştürücü.

THUNK_ORDINAL_VCALL  
Sanal çağrı dönüştürücü.

THUNK_ORDINAL_PCODE  
P-code dönüştürücü.

THUNK_ORDINAL_LOAD  
Gecikme yükü dönüştürücü.

THUNK_ORDINAL_TRAMP_INCREMENTAL  
Artımlı trampoline dönüştürücü (trampoline dönüştürücü çağrıları bir bellek alanından Sıçrama için kullanılır).

THUNK_ORDINAL_TRAMP_BRANCHISLAND  
Dal noktası trampoline dönüştürücü.

## <a name="remarks"></a>Açıklamalar
Bu sabit listesi değerleri çağrısından döndürülen [Idiasymbol::get_thunkordinal](../../debugger/debug-interface-access/idiasymbol-get-thunkordinal.md) yöntemi.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: cvconst.h

## <a name="see-also"></a>Ayrıca Bkz.
[Enumerations and Structures](../../debugger/debug-interface-access/enumerations-and-structures.md)  
[IDiaSymbol::get_thunkOrdinal](../../debugger/debug-interface-access/idiasymbol-get-thunkordinal.md)
