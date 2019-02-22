---
title: IDiaPropertyStorage::ReadBSTR | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaPropertyStorage::ReadBSTR
ms.assetid: 7214643b-3286-48ed-90aa-0fe95b4cae5b
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: f0bff81499fe8ea66ce5d4f50616adfec44d3002
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56610963"
---
# <a name="idiapropertystoragereadbstr"></a>IDiaPropertyStorage::ReadBSTR
Okur `BSTR` değerlerde özellik kümesi.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT ReadBSTR ( 
   PROPID id,
   BSTR*  pValue
);
```

#### <a name="parameters"></a>Parametreler
 `id`

[in] Okunacak özellik tanımlayıcısı (`PROPID` WTypes.h tanımlanan bir `ULONG`).

 `pValue`

[out] Özellik değeri döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür. Döndürür `E_INVALIDARG` özelliği türü değilse `BSTR`.

## <a name="remarks"></a>Açıklamalar
 A `BSTR` Windows geniş karakter sıfır ile sonlandırılmış dize olarak tanımlanır.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaPropertyStorage](../../debugger/debug-interface-access/idiapropertystorage.md)