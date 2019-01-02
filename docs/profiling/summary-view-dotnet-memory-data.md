---
title: Özet görünümü - .NET bellek verisi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- Summary view
ms.assetid: 0cb317c3-0ae6-4531-aaa8-447576eec037
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- dotnet
ms.openlocfilehash: f5f821f936ffa8e157eb61e5daab25d1421c6899
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53935224"
---
# <a name="summary-view---net-memory-data"></a>Özet görünümü - .NET bellek verileri
Özet görünümü .NET işlevleri ve en çok bellek ayrılmış türler ve çoğu zaman bir çalıştırma profil oluşturulan türler hakkında bilgi görüntüler. Rapor listeler ve bildirim bağlantıları açıklamasını dahil olmak üzere daha fazla bilgi için bkz. [Özet görünümü](../profiling/summary-view.md).  
  
## <a name="timeline-graph"></a>Zaman Çizelgesi grafiği  
 Özet görünümü zaman çizelgesi grafikte, profili oluşturulan uygulamanın profil oluşturma gerçekleşen zaman tarafından işlemci (CPU) kullanımı gösterir. Seçili zaman aralığı için görünüme filtre uygulamak için zaman çizelgesi Grafiği'ni kullanabilirsiniz. Daha fazla bilgi için [nasıl yapılır: Özet zaman çizelgesinden rapor görünümlerini filtreleme](../profiling/how-to-filter-report-views-from-the-summary-timeline.md).  
  
## <a name="functions-allocating-most-memory"></a>En çok bellek ayrılan İşlevler  
 En yüksek sayıda bayt profil oluşturma çalıştırmasını bellek ayrılan işlevler listelenir.  
  
|Sütun|Açıklama|  
|------------|-----------------|  
|**Ad**|İşlevin adı.|  
|**Bayt yüzdesi**|Bu işlev tarafından çağırılan bir alt işlevi veya bu işlev tarafından ayrılan profil oluşturma, tüm ayrılmış baytların yüzdesi.|  
  
## <a name="types-with-most-memory-allocated"></a>En çok bellek ayrılmış türler  
 Profil oluşturma çalışmasında kendisi için en yüksek sayıda bayt bellek ayrılan türlerini listeler.  
  
|Sütun|Açıklama|  
|------------|-----------------|  
|**Ad**|Tür adı.|  
|**Bayt yüzdesi**|Bu tür için ayrılan profil oluşturma, tüm ayrılmış baytların yüzdesi.|  
  
## <a name="types-with-most-instances"></a>En çok örneği olan türler  
 Profil oluşturma çalışması sırasında en çok kez oluşturulan türlerini listeler. vardı  
  
|Sütun|Açıklama|  
|------------|-----------------|  
|**Ad**|Tür adı.|  
|**Örnek sayısı yüzdesi**|Çalıştıran profil oluşturulan toplam sayı of.NET nesneleri yüzdesi bu türün örneklerinin yoktu.|  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Özet görünümü - örnekleme verileri](../profiling/summary-view-sampling-data.md)   
 [Özet görünümü - izleme verileri](../profiling/summary-view-instrumentation-data.md)