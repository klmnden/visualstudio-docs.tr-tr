---
title: Önalım zamanı | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.cv.threads.timeline.preemption
helpviewer_keywords:
- Concurrency Visualizer, Preemption Time
ms.assetid: 6b78f91e-a006-440c-83fb-e7368040951d
caps.latest.revision: 11
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 6fd209f65464126650106eb4509cd3de39ad8c25
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54752645"
---
# <a name="preemption-time"></a>Önalım Zamanı
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bu segmentlerde faaliyet zaman çizelgesi Önalım kategorilere ayrılır engelleme zamanı ile ilişkilidir. Bu kategori, bir iş parçacığı çıkış aşağıdaki nedenlerden biri nedeniyle geçiş, gelir:  
  
- Zamanlayıcı daha yüksek öncelikli iş parçacığı kullanarak değiştirildi.  
  
- İş parçacığının yürütme kuantum süresi doldu ve diğer iş parçacıklarını yürütmek hazır.  
  
  Bu süre boyunca, bir iş parçacığı eşzamanlılık görselleştiricisi Önalım sayılıyor bir çekirdek bekleme nedeni tarafından engellendi. Önalım segmentler mantıksal çekirdek dışında bir iş parçacığı gönderildiğinde ve yürütme iş parçacığı devam ettiğinde bitmelidir.  
  
  Araç İpucu preempted kesimin önalım neden iş parçacığı ve işlem adını görüntüler. Ancak, bu üstlenmesinden iş parçacığı ve işlem gerçekten preempted dönem çalıştığını göstermez.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [İş Parçacıkları Görünümü](../profiling/threads-view-parallel-performance.md)
