---
title: Idiaenumtables::Next | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaEnumTables::Next method
ms.assetid: 8d7bd359-d33e-4317-9674-d89283efd7de
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 15a9ebbd3a3993568e4b6496e04661a63290399e
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62832751"
---
# <a name="idiaenumtablesnext"></a>IDiaEnumTables::Next
Belirtilen bir sabit listesi sırası tablolarında sayısını alır.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT Next ( 
   ULONG       celt,
   IDiaTable** rgelt,
   ULONG*      pceltFetched
);
```

#### <a name="parameters"></a>Parametreler
 `celt`

[in] Alınacak Numaralandırıcı tablo sayısı.

 `rgelt`

[out] İle doldurulacak bir dizi [Idiatable](../../debugger/debug-interface-access/idiatable.md) istediğiniz tabloları temsil eden nesneleri.

 `pceltFetched`

[out] Tablo sayısı getirilen bir numaralandırıcı döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`. Döndürür `S_FALSE` daha fazla tablo varsa. Aksi takdirde bir hata kodu döndürür.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaEnumTables](../../debugger/debug-interface-access/idiaenumtables.md)
- [IDiaTable](../../debugger/debug-interface-access/idiatable.md)