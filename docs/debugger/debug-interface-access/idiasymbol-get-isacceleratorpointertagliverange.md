---
title: IDiaSymbol::get_isAcceleratorPointerTagLiveRange | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: d195aec4-6d3c-42e0-88a5-3d463539f0b8
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: c8bf20f43fcc8da48a6e1ec1dfd0f65b14f8ad86
ms.sourcegitcommit: 75807551ea14c5a37aa07dd93a170b02fc67bc8c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/12/2019
ms.locfileid: "62836908"
---
# <a name="idiasymbolgetisacceleratorpointertagliverange"></a>IDiaSymbol::get_isAcceleratorPointerTagLiveRange
Sembol için karşılık gelen olup olmadığını gösteren bir bayrak alır *tanımı aralığı sembol* bir C++ AMP Hızlandırıcısı için derlenmiş kodda bir işaretçi değişkeninin etiketi bileşeni. Tanımı aralığı sembol adres aralığı için bir değişken konumudur.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT get_isAcceleratorPointerTagLiveRange(
   BOOL* pFlag);
```

#### <a name="parameters"></a>Parametreler
 `pFlag`

[out] Bir işaretçi bir `BOOL` sembol tanımı aralığı sembole karşılık gelen olup olmadığını gösterir.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi halde döndürür `S_FALSE` veya bir hata kodu.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)