---
title: Idiaenumtables::Skip | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaEnumTables::Skip method
ms.assetid: 5c9db956-0654-4f1a-8775-530aa980d8ec
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 24232878452082dd1769c9bc9f1cd22d081968f2
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62832699"
---
# <a name="idiaenumtablesskip"></a>IDiaEnumTables::Skip
Bir numaralandırma sıralı tablolarda belirtilen sayıda atlar.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT Skip ( 
   ULONG celt
);
```

#### <a name="parameters"></a>Parametreler
 `celt`

[in] Atlamak için sabit listesi sırası tablo sayısı.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi halde döndürür `S_FALSE` atlamak için daha fazla tablo varsa.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaEnumTables](../../debugger/debug-interface-access/idiaenumtables.md)