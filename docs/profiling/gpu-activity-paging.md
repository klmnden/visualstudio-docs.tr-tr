---
title: GPU etkinliği (disk belleği) | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.cv.threads.timeline.gpuactivity
- vs.cv.threads.timeline.gpupaging
ms.assetid: 95284ac5-3492-4f7b-a79f-7d2840a07679
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 919f99ad24764017e823dbceda51bec4461401e4
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53942729"
---
# <a name="gpu-activity-paging"></a>GPU Etkinliği (Disk Belleği)
**GPU etkinliği (disk belleği)** üzerinde kesim **iş parçacıkları** sekmesinde temsil saatleri zaman GPU işleme sayfalandırma istekleri.  Bir segmenti uzunluğunu GPU doğrudan bellek erişimi (DMA) disk belleği paket işliyordu süreyi temsil eder. Genellikle, disk belleği paketleri bellek CPU ve GPU arasında aktarımı ile ilişkilidir.  
  
 Seçtiğinizde, bir GPU sayfalama segment, rapor üzerinde **geçerli** sekmesini işlenmiş DMA paket hakkında bilgileri görüntüler. Bu, DirectX altyapısı, DMA paket gönderilen işlem ve paket işlemek için gerekli olan zamanı ile ilişkili donanım kuyruğundaki, beklenen süre miktarını içerir.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Kullanım Görünümü](../profiling/utilization-view.md)