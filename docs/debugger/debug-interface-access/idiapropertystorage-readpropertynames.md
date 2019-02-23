---
title: IDiaPropertyStorage::ReadPropertyNames | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaPropertyStorage::ReadPropertyNames
ms.assetid: f8bcab77-afca-4a8f-8710-697842f8a518
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 7492e0eee0523fd102ecd057d075f2672bf3b25b
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56695849"
---
# <a name="idiapropertystoragereadpropertynames"></a>IDiaPropertyStorage::ReadPropertyNames
Dize adları için karşılık gelen alır, özellik tanımlayıcıları verilir.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT ReadPropertyNames (
   ULONG         cpropid,
   PROPID const* rgpropid,
   BSTR*         rglpwstrName
);
```

#### <a name="parameters"></a>Parametreler
 `cpropid`

[in] Özellik kimlikleri sayısı `rgpropid`.

 `rgpropid`

[in] Adları alınacağı özellik kimlikleri dizisi (`PROPID` WTypes.h tanımlanan bir `ULONG`).

 `rglpwstrName`

[out içinde] Belirtilen özellik kimliklerinin özellik adları dizisi. Dizi istenen sayıda özellik adları tutacak önceden ayrılmış olmalıdır ve en az tutabilecek özellikte `cpropid``BSTR` dizeleri.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Döndürülen özellik adlarının serbest (çağırarak `SysFreeString` işlevi) artık gerektiğinde.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaPropertyStorage](../../debugger/debug-interface-access/idiapropertystorage.md)