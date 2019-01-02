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
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 62e8cf9ce14be5fd45c579584c754394f1dfb83b
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53945411"
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
 `_Importance`  
 Önem düzeyi.  
  
 `_Category`  
 Kategori.  
  
## <a name="return-value"></a>Dönüş değeri  
  
## <a name="requirements"></a>Gereksinimler  
 **Başlık:** *cvmarkersobj.h*  
  
 **Namespace:** CONCURRENCY::Diagnostic  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [marker_series sınıfı](../profiling/marker-series-class.md)