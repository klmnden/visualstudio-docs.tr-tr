---
title: span::span Oluşturucusu | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- cvmarkersobj/Concurrency::diagnostic::span::span
helpviewer_keywords:
- Concurrency::diagnostic::span constructor
ms.assetid: 8b5578aa-5e5c-4ac7-87c7-ce87c4246e2c
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: f761e87c1658c11bfdfd93a4f4e22299d88575a8
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62979828"
---
# <a name="spanspan-constructor"></a>span::span Oluşturucusu

Yeni bir örneğini başlatır `span` sınıfı.

## <a name="syntax"></a>Sözdizimi

```cpp
span(
   const marker_series& _Series,
   _In_ LPCTSTR _Format,
   ...
);
span(
   const marker_series& _Series,
   marker_importance _Importance,
   _In_ LPCTSTR _Format,
   ...
);
span(
   const marker_series& _Series,
   int _Category,
   _In_ LPCTSTR _Format,
   ...
);
span(
   const marker_series& _Series,
   marker_importance _Importance,
   int _Category,
   _In_ LPCTSTR _Format,
   ...
);
```

#### <a name="parameters"></a>Parametreler

`_Series` Geçerli işaret serisi bağlamı.

`_Format` Bağımsız değişken listesindeki nesnelere karşılık gelen sıfır veya daha fazla biçim öğeleri ile karıştırılmış, metin içeren bir bileşik biçimlendirme dizesi.

`_Importance` Önem düzeyi.

`_Category` Kategori.

## <a name="requirements"></a>Gereksinimler

**Header:** *cvmarkersobj.h*

**Namespace:** CONCURRENCY::Diagnostic

## <a name="see-also"></a>Ayrıca bkz.

- [span sınıfı](../profiling/span-class.md)