---
title: Boş zaman çizelgesi segmenti | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.cv.threads.timeline.empty
helpviewer_keywords:
- Concurrency Visualizer, empty timeline segment
ms.assetid: f37b301f-3edc-4e56-8084-feec2dc5a9b1
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: a96cdc7ae4edc7ea7193d5b95dfc73fa1747c1fb
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62970115"
---
# <a name="empty-timeline-segment"></a>Boş zaman çizelgesi segmenti
Zaman çizelgesinin bir bölümü boş nedeni eşzamanlılık görselleştiricisi içinde (beyaz arka plan sahiptir) kanal türüne bağlıdır.

- Bir CPU iş parçacığı kanal için iş parçacığı zaman çizelgesi bu kısmı sırasında bulunmuyor anlamına gelir. İş parçacığında ilgileniyorsanız, yakınlaştırma denetimini kullanarak veya yatay kaydırma, yürütme bölümünde bulabilirsiniz.

- Bir g/ç kanalı için hiçbir disk erişimi hedef işlem adına zamandaki o noktada ortaya çıktığını anlamına gelir.

- Bir DirectX kanalı için hiçbir GPU işi zaman çizelgesi bu kısmı sırasında hedef işlem adına gerçekleştirildiğini anlamına gelir.

- Bir işaretleyici kanal için bir işaretleyici yok oluşturulan anlamına gelir.

## <a name="see-also"></a>Ayrıca bkz.
- [İş Parçacıkları Görünümü](../profiling/threads-view-parallel-performance.md)
- [Yakınlaştırma Denetimi (iş parçacıkları görünümü)](../profiling/zoom-control-threads-view.md)