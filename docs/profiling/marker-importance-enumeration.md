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
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 330ba15fa62272bd2c2f7ea7b40d6b527ab237c3
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53841696"
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
 **Başlık:** *cvmarkersobj.h*  
  
 **Namespace:** CONCURRENCY::Diagnostic  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Tanılama ad alanı](../profiling/diagnostic-namespace.md)