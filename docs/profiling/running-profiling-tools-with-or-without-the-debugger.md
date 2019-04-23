---
title: Profil oluşturma araçları ile veya hata ayıklayıcı olmadan çalıştırın | Microsoft Docs
ms.date: 11/04/2018
ms.topic: conceptual
ms.assetid: 3fcdccad-c1bd-4c67-bcec-bf33a8fb5d63
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 273dc6770f2928ed65d6a473b7f1986bc353687e
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60060819"
---
# <a name="run-profiling-tools-with-or-without-the-debugger"></a>Hata ayıklayıcı ile veya hata ayıklayıcı olmadan profil oluşturma araçları çalıştırma

Visual Studio performans ölçümlerini ve profil oluşturma araçları sunar. Gibi bazı araçlar **CPU kullanımı** ve **bellek kullanımı**, ile veya hata ayıklayıcı olmadan ve yayın çalıştırabilirsiniz veya hata ayıklama yapılandırmaları oluşturun. **Performans Profiler** gibi araçları **uygulama zaman çizelgesi** üzerinde hata ayıklama çalıştırabilir veya yayın oluşturur. Hata ayıklayıcı ile tümleşik Araçlar **tanılama araçları** penceresi ve **olayları** sekmesi yalnızca hata ayıklama oturumları sırasında çalıştırın.

>[!NOTE]
>Windows 7 ve daha sonra hata ayıklayıcı olmayan performans araçları kullanabilirsiniz. Hata ayıklayıcıyla tümleştirilmiş profil oluşturma araçları çalıştırmak için Windows 8 veya üzeri gereklidir.

Olmayan hata ayıklayıcısı **performans Profiler** ve hata ayıklayıcıyla tümleştirilmiş **tanılama araçları** farklı bilgi ve deneyimleri sağlar. Hata ayıklayıcıyla tümleştirilmiş araçları, kesme noktaları ve değişken değerlerini gösterir. Olmayan hata ayıklama araçları yakın sonuçları için son kullanıcı deneyimi sunar.

Hangi Araçlar ve sonuçları karar vermenize yardımcı olması için aşağıdaki noktaları göz önünde bulundurun:

- Dosya g/ç gibi dış performans sorunları veya ağ yanıt hızı sorunlarını olmaz hata ayıklayıcı veya hata ayıklayıcı olmayan araçları çok farklı görünür.
- CPU-yoğun çağrıları nedeniyle sorunlarda, sürüm ve hata ayıklama yapıları arasında önemli ölçüde performans farklar olabilir. Sorunu sürümde var olup olmadığını görmek için denetimi oluşturur.
- Sorun yalnızca hata ayıklama yapıları sırasında oluşursa hata ayıklayıcı olmayan araçları çalıştırmak gerekmez. İçin sürüm sorunları derleme, hata ayıklayıcı araçları daha fazla araştırma için yardımcı olacak karar.
- Yayın derlemeleri işlev çağrıları satır içi kullanım ve kullanılmayan kod yollarını ayıklama ve hata ayıklayıcı tarafından kullanılan yöntemler değişkenleri depolamak sabitler gibi iyileştirmeler sağlar. Hata ayıklayıcıyla tümleştirilmiş araçları performans numaraları daha az doğru olduklarından bu iyileştirmeler olmaması hata ayıklama derlemeleri.
- Özel durum ve modül yükleme olayları kesintiye gibi gerekli hata ayıklayıcı işlemler yaptığı gibi hata ayıklayıcının kendisi performans süreleri değişir.
- Yayın derleme performans numaraları **performans Profiler** araçlardır en hassas ve doğru. Hata ayıklayıcıyla tümleştirilmiş Aracı sonuçları diğer hata ayıklama ile ilgili ölçümleri ile Karşılaştırılacak ekseriyetle faydalıdır.

## <a name="BKMK_Quick_start__Collect_diagnostic_data"></a> Hata ayıklama sırasında profil oluşturma verilerini topla

Başlattığınızda seçerek Visual Studio'da hata ayıklama **hata ayıklama** > **hata ayıklamayı Başlat** ya basarak **F5**, **Tanılamaaraçları** penceresi varsayılan olarak görünür. El ile açmak için seçmeniz **hata ayıklama** > **Windows** > **tanılama araçlarını Göster**. **Tanılama araçları** penceresi olayları, işlem bellek ve CPU kullanımı hakkında bilgi gösterir.

![Tanılama Araçları](../profiling/media/diagnostictools-update1.png "tanılama araçları")

- Kullanım **ayarları** araç çubuğundaki görüntüleyip görüntülemeyeceğinizi seçin için simgesini **bellek kullanımı**, **UI analizi**, ve **CPU kullanımı**.

- Seçin **ayarları** içinde **ayarları** açmak için aşağı açılan **tanılama araçları özellik sayfaları** fazla.

- Visual Studio Enterprise çalıştırıyorsanız, etkinleştirebilir veya Visual Studio altında IntelliTrace devre dışı **Araçları** > **seçenekleri** > **IntelliTrace**.

Hata ayıklamayı durdurduğunuzda Tanılama oturumu sona erer.

Ayrıca görüntüleyebilirsiniz **tanılama araçları** için uzaktan hata ayıklama hedefleri. Uzaktan hata ayıklama ve profil oluşturma için Visual Studio uzaktan hata ayıklayıcı yüklendiğini ve uzak hedef üzerinde olmalıdır.
- Uzaktan hata ayıklama ve profil oluşturma masaüstü uygulaması projeleri için bkz. [uzaktan hata ayıklama](../debugger/remote-debugging.md).
- Uzaktan hata ayıklama ve profil oluşturma UWP uygulamaları için bkz. [uzak makinede hata ayıklama UWP uygulamaları](../debugger/run-windows-store-apps-on-a-remote-machine.md).

### <a name="the-events-tab"></a>Olaylar sekmesi

Bir hata ayıklama oturumu sırasında **olayları** sekmesinde **tanılama araçları** meydana gelen tanılama olayları penceresinde listeler. Kategori ön ekleri: **Kesme noktası**, **dosya**, ve diğerlerinin izin hızla listesi için bir kategori veya yoksa verdiğiniz kategorileri atlayın.

Kullanım **filtre** görünümü seçerek veya belirli olayların kategorilerini seçimini içine ve dışına olaylara filtre açılır.

![Tanılama olay filtresi](../profiling/media/diagnosticeventfilter.png "tanılama olay filtresi")

Olay listesinden belirli bir dizeyi bulmak için arama kutusunu kullanın. Dört olayları eşleşen "name" dize için arama sonuçlarını şunlardır:

![Tanılama Olay arama](../profiling/media/diagnosticseventsearch.png "Tanılama Olay arama")

Daha fazla bilgi için [arama ve filtreleme tanılama araçları penceresinin olaylar sekmesinde](https://devblogs.microsoft.com/devops/searching-and-filtering-the-events-tab-of-the-diagnostic-tools-window/).

## <a name="collect-profiling-data-without-debugging"></a>Hata ayıklama olmadan profil oluşturma verilerini topla

Hata ayıklama olmadan performans verilerini toplamak için çalıştırabileceğiniz **performans Profiler** araçları. Profil oluşturma araçlarından bazıları çalıştırmak için yönetici ayrıcalıkları gerektirir. Visual Studio'yu yönetici olarak açabileceğiniz veya Tanılama oturumu başlattığınızda, Araçlar yönetici olarak çalıştırabilirsiniz.

1. Projeyi Visual Studio'da Aç seçin **hata ayıklama** > **performans Profiler**, veya basın **Alt**+**F2**.

1. Tanılama başlatma sayfası üzerinde çalıştırılacak bir veya daha fazla araç seçin. Proje türü, işletim sistemi ve programlama dili için uygun olan araçlar görüntülenir. Seçin **tüm araçları Göster** Ayrıca bu Tanılama oturumu için devre dışı bırakılmış araçları görmek için. C# UWP uygulaması için yaptığınız seçimlere nasıl görünebileceği aşağıda verilmiştir:

   ![Tanılama Araçları](../profiling/media/diag_selecttool.png "DIAG_SelectTool")

1. Tanılama oturumu başlatmak için **Başlat**.

   Oturum çalışırken, bazı araçları gerçek zamanlı veri grafikleri tanılama araçları sayfasında görüntüler.

    ![Performans ve tanılama hub'ı hakkında veri toplamak](../profiling/media/pdhub_collectdata.png "Hub verileri toplama")

1. Tanılama oturumu sona erdirmek için seçin **toplamasını Durdur**.

   Analiz edilen verileri görüntüler üzerinde **rapor** sayfası.

Raporları kaydetme ve bunları açmak **son açılan oturumlar** tanılama araçlarını Başlat sayfasında listesi.

![Kaydedilen Tanılama oturumu dosyası açın](../profiling/media/pdhub_openexistingdiagsession.png "PDHUB_OpenExistingDiagSession")

### <a name="the-profiling-report"></a>Profil oluşturma raporu
 ![Tanılama araçları rapor](../profiling/media/diag_report.png "DIAG_Report")

|||
|-|-|
|![1. adım](../profiling/media/procguid_1.png "ProcGuid_1")|Zaman çizelgesi profil oluşturma oturumunun uzunluğunu, uygulama yaşam döngüsü etkinleştirme olaylarını ve kullanıcı işaretlerini gösterir.|
|![2. adım](../profiling/media/procguid_2.png "ProcGuid_2")|Mavi çubukları sürükleyip zaman çizelgesinde bir bölgeyi seçerek, raporu zaman çizelgesinin bir bölümüyle sınırlandırabilirsiniz.|
|![3. adım](../profiling/media/procguid_3.png "ProcGuid_3")|Her bir tanılama aracı, bir veya daha fazla ana grafikleri görüntüler. Tanılama oturumunuz birden fazla aracı sahipse tüm kullanıcıların ana grafikleri görüntülenir.|
|![4. adım](../profiling/media/procguid_4.png "ProcGuid_4")|Daralt ve her aracın bireysel grafikleri genişletin.|
|![5. adım](../profiling/media/procguid_6.png "ProcGuid_6")|Birden fazla aracı verilerini içerdiğinde, aracı ayrıntıları sekme altında toplanır.|
|![6. adım](../profiling/media/procguid_6a.png "ProcGuid_6a")|Alt rapor yarısı her aracı için bir veya daha fazla ayrıntı görünümleri gösterir. Görünümü zaman çizelgesi bölge seçerek filtreleyebilirsiniz.|

## <a name="run-diagnostic-sessions-on-installed-or-running-apps"></a>Tanılama oturumları üzerinde yüklü ya da çalışan uygulamaları çalıştırma

 Uygulamanızı Visual Studio projesinden başlayarak yanı sıra, tanılama oturumları alternatif hedefler üzerinde de çalıştırabilirsiniz. Örneğin, Windows App Store ' yüklenen bir uygulama üzerinde performans sorunlarını tanılayın isteyebilirsiniz.

 ![Tanılama araçları analiz hedefi seçin](../profiling/media/pdhub_chooseanalysistarget.png "PDHUB_ChooseAnalysisTarget")

 Zaten yüklü olan uygulamaları başlatabilir veya tanılama araçları, uygulamaları ve zaten çalışan işlemler ekleyin. Seçtiğinizde, **çalışan uygulama** veya **uygulamasının yüklü**, belirtilen dağıtım hedef uygulamaları bulduğu listesinden uygulamayı seçin. Bu hedef, yerel veya uzak bir makine olabilir.

 ![Tanılama için çalışan veya yüklü bir uygulama seçin](../profiling/media/pdhub_selectrunningapp.png "PDHUB_SelectRunningApp")

## <a name="see-also"></a>Ayrıca bkz.

Blog gönderileri ve MSDN makaleleri tanılama geliştirme ekibinin şunlardır:
- [MSDN Magazine: Visual Studio 2015'te hata ayıklama sırasında performansını çözümleme](https://msdn.microsoft.com/magazine/dn973013.aspx)

- [MSDN Magazine: Sorunları daha hızlı bir şekilde tanılamak için IntelliTrace'i kullanın](https://msdn.microsoft.com/magazine/dn973014.aspx)

- [Blog postası: Visual Studio 2015'te bellek kullanımı aracı ile olay işleyicisi sızıntılarını tanılama](https://devblogs.microsoft.com/devops/diagnosing-event-handler-leaks-with-the-memory-usage-tool-in-visual-studio-2015/)

- [Video: Microsoft Visual Studio içinde IntelliTrace geçmiş hata ayıklama Ultimate 2015](https://channel9.msdn.com/Events/Ignite/2015/BRK3716)

- [Video: Visual Studio 2015'i kullanarak performans sorunlarını ayıklama](https://channel9.msdn.com/Events/Build/2015/3-731)

- [PerfTips: Performans bilgileri bir Visual Studio ile hata ayıklarken bakışta](https://devblogs.microsoft.com/devops/perftips-performance-information-at-a-glance-while-debugging-with-visual-studio/)

- [Visual Studio 2015'te tanılama araçları hata ayıklayıcı penceresi](https://devblogs.microsoft.com/devops/diagnostic-tools-debugger-window-in-visual-studio-2015/)

- [Visual Studio Enterprise 2015'te IntelliTrace](https://devblogs.microsoft.com/devops/intellitrace-in-visual-studio-ultimate-2015/)
