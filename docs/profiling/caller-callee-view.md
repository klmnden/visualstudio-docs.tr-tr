---
title: Arayan-Aranan görünümü | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.performance.view.callercallee
helpviewer_keywords:
- profiling tools, reports, Caller/Callee view
- profiling tools, Caller/Callee view
- performance reports, Caller/Callee view
- Caller/Callee view
ms.assetid: d3511bcf-cce0-4cbe-aecb-b94c7c80ad1b
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 8a7960c871ff27a9b9825b47611df101ab625083
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54961380"
---
# <a name="callercallee-view"></a>Arayan/Aranan görünümü
Arayan/Aranan görünümü seçili işlev ve üst ve alt işlevleri için profil bilgilerini görüntüler. Arayan/Aranan görünümü üç Kılavuzlar içerir:  
  
 **Geçerli işlev** Orta Kılavuz ve bunun görüntülenen bilgi seçili işlev için profil oluşturmayı gösterir. Değerler, toplanan tüm işlev çağrıları profil oluşturma çalışması içerir.  
  
 **Geçerli işlevi çağırmış işlevler** üst kılavuz görüntülenir ve çağıran (üst) işlevi'öğesinden gelen çağrılar tarafından oluşturulan değerleri seçili (geçerli) işlevinin sayısını gösterir.  
  
 **Geçerli işlev tarafından çağrılan işlevler** alt kılavuz ve bunun görüntülenen geçerli işlev tarafından alt işlev çağrıldığında çağrılan (alt) işlevleri için seçili işlev bilgileri profil oluşturma gösterilmektedir.  
  
 Çağıran/çağrılan Görünümü'nde kullanılabilir olan sütunlarda veri toplamak için kullanılan profil oluşturma yöntemine (örnekleme veya Araçlar) bağlıdır ve .NET bellek verileri profil oluşturma çalışmasında toplanan açmasa da Çalıştır.  
  
 Rapor görünümü Orta kısmındaki geçerli işlevin herhangi bir görünümün diğer iki bölümü listelenen işlevlerin çift tıklayarak gereken farklı işlevi seçebilirsiniz. Rapor görünümü, değişiklikleri yansıtacak şekilde otomatik olarak güncelleştirilir.  
  
 Sütun adları tıklayarak verileri yeniden sıralayabilirsiniz. Ek sütunları çağıran/çağrılan görünümü eklenebilir. Daha fazla bilgi için [nasıl yapılır: Rapor görünümü sütunlarını özelleştirme](../profiling/how-to-customize-report-view-columns.md).  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Arayan/Aranan görünümü - örnekleme verileri](../profiling/caller-callee-view-sampling-data.md)   
 [Arayan/Aranan görünümü - izleme verileri](../profiling/caller-callee-view-instrumentation-data.md)   
 [Arayan/Aranan görünümü - .NET bellek izleme verileri](../profiling/caller-callee-view-net-memory-instrumentation-data.md)   
 [Arayan/Aranan görünümü - .NET bellek örnekleme verileri](../profiling/caller-callee-view-dotnet-memory-sampling-data.md)   
 [Arayan/Aranan görünümü - çakışma verileri](../profiling/caller-callee-view-contention-data.md)