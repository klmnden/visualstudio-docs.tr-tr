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
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: bb8765f6671914d145600be925cacadc87d51387
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53859808"
---
# <a name="locationtype"></a>LocationType
Konum bilgilerini bir sembol içinde yer alan türünü gösterir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
enum LocationType {   
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
 [Sabit listeleri ve yapıları](../../debugger/debug-interface-access/enumerations-and-structures.md)   
 [Idiasymbol](../../debugger/debug-interface-access/idiasymbol.md)   
 [Idiasymbol::get_locationtype](../../debugger/debug-interface-access/idiasymbol-get-locationtype.md)   
 [Simge Konumları](../../debugger/debug-interface-access/symbol-locations.md)