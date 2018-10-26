---
title: Önalım zamanı | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- vs.cv.threads.timeline.preemption
helpviewer_keywords:
- Concurrency Visualizer, Preemption Time
ms.assetid: 6b78f91e-a006-440c-83fb-e7368040951d
caps.latest.revision: 11
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: f302dff3ea72217c6325aca667aec8ff4d7f218f
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49905239"
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



