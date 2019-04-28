---
title: 'Nasıl yapılır: CPU sayaç verileri toplama | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.performance.property.cpucounters
helpviewer_keywords:
- profiling tools, using portable CPU counters
- performance tools, portable CPU counters
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: c607263c6b6f6472258aaeab1c3187efaf30a120
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62973987"
---
# <a name="how-to-collect-cpu-counter-data"></a>Nasıl yapılır: CPU sayaç verileri toplama

CPU olay sayaç donanıma özgü performans verilerini toplamak için kullanılır. Bu makalede, yöntemi profil oluşturma Araçları'nı kullandığınızda, olay sayacı verilerini toplama işlemini göstermektedir.

İki tür CPU sayaç olaylarını gerçekleşir:

- Taşınabilir olayları - bağımsız olarak belirli CPU toplanabilir CPU olayları.

- Platform olayları - belirli bir CPU'ya bağlı CPU olayları'nı tıklatın.

  Taşınabilir olayları yönergeleri Çekildi ve olmayan durdurulamaz döngüleri gibi genel olayları, CPU arabellek olayları, dallanma olayları ve L2 önbellek olayları içerir. Kullanılabilir platformu olay sayaç işlemci üreticisi tarafından belirlenir.

  Olayların kategorilerini taşınabilir ve platform sayaçları arasında paylaşılabilir. Örneğin, aşağıdaki veri kategorileri için her iki tür sık ortaktır:

- Bellek olayları.

- Ön uç etkinlikleri.

- Dal etkinlikleri.

  İki şekilde profil oluşturucu performans sayacı verilerini toplayabilirsiniz:

- Ölçümlü izlemeyle profil, bir veya daha fazla sayaçlarından veri toplayın.

- Örnekleme tarafından profil, bir sayaç olay örnekleme aralığı belirtin. Daha fazla bilgi için [nasıl yapılır: Örnekleme olayları seçme](../profiling/how-to-choose-sampling-events.md).

## <a name="to-collect-cpu-performance-counter-data-when-you-profile-by-instrumentation"></a>Ölçümlü izlemeyle profil, CPU performans sayacı verilerini toplamak için

1. Performans oturum **özellik sayfaları**, tıklayın **CPU sayaçları.**

2. Seçin **CPU sayaçlarını Topla** onay kutusu.

3. Genişletin **ulaşılabilir performans sayaçları** toplamak istediğiniz örnek olaylar bulana kadar ağaç.

4. Toplamak istediğiniz her olay, olay seçin ve ardından olaya eklemek için sağ oka tıklayın **sayaçları seçildi** listesi.

    > [!NOTE]
    > **Ulaşılabilir performans sayaçları** yalnızca seçerseniz etkin **toplamak CPU sayaçları** onay kutusu.

## <a name="see-also"></a>Ayrıca bkz.

[Performans oturumlarını yapılandırma](../profiling/configuring-performance-sessions.md)
[performans oturumu özellikleri](../profiling/performance-session-properties.md)
[CPU ve Windows sayaçları](../profiling/cpu-and-windows-counters.md)
[nasıl yapılır: Örnekleme olayları seçme](../profiling/how-to-choose-sampling-events.md)