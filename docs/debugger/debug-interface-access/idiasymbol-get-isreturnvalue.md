---
title: IDiaSymbol::get_isReturnValue | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: 37aaf48a-65cb-4ec2-823e-1c637a9f939c
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 14ae065f16c2d047311308d63da7680a61fa22ad
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62836474"
---
# <a name="idiasymbolgetisreturnvalue"></a>IDiaSymbol::get_isReturnValue
Değişkeni dönüş değeri taşıyan olup olmadığını belirtir.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT get_isReturnValue(
   BOOL* pRetVal);
```

#### <a name="parameters"></a>Parametreler
 `pRetVal`

[out] Bir işaretçi bir `BOOL` değişkeni dönüş değeri taşıyan olup olmadığını belirtir.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi halde döndürür `S_FALSE` veya bir hata kodu.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)