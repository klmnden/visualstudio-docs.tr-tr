---
title: Idiasourcefile::get_uniqueıd | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSourceFile::get_uniqueId method
ms.assetid: e0b8dbc0-6061-4f31-bead-2cd72be44e41
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: c4a204e04c1c99dcbe8c6ba6d5e3457ca875dde4
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62832259"
---
# <a name="idiasourcefilegetuniqueid"></a>IDiaSourceFile::get_uniqueId
Bu görüntü için benzersiz olan bir basit tamsayı anahtar değeri alır.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT get_uniqueId ( 
   DWORD* pRetVal
);
```

#### <a name="parameters"></a>Parametreler
 `pRetVal`

[out] Bu görüntü için benzersiz olan bir basit tamsayı anahtar değeri döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Dizeleri satır numarası işleme hızlandırabilir yerine anahtarları karşılaştırma.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaSourceFile](../../debugger/debug-interface-access/idiasourcefile.md)