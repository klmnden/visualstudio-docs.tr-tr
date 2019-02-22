---
title: Önalım zamanı | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.cv.threads.timeline.preemption
helpviewer_keywords:
- Concurrency Visualizer, Preemption Time
ms.assetid: 6b78f91e-a006-440c-83fb-e7368040951d
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: de7a02f7247e09876bc4598d44fc1c395161ebc2
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56620102"
---
# <a name="preemption-time"></a>Önalım zamanı
Bu segmentlerde faaliyet zaman çizelgesi ön alım kategorilere engelleme zamanı ile ilişkilidir. Bu kategori, bir iş parçacığı çıkış aşağıdaki nedenlerden biri nedeniyle geçiş, gelir:

- Zamanlayıcı daha yüksek öncelikli iş parçacığı kullanarak değiştirildi.

- İş parçacığının yürütme kuantum süresi doldu ve diğer iş parçacıklarını yürütmek hazır.

  Bu süre boyunca, bir iş parçacığı eşzamanlılık görselleştiricisi ön alım sayılıyor bir çekirdek bekleme nedeni tarafından engellendi. Ön alım segmentler mantıksal çekirdek dışında bir iş parçacığı gönderildiğinde ve yürütme iş parçacığı devam ettiğinde bitmelidir.

  Araç İpucu biterse bir kesim için ön alım neden iş parçacığı ve işlem adını görüntüler. Ancak, bu üstlenmesinden iş parçacığı ve işlem gerçekten preempted dönem çalıştığını göstermez.

## <a name="see-also"></a>Ayrıca bkz.
- [İş Parçacıkları Görünümü](../profiling/threads-view-parallel-performance.md)