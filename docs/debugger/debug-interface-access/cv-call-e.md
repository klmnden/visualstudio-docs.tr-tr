---
title: CV_call_e | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- CV_call_e enumeration
ms.assetid: f230560b-4243-432d-8f19-46df112043b9
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: ec5fea99994b891250dad85cfc43320848df98f9
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62555110"
---
# <a name="cvcalle"></a>CV_call_e
Bir işlev çağırma kuralını belirtir.

> [!NOTE]
> En yaygın numaralandırma değerlerinden yalnızca aşağıda belirtilmiştir. Tam numaralandırma cvconst.h üstbilgi dosyasında kullanılabilir.

## <a name="syntax"></a>Sözdizimi

```C++
typedef enum CV_call_e {
    CV_CALL_NEAR_C    = 0x00,
    CV_CALL_NEAR_FAST = 0x04,
    CV_CALL_NEAR_STD  = 0x07,
    CV_CALL_NEAR_SYS  = 0x09,
    CV_CALL_THISCALL  = 0x0b,
    CV_CALL_CLRCALL   = 0x16
} CV_call_e;
```

## <a name="elements"></a>Öğeleri
CV_CALL_NEAR_C yakın sağdan sola push kullanarak bir işlev çağırma kuralını belirtir. Çağıran işlev, yığını temizler.

CV_CALL_NEAR_FAST belirtir, bir yakın soldan sağa itme ile kullanarak bir işlev çağırma kuralı kaydeder. Çağrılan işlev parametresi baytların toplamından yığın temizlemek için kullanır.

CV_CALL_NEAR_STD yakın standart çağrısı (sağdan sola anında iletme) kullanarak bir işlev çağırma kuralını belirtir.

CV_CALL_NEAR_SYS belirtir, yakın bir sistemi kullanarak bir işlev-çağrı kuralı çağırın.

CV_CALL_THISCALL belirtir kullanarak bir işlev çağırma kuralı `this` çağırın (`this` işaretçi geçirildi kayıttaki).

CV_CALL_CLRCALL ortak dil çalışma zamanı (CLR tarafından) (çağırma kuralı olarak da bilinen bir yönetilen kod için) kullanılan bir işlevi çağırma kuralını belirtir.

## <a name="remarks"></a>Açıklamalar
Bu numaralandırma değerleri için yapılan bir çağrı tarafından döndürülen [Idiasymbol::get_callingconvention](../../debugger/debug-interface-access/idiasymbol-get-callingconvention.md) yöntemi.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: cvconst.h

## <a name="see-also"></a>Ayrıca Bkz.
- [Enumerations and Structures](../../debugger/debug-interface-access/enumerations-and-structures.md)
- [IDiaSymbol::get_callingConvention](../../debugger/debug-interface-access/idiasymbol-get-callingconvention.md)
