---
title: marker_series::is_enabled yöntemi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- cvmarkersobj/Concurrency::diagnostic::marker_series::is_enabled
helpviewer_keywords:
- Concurrency::diagnostic::marker_series::is_enabled method
ms.assetid: 8ce4dd50-ca29-4c72-98d6-582693f7d501
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 22a7baa08a29cd77506e48762179118b3bbb2d1a
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63002756"
---
# <a name="markerseriesisenabled-method"></a>marker_series::is_enabled yöntemi
Tüm oturum sağlayıcısı etkin olmadığını belirler.

## <a name="syntax"></a>Sözdizimi

```cpp
bool is_enabled();
bool is_enabled(
   marker_importance _Importance,
   int _Category
);
```

#### <a name="parameters"></a>Parametreler
 `_Importance` Önem düzeyi.

 `_Category` Kategori.

## <a name="return-value"></a>Dönüş değeri

## <a name="requirements"></a>Gereksinimler
 **Header:** *cvmarkersobj.h*

 **Namespace:** CONCURRENCY::Diagnostic

## <a name="see-also"></a>Ayrıca bkz.
- [marker_series class](../profiling/marker-series-class.md)