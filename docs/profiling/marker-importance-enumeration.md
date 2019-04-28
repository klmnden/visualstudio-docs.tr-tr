---
title: marker_importance sabit listesi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- cvmarkersobj/Concurrency::diagnostic::marker_importance
helpviewer_keywords:
- Concurrency::diagnostic::marker_importance enumeration
ms.assetid: d5524ea0-0227-4d8e-9122-332291042df5
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: b3f5cfb583ec4fceb9fb7428b08c00f6ca8e26b6
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62999967"
---
# <a name="markerimportance-enumeration"></a>marker_importance numaralandırması
Eşzamanlılık görselleştiricisi işaretleyicisi önem düzeyini temsil eder.

## <a name="syntax"></a>Sözdizimi

```cpp
enum marker_importance;
```

## <a name="members"></a>Üyeler

### <a name="values"></a>Değerler

|Ad|Açıklama|
|----------|-----------------|
|`critical_importance`|İşaretin kritik öneme sahip olduğunu belirtir.|
|`high_importance`|İşaretin yüksek önem sahip olduğunu belirtir.|
|`low_importance`|İşaretin düşük öneme sahip olduğunu belirtir.|
|`normal_importance`|İşaretin normal önem sahip olduğunu belirtir.|

## <a name="requirements"></a>Gereksinimler
 **Header:** *cvmarkersobj.h*

 **Namespace:** CONCURRENCY::Diagnostic

## <a name="see-also"></a>Ayrıca bkz.
- [Tanılama ad alanı](../profiling/diagnostic-namespace.md)