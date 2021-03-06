---
title: 'Nasıl yapılır: Rapor görünümlerinde gürültü azaltmayı yapılandırma | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.performance.noisereduction.dialog
helpviewer_keywords:
- profiling tools, trimming
- profiling tools, report noise reduction
- profiling tools, folding
ms.assetid: b07e0375-bb73-47e3-8d1d-b9b492fb16c9
caps.latest.revision: 18
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 5871473eaba749833714d6382beb487702ebe02d
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63432763"
---
# <a name="how-to-configure-noise-reduction-in-report-views"></a>Nasıl yapılır: Rapor Görünümlerinde Gürültü Azaltmayı Yapılandırma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Performans raporları çağrı ağacı görünümü ve ayırma görünümünde görüntülenen veri miktarını sınırlamak için gürültü azaltma yapılandırılabilir. Gürültü azaltma kullanarak performans sorunlarını daha belirgin. Performans raporları çözümlemek istediğinizde yararlıdır.  
  
 Gürültü azaltma yapılandırma seçenekleri aşağıdaki ayarları içerir:  
  
- **Kırpma** rapor analiz edilirken görünümü içinde yapılandırdığınız, değer ve eşik ayarları izleyen kesme yordamında açıklandığı kalan işlevleri atlayacak. Varsayılan olarak, kırpma etkinleştirilir.  
  
- **Katlama** katlamayı etkinleştirirseniz, yapılandırdığınız ayarlarını karşılayan art arda gelen işlevlerle yola, izleyen kırılma yordamında açıklandığı birleştirilir. Varsayılan olarak, katlama varsayılan olarak etkindir.  
  
### <a name="to-configure-trimming-for-a-performance-report"></a>Bir performans raporu için kırpmayı yapılandırmak için  
  
1. Ne zaman bir çağrı ağacı görünümü veya ayırma görünümü görüntülenir oluşturulan raporda **Geliştirici** menüsünde tıklatın **Profiler** ve ardından **gürültü azaltma seçenekleri**.  
  
     **Gürültü azaltma** iletişim kutusu görüntülenir.  
  
2. Kırpma etkinleştirmek için aşağıdaki adımları izleyin:  
  
    1. Seçin **kırpmayı etkinleştirme**. Varsayılan ayar budur.  
  
        > [!NOTE]
        > Gürültü azaltma etkinleştirildiğinde, bir bilgi çubuğu raporunda görüntülenir. Daha fazla bilgi için [çağrı ağacı görünümü](../profiling/call-tree-view.md) ve [ayırma görünümü](../profiling/dotnet-memory-allocations-view.md).  
  
    2. Değer ayarı kullanarak yapılandırma **değer** aşağı açılan liste ve geçerli ayarı seçme.  
  
    3. Yüzde değerindeki yazarak istenen eşik ayarı yapılandırmak **eşiği** metin kutusu.  
  
    4. Oluşturulan rapor gürültüsünü azaltma uyarıda etkinleştirmek için seçin **gürültü azaltma etkinleştirildiğinde uyarı görüntüler**. Varsayılan ayar budur.  
  
3. Temizleyin, kırpma devre dışı bırakmak için **kırpmayı etkinleştirme**.  
  
4. **Tamam**'ı tıklatın.  
  
### <a name="to-configure-folding-for-a-performance-report"></a>Bir performans raporu için Katlama yapılandırmak için  
  
1. Üzerinde **Geliştirici** menüsünü tıklatın **Profiler** ve ardından **gürültü azaltma seçenekleri**.  
  
     **Gürültü azaltma** iletişim kutusu görüntülenir.  
  
2. Katlamayı etkinleştirmek için aşağıdaki adımları izleyin:  
  
    1. Seçin **katlamayı etkinleştirmek**. Varsayılan ayar budur.  
  
        > [!NOTE]
        > Gürültü azaltma etkinleştirildiğinde, bir bilgi çubuğu raporunda görüntülenir. Daha fazla bilgi için [çağrı ağacı görünümü](../profiling/call-tree-view.md) ve [ayırma görünümü](../profiling/dotnet-memory-allocations-view.md).  
  
    2. Değer ayarı kullanarak yapılandırma **değer** aşağı açılan liste ve geçerli ayarı seçme.  
  
    3. Yüzde değerindeki yazarak istenen eşik ayarı yapılandırmak **eşiği** metin kutusu.  
  
    4. Oluşturulan rapor gürültüsünü azaltma uyarıda etkinleştirmek için seçin **gürültü azaltma etkinleştirildiğinde uyarı görüntüler**. Varsayılan ayar budur.  
  
3. Katlama devre dışı bırakmak için işareti kaldırın **katlamayı etkinleştirmek**.  
  
4. **Tamam**'ı tıklatın.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Rapor görünümlerini özelleştirme performans araçları](../profiling/customizing-performance-tools-report-views.md)   
 [Nasıl yapılır: Hariç tutma veya kısa işlevleri izlemeden içerir](../profiling/how-to-exclude-or-include-short-functions-from-instrumentation.md)   
 [Çağrı ağacı görünümü](../profiling/call-tree-view.md)   
 [Ayırmalar Görünümü](../profiling/dotnet-memory-allocations-view.md)
