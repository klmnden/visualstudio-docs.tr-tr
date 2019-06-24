---
title: Idialoadcallback::notifyopenpdb | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaLoadCallback::NotifyOpenPDB method
ms.assetid: c0547f99-8468-4e57-82ca-9ef7d6707c8a
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: e5945ba54f1c09f4f13d2a982e90a3bb58cfb5f9
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62839764"
---
# <a name="idialoadcallbacknotifyopenpdb"></a>IDiaLoadCallback::NotifyOpenPDB
Bir aday .pdb dosyası açıldığında çağrılır.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT NotifyOpenPDB ( 
   LPCOLESTR pdbPath,
   HRESULT   resultCode
);
```

#### <a name="parameters"></a>Parametreler
 `pdbPath`

[in] .Pdb dosyasının tam yolu.

 `resultCode`

[in] Başarıyı gösteren kod (`S_OK`) veya bu dosyaya uygulanan yük hatası.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür. Dönüş kodu genellikle göz ardı edilir.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaLoadCallback2](../../debugger/debug-interface-access/idialoadcallback2.md)