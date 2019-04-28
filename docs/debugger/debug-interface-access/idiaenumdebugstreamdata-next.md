---
title: Idiaenumdebugstreamdata::Next | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaEnumDebugStreamData::Next method
ms.assetid: 114171dd-38fd-4bd7-a702-8ff887ffc99b
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: cf641fde4c03053496c732aa7904ddcad671af20
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62838613"
---
# <a name="idiaenumdebugstreamdatanext"></a>IDiaEnumDebugStreamData::Next
Belirtilen sayıda numaralandırılan sıralı kayıtları alır.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT Next ( 
   ULONG  celt,
   DWORD  cbData,
   DWORD* pcbData,
   BYTE   data[],
   ULONG* pceltFetched
);
```

#### <a name="parameters"></a>Parametreler
 celt

[in] Alınacak kayıt sayısı.

 cbData

[in] Veri arabelleğin bayt cinsinden boyutu.

 pcbData

[out] Döndürülen bayt sayısını döndürür. Varsa `data` NULL ise `pcbData` tüm kayıtları istenen bayt veri kullanılabilir toplam sayısını içerir.

 veri]

[out] Hata ayıklama akışı kaydı veri ile doldurulacak olan bir arabellek.

 pceltFetched

[out içinde] Kayıt sayısını döndürür `data`.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`. Döndürür `S_FALSE` daha fazla kayıt varsa. Aksi takdirde bir hata kodu döndürür.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaEnumDebugStreamData](../../debugger/debug-interface-access/idiaenumdebugstreamdata.md)
- [IDiaEnumDebugStreams::Next](../../debugger/debug-interface-access/idiaenumdebugstreams-next.md)