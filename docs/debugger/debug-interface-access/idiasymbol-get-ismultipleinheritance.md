---
title: IDiaSymbol::get_isMultipleInheritance | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: 0aa356a1-5c5c-4ee4-8b48-bae0a2610013
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: a353f9fc3605d1f2d26248b3ce907fb76b947c68
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62836622"
---
# <a name="idiasymbolgetismultipleinheritance"></a>IDiaSymbol::get_isMultipleInheritance
Belirtir olup olmadığını `this` işaretçi birden çok devralma ile veri üyesine işaret eder.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT get_isMultipleInheritance(
   BOOL* pRetVal);
```

#### <a name="parameters"></a>Parametreler
 `pRetVal`

[out] Bir işaretçi bir `BOOL` belirtir olup olmadığını `this` işaretçi birden çok devralma ile veri üyesine işaret eder.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi halde döndürür `S_FALSE` veya bir hata kodu.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)