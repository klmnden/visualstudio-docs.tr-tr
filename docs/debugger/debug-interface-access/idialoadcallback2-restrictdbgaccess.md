---
title: Idialoadcallback2::restrictdbgaccess | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaLoadCallback2::RestrictDBGAccess method
ms.assetid: 63b67a93-2910-4fff-aa70-6b2eaa08e5c8
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 24317ff7a79815e5af2306b09cc8d2aa3bfdde0d
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62832692"
---
# <a name="idialoadcallback2restrictdbgaccess"></a>IDiaLoadCallback2::RestrictDBGAccess
Hata ayıklama ile ilgili bilgi arayan .dbg dosyaları izin verilip verilmediğini belirler.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT RestrictDBGAccess();
```

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Herhangi bir başka değer dönüş `S_OK` hata ayıklama bilgileri .dbg dosyaları aranıyor önlemek için.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaLoadCallback2](../../debugger/debug-interface-access/idialoadcallback2.md)