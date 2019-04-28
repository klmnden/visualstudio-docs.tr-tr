---
title: Idiasectioncontrib::get_code16bit | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSectionContrib::get_code16bit method
ms.assetid: 8cde8fc5-9546-4f82-b4a8-afd0d835039e
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: d4e9c190108cdbf1eb7be2d21927a95fe56fca75
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62832476"
---
# <a name="idiasectioncontribgetcode16bit"></a>IDiaSectionContrib::get_code16bit
Bölüm 16-bit kod içerip içermediğini gösteren bir bayrak alır.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT get_code16bit(
   BOOL *pRetVal
};
```

#### <a name="parameters"></a>Parametreler
 `pRetVal`

[out] Döndürür `TRUE` kod bölümünde ise 16-bit; Aksi halde döndürür `FALSE`.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bu yöntem, yalnızca kod 16-bit olup olmadığını gösterir. Kodu 16-bit ise, 32 bit veya 64-bit kod gibi başka bir şey olabilir.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaSectionContrib](../../debugger/debug-interface-access/idiasectioncontrib.md)