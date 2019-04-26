---
title: Idiaframedata::get_lengthprolog | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaFrameData::get_lengthProlog method
ms.assetid: 5f042ff1-e74e-430a-be34-d2cf1b18eff2
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 1542435d38f4b528c52ecc648ad6ef8f79378bd5
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62552565"
---
# <a name="idiaframedatagetlengthprolog"></a>IDiaFrameData::get_lengthProlog
Bloğu içindeki kod prolog bayt sayısını alır.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT get_lengthProlog ( 
   DWORD* pRetVal
);
```

#### <a name="parameters"></a>Parametreler
 `pRetVal`

[out] Prolog kodunun bayt sayısını döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`. Döndürür `S_FALSE` varsa bu özelliği desteklenmiyor. Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Yazmaçları korur, CPU durumu ayarlar ve işlev için yığını kurar bir dizi yönergeleri prolog kodudur.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaFrameData](../../debugger/debug-interface-access/idiaframedata.md)