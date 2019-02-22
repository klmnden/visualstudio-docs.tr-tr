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
ms.openlocfilehash: 5a68a2a9f0ca96b943c0b09da5c60268963bc6a7
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56608246"
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
- [Örnekleme yöntemi veri görünümleri](../profiling/profiler-sampling-method-data-views.md)
- [İzleme metodu veri görünümleri](../profiling/instrumentation-method-data-views.md)
- [.NET bellek verisi görünümleri](../profiling/dotnet-memory-data-views.md)