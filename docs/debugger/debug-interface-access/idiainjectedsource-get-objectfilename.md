---
title: Idiaınjectedsource::get_objectfilename | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaInjectedSource::get_objectFilename method
ms.assetid: 7c42847a-f0df-443a-a9fe-c495c1271ea8
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 4bf9b325354bd95678969e5d1db4c13370d6d8b3
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62839894"
---
# <a name="idiainjectedsourcegetobjectfilename"></a>IDiaInjectedSource::get_objectFilename
Kaynak için derlenen nesne dosyası adını alır.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT get_objectFilename ( 
   BSTR* pRetVal
);
```

#### <a name="parameters"></a>Parametreler
 `pRetVal`

[out] Kaynak için derlenen nesne dosyası adını döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`. Döndürür `S_FALSE` varsa bu özelliği desteklenmiyor. Aksi takdirde bir hata kodu döndürür.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaInjectedSource](../../debugger/debug-interface-access/idiainjectedsource.md)