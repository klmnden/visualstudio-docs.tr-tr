---
title: Yürütme zamanı (iş parçacıkları görünümü) | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.cv.threads.timeline.execution
helpviewer_keywords:
- Concurrency Visualizer, Execution Time (Threads View)
ms.assetid: 80c100f8-2502-4613-bfef-4f4f2e09cc8d
caps.latest.revision: 15
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: b4306e030c2f48d87b12ba6338a847dc9e9aa892
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54766250"
---
# <a name="execution-time-threads-view"></a>Yürütme Zamanı (İş Parçacıkları Görünümü)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

İş parçacığı etkin bir sistemde bir mantıksal çekirdek çalışmaları yaparken bu segmentlerde faaliyet iş parçacıkları görünümü zaman çizelgesi yürütme zamanı temsil eder.  
  
 İş parçacığı durumu değişiklikleri çekirdek bağlam anahtar olayları algılanır. Olay izleme için Windows (ETW), her bir milisaniyeden kısa örnek yığınları yakalar. Çok kısa yeşil Segmentte hiç örnek alındıktan mümkündür. Bu nedenle, bazı kısa yürütme kesimlerinin hiçbir çağrı yığını gösterebilir.  
  
 Yürütme bölütü tıkladığınızda, Concurrency Visualizer tıklayarak konumuna yakın bir örnek yığını görüntüler. Bu örnek yığın konumunu siyah bir okla gösterilen ya da giriş işaretini bir zaman çizelgesi ve örnek yığını üzerinde görünür **geçerli** sekmesi.  
  
 Geçerli görünümdeki tüm yürütme kesimlerinin geleneksel örnekleme profil görmek için tıklayın **yürütme** görünür zaman çizelgesi profili içinde.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Yürütme Profil raporu](../profiling/execution-profile-report.md)   
 [İş Parçacıkları Görünümü](../profiling/threads-view-parallel-performance.md)
