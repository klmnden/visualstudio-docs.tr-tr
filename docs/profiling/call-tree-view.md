---
title: Çağrı ağacı görünümü | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.performance.view.calltree
helpviewer_keywords:
- Call Tree view
- profiling tools reports, Call Tree view
- performance reports, Call Tree view
- profiling tools, Call Tree view
ms.assetid: b2dbc033-bf95-4d10-8e51-f9462979133e
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 44bfbf4f5fb0a0b158d08254656d9c3831c77e86
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54948433"
---
# <a name="call-tree-view"></a>Çağrı Ağacı görünümü
Çağrı ağacı görünümü, profili oluşturulan uygulamada geçiş işlev yürütme yollarını görüntüler. Ağacının kökü, uygulama veya bileşen giriş noktasıdır. Her işlev düğümü, çağrılan işlevlerin ve bu işlev çağrıları ile ilgili performans verilerini listeler.  
  
 Çağrı ağacı görünümü ayrıca genişletin ve en çok zaman harcanan veya sık örneklenen bir işlev yürütme yolunu vurgulayın. Yolun en pahalı performans görüntülemek için işlev sağ tıklayın ve ardından **etkin yolu Genişlet**.  
  
 Profil oluşturma çalıştırmasını her işlem, bir kök düğümü olarak görüntülenir. Çağrı ağacı görünümü başlangıç düğümü başlangıç düğümü olarak ayarlamak istediğiniz düğüme sağ tıklayın ve ardından seçerek ayarlayabilirsiniz **kümesi kök**.  
  
 Kök düğümü ayarladığınızda, Seçili düğümün alt ağacı dışında görünümünden diğer tüm girişleri kaldırın. Görüntülemekte olduğunuz düğüme geri kök düğümü sıfırlayabilirsiniz. Çağrı ağacı Görünümü penceresi sağ tıklayın ve ardından **sıfırlama kök**.  
  
 Çağrı ağacı görünümü sütun ekleme veya kaldırma için özelleştirilebilir. Sağ **sütun adı başlık çubuğu**ve ardından **sütunları Ekle/Kaldır**.  
  
 Çağrı ağacı görünümü sunulan veri miktarını sınırlamak için gürültü azaltma yapılandırılabilir. Gürültü azaltma kullanarak performans sorunlarını Görünümü'nde daha belirgin. Performans sorunlarını kolayca ayırt etmek için analiz daha kolay olur. Daha fazla bilgi için [nasıl yapılır: Rapor görünümlerinde gürültü azaltmayı yapılandırma](../profiling/how-to-configure-noise-reduction-in-report-views.md).  
  
> [!NOTE]
>  Gürültü azaltma etkinleştirildiğinde, bir uyarı görüntüleyecek şekilde yapılandırılması durumunda rapora bir bilgi çubuğu görüntülenir.  
  
 Çağrı ağacı görünümü içinde sütunların tanımları hakkında daha fazla bilgi için aşağıdakilere bakın:  
  
 [Çağrı ağacı görünümü](../profiling/call-tree-view-sampling-data.md)  
  
 [Çağrı ağacı görünümü](../profiling/call-tree-view-instrumentation-data.md)  
  
 [Çağrı ağacı görünümü - örnekleme](../profiling/call-tree-view-dotnet-memory-sampling-data.md)  
  
 [Çağrı ağacı görünümü](../profiling/call-tree-view-contention-data.md)  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Performans raporu görünümleri](../profiling/performance-report-views.md)   
 [İzleme veri değerlerini anlama](../profiling/understanding-instrumentation-data-values.md)   
 [Örnekleme veri değerlerini anlama](../profiling/understanding-sampling-data-values.md)