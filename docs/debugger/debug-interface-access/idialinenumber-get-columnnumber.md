---
title: Idialinenumber::get_columnnumber | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaLineNumber::get_columnNumber method
ms.assetid: e317f29a-6525-46a7-8421-33985392f8fd
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 72f01745ff7274719d6a967a50274eb316718c3b
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56632127"
---
# <a name="idialinenumbergetcolumnnumber"></a>IDiaLineNumber::get_columnNumber
İfade veya deyimin başladığı sütun sayısını alır.

## <a name="syntax"></a>Sözdizimi

```
- [C++]
HRESULT get_columnNumber ( 
   DWORD* pRetVal
);
```

#### <a name="parameters"></a>Parametreler
 `pRetVal`

[out] İfade veya deyimin başladığı sütun sayısını döndürür. Değer sıfır ise sütun bilgisi mevcut değil.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`. Döndürür `S_FALSE` varsa bu özelliği desteklenmiyor. Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bu yöntem tarafından döndürülen sütun satırına satırında deyiminin ilk karaktere bir bayt uzaklığı değerdir.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaLineNumber](../../debugger/debug-interface-access/idialinenumber.md)