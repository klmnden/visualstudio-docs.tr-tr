---
title: IDiaPropertyStorage::ReadULONGLONG | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaPropertyStorage::ReadULONGLONG
ms.assetid: f80a2e24-5744-4fec-bab0-3ed51aef6e58
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: f365578aba73ed94bdcd1d87801fc53030cfecdb
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56616020"
---
# <a name="idiapropertystoragereadulonglong"></a>IDiaPropertyStorage::ReadULONGLONG
Okur `ULONGLONG` değerlerde özellik kümesi.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT ReadULONGLONG ( 
   PROPID     id,
   ULONGLONG* pValue
);
```

#### <a name="parameters"></a>Parametreler
 `id`

[in] Okunacak özellik tanımlayıcısı (`PROPID` WTypes.h tanımlanan bir `ULONG`).

 `pValue`

[out] Özellik değeri döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür. Döndürür `E_INVALIDARG` özelliği türü değilse `ULONGLONG`.

## <a name="remarks"></a>Açıklamalar
 A `ULONGLONG` Windows 64-bit işaretsiz tamsayı olarak tanımlanır.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaPropertyStorage](../../debugger/debug-interface-access/idiapropertystorage.md)