---
title: Idiaframedata::get_functionparent | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaFrameData::get_functionParent method
ms.assetid: f00b9ab1-d4da-4818-973a-58f8f0e66769
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 20f9dac750f9ff9723e4f3669f9e9a124d728a9a
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62830350"
---
# <a name="idiaframedatagetfunctionparent"></a>IDiaFrameData::get_functionParent
Kapsayan işlevin bir çerçeve veri arabirimi alır.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT get_functionParent ( 
   IDiaFrameData** pRetVal
);
```

#### <a name="parameters"></a>Parametreler
 `pRetVal`

[out] Döndürür bir [Idiaframedata](../../debugger/debug-interface-access/idiaframedata.md) kapsayan işlev nesnesi.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaFrameData](../../debugger/debug-interface-access/idiaframedata.md)