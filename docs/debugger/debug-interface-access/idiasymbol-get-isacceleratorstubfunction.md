---
title: IDiaSymbol::get_isAcceleratorStubFunction | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: cc4ea375-76f6-4ba8-baed-c5fa82108137
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: bbcfbfcd1e95a45388d0b7c0626f1cd529607ce4
ms.sourcegitcommit: 75807551ea14c5a37aa07dd93a170b02fc67bc8c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/12/2019
ms.locfileid: "62836635"
---
# <a name="idiasymbolgetisacceleratorstubfunction"></a>IDiaSymbol::get_isAcceleratorStubFunction
Sembol üst düzey işlev sembole karşılık gelen bir Hızlandırıcı için derlenmiş gölgelendirici için karşılık gelen olup olmadığını gösteren bir `parallel_for_each` çağırın.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT get_isAcceleratorStubFunction(
   BOOL* pFlag);
```

#### <a name="parameters"></a>Parametreler
 `pFlag`

[out] Bir işaretçi bir `BOOL` sembol üst düzey işlev sembole karşılık gelen bir Hızlandırıcı için derlenmiş gölgelendirici için karşılık gelen olmadığını bildiren bir `parallel_for_each` çağırın.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi halde döndürür `S_FALSE` veya bir hata kodu.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)