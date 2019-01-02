---
title: marker_series sınıfı | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- cvmarkersobj/Concurrency::diagnostic::marker_series
helpviewer_keywords:
- Concurrency::diagnostic::marker_series class
ms.assetid: b8445ed0-c512-4f92-b6b4-3d05c044f939
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: e8ecc6a14cce80197c1221734aadb4ce7e6758cf
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53869826"
---
# <a name="markerseries-class"></a>marker_series sınıfı
Tek bir sağlayıcı tarafından oluşturulan olayları seri bir kanalı temsil eder.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
class marker_series;  
```  
  
## <a name="members"></a>Üyeler  
  
### <a name="public-constructors"></a>Genel oluşturucular  
  
|Ad|Açıklama|  
|----------|-----------------|  
|[marker_series::marker_series Oluşturucusu](../profiling/marker-series-marker-series-constructor.md)|Yeni bir örneğini başlatır `marker_series` sınıfı.|  
|[marker_series:: ~ marker_series yok Edicisi](../profiling/marker-series-tilde-marker-series-destructor.md)|Marker_series nesnesini yok eder ve ayrılan tüm kaynakları serbest bırakır.|  
  
### <a name="public-methods"></a>Genel yöntemler  
  
|Ad|Açıklama|  
|----------|-----------------|  
|[marker_series::is_enabled yöntemi](../profiling/marker-series-is-enabled-method.md)|Tüm oturum sağlayıcısı etkin olmadığını belirler.|  
|[marker_series::write_alert yöntemi](../profiling/marker-series-write-alert-method.md)|Bir uyarı eşzamanlılık görselleştiricisi izleme dosyasına yazar.|  
|[marker_series::write_flag yöntemi](../profiling/marker-series-write-flag-method.md)|Bayrak eşzamanlılık görselleştiricisi izleme dosyasına yazar.|  
|[marker_series::write_message yöntemi](../profiling/marker-series-write-message-method.md)|Eşzamanlılık görselleştiricisi izleme dosyasının bir ileti yazar.|  
  
## <a name="inheritance-hierarchy"></a>Devralma Hiyerarşisi  
 `marker_series`  
  
## <a name="requirements"></a>Gereksinimler  
 **Başlık:** *cvmarkersobj.h*  
  
 **Namespace:** CONCURRENCY::Diagnostic  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Tanılama ad alanı](../profiling/diagnostic-namespace.md)