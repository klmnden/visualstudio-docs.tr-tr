---
title: Idiasymbol::get_localbasepointerregisterıd | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSymbol::get_localBasePointerRegisterId method
ms.assetid: 9cbcaf00-9ace-45e1-b164-7a9439e08083
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: f2c556d67ca8823ce54da19de51c934181465807
ms.sourcegitcommit: 75807551ea14c5a37aa07dd93a170b02fc67bc8c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/12/2019
ms.locfileid: "64803581"
---
# <a name="idiasymbolgetlocalbasepointerregisterid"></a>IDiaSymbol::get_localBasePointerRegisterId
Yerel değişkenler yığında için temel bir işaretçi tutan kayıt Kimliğini alır. Şu durumlarda kullanın [SymTagEnum numaralandırması](../../debugger/debug-interface-access/symtagenum.md) ayarlanır `SymTagFunction`.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT get_localBasePointerRegisterId ( 
   DWORD* pRetVal
);
```

#### <a name="parameters"></a>Parametreler
 `pRetVal`

[out] Yerel değişkenler yığında için temel bir işaretçi tutan kayıt Kimliğini döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi halde döndürür `S_FALSE` veya bir hata kodu.

> [!NOTE]
> Dönüş değeri `S_FALSE` özelliği simge için kullanılabilir değil anlamına gelir.

## <a name="remarks"></a>Açıklamalar

## <a name="requirements"></a>Gereksinimler
 Üst bilgi: dia2.h

 Kitaplık: diaguids.lib

 DLL: msdia100.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)