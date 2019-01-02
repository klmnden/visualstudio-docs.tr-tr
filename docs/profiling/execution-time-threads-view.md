---
title: Yürütme zamanı (iş parçacıkları görünümü) | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.cv.threads.timeline.execution
helpviewer_keywords:
- Concurrency Visualizer, Execution Time (Threads View)
ms.assetid: 80c100f8-2502-4613-bfef-4f4f2e09cc8d
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 4131b70a0d76f5245152e397032f55833421c424
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53905961"
---
# <a name="execution-time-threads-view"></a>Yürütme zamanı (iş parçacıkları görünümü)
İş parçacığı etkin bir sistemde bir mantıksal çekirdek çalışmaları yaparken bu segmentlerde faaliyet iş parçacıkları görünümü zaman çizelgesi yürütme zamanı temsil eder.  
  
 İş parçacığı durumu değişiklikleri çekirdek bağlam anahtar olayları algılanır. Olay izleme için Windows (ETW), her bir milisaniyeden kısa örnek yığınları yakalar. Çok kısa yeşil Segmentte hiç örnek alındıktan mümkündür. Bu nedenle, bazı kısa yürütme kesimlerinin hiçbir çağrı yığını gösterebilir.  
  
 Yürütme bölütü tıkladığınızda, Concurrency Visualizer tıklayarak konumuna yakın bir örnek yığını görüntüler. Bu örnek yığın konumunu siyah bir okla gösterilen ya da giriş işaretini bir zaman çizelgesi ve örnek yığını üzerinde görünür **geçerli** sekmesi.  
  
 Geçerli görünümdeki tüm yürütme kesimlerinin geleneksel örnekleme profil görmek için tıklayın **yürütme** görünür zaman çizelgesi profili içinde.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Yürütme Profil raporu](../profiling/execution-profile-report.md)   
 [İş Parçacıkları Görünümü](../profiling/threads-view-parallel-performance.md)