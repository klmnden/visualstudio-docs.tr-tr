---
title: Boş zaman çizelgesi segmenti | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.cv.threads.timeline.empty
helpviewer_keywords:
- Concurrency Visualizer, empty timeline segment
ms.assetid: f37b301f-3edc-4e56-8084-feec2dc5a9b1
caps.latest.revision: 16
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 0291cfe93492c357401ce371d58683c6815aa12b
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60052824"
---
# <a name="empty-timeline-segment"></a>Boş Zaman Çizelgesi Segmenti
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Zaman çizelgesinin bir bölümü boş nedeni eşzamanlılık görselleştiricisi içinde (beyaz arka plan sahiptir) kanal türüne bağlıdır.  
  
- Bir CPU iş parçacığı kanal için iş parçacığı zaman çizelgesi bu kısmı sırasında bulunmuyor anlamına gelir. İş parçacığında ilgileniyorsanız, yakınlaştırma denetimini kullanarak veya yatay kaydırma, yürütme bölümünde bulabilirsiniz.  
  
- Bir g/ç kanalı için hiçbir disk erişimi hedef işlem adına zamandaki o noktada ortaya çıktığını anlamına gelir.  
  
- Bir DirectX kanalı için hiçbir GPU işi zaman çizelgesi bu kısmı sırasında hedef işlem adına gerçekleştirildiğini anlamına gelir.  
  
- Bir işaretleyici kanal için bir işaretleyici yok oluşturulan anlamına gelir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [İş Parçacıkları görünümü](../profiling/threads-view-parallel-performance.md)   
 [Yakınlaştırma Denetimi (İş Parçacıkları Görünümü)](../profiling/zoom-control-threads-view.md)
