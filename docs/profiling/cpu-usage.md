---
title: Visual Studio'da CPU kullanımını analiz etme | Microsoft Docs
ms.custom: H1Hack27Feb2017
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
ms.assetid: 7501a20d-04a1-480f-a69c-201524aa709d
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 1f63e4f43db3f8c4b24b43bda02cf00b52befc94
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49842189"
---
# <a name="analyze-cpu-usage"></a>CPU kullanımını analiz etme
Uygulamanızdaki performans sorunlarını araştırmak gerektiğinde başlatmak için iyi bir yerdir, CPU kullanma anlamaktır. **CPU kullanımı** aracı gösterir, burada CPU, Visual C++, Visual C# ' ı yürütürken zaman harcadığı yerleri / Visual Basic ve JavaScript kodu. Visual Studio 2015 güncelleştirme 1'de başlayarak, hata ayıklayıcı çıkmadan bir işlev başına kırılımını CPU kullanımının görebilirsiniz. Hata ayıklama sırasında CPU açıp profil açın ve yürütme, örneğin bir kesme noktasında kesildiğinde sonuçları görüntüleyin.  
  
Çalıştıran ve tanılama oturumunuzu yönetmek için birkaç seçeneğiniz vardır. Örneğin, çalıştırabileceğiniz **CPU kullanımı** aracı yerel veya uzak makinelerde veya açık bir simülatörü veya öykünücü. Visual Studio, çalışan bir uygulama için bağlı açık bir projedeymiş performansını analiz ya da Microsoft Store yüklü olduğu bir uygulamayı başlatın. Daha fazla bilgi için [çalıştırma profil oluşturma araçları ile veya hata ayıklayıcı olmadan](../profiling/running-profiling-tools-with-or-without-the-debugger.md). 

Burada, toplamak ve sürüm yapıları ile CPU kullanımını analiz etme nasıl gösteriyoruz. Hata ayıklama sırasında CPU kullanımını analiz etme hakkında bilgi için bkz: [performans profili oluşturma Başlangıç Kılavuzu](../profiling/beginners-guide-to-performance-profiling.md).

Windows 7 veya üzeri olan bu makalede gösterilen profil oluşturma aracı kullanmak için gerekli [performans Profiler](../profiling/profiling-feature-tour.md).
  
##  <a name="collect-cpu-usage-data"></a>CPU kullanım verileri toplama  
  
1. Visual Studio'da çözüm yapılandırması ayarlanmış **yayın** ve dağıtım hedefini seçin.  
  
    ![Yayın ve yerel makine seçin](../profiling/media/cpuuse_selectreleaselocalmachine.png "CPUUSE_SelectReleaseLocalMachine")  
  
   -   Uygulamayı çalışır durumda **yayın** modu gerçek uygulamanızın performansını daha iyi bir görünümünü sağlar.  
  
   -   Uygulamayı yerel makinede en iyi çalışan yüklü uygulama yürütülmesini çoğaltır.  
  
   -   Uzak bir CİHAZDAN veri topluyorsanız, uygulamayı doğrudan cihazda ve Uzak Masaüstü bağlantısı kullanarak değil çalıştırın.  
  
   -   Windows Phone uygulamaları için doğrudan veri toplama **cihaz** en doğru veriler sağlar.  
  
2. Üzerinde **hata ayıklama** menüsünde seçin **performans Profiler**.  
  
3. Seçin **CPU kullanımı** seçip **Başlat**.  
  
    ![CPU kullanımı seçin](../profiling/media/cpuuse_lib_choosecpuusage.png "CPUUSE_LIB_ChooseCpuUsage")  
  
4. Uygulama başlatıldığında tıklayın **alma sınırı**. Çıkış görüntülendikten sonra ikinci bir bekleyin ve ardından **alma en fazla sayı Async**. Düğme tıklamaları yapar bekleyen düğme yalıtmak daha kolay tıklayın tanılama raporu yordamları.  
  
5. İkinci çıktı satırı göründükten sonra seçin **toplamasını Durdur** performans ve tanılama hub'ında.  
  
   ![CpuUsage veri toplamayı Durdur](../profiling/media/cpu_use_wt_stopcollection.png "CPU_USE_WT_StopCollection")  
  
   CPU kullanımı aracı verileri çözümler ve rapor görüntüler.  
  
   ![CpuUsage rapor](../profiling/media/cpu_use_wt_report.png "CPU_USE_WT_Report")  
  
## <a name="analyze-the-cpu-usage-report"></a>CPU kullanım raporunu analiz etme  
  
###  <a name="BKMK_The_CPU_Usage_call_tree"></a> CPU kullanımı çağrı ağacı  
 Çağrı ağacı bilgileri anlama kullanmaya başlamak için yeniden `GetMaxNumberButton_Click` segmentlere ayırın ve çağrı ağacı ayrıntılarını inceleyin.  
  
####  <a name="BKMK_Call_tree_structure"></a> Çağrı ağacı yapısı  
 ![GetMaxNumberButton&#95;tıklayın çağrı ağacı](../profiling/media/cpu_use_wt_getmaxnumbercalltree_annotated.png "CPU_USE_WT_GetMaxNumberCallTree_annotated")  
  
|||  
|-|-|  
|![1. adım](../profiling/media/procguid_1.png "ProcGuid_1")|CPU kullanımı çağrı ağaçları en üst düzey düğüm sözde düğümüdür|  
|![2. adım](../profiling/media/procguid_2.png "ProcGuid_2")|Çoğu uygulama, zaman **harici kodu Göster** seçeneği devre dışıdır, ikinci düzey düğüm bir **[harici kod]** başlatır ve durdurur, uygulamanın sistem ve framework kodu içeren bir düğüm UI çizer iş parçacığı zamanlama denetler ve uygulamayı diğer alt düzey hizmetler sağlar.|  
|![3. adım](../profiling/media/procguid_3.png "ProcGuid_3")|İkinci düzey düğümünün alt öğeleri, kullanıcı kodu yöntemleri ve çağrılan veya framework kodu ve ikinci düzey sistem tarafından oluşturulan zaman uyumsuz yordamlarını verilmiştir.|  
|![4. adım](../profiling/media/procguid_4.png "ProcGuid_4")|Bir yöntemin alt düğümleri yalnızca üst yöntem çağrıları için veri içerir. Zaman **harici kodu Göster** olduğundan devre dışı, uygulama yöntemlerini de içerebilir bir **[harici kod]** düğümü.|  
  
####  <a name="BKMK_External_Code"></a> Dış kod  
 Dış kod yazdığınız kod tarafından yürütülen sistem ve framework bileşenlerinin işlevleri olan. Dış kod Başlat ve uygulamayı durdurun, UI çizme, iş parçacığı oluşturma denetleyen ve uygulama diğer alt düzey hizmetler sağlayan işlevler içerir. Çoğu durumda, dış kod içinde olacak ve bu nedenle CPU kullanımı çağırma ağacı toplar harici işlevler kullanıcı yöntemi birine **[harici kod]** düğümü.  
  
 Dış kod arama yollarını görüntülemek istediğinizde seçin **harici kodu Göster** gelen **filtre görünümü** listeleyin ve ardından **Uygula**.  
  
 ![Filtre görünümü seçin, ardından dış Kodu Göster](../profiling/media/cpu_use_wt_filterview.png "CPU_USE_WT_FilterView")  
  
 Böylece işlev adı sütun genişliğini tüm bilgisayar monitörü en büyük görüntü genişliğini aşabilir birçok dış kod arama zincirleri iç içe girmiş olduğunu, unutmayın. Bu durumda, işlev adları olarak gösterilir **[...]** :  
  
 ![Çağrı ağacında dış kod iç içe geçmiş](../profiling/media/cpu_use_wt_showexternalcodetoowide.png "CPU_USE_WT_ShowExternalCodeTooWide")  
  
 Aradığınız bir düğüm bulmak için arama kutusunu kullanın ve ardından verilerin görüntülenebilmesi için yatay kaydırma çubuğunu kullanın:  
  
 ![İç içe geçmiş bir dış kod arama](../profiling/media/cpu_use_wt_showexternalcodetoowide_found.png "CPU_USE_WT_ShowExternalCodeTooWide_Found")  
  
###  <a name="BKMK_Call_tree_data_columns"></a> Ağaç veri sütunları arayın  
  
|||  
|-|-|  
|**Toplam CPU (%)**|![Toplam % veri Denklem](../profiling/media/cpu_use_wt_totalpercentequation.png "CPU_USE_WT_TotalPercentEquation")<br /><br /> Seçili zaman aralığındaki işlevi ve işlev tarafından çağırılan işlevlerde yapılan çağrılar tarafından kullanılan uygulamanın CPU etkinliği yüzdesi. Bu farklı olduğunu unutmayın **CPU kullanımı** toplam etkinlik uygulamanın toplam kullanılabilir CPU kapasitesi için bir zaman aralığında karşılaştıran zaman çizelgesi grafiği.|  
|**Kendi kendine CPU (%)**|![Kendi kendine % Denklem](../profiling/media/cpu_use_wt_selflpercentequation.png "CPU_USE_WT_SelflPercentEquation")<br /><br /> İşlev tarafından çağırılan işlevlerdeki etkinlik hariç bu işleve yapılan çağrılar tarafından kullanılan seçili zaman aralığındaki uygulamanın CPU etkinliği yüzdesi.|  
|**Toplam CPU (ms)**|Seçili zaman aralığındaki işlevi ve işlev tarafından çağrılan işlevler çağrılarında harcanan milisaniye sayısı.|  
|**Kendi kendine CPU (ms)**|Seçili zaman aralığındaki işlevi ve işlev tarafından çağırılan işlevlerdeki etkinlik hariç bu işlev tarafından çağrılan işlevler çağrılarında harcanan milisaniye sayısı.|  
|**Modülü**|İşlev veya bir [harici kod] düğümünde işlevler içeren modül sayısı içeren modül adı.|  
  
###  <a name="BKMK_Asynchronous_functions_in_the_CPU_Usage_call_tree"></a> Zaman uyumsuz işlevleri CPU kullanımına çağrı ağacı  
 Derleyici, zaman uyumsuz bir yöntem karşılaştığında, yöntemin yürütmesini denetlemek için gizli bir sınıf oluşturur. Kavramsal olarak, derleyicinin ürettiği işlevleri, özgün metodun işlemlerini zaman uyumsuz olarak çağırın ve geri çağırmaları, Zamanlayıcı ve doğru bir şekilde yürütmek için gerekli yineleyiciler listesini içeren bir durum makinesindeki bir sınıftır. Özgün yöntemi tarafından bir üst yöntem çağrıldığında, çalışma zamanı üst yürütme bağlamında yöntemi kaldırır ve gizli sınıfı yöntemleri uygulamanın yürütmesini denetlemek sistem ve framework kod bağlamında çalışır. Zaman uyumsuz yöntemler genellikle, ancak her zaman, bir veya daha fazla farklı iş parçacıkları üzerinde yürütülür. Bu kod CPU kullanımı çağrı ağacında altı olarak gösterilen **[harici kod]** düğümünün üst ağaç düğümünü hemen altındaki.  
  
 Bu örneğimizde görmek için yeniden seçin `GetMaxNumberAsyncButton_Click` zaman çizelgesi segmenti.  
  
 ![GetMaxNumberAsyncButton&#95;tıklayın rapor seçim](../profiling/media/cpu_use_wt_getmaxnumberasync_selected.png "CPU_USE_WT_GetMaxNumberAsync_Selected")  
  
 İlk iki düğüm altında **[harici kod]** durum makine sınıfın derleyici tarafından oluşturulan yöntemler. Üçüncü özgün yöntem çağrısı var. Oluşturulan yöntemler genişletme neler olduğunu gösterir.  
  
 ![GetMaxNumberAsyncButton Genişletilmiş&#95;tıklayın çağrı ağacı](../profiling/media/cpu_use_wt_getmaxnumberasync_expandedcalltree.png "CPU_USE_WT_GetMaxNumberAsync_ExpandedCallTree")  
  
-   `MainPage::GetMaxNumberAsyncButton_Click` çok az yapar; Görev değerlerin bir listesini yönetir, en fazla sonuçları hesaplar ve çıktıyı görüntüler.  
  
-   `MainPage+<GetMaxNumberAsyncButton_Click>d__3::MoveNext` zamanlama ve çağrısını sarmalamak 48 görevleri başlatmak için gereken etkinlik gösterir `GetNumberAsync`.  
  
-   `MainPage::<GetNumberAsync>b__b` çağıran görevler etkinliğini gösterir `GetNumber`.
