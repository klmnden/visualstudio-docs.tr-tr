---
title: IDiaPropertyStorage::ReadDWORD | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaPropertyStorage::ReadDWORD
ms.assetid: 5f4c034e-a9d3-4560-94b5-ede524741439
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 5b4709a218f6586320e96f79ea8a9f423f537c7f
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62839660"
---
# <a name="idiapropertystoragereaddword"></a>IDiaPropertyStorage::ReadDWORD
Okur `DWORD` değerlerde özellik kümesi.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT ReadDWORD ( 
   PROPID id,
   DWORD* pValue
);
```

#### <a name="parameters"></a>Parametreler
 `id`

[in] Okunacak özellik tanımlayıcısı (`PROPID` WTypes.h tanımlanan bir `ULONG`).

 `pValue`

[out] Özellik değeri döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür. Döndürür `E_INVALIDARG` özelliği türü değilse `DWORD`.

## <a name="remarks"></a>Açıklamalar
 A `DWORD` Windows 32-bit işaretsiz tamsayı olarak tanımlanır.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaPropertyStorage](../../debugger/debug-interface-access/idiapropertystorage.md)