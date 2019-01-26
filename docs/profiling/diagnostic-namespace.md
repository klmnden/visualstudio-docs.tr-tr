---
title: Tanılama Namespace | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- cvmarkersobj/Concurrency::diagnostic
helpviewer_keywords:
- Concurrency::diagnostic namespace
ms.assetid: ad786b19-7c4c-46ee-bfb6-c4752b373a09
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 68f365210c2ed365a7e9ce75ab3c6fbcd309e01a
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54984060"
---
# <a name="diagnostic-namespace"></a>Tanılama ad alanı
`diagnostics` Ad alanı için eşzamanlılık görselleştiricisi işaretleyicileri yayma işlevselliği sağlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
namespace diagnostic;  
```  
  
## <a name="members"></a>Üyeler  
  
### <a name="classes"></a>Sınıflar  
  
|Ad|Açıklama|  
|----------|-----------------|  
|[marker_series Sınıfı](../profiling/marker-series-class.md)|Tek bir sağlayıcı tarafından oluşturulan olayları seri bir kanalı temsil eder.|  
|[span Sınıfı](../profiling/span-class.md)|Uygulamanın bir aşama tanımlar.|  
  
### <a name="enumerations"></a>Numaralandırmalar  
  
|Ad|Açıklama|  
|----------|-----------------|  
|[marker_importance Sabit Listesi](../profiling/marker-importance-enumeration.md)|Eşzamanlılık görselleştiricisi işaretleyicisi önem düzeyini temsil eder.|  
  
## <a name="requirements"></a>Gereksinimler  
 **Header:** *cvmarkersobj.h*  
  
 **Namespace:** Eşzamanlılık  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Eşzamanlılık ad alanı (eşzamanlılık görselleştiricisi)](../profiling/concurrency-namespace-concurrency-visualizer.md)