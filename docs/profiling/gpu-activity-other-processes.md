---
title: GPU etkinliği (diğer işlemler) | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.cv.threads.timeline.gpuother
- vs.cv.threads.timeline.gpuactivity
ms.assetid: 8a68df65-eb63-452f-9285-fb4ffc92f2b2
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 570e5d313b6246903f5e6a931b10f33fa40bf3ac
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53913416"
---
# <a name="gpu-activity-other-processes"></a>GPU Etkinliği (Diğer İşlemler)
**GPU etkinliği (diğer işlemler)** kesimlerinde eşzamanlılık görselleştiricisi iş parçacıkları görünümü zaman GPU işleme sistemdeki diğer işlemleri adına istekleri bir kez temsil eder. Bu istekler GPU doğrudan bellek erişimi (DMA) paketleri gönderilir.  Bir segmenti uzunluğunu paket GPU tarafından işlendiği süreyi temsil eder.  
  
 Seçtiğinizde, bu tür bir segment, rapor üzerinde **geçerli** sekmesini işlenmiş paketi hakkında bilgileri görüntüler.  Bu bilgiler, DirectX altyapısı, paketi gönderilen işlem ve paket işlemek için gereken zamanı ile ilişkili donanım kuyruğundaki paket beklenen süre miktarını içerir.