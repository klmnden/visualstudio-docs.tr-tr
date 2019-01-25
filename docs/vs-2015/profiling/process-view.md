---
title: İşlem görünümü | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
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
caps.latest.revision: 17
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 0436401c458a7d6771a2785028a8b5fe0ef57546
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54802333"
---
# <a name="process-view"></a>İşlem Görünümü
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

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
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Örnekleme yöntemi veri görünümleri](../profiling/profiler-sampling-method-data-views.md)   
 [İzleme metodu veri görünümleri](../profiling/instrumentation-method-data-views.md)   
 [.NET Bellek Verisi Görünümleri](../profiling/dotnet-memory-data-views.md)
