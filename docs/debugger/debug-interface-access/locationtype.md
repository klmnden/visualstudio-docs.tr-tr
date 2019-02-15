---
title: LocationType | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- LocationType enumeration
ms.assetid: d3e1eedc-bfd3-4c91-881b-d69565138d0f
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 779df14d01950b90a45764ba9d84760a1448d475
ms.sourcegitcommit: 752f03977f45169585e407ef719450dbe219b7fc
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2019
ms.locfileid: "56318660"
---
# <a name="locationtype"></a>LocationType
Konum bilgilerini bir sembol içinde yer alan türünü gösterir.

## <a name="syntax"></a>Sözdizimi

```C++
enum LocationType {
    LocIsNull,
    LocIsStatic,
    LocIsTLS,
    LocIsRegRel,
    LocIsThisRel,
    LocIsEnregistered,
    LocIsBitField,
    LocIsSlot,
    LocIsIlRel,
    LocInMetaData,
    LocIsConstant,
    LocTypeMax
};
```

## <a name="elements"></a>Öğeleri
`LocIsNull`  
Konum bilgileri kullanılamıyor.

`LocIsStatic`  
Statik konumdur.

`LocIsTLS`  
İş parçacığı yerel depolama alanında konumdur.

`LocIsRegRel`  
Kayıt göreli konumu.

`LocIsThisRel`  
Konum `this`-göreli.

`LocIsEnregistered`  
Bir kayıttaki konumdur.

`LocIsBitField`  
Bir bit alanına konumdur.

`LocIsSlot`  
Bir Microsoft Ara dil (MSIL) yuvası konumdur.

`LocIsIlRel`  
MSIL göreli konumdur.

`LocInMetaData`  
Meta verilerde konumdur.

`LocIsConstant`  
Bir sabit değer konumdur.

`LocTypeMax`  
Bu numaralandırma, konum türleri sayısı.

## <a name="remarks"></a>Açıklamalar
Kullanılabilir özellikler [Idiasymbol](../../debugger/debug-interface-access/idiasymbol.md) sembolün konumu resim dosyası içinde arabirimi bağlıdır. Daha fazla bilgi için [simge konumları](../../debugger/debug-interface-access/symbol-locations.md).

Bu numaralandırma değerleri için yapılan bir çağrı tarafından döndürülen [Idiasymbol::get_locationtype](../../debugger/debug-interface-access/idiasymbol-get-locationtype.md) yöntemi.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: cvconst.h

## <a name="see-also"></a>Ayrıca Bkz.
[Enumerations and Structures](../../debugger/debug-interface-access/enumerations-and-structures.md)  
[IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)  
[IDiaSymbol::get_locationType](../../debugger/debug-interface-access/idiasymbol-get-locationtype.md)  
[Simge Konumları](../../debugger/debug-interface-access/symbol-locations.md)
