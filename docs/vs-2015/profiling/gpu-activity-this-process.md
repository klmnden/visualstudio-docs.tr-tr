---
title: GPU etkinliği (Bu işlem) | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.cv.threads.timeline.gpuexecution
- vs.cv.threads.timeline.gpuactivity
ms.assetid: 0956edbf-9bcd-4afe-9287-fda628648ca0
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: b616e307b3c42b09662be3fdad290ea9f740637c
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62434156"
---
# <a name="gpu-activity-this-process"></a>GPU Etkinliği (Bu İşlem)
**GPU etkinliği (Bu işlem)** kesimlerinde eşzamanlılık görselleştiricisi'ndeki iş parçacıkları görünümü zaman GPU işlem istekleri geçerli işlem adına bir kez temsil eder. Bu istekler GPU'ya doğrudan bellek erişimi (DMA) paketleri gönderilir. Segment uzunluğunu GPU DMA paket adına geçerli işlem işleme zamanı temsil eder.

 Üzerinde GPU etkinliği segment, raporun seçtiğinizde **geçerli** sekmesini işlenmiş DMA paket hakkında bilgileri görüntüler. Bu bilgiler, DirectX altyapısı, paketi gönderilen işlem ve paket işlemek için gereken zamanı ile ilişkili donanım kuyruğundaki paket beklenen süre miktarını içerir. Geçerli işlemin dışında bir işlem GPU DMA paketi fiziksel olarak gönderilen. Eşzamanlılık görselleştiricisi, başka bir işlem geçerli işlemin adına GPU iş gönderildiğinde algılayabilir.