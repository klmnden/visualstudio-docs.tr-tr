---
title: Idiasymbol::get_thunkordinal | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSymbol::get_thunkOrdinal method
ms.assetid: 4b28d78a-1974-4d8a-8bb7-781bf630f2f4
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 6dadfff62502af59652e9113553e13b4942c540f
ms.sourcegitcommit: 75807551ea14c5a37aa07dd93a170b02fc67bc8c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/12/2019
ms.locfileid: "64822636"
---
# <a name="idiasymbolgetthunkordinal"></a>IDiaSymbol::get_thunkOrdinal
Bir işlev dönüştürücü türünü alır.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT get_thunkOrdinal ( 
   DWORD* pRetVal
);
```

#### <a name="parameters"></a>Parametreler
 `pRetVal`

[out] Bir değer döndürür [thunk_ordınal numaralandırması](../../debugger/debug-interface-access/thunk-ordinal.md) bir işlev dönüştürücü türünü belirten sabit listesi.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi halde döndürür `S_FALSE` veya bir hata kodu.

> [!NOTE]
> Dönüş değeri `S_FALSE` özelliği simge için kullanılabilir değil anlamına gelir.

## <a name="remarks"></a>Açıklamalar
 Bu özellik geçerli yalnızca simgesi olarak bir [SymTagEnum numaralandırması](../../debugger/debug-interface-access/symtagenum.md) değerini `SymTagThunk`.

 Bir "dönüştürücü" dönüştürür (segmentlere ayrılmış adres alanı olarak da bilinir) bir 16 bit adres alanı ile bir 32-bit bellek adres alanı (düz adres alanı olarak da bilinir) arasındaki kod parçasıdır.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)
- [THUNK_ORDINAL Numaralandırması](../../debugger/debug-interface-access/thunk-ordinal.md)
- [SymTagEnum Numaralandırması](../../debugger/debug-interface-access/symtagenum.md)