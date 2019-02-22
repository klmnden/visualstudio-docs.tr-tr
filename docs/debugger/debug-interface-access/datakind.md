---
title: DataKind | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- DataKind enumeration
ms.assetid: b64be708-22d6-4360-99e7-8f4e6b196de7
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 21630bea3022769d18748190c2a2d24c0e519a3c
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56608506"
---
# <a name="datakind"></a>DataKind
Veri değeri belirli kapsamını belirtir.

## <a name="syntax"></a>Sözdizimi

```C++
enum DataKind {
    DataIsUnknown,
    DataIsLocal,
    DataIsStaticLocal,
    DataIsParam,
    DataIsObjectPtr,
    DataIsFileStatic,
    DataIsGlobal,
    DataIsMember,
    DataIsStaticMember,
    DataIsConstant
};
```

## <a name="elements"></a>Öğeleri
DataIsUnknown veri sembol belirlenemiyor.

Yerel bir değişken DataIsLocal veri öğesidir.

Statik bir yerel değişken DataIsStaticLocal veri öğesidir.

Biçimsel parametre DataIsParam veri öğesidir.

DataIsObjectPtr veri öğesi olan bir nesne işaretçisi (`this`).

DataIsFileStatic veri öğesi dosya kapsamlı bir değişkendir.

DataIsGlobal veri öğesi genel bir değişkendir.

Bir nesne üye değişkeni DataIsMember veri öğesidir.

Bir sınıfın statik değişken DataIsStaticMember veri öğesidir.

DataIsConstant veri öğesi, bir sabit değerdir.

## <a name="remarks"></a>Açıklamalar
Bu sabit listesi değerleri tarafından döndürülen [Idiasymbol::get_datakind](../../debugger/debug-interface-access/idiasymbol-get-datakind.md) yöntemi.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: cvconst.h

## <a name="see-also"></a>Ayrıca Bkz.
- [Enumerations and Structures](../../debugger/debug-interface-access/enumerations-and-structures.md)
- [IDiaSymbol::get_dataKind](../../debugger/debug-interface-access/idiasymbol-get-datakind.md)
