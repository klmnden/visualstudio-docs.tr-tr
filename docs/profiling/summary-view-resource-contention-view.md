---
title: Özet görünümü - kaynak çakışması görünümü | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- Summary view
ms.assetid: 6da57b83-7b42-4d7c-9aea-8e0a830faf6b
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 32bd10c1260309856eba14a3a42d2acaac939f6e
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55029225"
---
# <a name="summary-view---resource-contention-view"></a>Özet Görünümü - Kaynak Çakışması Görünümü
Özet görünümü, bir kaynağa erişim için beklenen karşın, bir iş parçacığı veya işlemi askıya alındı, uygulamanızda olaylar hakkında bilgi görüntüler.  
  
 Rapor listeler ve bildirim bağlantıları açıklamasını dahil olmak üzere daha fazla bilgi için bkz. [özeti görünümünü](../profiling/summary-view.md).  
  
## <a name="timeline-graph"></a>Zaman Çizelgesi grafiği  
 Özet görünümü zaman çizelgesi grafikte, profil oluşturma gerçekleşen zaman içinde oluşturulan uygulamanın Çekişme olayları sayısını gösterir. Seçili zaman aralığı için görünüme filtre uygulamak için zaman çizelgesi Grafiği'ni kullanabilirsiniz. Daha fazla bilgi için [nasıl yapılır: Özet zaman çizelgesinden rapor görünümlerini filtreleme](../profiling/how-to-filter-report-views-from-the-summary-timeline.md).  
  
## <a name="most-contended-resources"></a>En çekişmeli kaynaklar  
 **En fazla kaynak Contended** Çekişme olayları en nedeniyle uygulama kaynakları listeler. Çekişmelerini görüntülemek için bir kaynak adı tıklayabilirsiniz. Çekişmeleri görünümü kaynak çakışması ayrıntılı bir zaman çizelgesi iş parçacığı tarafından sağlar.  
  
 **En fazla kaynak Contended** her bir kaynak olarak aşağıdaki verileri içerir.  
  
|Sütun|Açıklama|  
|------------|-----------------|  
|**Ad**|Kaynak adı.|  
|**Çekişme yüzdesi**|Bu kaynak üzerinde Çekişme olan profil oluşturma veri tüm Çekişme olayları yüzdesi.|  
  
## <a name="most-contended-thread"></a>En çekişmeli iş parçacığı  
 **Çoğu Contended iş parçacıkları** iş parçacığı Çekişme olayları en çok sayıda olan uygulamada listeler. İş parçacığı tarafından ayrıntılı bir zaman çizelgesi kaynak çakışması sağlayan çekişmelerini görüntülemek için iş parçacığı adı tıklayabilirsiniz.  
  
 **Çoğu Contended iş parçacıkları** her iş parçacığı için aşağıdaki veriler içerir.  
  
|Sütun|Açıklama|  
|------------|-----------------|  
|**ID**|İş parçacığı tanımlayıcısı.|  
|**Ad**|İş parçacığı sahibi olan işlemin adı.|  
|**Çekişme yüzdesi**|Bu kaynak üzerinde Çekişme olan profil oluşturma veri tüm Çekişme olayları yüzdesi.|