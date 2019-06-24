---
title: Idiasectioncontrib::get_notpaged | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSectionContrib::get_notPaged method
ms.assetid: bb6baa40-fece-4a4c-aba9-f4b41f418f8b
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 1fb132b4cf36eb686424e0f756ffe0387a432eb0
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62827642"
---
# <a name="idiasectioncontribgetnotpaged"></a>IDiaSectionContrib::get_notPaged
Bölüm bellek yetersiz disk belleğine alınacak olamaz olup olmadığını gösteren bir bayrak alır.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT get_notPaged ( 
   BOOL* pRetVal
);
```

#### <a name="parameters"></a>Parametreler
 `pRetVal`
- [out, retval] Döndürür `TRUE` bölümü havuzda aşımına uğramazsa döndürür `FALSE`.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`. Döndürür `S_FALSE` varsa bu özelliği desteklenmiyor. Aksi takdirde bir hata kodu döndürür.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaSectionContrib](../../debugger/debug-interface-access/idiasectioncontrib.md)