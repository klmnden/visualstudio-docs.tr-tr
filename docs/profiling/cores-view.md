---
title: Çekirdek görünümü | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.performance.view.cores
helpviewer_keywords:
- Concurrency Visualizer, Cores View
ms.assetid: e47af672-9785-4899-bd45-4d9dda3c396f
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 3dea7eca97ed938271977fea8e8fa5e41dbd19aa
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53933709"
---
# <a name="cores-view"></a>Çekirdekler Görünümü
**Çekirdekler görünümü** iş parçacığı için mantıksal işlemci çekirdeği nasıl eşlendi gösterir (seçin **Çözümle** > **eşzamanlılık görselleştiricisi** başlatmak için Eşzamanlılık görselleştiricisi). Bu görünüm sunucu uygulamaları yazıyorsanız, iş parçacığı benzeşimini veya iş parçacığı havuzu Yönetimi'ni kullanarak önbellek performansını iyileştirmenize yardımcı olabilir. Da burada iş parçacığı benzeşimini kullanımını çekirdek arası geçiş sorununu worsened durumlarda incelemenize yardımcı olabilir. Çekirdekler görünümü, grafik ve bir gösterge olmak üzere iki bölümden sahiptir.  
  
 Graf y ekseni ve x eksenindeki zaman mantıksal çekirdek gösterir. Graftaki her iş parçacığı benzersiz bir renk sahiptir; böylece zamanla Çekirdekte hareketini izleyebilirsiniz. İş parçacıkları Bu grafikte gösterge alanında seçerek filtreleyebilirsiniz.  
  
 Açıklama alanına grafikte her renk girişi var. Her giriş, iş parçacığı rengi ve adı, çapraz-çekirdek bağlam anahtarları sayısı, toplam bağlam anahtarları sayısı ve çekirdekleri çaprazlayan bağlam anahtarlarının yüzdesi gösterilmektedir. Gösterge, azalan olarak çekirdekler arası bağlam anahtarları sayısına göre sıralanır. Görüntülenen zaman aralığı içinde yürütülen iş parçacıkları listeler.  Yakınlaştırma veya kaydırma listesi güncelleştirilir.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Eşzamanlılık görselleştiricisi](../profiling/concurrency-visualizer.md)   
 [Kullanım Görünümü](../profiling/utilization-view.md)   
 [İş Parçacıkları Görünümü](../profiling/threads-view-parallel-performance.md)