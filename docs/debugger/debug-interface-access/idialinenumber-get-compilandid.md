---
title: Idialinenumber::get_compilandıd | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaLineNumber::get_compilandId method
ms.assetid: 2cd6f551-8091-47c7-803f-3f79a766a211
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 9874dec57c873164ec1875f31fd15c817781bb7a
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62839933"
---
# <a name="idialinenumbergetcompilandid"></a>IDiaLineNumber::get_compilandId
Bu satırı katkıda derlenecek için benzersiz bir tanımlayıcı alır.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT get_compilandId ( 
   DWORD* pRetVal
);
```

#### <a name="parameters"></a>Parametreler
 `pRetVal`

[out] Döndürür `DWORD` bu satırı katkıda derlenecek için benzersiz tanımlayıcısını içermektedir.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`. Döndürür `S_FALSE` varsa bu özelliği desteklenmiyor. Aksi takdirde bir hata kodu döndürür.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaLineNumber](../../debugger/debug-interface-access/idialinenumber.md)