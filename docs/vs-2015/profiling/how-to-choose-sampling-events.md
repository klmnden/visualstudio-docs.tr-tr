---
title: 'Nasıl yapılır: Örnekleme olayları seçme | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.performance.property.sampling
helpviewer_keywords:
- clock cycles sample event
- sample events, choosing
- profiling tools, sample events
- page faults sample event
- system calls sample event
- performance counter sample event
- performance tools, sample events
ms.assetid: ce7cb734-80ac-4930-a4ef-e24395e1cc07
caps.latest.revision: 28
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 017414bdbf8e0e1a3a664782aab1ea44bda030c4
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63432831"
---
# <a name="how-to-choose-sampling-events"></a>Nasıl yapılır: Örnekleme olayları seçme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Varsayılan olarak, [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] profil oluşturma araçları profili oluşturulmuş bir işlem tarafından kullanılan işlemci döngülerini sayısı olarak belirtilen bir aralıkta performans verilerini toplar. Varsayılan döngüsü bir aralıkta 10,000,000, yaklaşık 1 GH bilgisayarda 0,01 saniye olan sayısıdır. Bir aralıktaki döngüsü sayısını değiştirebilirsiniz ve örnek olay değiştirebilirsiniz. Aşağıdaki örnek olayları kullanılabilir:  
  
- Saat döngüsü - CPU bağımlı sorunları için.  
  
- Sayfa hataları - bellek ile ilgili sorunlar için.  
  
- Sistem çağrıları - ı GÇ ile ilgili sorunlar için.  
  
- Performans sayacı - alt düzey performans sorunları için CPU sayaçları.  
  
> [!IMPORTANT]
> .NET bellek verileri (ayırmalar veya nesne kullanım ömrü veya her ikisi de) örnekleme yöntemini kullanarak topladığınız gerekirse tüm kullanıcı tarafından belirtilen örnekleme olayları göz ardı edilir ve uygun bellek ayırmaları veya çöp toplama olayları veya her ikisi de, veri toplamak üzere kullanılır.  
  
### <a name="to-select-a-sample-event"></a>Örnek olay seçmek için  
  
1. İçinde **performans Gezgini**performans oturumu sağ tıklayın ve ardından **özellikleri**.  
  
2. İçinde **özellik sayfaları**, tıklayın **örnekleme** özellikleri.  
  
3. Gelen **örnek olay** aşağı açılan listesinde, uygulamanızın profilini için kullanmak istediğiniz örnek olayı seçin.  
  
    > [!NOTE]
    > **Ulaşılabilir performans sayaçları** yalnızca seçerseniz etkin **performans sayacı** gelen **örnek olay** aşağı açılan listesi.  
  
4. Seçerseniz **performans sayacı**, alınan belirli bir CPU sayaçlarını seçin **ulaşılabilir performans sayaçları** ağaç görünümü denetimi.  
  
    - İçindeki sayaçları **taşınabilir olayları** düğüm tüm işlemcilerin türlerinde kullanılabilir.  
  
    - İçindeki sayaçları **Platform olaylarını** düğümü geçerli bilgisayarda işlemci özgüdür ve diğer türde işlemci kullanılabilir olmayabilir.  
  
5. Örnek olay seçtiğinizde, varsayılan bir örnekleme aralığı değeri görüntülenen **örnekleme aralığı** metin kutusu. Gerekirse, metin kutusuna istediğiniz değer girebilirsiniz.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Performans oturumlarını yapılandırma](../profiling/configuring-performance-sessions.md)   
 [Nasıl yapılır: Koleksiyon metotları seçme](../profiling/how-to-choose-collection-methods.md)   
 [CPU ve Windows sayaçları](../profiling/cpu-and-windows-counters.md)   
 [Örnekleme veri değerlerini anlama](../profiling/understanding-sampling-data-values.md)   
 [Komut Satırından Profil Oluşturma](../profiling/using-the-profiling-tools-from-the-command-line.md)
