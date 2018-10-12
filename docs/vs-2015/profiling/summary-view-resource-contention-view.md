---
title: Özet görünümü - kaynak çakışması görünümü | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- Summary view
ms.assetid: 6da57b83-7b42-4d7c-9aea-8e0a830faf6b
caps.latest.revision: 13
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 7cf00fbb7237194b88edc9e748abfa06483a44a5
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49229755"
---
# <a name="summary-view---resource-contention-view"></a>Özet Görünümü - Kaynak Çakışması Görünümü
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

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



