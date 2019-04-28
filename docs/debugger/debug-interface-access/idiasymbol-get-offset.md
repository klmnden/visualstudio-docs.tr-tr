---
title: Idiasymbol::get_offset | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSymbol::get_offset method
ms.assetid: 8292bb08-4dc8-4663-beb4-258f5d5a448d
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 0016ca267b3eaf2535896aab1ee58a470a192c9a
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63399447"
---
# <a name="idiasymbolgetoffset"></a>IDiaSymbol::get_offset
Sembol konumunun uzaklığını alır. Şu durumlarda kullanın [LocationType numaralandırması](../../debugger/debug-interface-access/locationtype.md) olduğu `LocIsRegRel` veya `LocIsBitField`.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT get_offset ( 
   LONG* pRetVal
);
```

#### <a name="parameters"></a>Parametreler
 `pRetVal`

[out] Sembol konumunun bayt uzaklığını döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi halde döndürür `S_FALSE` veya bir hata kodu.

> [!NOTE]
> Dönüş değeri `S_FALSE` özelliği simge için kullanılabilir değil anlamına gelir.

## <a name="remarks"></a>Açıklamalar
 Uzaklık daha önceden belirlenen bazı bilinen noktasından dayalıdır. Örneğin, uzaklığı bir `LocIsBitField` konum türü, genellikle kapsayan sınıfı başlangıcından.

## <a name="requirements"></a>Gereksinimler

|Gereksinim|Açıklama|
|-----------------|-----------------|
|Üst bilgi:|dia2.h|
|Sürüm:|DIA SDK v7.0|

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)
- [LocationType Numaralandırması](../../debugger/debug-interface-access/locationtype.md)