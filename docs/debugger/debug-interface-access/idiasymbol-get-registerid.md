---
title: Idiasymbol::get_registerıd | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSymbol::get_registerId method
ms.assetid: f881e793-eb9e-48dc-a847-dd61d77174fc
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 3e2b1cbb6837ca139e735bef17bc0c2712d9cae7
ms.sourcegitcommit: 75807551ea14c5a37aa07dd93a170b02fc67bc8c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/12/2019
ms.locfileid: "64786580"
---
# <a name="idiasymbolgetregisterid"></a>IDiaSymbol::get_registerId
Kayıt gösterge konumunun alır, [LocationType numaralandırması](../../debugger/debug-interface-access/locationtype.md) ayarlanır `LocIsEnregistered`.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT get_registerId ( 
   DWORD* pRetVal
);
```

#### <a name="parameters"></a>Parametreler
 `pRetVal`

[out] Kayıt gösterge konumunun döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi halde döndürür `S_FALSE` veya bir hata kodu.

> [!NOTE]
> Dönüş değeri `S_FALSE` özelliği simge için mevcut olmadığı anlamına gelir.

## <a name="remarks"></a>Açıklamalar
 Simge bir kayıt göre diğer bir deyişle, ise, sembolün [LocationType numaralandırması](../../debugger/debug-interface-access/locationtype.md) ayarlanır `LocIsRegRel`, kullanın `get_registerId` yöntemine bir çağrı tarafından izlenen [Idiasymbol::get_offset](../../debugger/debug-interface-access/idiasymbol-get-offset.md) uzaklık simgenin bulunduğu kasadan almak için yöntemi.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)
- [LocationType Numaralandırması](../../debugger/debug-interface-access/locationtype.md)