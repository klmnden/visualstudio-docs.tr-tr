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
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 98917d9f0492a59b832d9e91da8f8e16059faae9
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54948797"
---
# <a name="gpu-activity-paging"></a>GPU Etkinliği (Disk Belleği)
**GPU etkinliği (disk belleği)** üzerinde kesim **iş parçacıkları** sekmesinde temsil saatleri zaman GPU işleme sayfalandırma istekleri.  Bir segmenti uzunluğunu GPU doğrudan bellek erişimi (DMA) disk belleği paket işliyordu süreyi temsil eder. Genellikle, disk belleği paketleri bellek CPU ve GPU arasında aktarımı ile ilişkilidir.  
  
 Seçtiğinizde, bir GPU sayfalama segment, rapor üzerinde **geçerli** sekmesini işlenmiş DMA paket hakkında bilgileri görüntüler. Bu, DirectX altyapısı, DMA paket gönderilen işlem ve paket işlemek için gerekli olan zamanı ile ilişkili donanım kuyruğundaki, beklenen süre miktarını içerir.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Kullanım Görünümü](../profiling/utilization-view.md)