---
title: İşlem görünümü | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.performance.view.process
helpviewer_keywords:
- performance tools reports, process view
- Process view
- performance tools, process view
- Profiling Tools,process view
- Profiling Tools,process report
ms.assetid: 6d4e2a5d-9f17-4ece-a6f1-75836e1fc382
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: fe2e87613cc73682548c278942e17c59026828d6
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/26/2019
ms.locfileid: "55068972"
---
# <a name="process-view"></a>İşlem Görünümü
İşlem görünümü, profil oluşturma çalışması sırasında yürütülen iş parçacıkları ve işlemler için profil oluşturma verilerini görüntüler.  
  
 İşlem adına göre listelenmiştir. İş parçacıkları, onları oluşturan işlem alt düğümleri olarak listelenir. İş parçacıkları adlı etiketi veya iş parçacığı çalışmaya işlevi tarafından **[ntdll.dll]** sembol varsa.  
  
 Sütun ekleme veya kaldırma için görünümü sağ tıklayın ve ardından **sütunları Ekle/Kaldır**. Ayrıca, bir sütun adına tıklayarak verileri yeniden sıralayabilirsiniz. Daha fazla bilgi için [nasıl yapılır: Rapor görünümü sütunlarını özelleştirme](../profiling/how-to-customize-report-view-columns.md).  
  
 İşlem görünümü sütunlarını ve .NET bellek verileri içeren veri örnekleme ve izleme yöntemleri kullanarak oluşturulan verileri için aynıdır. Sütun değerleri aşağıdaki tabloda açıklanmaktadır.  
  
|Sütun|Açıklama|  
|------------|-----------------|  
|**Benzersiz kimliği**|İş parçacığı ve işlem için benzersiz olan bir profil oluşturucu tarafından oluşturulan bir tanımlayıcı.|  
|**ID**|Sistem tarafından oluşturulan bir tanımlayıcı işlem veya iş parçacığı.|  
|**Ad**|İşlem veya iş parçacığı adı.|  
|**Başlangıç zamanı**|Milisaniye veya işlemci sayısını, işlem veya iş parçacığı başına profil oluşturma başlangıç geçiş yapar.|  
|**Bitiş zamanı**|Milisaniye veya işlemci sayısını başından sonuna kadar işlem veya iş parçacığı profil oluşturma.|  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Örnekleme yöntemi veri görünümleri](../profiling/profiler-sampling-method-data-views.md)   
 [İzleme metodu veri görünümleri](../profiling/instrumentation-method-data-views.md)   
 [.NET bellek verisi görünümleri](../profiling/dotnet-memory-data-views.md)