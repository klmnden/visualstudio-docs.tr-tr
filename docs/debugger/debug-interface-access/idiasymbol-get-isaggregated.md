---
title: Idiasymbol::get_isaggregated | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSymbol::get_isAggregated method
ms.assetid: 24d280ef-6ea3-4958-9418-4ad3ca7c67c1
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: db6c2e47d9f316f758b854e5ce40dfc19acb592b
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63400007"
---
# <a name="idiasymbolgetisaggregated"></a>IDiaSymbol::get_isAggregated
Veri simgenin bir toplama veya semboller koleksiyonunu parçası olup olmadığını belirten bir bayrak alır; Derleyici, toplanan sembolleri ayrı varlıklar olarak değerlendirir, ancak bunlar gerçekten tek bir büyük simge bir parçası.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT get_isAggregated(
   BOOL *pFlag
);
```

#### <a name="parameters"></a>Parametreler
 `pFlag`

[out] Döndürür `TRUE` veriler birleştirilmesinden üst sembol; split simgeleri bir parçasıdır, aksi halde döndürür `FALSE`.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi halde döndürür `S_FALSE` veya bir hata kodu.

> [!NOTE]
> Dönüş değeri `S_FALSE` özelliği simge için kullanılabilir değil anlamına gelir.

## <a name="remarks"></a>Açıklamalar
 [Idiasymbol::get_issplitted](../../debugger/debug-interface-access/idiasymbol-get-issplitted.md) yöntemi `TRUE` toplanmış sembol üst simge için.

## <a name="requirements"></a>Gereksinimler

|Gereksinim|Açıklama|
|-----------------|-----------------|
|Üst bilgi:|dia2.h|
|Sürüm:|DIA SDK v8.0|

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)
- [IDiaSymbol::get_isSplitted](../../debugger/debug-interface-access/idiasymbol-get-issplitted.md)