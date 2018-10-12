---
title: GPU etkinliği (disk belleği) | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- vs.cv.threads.timeline.gpuactivity
- vs.cv.threads.timeline.gpupaging
ms.assetid: 95284ac5-3492-4f7b-a79f-7d2840a07679
caps.latest.revision: 11
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 015fa34d2bb87cf98a64fb3431a6440202cf729b
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49195864"
---
# <a name="gpu-activity-paging"></a>GPU Etkinliği (Disk Belleği)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

**GPU etkinliği (disk belleği)** segmentleri iş parçacıkları sekmesinde zaman GPU işleme sayfalandırma istekleri bir kez temsil eder.  Bir segmenti uzunluğunu GPU doğrudan bellek erişimi (DMA) disk belleği paket işliyordu süreyi temsil eder. Genellikle, disk belleği paketleri bellek CPU ve GPU arasında aktarımı ile ilişkilidir.  
  
 Seçtiğinizde, bir GPU sayfalama segment, rapor üzerinde **geçerli** sekmesini işlenmiş DMA paket hakkında bilgileri görüntüler. Bu, DirectX altyapısı, DMA paket gönderilen işlem ve paket işlemek için gerekli olan zamanı ile ilişkili donanım kuyruğundaki, beklenen süre miktarını içerir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Kullanım Görünümü](../profiling/utilization-view.md)



