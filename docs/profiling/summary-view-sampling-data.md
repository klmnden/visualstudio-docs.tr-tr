---
title: Özet görünümü - örnekleme verileri | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- sampling profiling method, Summary view
- Summary view
ms.assetid: 79056873-2985-40be-9112-cdbc26a65156
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: d0b1c1da6bd493fc53419ef5b371b74488002e27
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53938611"
---
# <a name="summary-view---sampling-data"></a>Özet görünümü - örnekleme verileri
Özet görünümü, bir profil oluşturma çalışmasında en pahalı performans işlevleri hakkında bilgi görüntüler. Rapor listeler ve bildirim bağlantıları açıklamasını dahil olmak üzere daha fazla bilgi için bkz. [özeti görünümünü](../profiling/summary-view.md).  
  
> [!NOTE]
>  Windows 8 ve Windows Server 2012'deki Gelişmiş güvenlik özellikleri Visual Studio profil oluşturucu bu platformlarda veri toplayan bir şekilde önemli değişiklikler gerekmiştir. UWP uygulamaları, ayrıca yeni toplama teknikleri gerektirir. Bkz: [Windows 8 ve Windows Server 2012 uygulamalarında performans araçları](../profiling/performance-tools-on-windows-8-and-windows-server-2012-applications.md).  
  
## <a name="timeline-graph"></a>Zaman Çizelgesi grafiği  
 Özet görünümü zaman çizelgesi grafikte profil oluşturma gerçekleşen zaman içinde oluşturulan uygulamanın işlemci (CPU) kullanım yüzdesini gösterir. Seçili zaman aralığı için görünüme filtre uygulamak için zaman çizelgesi Grafiği'ni kullanabilirsiniz. Daha fazla bilgi için [nasıl yapılır: Özet zaman çizelgesinden rapor görünümlerini filtreleme](../profiling/how-to-filter-report-views-from-the-summary-timeline.md).  
  
## <a name="hot-path"></a>Etkin yol  
 **Etkin yolu** çoğu örnek toplandı yürütme yolunu görüntüler. İşlev için işlev ayrıntıları görüntülemek için bir işlev tıklayabilirsiniz. İşlevi için diğer görünümleri görüntülemek için işlev sağ tıklayın ve sonra listeden bir görünümü tıklatın.  
  
 **Etkin yolu** her işlevine yönelik olarak aşağıdaki verileri içerir:  
  
|Sütun|Açıklama|  
|------------|-----------------|  
|**Ad**|İşlevin adı.|  
|**Kapsamlı örnek yüzdesi**|Bu işlev veya bu işlev tarafından çağrılan bir işlev yürütülürken gerçekleşen tüm örneklerin yüzdesi.|  
|**Dışlamalı örnek yüzdesi**|İşlev işlev gövdesinde kod yürütülürken gerçekleşen tüm örneklerin yüzdesi. Bu işlev tarafından çağırılan işlevlerdeki toplanan örnekler dahil edilmez.|  
  
## <a name="functions-doing-most-individual-work"></a>En bireysel işleri yapan işlevler  
 **İşlevleri en bireysel işleri yapan** en yüksek sayıda profil oluşturma çalışması içinde dışlamalı örnek işlevleri görüntüler. Özel bir örnek, örnek toplandığında, kendi kod işlevi yürütülüyorsa bir işleve atanır. Örnek toplandığında işlevi başka bir işlevi çağırıyorsa, özel bir örnek için bir işlev atanmadı. Dışlamalı örnek çok sayıda önemli zaman işlevde harcanan gösterir.  
  
 İşlev için işlev ayrıntıları görüntülemek için bir işlev tıklayabilirsiniz. İçin işlev sağ işlevi için diğer görünümleri görüntülemek ve sonra listeden bir görünümü tıklatın.  
  
 **En bireysel işleri yapan işlevler** her işlevine yönelik olarak aşağıdaki verileri içerir:  
  
|Sütun|Açıklama|  
|------------|-----------------|  
|**Ad**|İşlevin adı.|  
|**Dışlamalı örnek yüzdesi**|İşlev kendi işlev gövdesindeki kod yürütülürken, toplanmış olan profil oluşturma, tüm örneklerin yüzdesi. Bu işlevi çağıran işlevler yürütülürken toplanan örnekler yüzdeyi dışlar.|  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Özet görünümü - .NET bellek verileri](../profiling/summary-view-dotnet-memory-data.md)   
 [Özet görünümü - izleme verileri](../profiling/summary-view-instrumentation-data.md)