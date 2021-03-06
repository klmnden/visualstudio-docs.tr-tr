---
title: Bellek yönetimi zamanı | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.cv.threads.timeline.paging
helpviewer_keywords:
- Concurrency Visualizer, Paging Time
ms.assetid: 67af3509-3a7d-435d-bc37-5262448da915
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 442973edb18e75bafda8a9397eac799286c69dfa
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62963787"
---
# <a name="memory-management-time"></a>Bellek yönetimi zamanı
Bu segmentlerde faaliyet zaman çizelgesi, bellek yönetimi sınıflandırılmış bir kez engelleme ile ilişkilidir. Bu senaryo, bir iş parçacığı bir bellek yönetimi işlemi gibi disk belleği ile ilişkili bir olay tarafından engellendiğini anlamına gelir. Bu süre boyunca, bir iş parçacığı eşzamanlılık görselleştiricisi bellek yönetimi sayılıyor bir API veya çekirdek durumda engellendi. Bunlar, sayfalama ve bellek ayırma gibi olayları içerir.

 Bellek yönetimi sınıflandırılmış blokları temel nedenleri daha iyi anlamak için profil raporlarını ve ilişkili çağrı yığınları inceleyin.

## <a name="see-also"></a>Ayrıca bkz.
- [İş Parçacıkları Görünümü](../profiling/threads-view-parallel-performance.md)