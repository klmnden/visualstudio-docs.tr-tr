---
title: Idiaaddressmap::set_addressmap | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaAddressMap::set_addressMap method
ms.assetid: 81e82073-089b-43d5-af39-49d7a4907c7a
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 963ee64b639780bae60a4c2655db8b666d87c702
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62554254"
---
# <a name="idiaaddressmapsetaddressmap"></a>IDiaAddressMap::set_addressMap
Görüntü düzen çevirileri desteklemek için bir adres Haritası sağlar.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT set_addressMap ( 
   DWORD                     cbData,
   struct DiaAddressMapEntry data[],
   BOOL                      imagetoSymbols
);
```

#### <a name="parameters"></a>Parametreler
 `cbData`

[in] İçindeki öğelerin sayısını `data` parametresi.

 `data[]`

[in] Bir dizi [DiaAddressMapEntry yapısı](../../debugger/debug-interface-access/diaaddressmapentry.md) çevirisi eşlemesini tanımlayan yapılar.

 `imagetoSymbols`

[in] `TRUE` varsa `data` parametre (hata ayıklama sembolleri tarafından açıklandığı gibi) yeni görüntü düzen bir eşlemden özgün düzene tanımlar. `FALSE` varsa `data` özgün düzenden yapılan yeni görüntü düzen haritasıdır.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Genellikle, DIA adres çevirisi haritalar program veritabanı (.pdb) dosyasından alır. Bu değerleri eksikse [Idiaaddressmap::set_imageheaders](../../debugger/debug-interface-access/idiaaddressmap-set-imageheaders.md) yöntemi iki kez çağrılır kez `imagetoSymbols` parametresini `TRUE` ve bir kez `imagetoSymbols` parametresini `FALSE`. Adres eşlemesi çevirileri kullanarak etkinleştirilemez [Idiaaddressmap::put_addressmapenabled](../../debugger/debug-interface-access/idiaaddressmap-put-addressmapenabled.md) yöntemi sürece her iki çeviri haritalar sağlanır.

## <a name="see-also"></a>Ayrıca Bkz.
- [DiaAddressMapEntry Yapısı](../../debugger/debug-interface-access/diaaddressmapentry.md)
- [IDiaAddressMap](../../debugger/debug-interface-access/idiaaddressmap.md)
- [IDiaAddressMap::put_addressMapEnabled](../../debugger/debug-interface-access/idiaaddressmap-put-addressmapenabled.md)
- [IDiaAddressMap::set_imageHeaders](../../debugger/debug-interface-access/idiaaddressmap-set-imageheaders.md)