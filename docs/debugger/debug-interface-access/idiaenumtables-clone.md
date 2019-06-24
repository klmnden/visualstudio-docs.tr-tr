---
title: Idiaenumtables::Clone | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaEnumTables::Clone method
ms.assetid: beb21109-b12c-44d8-8c1f-a332216b3713
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 2f9fc227983818aa1d1c91e147a5dce650844ad8
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62832831"
---
# <a name="idiaenumtablesclone"></a>IDiaEnumTables::Clone
Geçerli Numaralandırıcı aynı numaralandırma duruma içeren bir numaralandırıcı oluşturur.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT Clone ( 
   IDiaEnumTables** ppenum
);
```

#### <a name="parameters"></a>Parametreler
 `ppenum`

[out] Döndürür bir [Idiaenumtables](../../debugger/debug-interface-access/idiaenumtables.md) Numaralandırıcı bir kopyasını içeren nesne. Tabloları çoğaltılmadığından, numaralandırıcı.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaEnumTables](../../debugger/debug-interface-access/idiaenumtables.md)