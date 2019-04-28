---
title: Idiasymbol::get_upperbound | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSymbol::get_upperBound method
ms.assetid: a77dcafa-ea3f-45da-826d-8f9b4489a03f
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 4a25db69ac60fcc045637b797a4be3c45a4147cf
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63400601"
---
# <a name="idiasymbolgetupperbound"></a>IDiaSymbol::get_upperBound
FORTRAN dizi boyutu üst sınırı temsil eden bir simge alır.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT get_upperBound ( 
   IDiaSymbol** pRetVal
);
```

#### <a name="parameters"></a>Parametreler
 `pRetVal`

[out] Döndürür bir [Idiasymbol](../../debugger/debug-interface-access/idiasymbol.md) FORTRAN dizi boyutu üst sınırı temsil eden nesne.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi halde döndürür `S_FALSE` veya bir hata kodu.

> [!NOTE]
> Dönüş değeri `S_FALSE` özelliği simge için kullanılabilir değil anlamına gelir.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)