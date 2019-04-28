---
title: Idialinenumber::get_addresssection | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaLineNumber::get_addressSection method
ms.assetid: a01c1bae-04b2-4c30-8621-60939a3124c2
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 56a79ea8ba7c4e5622ee468cec8fe6cb53dd197c
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62839868"
---
# <a name="idialinenumbergetaddresssection"></a>IDiaLineNumber::get_addressSection
Bir blok başladığı bellek adresi bölüm parçası alır.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT get_addressSection ( 
   DWORD* pRetVal
);
```

#### <a name="parameters"></a>Parametreler
 pRetVal

[out] Bir blok başladığı bellek adresi bölüm bölümünü döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`. Döndürür `S_FALSE` varsa bu özelliği desteklenmiyor. Aksi takdirde bir hata kodu döndürür.

## <a name="example"></a>Örnek

```C++
CComPtr< IDiaLineNumber > pLine;
DWORD seg;
pLine->get_addressSection( &seg );
```

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaLineNumber](../../debugger/debug-interface-access/idialinenumber.md)
- [IDiaLineNumber::get_addressOffset](../../debugger/debug-interface-access/idialinenumber-get-addressoffset.md)