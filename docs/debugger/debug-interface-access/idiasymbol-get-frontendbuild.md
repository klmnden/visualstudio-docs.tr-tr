---
title: Idiasymbol::get_frontendbuild | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSymbol::get_frontEndBuild method
ms.assetid: f7dab1c6-112b-4966-baa5-afc976949c76
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: ef83579eb1fe79317d1a2be3ab384d3ec11b6eb2
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56629865"
---
# <a name="idiasymbolgetfrontendbuild"></a>IDiaSymbol::get_frontEndBuild
Ön uç yapı numarasını alır.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT get_frontEndBuild ( 
   DWORD* pRetVal
);
```

#### <a name="parameters"></a>Parametreler
 `pRetVal`

[out] Ön uç yapı numarasını döndürür. Açıklamalara bakın.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi halde döndürür `S_FALSE` veya bir hata kodu.

> [!NOTE]
>  Dönüş değeri `S_FALSE` özelliği simge için mevcut olmadığı anlamına gelir.

## <a name="remarks"></a>Açıklamalar
 Bir derleyici genellikle birincil iki öğeden oluşur: bir ara forma kaynak kodu ayrıştırma işleyen ön uç (ayrıştırıcının) ve derlemeye Ara formun dönüştüren bir arka uç (Kod Oluşturucu). Arka uçtan farklı bir sürüm ön uç için sık karşılaşılan bir durum değil.

 Ön uç veya arka uç sürüm numarası, üç bölümden oluşur: \<ana >.\< küçük >. \<Yapı >, burada \<ana > ana sürüm numarası \<küçük > alt sürüm numarası ve \<Yapı > yapı numarasıdır. Örneğin, 13.10.3077.

## <a name="requirements"></a>Gereksinimler

|Gereksinim|Açıklama|
|-----------------|-----------------|
|Üst bilgi:|dia2.h|
|Sürüm:|DIA SDK v7.0|

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)