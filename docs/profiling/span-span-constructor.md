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
ms.openlocfilehash: 3b04f9edc946b83f8785c6a6fb3e9720db4840f0
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56596204"
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