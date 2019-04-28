---
title: Idiaenumframedata::Item | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaEnumFrameData::Item method
ms.assetid: 2761a72d-1868-4f5b-a32e-c2a1d9358c91
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: a8d083cea518032c121a5cb9e9213abbbd7eaaf8
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62829865"
---
# <a name="idiaenumframedataitem"></a>IDiaEnumFrameData::Item
Bir dizini yoluyla bir çerçeve veri öğesi alır.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT Item ( 
   DWORD           index,
   IDiaFrameData** section
);
```

#### <a name="parameters"></a>Parametreler
 dizin

[in] Dizin [Idiaframedata](../../debugger/debug-interface-access/idiaframedata.md) alınacak nesne. İçin 0 aralığındaki dizinidir `count`-1, burada `count` tarafından döndürülen [Idiaenumframedata::get_Count](../../debugger/debug-interface-access/idiaenumframedata-get-count.md) yöntemi.

 section

[out] Döndürür bir [Idiaframedata](../../debugger/debug-interface-access/idiaframedata.md) istenen çerçeve veri öğesini temsil eden nesne.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaEnumFrameData](../../debugger/debug-interface-access/idiaenumframedata.md)
- [IDiaFrameData](../../debugger/debug-interface-access/idiaframedata.md)