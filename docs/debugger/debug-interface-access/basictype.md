---
title: BasicType | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- BasicType enumeration
ms.assetid: 19ae53ba-cd6e-47b6-9f94-27ae663ce955
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 03e82a8c17b33aa085b4ed64b9ba609bee183e1d
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62829738"
---
# <a name="basictype"></a>BasicType
Simgenin temel türünü belirtir.

## <a name="syntax"></a>Sözdizimi

```C++
enum BasicType {
    btNoType   = 0,
    btVoid     = 1,
    btChar     = 2,
    btWChar    = 3,
    btInt      = 6,
    btUInt     = 7,
    btFloat    = 8,
    btBCD      = 9,
    btBool     = 10,
    btLong     = 13,
    btULong    = 14,
    btCurrency = 25,
    btDate     = 26,
    btVariant  = 27,
    btComplex  = 28,
    btBit      = 29,
    btBSTR     = 30,
    btHresult  = 31,
    btChar16   = 32,  // char16_t
    btChar32   = 33,  // char32_t
};
```

## <a name="elements"></a>Öğeleri
btNoType hiçbir temel türü belirtildi.

btVoid temel türü olan bir `void`.

btChar temel türü olan bir `char` (C/C++ türü).

btWChar temel türü olan geniş karakter (Unicode) (`WCHAR`).

btInt temel türü olan `signed int` (C/C++ türü).

btUInt temel türü olan `unsigned int` (C/C++ türü).

btFloat temel türü olan bir kayan noktalı sayı (`FLOAT`).

ikili dosya kodlanmış bir ondalık btBCD temel türü olduğundan (`BCD`).

btBool temel türü olan bir Boole değeri (`BOOL`).

btLong temel türü olan bir `long int` (C/C++ türü).

btULong temel türü olan bir `unsigned long int` (C/C++ türü).

para birimi btCurrency temel birimidir.

btDate temel türü olan tarih/saat (`DATE`).

btVariant temel türü olan bir değişken türü yapısı (`VARIANT`).

btComplex temel türü karmaşık bir sayıdır.

bir bit btBit temel türü.

btBSTR temel türü olan temel ya da ikili bir dize (`BSTR`).

btHresult temel türü olan bir `HRESULT`.

## <a name="remarks"></a>Açıklamalar
Bu sabit listesi değerleri tarafından döndürülen [Idiasymbol::get_basetype](../../debugger/debug-interface-access/idiasymbol-get-basetype.md) yöntemi.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: cvconst.h

## <a name="see-also"></a>Ayrıca Bkz.
- [Enumerations and Structures](../../debugger/debug-interface-access/enumerations-and-structures.md)
- [IDiaSymbol::get_baseType](../../debugger/debug-interface-access/idiasymbol-get-basetype.md)
- [IDiaSymbol::get_length](../../debugger/debug-interface-access/idiasymbol-get-length.md)
