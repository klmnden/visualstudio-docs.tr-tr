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
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: ac0cf2a60fd194176b7cd9091f4e7dc7a758006f
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62969920"
---
# <a name="execution-time-threads-view"></a>Yürütme zamanı (iş parçacıkları görünümü)
İş parçacığı etkin bir sistemde bir mantıksal çekirdek çalışmaları yaparken bu segmentlerde faaliyet iş parçacıkları görünümü zaman çizelgesi yürütme zamanı temsil eder.

 İş parçacığı durumu değişiklikleri çekirdek bağlam anahtar olayları algılanır. Olay izleme için Windows (ETW), her bir milisaniyeden kısa örnek yığınları yakalar. Çok kısa yeşil Segmentte hiç örnek alındıktan mümkündür. Bu nedenle, bazı kısa yürütme kesimlerinin hiçbir çağrı yığını gösterebilir.

 Yürütme bölütü tıkladığınızda, Concurrency Visualizer tıklayarak konumuna yakın bir örnek yığını görüntüler. Bu örnek yığın konumunu siyah bir okla gösterilen ya da giriş işaretini bir zaman çizelgesi ve örnek yığını üzerinde görünür **geçerli** sekmesi.

 Geçerli görünümdeki tüm yürütme kesimlerinin geleneksel örnekleme profil görmek için tıklayın **yürütme** görünür zaman çizelgesi profili içinde.

## <a name="see-also"></a>Ayrıca bkz.
- [Yürütme Profil Raporu](../profiling/execution-profile-report.md)
- [İş Parçacıkları Görünümü](../profiling/threads-view-parallel-performance.md)