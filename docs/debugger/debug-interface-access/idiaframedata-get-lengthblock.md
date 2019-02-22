---
title: Idiaframedata::get_lengthblock | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaFrameData::get_lengthBlock method
ms.assetid: 2e54deb7-7744-428e-913c-1d47a2aa89b0
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 468e3bee84c7312def06c32cb411c00526ba3b1d
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56619166"
---
# <a name="idiaframedatagetlengthblock"></a>IDiaFrameData::get_lengthBlock
Çerçeve tarafından açıklanan bir kod bloğunu bayt cinsinden uzunluğunu alır.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT get_lengthBlock ( 
   DWORD* pRetVal
);
```

#### <a name="parameters"></a>Parametreler
 `pRetVal`

[out] Çerçevede kodunun bayt sayısını döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`. Döndürür `S_FALSE` varsa bu özelliği desteklenmiyor. Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bu yöntem tarafından döndürülen değer, genellikle bir programı dizenin yorumu kullanılır (bkz [Idiaframedata::get_program](../../debugger/debug-interface-access/idiaframedata-get-program.md) yöntemi bir program dize tanımı için).

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaFrameData](../../debugger/debug-interface-access/idiaframedata.md)
- [IDiaFrameData::get_program](../../debugger/debug-interface-access/idiaframedata-get-program.md)