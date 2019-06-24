---
title: Idiaenumframedata::Clone | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaEnumFrameData::Clone Method
ms.assetid: 28a17300-1626-422f-a17a-3a4d3872c37c
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: b5c86d9f4f8eb02b0389e7ea28b5858f8576f6c6
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62838408"
---
# <a name="idiaenumframedataclone"></a>IDiaEnumFrameData::Clone
Geçerli Numaralandırıcı aynı numaralandırma duruma içeren bir numaralandırıcı oluşturur.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT Clone( 
   IDiaEnumFrameData** ppenum
);
```

#### <a name="parameters"></a>Parametreler
 ppenum

[out] Döndürür bir [Idiaenumframedata](../../debugger/debug-interface-access/idiaenumframedata.md) Numaralandırıcı bir kopyasını içeren nesne. Yinelenen çerçevenin verileri değil, yalnızca Numaralandırıcı.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaEnumFrameData](../../debugger/debug-interface-access/idiaenumframedata.md)