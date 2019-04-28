---
title: Idiasession::symsareequiv | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSession::symsAreEquiv method
ms.assetid: 9941d520-e203-46c0-83c3-b3a967f4fc59
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 0253104cf29e86825fadc8c8bd18133e0d3cf593
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62839081"
---
# <a name="idiasessionsymsareequiv"></a>IDiaSession::symsAreEquiv
İki simge eşdeğer olup olmadığını denetler.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT symsAreEquiv ( 
   IDiaSymbol* symbolA,
   IDiaSymbol* symbolB
);
```

#### <a name="parameters"></a>Parametreler
 `symbolA`

[in] İlk [Idiasymbol](../../debugger/debug-interface-access/idiasymbol.md) Karşılaştırmada kullanılan nesne.

 `symbolB`

[in] İkinci `IDiaSymbol` Karşılaştırmada kullanılan nesne.

## <a name="return-value"></a>Dönüş Değeri
 Simgeleri eşdeğer ise döndürür `S_OK`; Aksi halde döndürür `S_FALSE`, simgeler eşdeğer değildir. Aksi takdirde bir hata kodunu döndürür.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaSession](../../debugger/debug-interface-access/idiasession.md)
- [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)