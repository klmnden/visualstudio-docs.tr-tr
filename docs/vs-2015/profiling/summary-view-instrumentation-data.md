---
title: Özet görünümü - izleme verileri | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
helpviewer_keywords:
- Summary view
ms.assetid: 0a3b3a1f-e22b-4ac8-b46e-71694e9b2cf1
caps.latest.revision: 16
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 5dc0b4195d33a7bf72d17681b6d71e78f1bacfe5
ms.sourcegitcommit: a83c60bb00bf95e6bea037f0e1b9696c64deda3c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/19/2019
ms.locfileid: "54784592"
---
# <a name="summary-view---instrumentation-data"></a>Özet Görünümü - İzleme Verileri
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Özet görünümü, bir profil oluşturma çalışmasında en pahalı performans işlevleri hakkında bilgi görüntüler. Rapor listeler ve bildirim bağlantıları açıklamasını dahil olmak üzere daha fazla bilgi için bkz. [özeti görünümünü](../profiling/summary-view.md).  
  
## <a name="timeline-graph"></a>Zaman Çizelgesi grafiği  
 Özet görünümü zaman çizelgesi grafikte, profili oluşturulan uygulamanın profil oluşturma gerçekleşen zaman tarafından işlemci (CPU) kullanımı gösterir. Seçili zaman aralığı için görünüme filtre uygulamak için zaman çizelgesi Grafiği'ni kullanabilirsiniz. Daha fazla bilgi için [nasıl yapılır: Özet zaman çizelgesinden rapor görünümlerini filtreleme](../profiling/how-to-filter-report-views-from-the-summary-timeline.md).  
  
## <a name="hot-path"></a>Etkin yol  
 **Etkin yolu** en çok zaman harcanan yürütme yolunu görüntüler. İşlev için işlev ayrıntıları görüntülemek için bir işlev tıklayabilirsiniz. İçin işlev sağ işlevi için diğer görünümleri görüntülemek ve sonra listeden bir görünümü tıklatın.  
  
 **Etkin yolu** her işlevine yönelik olarak aşağıdaki verileri içerir:  
  
|Sütun|Açıklama|  
|------------|-----------------|  
|**Ad**|İşlevin adı.|  
|**Geçen kapsamlı süre yüzdesi**|İşlevi, işlev gövdesinde ve onu çağıran işlevler kodu yürütürken harcanan profil oluşturma verilerinin tüm süre yüzdesi.|  
|**Geçen dışlamalı süre yüzdesi**|Tüm profil oluşturma verilerinin işlevi, işlev gövdesinde kod çalıştırırken harcadığı süre yüzdesi. İşlev çağrılan işlevlerde geçen süre dahil değildir.|  
  
## <a name="functions-with-most-individual-work"></a>En bireysel işlerle İşlevler  
 Çoğu zaman kodu yürütürken işlevinin gövdesi ve onu çağıran işlevlerini tüketilen işlevlerin listesi.  
  
 **En bireysel işleri işlevleriyle** her işlevine yönelik olarak aşağıdaki verileri içerir:  
  
|Sütun|Açıklama|  
|------------|-----------------|  
|**Ad**|İşlevin adı.|  
|**Dışlamalı süre yüzdesi**|Tüm profil oluşturma verilerinin işlevi, işlev gövdesinde kod çalıştırırken harcadığı süre yüzdesi. İşlev çağrılan işlevlerde geçen süre dahil değildir.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Özet görünümü](../profiling/summary-view-sampling-data.md)   
 [Özet Görünümü](../profiling/summary-view-dotnet-memory-data.md)
