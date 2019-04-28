---
title: Bekleme süresi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.cv.threads.timeline.sleep
helpviewer_keywords:
- Concurrency Visualizer, Sleep Time
ms.assetid: 3ddb96f9-9bda-4a68-ad4d-ef488a0a68dc
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: be2d566228367e2cdb07aecc2d73eaf82a6d961f
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62980219"
---
# <a name="sleep-time"></a>Bekleme süresi
Bu segmentlerde faaliyet zaman çizelgesi uyku kategorilere ayrılır engelleme zamanı ile ilişkilidir. Uyku kategori, bir iş parçacığı, mantıksal çekirdek gönüllü verdiği ve herhangi bir çalışma yapılması anlamına gelir. Bu süre boyunca, bir iş parçacığı eşzamanlılık görselleştiricisi uyku sayılıyor bir API'de engellendi. API'leri gibi `Sleep()` ve `SwitchToThread()` bu gruba girer.

## <a name="see-also"></a>Ayrıca bkz.
- [İş Parçacıkları görünümü](../profiling/threads-view-parallel-performance.md)