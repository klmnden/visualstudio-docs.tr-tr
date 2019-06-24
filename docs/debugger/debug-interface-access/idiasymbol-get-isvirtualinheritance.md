---
title: IDiaSymbol::get_isVirtualInheritance | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: 72906b92-dd4a-42e3-9b24-b77628fa48c1
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: f5d1630b46ca2203e9f935517e96b11856b273b9
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62842130"
---
# <a name="idiasymbolgetisvirtualinheritance"></a>IDiaSymbol::get_isVirtualInheritance
Belirtir olup olmadığını `this` işaretçi sanal devralma ile veri üyesine işaret eder.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT get_isVirtualInheritance(
   BOOL* pRetVal);
```

#### <a name="parameters"></a>Parametreler
 `pRetVal`

[out] Bir işaretçi bir `BOOL` belirtir olup olmadığını `this` işaretçi sanal devralma ile veri üyesine işaret eder.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi halde döndürür `S_FALSE` veya bir hata kodu.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)