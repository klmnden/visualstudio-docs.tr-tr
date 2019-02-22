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
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 9a502590c20fce1455d9259ae681178d9cd48e33
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56624158"
---
# <a name="gpu-activity-other-processes"></a>GPU Etkinliği (Diğer İşlemler)
**GPU etkinliği (diğer işlemler)** kesimlerinde eşzamanlılık görselleştiricisi iş parçacıkları görünümü zaman GPU işleme sistemdeki diğer işlemleri adına istekleri bir kez temsil eder. Bu istekler GPU doğrudan bellek erişimi (DMA) paketleri gönderilir.  Bir segmenti uzunluğunu paket GPU tarafından işlendiği süreyi temsil eder.

 Seçtiğinizde, bu tür bir segment, rapor üzerinde **geçerli** sekmesini işlenmiş paketi hakkında bilgileri görüntüler.  Bu bilgiler, DirectX altyapısı, paketi gönderilen işlem ve paket işlemek için gereken zamanı ile ilişkili donanım kuyruğundaki paket beklenen süre miktarını içerir.