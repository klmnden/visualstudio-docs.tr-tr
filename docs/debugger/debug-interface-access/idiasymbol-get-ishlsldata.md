---
title: IDiaSymbol::get_isHLSLData | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: 4662058b-c505-4ccf-ae03-739a62c814ca
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 03b0bf45d4b8100f4ebfd1d6a61dc73547312fe6
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62836709"
---
# <a name="idiasymbolgetishlsldata"></a>IDiaSymbol::get_isHLSLData
Bu sembol üst düzey gölgelendirici dili (HLSL) veri temsil edip etmediğini belirtir.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT get_isHLSLData(
   BOOL* pRetVal);
```

#### <a name="parameters"></a>Parametreler
 `pRetVal`

[out] Bir işaretçi bir `BOOL` bu sembol HLSL veri temsil edip etmediğini belirtir.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi halde döndürür `S_FALSE` veya bir hata kodu.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)