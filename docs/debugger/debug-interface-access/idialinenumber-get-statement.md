---
title: Idialinenumber::get_statement | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaLineNumber::get_statement method
ms.assetid: 22b8ee29-79ef-427f-bd05-00d255ab836b
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 397873a65176024327f371e9727b15984cd7d03f
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62828394"
---
# <a name="idialinenumbergetstatement"></a>IDiaLineNumber::get_statement
Bu satır bilgileri bir ifadede, program kaynağı yerine bir deyim başına açıklayan belirten bir bayrak alır.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT get_statement ( 
   BOOL* pRetVal
);
```

#### <a name="parameters"></a>Parametreler
 `pRetVal`

[out] Döndürür `TRUE` bu satır bilgileri program kaynak deyiminde başına tanımlıyorsa.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`. Döndürür `S_FALSE` varsa bu özelliği desteklenmiyor. Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Çok satırlı ifadeleri yayılabilir. Bu yöntem, ilişkili satır numarası gibi bir çok satırlı deyimi başlangıcını işaretleyen olmadığını gösterir.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaLineNumber](../../debugger/debug-interface-access/idialinenumber.md)