---
title: Profil oluşturma araçları ile veya hata ayıklayıcı olmadan çalışan | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
ms.assetid: 3fcdccad-c1bd-4c67-bcec-bf33a8fb5d63
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: adb0180d892f34374ce58db3a4830fb7e5c21f10
ms.sourcegitcommit: bccb05b5b4e435f3c1f7c36ba342e7d4031eb398
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/06/2018
ms.locfileid: "51220989"
---
# <a name="run-profiling-tools-with-or-without-the-debugger"></a>Hata ayıklayıcı ile veya hata ayıklayıcı olmadan profil oluşturma araçları çalıştırma
Sunan Visual Studio artık, bir performans, tercih ettiğiniz araçları, bazıları (örneğin, **CPU kullanımı** ve **bellek kullanımı**) ile veya hata ayıklayıcı olmadan çalıştırın. Olmayan hata ayıklayıcı performans araçları yayın yapılandırmaları, hata ayıklayıcı ile tümleşik araçları hata ayıklama yapılandırmaları üzerinde çalıştırmak için tasarlanmış olsa da çalıştırmak üzere tasarlanmıştır.  

Windows 7 ve daha sonra hata ayıklayıcı olmadan profil oluşturma araçları kullanabilirsiniz. Windows 8 ve üzeri, hata ayıklayıcısı ile profil oluşturma araçları çalıştırmak için gereklidir (**tanılama araçları** pencere).
  
## <a name="should-i-run-the-tool-with-or-without-the-debugger"></a>Aracı ile veya hata ayıklayıcı olmadan çalıştırın?  
 Performans hata ayıklayıcı ile tümleşik araçları birçok nesnelerin interneti, hata ayıklayıcı olmayan araçları olamaz, örneğin kesme noktaları ayarlayın ve değişken değerleri denetlemenize olanak tanır. Olmayan hata ayıklama araçları yayımlanan uygulamanın kullanıcıların göreceği yakın bir deneyim sunar.  
  
 Ne tür bir aracı amacınız için doğru olduğuna karar vermenize yardımcı olabilecek bazı sorular şunlardır:  
  
1.  Sorun uygulama geliştirildiği bilgisayardakinden ya da bu bulundu, yayımlanmış bir sürüm bulundu?  
  
     Geliştirme sırasında ilgilendiğiniz sorun bulunursa, bir yayın performans araçları çalıştırdığınız gerekmez. Bir sürümde bulunmazsa, bir yayın yapılandırmasına sahip sorunu yeniden oluşturun ve sonra hata ayıklayıcı daha fazla araştırma için yardımcı olup olmadığına karar gerekir.  
  
2.  CPU-yoğun tarafından neden sorun işliyor?  
  
     Performans araçları ile veya hata ayıklayıcı olmadan çalışan çok fark yaratmak olmaması gerekir böylece birçok dosya g/ç veya ağ yanıtlama, gibi dış performans sorunları nedeniyle sorunlardır. Sorunu nedeniyle CPU yoğunluklu çağrıdır, sürüm ve hata ayıklama yapılandırmaları arasındaki fark önemli olabilir ve büyük olasılıkla gereken hata ayıklayıcı ile tümleşik araçları kullanarak önce sorun yayın yapıda var olup olmadığını denetleyin  
  
3.  Tam olarak performansını ölçmek ihtiyacınız ya da yaklaşık bir sayı kabul edilebilirdir?  
  
     Yapılar olmaması sürüm yapıları sağlayan bazı iyileştirmeler hata ayıklamak için örneğin satır içi işlev çağrıları ve sabitler, ayıklama kullanılmayan kod yollarını ve hata ayıklayıcı tarafından kullanılan bir şekilde depolanmasını değişkenleri. (Örneğin özel durum ve modül yükleme olayları kesintiye) hata ayıklama için gereken belirli işlemler gerçekleştirdiğinden hata ayıklayıcının kendisi performans süreleri değişir. Hata ayıklayıcı iyileştirmeler için hesap değildir ancak yine de hata ayıklama sırasında gerçekleştirilen diğer ilgili ölçümleri ile karşılaştırıldığında yararlı olabilir hata ayıklayıcısıyla tümleştirilmiş araçları performans numaraları daha düşüktür. Performans hata ayıklayıcı olmayan araçlarla yayın yapılandırmaları için daha kesin sayılardır.
  
##  <a name="BKMK_Quick_start__Collect_diagnostic_data"></a> Hata ayıklama sırasında profil oluşturma verilerini topla  
 Aşağıdaki bölümde, yerel olarak hata ayıklama ile ilgilidir. Bir cihaz veya uzaktan, sonraki bölümlerde hata ayıklama hata ayıklama hakkında bilgi edinebilirsiniz.  
  
1. Açık ayıklamak istediğiniz proje ardından **hata ayıklama** > **hata ayıklamayı Başlat** (veya **Başlat** araç çubuğunda veya **F5**).  
  
2. **Tanılama araçları** penceresi görünür otomatik olarak, bunu devre dışı bırakmış sürece. Pencereyi ayarlayıp yeniden getirmek için tıklayın **hata ayıklama** > **Windows** > **tanılama araçlarını Göster**.  
  
3. Verileri toplamak istediğiniz senaryoları çalıştırın.  
  
    Oturum çalışırken, olaylar, işlem belleğini ve CPU kullanımı hakkında daha fazla bilgi görebilirsiniz.  
  
    Aşağıdaki grafik gösterildiği **tanılama araçları** penceresi Visual Studio 2015 güncelleştirme 1'de:  
  
    ![DiagnosticTools&#45;güncelleştirme 1](../profiling/media/diagnostictools-update1.png "DiagnosticTools-güncelleştirme 1")  
  
4. Görmek isteyip istemediğinizi seçebilirsiniz **bellek kullanımı** veya **CPU kullanımı** (veya her ikisi) ile **seçtiğiniz Araçları** araç ayarlama. Visual Studio Enterprise çalıştırıyorsanız, etkinleştirebilir veya IntelliTrace içinde devre dışı **Araçları** > **seçenekleri** > **IntelliTrace**.  
  
5. Hata ayıklamayı durdurduğunuzda Tanılama oturumu sona erer.  
  
   Visual Studio 2015 güncelleştirme 1'de **tanılama araçları** penceresi kolaylaştırır, ilgilendiğiniz olay odaklanmak için.   Olay adları artık kategori ön ekleri gösterilir (**hareket**, **Program çıktısı**, **kesme noktası**, **dosya**, vs.) hızlı şekilde belirli bir kategorideki listesi veya hakkında umursamaz kategorileri atlayabilirsiniz.  
  
   Herhangi bir olay listesinden belirli bir dizeyi bulabilmesi penceresi artık bir arama kutusu sahiptir. Örneğin, aşağıdaki dize için arama sonuçlarının "dört olayları eşleşen Yükle" gösterir:  
  
   ![DiagnosticsEventSearch](../profiling/media/diagnosticseventsearch.png "DiagnosticsEventSearch")  
  
   Ayrıca, Görünüm penceresinde içine ve dışına olayları filtreleyebilirsiniz. İçinde **filtre** açılır listesinde, kontrol edin veya belirli olayların kategorilerini işaretini kaldırın:. Kategori adları önek adı ile aynıdır.  
  
   ![DiagnosticEventFilter](../profiling/media/diagnosticeventfilter.png "DiagnosticEventFilter")  
  
   Daha fazla bilgi için [arama ve filtreleme tanılama araçları penceresinin olaylar sekmesinde](https://blogs.msdn.microsoft.com/devops/2015/11/12/searching-and-filtering-the-events-tab-of-the-diagnostic-tools-window/).  
  
## <a name="collect-profiling-data-without-debugging"></a>Hata ayıklama olmadan profil oluşturma verilerini topla  
 Bazı profil oluşturma araçları çalıştırmak için yönetici ayrıcalıkları gerektirir. Visual Studio'yu yönetici olarak başlatın veya Tanılama oturumu başlattığınızda araçları yönetici olarak çalıştırmak seçebilirsiniz.  
  
1. Projeyi Visual Studio'da açın.  
  
2. Üzerinde **hata ayıklama** menüsünde seçin **performans Profiler** (kısayol tuşu: **Alt**+**F2**).  
  
3. Tanılama başlatma sayfasında oturumunda çalıştırmak için bir veya daha fazla araç seçin. Proje türü, işletim sistemi ve programlama dili için uygun olan araçlar görüntülenir. Bir tanılama aracı seçtiğinizde, aynı Tanılama oturumu çalıştırılamaz araçları seçimlerini devre dışı bırakıldı. C# UWP uygulaması için yaptığınız seçimlere nasıl görünebileceği aşağıda verilmiştir:  
  
    ![Tanılama Araçları](../profiling/media/diag_selecttool.png "DIAG_SelectTool")  
  
4. Tanılama oturumu başlatmak için tıklatın **Başlat**.  
  
5. Verileri toplamak istediğiniz senaryoları çalıştırın.  
  
    Oturum çalışırken bazı araçlar gerçek zamanlı veri grafikleri tanılama araçlarını Başlat sayfasında görüntüler.  
  
    ![Performans ve tanılama fası üzerinde veri toplama](../profiling/media/pdhub_collectdata.png "PDHUB_CollectData")  
  
6. Tanılama oturumu sona erdirmek için tıklatın **koleksiyonu Durdur**.  
  
   Bir tanılama oturumu veri toplamayı durdurduğunuzda, veriler, analiz ve Tanılama sayfasında rapor görüntülenir.  
  
   Ayrıca, tanılama araçları en son açılan listeden dosyalarda sayfasını başlatmak kaydedilmiş .diagnostic oturum açabilirsiniz.  
  
   ![Kaydedilen Tanılama oturumu dosyası açın](../profiling/media/pdhub_openexistingdiagsession.png "PDHUB_OpenExistingDiagSession")  
  
## <a name="the-profiling-report"></a>Profil oluşturma raporu  
 ![Tanılama araçları rapor](../profiling/media/diag_report.png "DIAG_Report")  
  
|||  
|-|-|  
|![1. adım](../profiling/media/procguid_1.png "ProcGuid_1")|Zaman çizelgesi profil oluşturma oturumunun uzunluğunu, uygulama yaşam döngüsü etkinleştirme olaylarını ve kullanıcı işaretlerini gösterir.|  
|![2. adım](../profiling/media/procguid_2.png "ProcGuid_2")|Mavi çubukları sürükleyip zaman çizelgesinde bir bölgeyi seçerek, raporu zaman çizelgesinin bir bölümüyle sınırlandırabilirsiniz.|  
|![3. adım](../profiling/media/procguid_3.png "ProcGuid_3")|Bir aracı, bir veya daha fazla ana grafikleri görüntüler. Tanılama oturumunuz birden çok araçları ile oluşturulursa tüm ana grafikleri görüntülenir.|  
|![4. adım](../profiling/media/procguid_4.png "ProcGuid_4")|Daralt ve bireysel grafikleri genişletin.|  
|![5. adım](../profiling/media/procguid_6.png "ProcGuid_6")|Verilerinizi birden çok Araçları'ndan bilgi içerdiğinde, aracı ayrıntıları sekme altında toplanır.|  
|![6. adım](../profiling/media/procguid_6a.png "ProcGuid_6a")|Bir aracı, bir veya daha fazla ayrıntı görünümleri olabilir. Görünümü, zaman çizelgesinin seçili bölgeye göre filtrelenir.|  
  
## <a name="set-the-analysis-target-to-another-device"></a>Analiz hedefi için başka bir cihaz ayarlama  
 Uygulamanızı Visual Studio projesinden başlayarak yanı sıra, tanılama oturumları alternatif hedefler üzerinde de çalıştırabilirsiniz. Örneğin, sürümünü, Windows App Store ' yüklenen uygulama performans sorunlarını tanılayın isteyebilirsiniz.  
  
 ![Tanılama araçları analiz hedefi seçin](../profiling/media/pdhub_chooseanalysistarget.png "PDHUB_ChooseAnalysisTarget")  
  
 Bir cihazda zaten yüklü olan uygulamaları başlatabilir veya çalışmakta olan bazı uygulamalar için tanılama araçları ekleyebilirsiniz. Seçeneğini belirlediğinizde **çalışan uygulama** veya **uygulamasının yüklü**, bulur belirtilen dağıtım hedefi üzerinde uygulamalar listesinden uygulamayı seçin.  
  
 ![Tanılama için çalışan veya yüklü bir uygulama seçin](../profiling/media/pdhub_selectrunningapp.png "PDHUB_SelectRunningApp")  
  
 Seçeneğini belirlediğinizde **Internet Explorer**URL'sini belirtin ve telefon dağıtım hedefi değiştirebilirsiniz.  
  
 ![Internet Explorer'da görüntülemek için URL'yi belirtin](../profiling/media/pdhub_choosephoneanalysistarget.png "PDHUB_ChoosePhoneAnalysisTarget")  
  
## <a name="remote-debugging"></a>Uzaktan Hata Ayıklama  
 Tanılama oturumu uzak bir bilgisayar veya tablette çalışan, Visual Studio uzak araçları yüklü ve uzak hedef üzerinde olmasını gerektirir. Masaüstü uygulamaları için bkz: [uzaktan hata ayıklama](../debugger/remote-debugging.md).  UWP uygulamaları için bkz: [uzak bir makinede çalıştırmak UWP uygulamaları](../debugger/run-windows-store-apps-on-a-remote-machine.md).  
  
## <a name="blog-posts-and-msdn-articles-from-the-diagnostics-development-team"></a>Blog gönderileri ve tanılama geliştirme ekibinin MSDN makaleleri  
 [MSDN Magazine: Visual Studio 2015'te hata ayıklama sırasında performansını çözümleme](https://msdn.microsoft.com/magazine/dn973013.aspx)
  
 [MSDN Magazine: IntelliTrace sorunlarını daha hızlı bir şekilde tanılamak için kullanın.](https://msdn.microsoft.com/magazine/dn973014.aspx)
  
 [Blog gönderisi: olay işleyicisi sızıntılarını ile bellek kullanımı aracı Visual Studio 2015'te tanılama](https://blogs.msdn.microsoft.com/devops/2015/04/29/diagnosing-event-handler-leaks-with-the-memory-usage-tool-in-visual-studio-2015/)
  
 [Video: Geçmiş Microsoft Visual Studio'da IntelliTrace ile hata ayıklama Ultimate 2015](https://channel9.msdn.com/Events/Ignite/2015/BRK3716)
  
 [Video: Visual Studio 2015'i kullanarak performans sorunlarını hata ayıklama](https://channel9.msdn.com/Events/Build/2015/3-731)
  
 [PerfTips: Performans bilgilerini bir bakışta Visual Studio ile hata ayıklama sırasında](https://blogs.msdn.microsoft.com/devops/2014/08/18/perftips-performance-information-at-a-glance-while-debugging-with-visual-studio/)
  
 [Visual Studio 2015'te tanılama araçları hata ayıklayıcı penceresi](https://blogs.msdn.microsoft.com/devops/2015/01/16/diagnostic-tools-debugger-window-in-visual-studio-2015/)
  
 [Visual Studio Enterprise 2015'te IntelliTrace](https://blogs.msdn.microsoft.com/devops/2015/01/16/intellitrace-in-visual-studio-ultimate-2015/)
