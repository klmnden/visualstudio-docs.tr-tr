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
ms.openlocfilehash: 3d4049a3792fcc529352baef3e4649c6157aa7f0
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54992158"
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
 [Tanılama ad alanı](../profiling/diagnostic-namespace.md)