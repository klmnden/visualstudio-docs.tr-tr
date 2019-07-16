---
title: marker_series sınıfı | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- cvmarkersobj/Concurrency::diagnostic::marker_series
helpviewer_keywords:
- Concurrency::diagnostic::marker_series class
ms.assetid: b8445ed0-c512-4f92-b6b4-3d05c044f939
caps.latest.revision: 8
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: cb199d74ade593d0bc8318c27bc96ffbf70e4dcf
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68194939"
---
# <a name="markerseries-class"></a>marker_series Sınıfı
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Tek bir sağlayıcı tarafından oluşturulan olayları seri bir kanalı temsil eder.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
class marker_series;  
```  
  
## <a name="members"></a>Üyeler  
  
### <a name="public-constructors"></a>Ortak Oluşturucular  
  
|Ad|Açıklama|  
|----------|-----------------|  
|[marker_series::marker_series Oluşturucusu](../profiling/marker-series-marker-series-constructor.md)|Yeni bir örneğini başlatır `marker_series` sınıfı.|  
|[marker_series::~marker_series Yok Edicisi](../profiling/marker-series-tilde-marker-series-destructor.md)|Marker_series nesnesini yok eder ve ayrılan tüm kaynakları serbest bırakır.|  
  
### <a name="public-methods"></a>Ortak Yöntemler  
  
|Ad|Açıklama|  
|----------|-----------------|  
|[marker_series::is_enabled Metodu](../profiling/marker-series-is-enabled-method.md)|Tüm oturum sağlayıcısı etkin olmadığını belirler.|  
|[marker_series::write_alert Metodu](../profiling/marker-series-write-alert-method.md)|Bir uyarı eşzamanlılık görselleştiricisi izleme dosyasına yazar.|  
|[marker_series::write_flag Metodu](../profiling/marker-series-write-flag-method.md)|Bayrak eşzamanlılık görselleştiricisi izleme dosyasına yazar.|  
|[marker_series::write_message Metodu](../profiling/marker-series-write-message-method.md)|Eşzamanlılık görselleştiricisi izleme dosyasının bir ileti yazar.|  
  
## <a name="inheritance-hierarchy"></a>Devralma Hiyerarşisi  
 `marker_series`  
  
## <a name="requirements"></a>Gereksinimler  
 **Başlık:** cvmarkersobj.h  
  
 **Namespace:** CONCURRENCY::Diagnostic  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Tanılama Ad Alanı](../profiling/diagnostic-namespace.md)
