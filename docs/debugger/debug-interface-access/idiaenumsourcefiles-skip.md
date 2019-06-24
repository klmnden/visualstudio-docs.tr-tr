---
title: Idiaenumsourcefiles::Skip | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaEnumSourceFiles::Skip method
ms.assetid: 4821e6dd-d33f-403d-857d-e3ae81e4a9e3
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: b80a2a0f270ccd76d052d4c7863170448648e138
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62833369"
---
# <a name="idiaenumsourcefilesskip"></a>IDiaEnumSourceFiles::Skip
Bir numaralandırma sıralı kaynak dosyalarında belirtilen sayıda atlar.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT Skip ( 
   ULONG celt
);
```

#### <a name="parameters"></a>Parametreler
 celt

[in] Sabit listesi sırası atlamak için kaynak dosya sayısı.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi halde döndürür `S_FALSE` atlamak için daha fazla kaynak dosya yoksa.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaEnumSourceFiles](../../debugger/debug-interface-access/idiaenumsourcefiles.md)