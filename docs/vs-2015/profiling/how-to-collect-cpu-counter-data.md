---
title: 'Nasıl yapılır: CPU sayaç verileri toplama | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.performance.property.cpucounters
helpviewer_keywords:
- profiling tools, using portable CPU counters
- performance tools, portable CPU counters
ms.assetid: 102fb6ca-5fbf-4b05-925f-56912ce3f44b
caps.latest.revision: 26
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 2a774ce8b36ceddb4d4b53f90c63bec30acc0273
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54762938"
---
# <a name="how-to-collect-cpu-counter-data"></a>Nasıl yapılır: CPU sayaç verileri toplama
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

CPU olay sayaç donanıma özgü performans verilerini toplamak için kullanılır. Bu konuda yöntemi profil oluşturma Araçları'nı kullandığınızda olay sayacı verilerini nasıl toplayacağınızı gösterilmektedir.  
  
 **Gereksinimler**  
  
- [!INCLUDE[vsUltLong](../includes/vsultlong-md.md)], [!INCLUDE[vsPreLong](../includes/vsprelong-md.md)], [!INCLUDE[vsPro](../includes/vspro-md.md)]  
  
  İki tür CPU sayaç olaylarını gerçekleşir:  
  
- Taşınabilir olayları - bağımsız olarak belirli CPU toplanabilir CPU olayları.  
  
- Platform olayları - belirli bir CPU'ya bağlı CPU olayları'nı tıklatın.  
  
  Taşınabilir olayları yönergeleri Çekildi ve olmayan durdurulamaz döngüleri gibi genel olayları, CPU arabellek olayları, dallanma olayları ve L2 önbellek olayları içerir. Kullanılabilir platformu olay sayaç işlemci üreticisi tarafından belirlenir.  
  
  Olayların kategorilerini taşınabilir ve platform sayaçları arasında paylaşılabilir. Örneğin, aşağıdaki veri kategorileri için her iki tür sık ortaktır:  
  
- Bellek olayları.  
  
- Ön uç etkinlikleri.  
  
- Dal etkinlikleri.  
  
  Profiler iki yolla performans sayacı verilerini toplayabilirsiniz:  
  
- Ölçümlü izlemeyle profil, bir veya daha fazla sayaçlarından veri toplayın.  
  
- Örnekleme tarafından profil, bir sayaç olay örnekleme aralığı belirtin. Daha fazla bilgi için [nasıl yapılır: Örnekleme olayları seçme](../profiling/how-to-choose-sampling-events.md).  
  
### <a name="to-collect-cpu-performance-counter-data-when-you-profile-by-instrumentation"></a>Ölçümlü izlemeyle profil, CPU performans sayacı verilerini toplamak için  
  
1.  Performans oturum **özellik sayfaları**, tıklayın **CPU sayaçları.**  
  
2.  Seçin **CPU sayaçlarını Topla** onay kutusu.  
  
3.  Genişletin **ulaşılabilir performans sayaçları** toplamak istediğiniz örnek olaylar bulana kadar ağaç.  
  
4.  Toplamak istediğiniz her olay, olay seçin ve ardından olaya eklemek için sağ oka tıklayın **sayaçları seçildi** listesi.  
  
    > [!NOTE]
    >  **Ulaşılabilir performans sayaçları** yalnızca seçerseniz etkin **toplamak CPU sayaçları** onay kutusu.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Performans oturumlarını yapılandırma](../profiling/configuring-performance-sessions.md)   
 [Performans oturum özellikleri](../profiling/performance-session-properties.md)   
 [CPU ve Windows sayaçları](../profiling/cpu-and-windows-counters.md)   
 [Nasıl yapılır: Örnekleme Olaylarını Seçme](../profiling/how-to-choose-sampling-events.md)
