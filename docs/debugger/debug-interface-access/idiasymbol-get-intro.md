---
title: Idiasymbol::get_intro | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSymbol::get_intro method
ms.assetid: 101afe4a-4c57-45de-87b4-330394c6de10
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 153daa1f43ba4945a5eb32aea82c5d58ff57c5f6
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62836806"
---
# <a name="idiasymbolgetintro"></a>IDiaSymbol::get_intro
İşlev Giriş bir sanal işlev olup olmadığını belirten bir bayrak alır.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT get_intro ( 
    BOOL* pRetVal
);
```

#### <a name="parameters"></a>Parametreler
`pRetVal`

[out] Döndürür `TRUE` işlev giriş sanal; ise döndürür, aksi takdirde, `FALSE`.

## <a name="return-value"></a>Dönüş Değeri
Başarılı olursa döndürür `S_OK`; Aksi halde döndürür `S_FALSE` veya hata kodu.

> [!NOTE]
> Dönüş değeri `S_FALSE` özelliği simge için kullanılabilir değil anlamına gelir.

## <a name="example"></a>Örnek

```C++
class A {
    virtual int f1();
}
class B : public A {
    int f1();
}
```

Her ikisi de `A::f1` ve `B::f1` sanal işlevler, ancak `A::f1` giriş sanaldır.

## <a name="requirements"></a>Gereksinimler

|Gereksinim|Açıklama|
|-----------------|-----------------|
|Üst bilgi:|dia2.h|
|Sürüm:|DIA SDK v7.0|

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)
