---
title: Anlık görüntü hata ayıklama sorunlarını giderme | Microsoft Docs
ms.custom: ''
ms.date: 04/24/2019
ms.topic: troubleshooting
helpviewer_keywords:
- debugger
ms.assetid: 511a0697-c68a-4988-9e29-8d0166ca044a
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: e3c66ba4a5031326ec288d3a5f2f3c4851d17ca6
ms.sourcegitcommit: 74c5360186731de07828764eb32ea1033a8c2275
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/03/2019
ms.locfileid: "67559748"
---
# <a name="troubleshooting-and-known-issues-for-snapshot-debugging-in-visual-studio"></a>Visual Studio'da anlık görüntü hata ayıklama için sorun giderme ve bilinen sorunlar

Bu makalede açıklanan adımlar sorunu çözmezse, sorun için arama [Geliştirici topluluğu](https://developercommunity.visualstudio.com/spaces/8/index.html) veya seçerek yeni bir sorun bildirin **yardımcı** > **geri bildirim gönder**   >  **Sorun bildir** Visual Studio'da.

## <a name="issue-attach-snapshot-debugger-encounters-an-http-status-code-error"></a>Sorun: "Snapshot Debugger iliştirebilmek" karşılaştığında bir HTTP durum kodu hatası

Aşağıdaki hatayı görürseniz **çıkış** penceresi iliştirme girişimi sırasında aşağıda listelenen bilinen bir sorun olabilir. Önerilen çözümleri deneyin ve sorun devam ederse diğer adı önceki başvurun.

`[TIMESTAMP] Error --- Unable to Start Snapshot Debugger - Attach Snapshot Debugger failed: System.Net.WebException: The remote server returned an error: (###) XXXXXX`

### <a name="401-unauthorized"></a>(401) yetkisiz

Bu hata, REST araması için Azure kullanan Visual Studio tarafından geçersiz bir kimlik bilgisi verilen gösterir. Bu hata Azure Active Directory kolay OAuth modülü ile bilinen bir hatayı oluşturabilir.

Aşağıdaki adımları gerçekleştirin:

* Visual Studio kişiselleştirme hesabınız ve Azure aboneliği için iliştirmekte olduğunuz kaynak izni olduğundan emin olun. Bunu belirlemek için hızlı bir kaynak iletişim kutusunda kullanılabilir olup olmadığını denetlemek için yoludur **hata ayıklama** > **Snapshot Debugger Ekle...**   >  **Azure kaynak** > **var olanı Seç**, veya Bulut Gezgini'nde.
* Bu hata devam ederse, bu makalenin başında açıklanan geri bildirim kanallarını kullanın.

### <a name="403-forbidden"></a>(403) Yasak

İzin reddedildi bu hatayı gösterir. Bu, birçok farklı nedenlerden kaynaklanabilir.

Aşağıdaki adımları gerçekleştirin:

* Visual Studio hesabınızı geçerli bir Azure aboneliği için kaynak gerekli rol tabanlı erişim denetimi (RBAC) izinlere sahip olduğunu doğrulayın. AppService için izni olup olmadığını denetlemek [sorgu](https://docs.microsoft.com/rest/api/appservice/appserviceplans/get) uygulamanızı barındıran App Service planı.
* İstemci makinenizde zaman damgası doğru ve güncel olduğunu doğrulayın. 15 dakikadan fazla istek zaman damgası, genellikle tarafından devre dışı damgalı sunucuları bu hatayı üretir.
* Bu hata devam ederse, bu makalenin başında açıklanan geri bildirim kanallarını kullanın.

### <a name="404-not-found"></a>(404) bulunamadı

Bu hata, sunucu üzerinde Web sitesi bulunamadı gösterir.

Aşağıdaki adımları gerçekleştirin:

* Dağıtılan ve için iliştirmekte App Service kaynak üzerinde çalışan bir Web sitesi sahip olduğunuzu doğrulayın.
* Site https:// kullanılabilir olduğundan emin olun\<kaynak\>. azurewebsites.net
* Bu hata devam ederse, bu makalenin başında açıklanan geri bildirim kanallarını kullanın.

### <a name="406-not-acceptable"></a>(406) kabul edilemez

Bu hata, sunucunun isteği kabul et üstbilgisinde ayarlanan türüne yanıt verip vermediğini gösterir.

Aşağıdaki adımları gerçekleştirin:

* Sitenizi https:// kullanılabilir olduğunu doğrulamak\<kaynak\>. azurewebsites.net
* Siteniz için yeni örnekleri geçirildiğini değil doğrulayın. Anlık görüntü hata ayıklayıcı bu hataya aralıklı olarak belirli örneklerine istekleri yönlendirmeye ARRAffinity kavramını kullanır.
* Bu hata devam ederse, bu makalenin başında açıklanan geri bildirim kanallarını kullanın.

### <a name="409-conflict"></a>Çakışma (409)

Bu hata, istek geçerli sunucu durumu ile çakışıyor gösterir.

Bu bir kullanıcı göre Applicationınsights etkinleştirilmiş bir AppService Snapshot Debugger iliştirebilmek çalıştığında oluşan bilinen bir sorundur. Applicationınsights bu soruna neden Visual Studio değerinden farklı bir kasa ile AppSettings ayarlar.

::: moniker range=">= vs-2019"
Biz bu Visual Studio 2019 giderilmiştir.
::: moniker-end

Aşağıdaki adımları gerçekleştirin:

::: moniker range="vs-2017"

* Azure portalında AppSettings ayıklayıcısı (SNAPSHOTDEBUGGER_EXTENSION_VERSION) ve InstrumentationEngine (INSTRUMENTATIONENGINE_EXTENSION_VERSION) büyük harf olduğundan emin olun. Aksi takdirde, ayarları güncelleştirmek el ile hangi site yeniden başlatılmasını zorlar.
::: moniker-end
* Bu hata devam ederse, bu makalenin başında açıklanan geri bildirim kanallarını kullanın.

### <a name="500-internal-server-error"></a>İç sunucu hatası (500)

Bu hata sitenin tamamen çalışmıyor veya sunucu isteği işleyemiyor gösterir. Çalışan uygulamalar üzerinde anlık görüntü hata ayıklayıcısı yalnızca işlevler. [Application Insights Snapshot Debugger](https://docs.microsoft.com/azure/azure-monitor/app/snapshot-debugger) özel durumları olarak anlık görüntüsünün alınması sağlar ve gereksinimlerinize en uygun aracı olabilir.

### <a name="502-bad-gateway"></a>(502) hatalı ağ geçidi

Bu hata, bir sunucu tarafı ağ sorunu gösterir ve geçici olabilir.

Aşağıdaki adımları gerçekleştirin:

* Snapshot Debugger'ı yeniden eklemeyi önce birkaç dakika bekleyen deneyin.
* Bu hata devam ederse, bu makalenin başında açıklanan geri bildirim kanallarını kullanın.

## <a name="issue-snappoint-does-not-turn-on"></a>Sorun: Anlık görüntü noktası açılmıyor

Bir uyarı simgesi görürseniz ![anlık görüntü noktası uyarı simgesi](../debugger/media/snapshot-troubleshooting-snappoint-warning-icon.png "anlık görüntü noktası uyarı simgesi") , anlık görüntü noktası ile yerine normal bir anlık görüntü noktası simgesi, sonra anlık görüntü noktası açık değil.

![Anlık görüntü noktası olmayan açma](../debugger/media/snapshot-troubleshooting-dont-turn-on.png "anlık görüntü noktası olmayan Aç")

Aşağıdaki adımları gerçekleştirin:

1. Derleme ve uygulamanızı dağıtmak için kullanılan kaynak kodu aynı sürümüne sahip olduğunuzdan emin olun. Dağıtımınız için doğru semboller yükleniyor emin olun. Bunu yapmak için görüntüleme **modülleri** penceresi açıkken anlık görüntü hata ayıklama ve sembol dosyası sütun .pdb dosyasını ayıkladığınız modül için yüklenmiş görüntülendiğini doğrulama. Snapshot Debugger otomatik olarak indirmeyi ve dağıtımınız için semboller kullanın dener.

## <a name="issue-symbols-do-not-load-when-i-open-a-snapshot"></a>Sorun: Anlık görüntü açtığımda sembolleri yüklenmiyor

Pencere görürseniz, semboller yüklenmedi.

![Sembolleri yükleme](../debugger/media/snapshot-troubleshooting-symbols-wont-load.png "sembolleri yükleme")

Aşağıdaki adımları gerçekleştirin:

- Tıklayın **sembol ayarlarını değiştir...** Bu sayfada bağlayın. İçinde **hata ayıklama > Sembol** ayarları, sembol önbellek dizini ekleyin. Sembol yolu ayarladıktan sonra anlık görüntü hata ayıklamayı yeniden başlatın.

   App Service dağıtımınızda simgeleri veya .pdb dosyaları, projenizde kullanılabilen eşleşmelidir. Çoğu dağıtım (Visual Studio, Kudu, ya da Azure işlem hatları ile CI/CD ile dağıtım vb.) sembol dosyalarınızı boyunca uygulama hizmetinize yayımlar. Sembol önbellek dizini ayarlamak, bu sembolleri kullanmak Visual Studio sağlar.

   ![Sembol ayarları](../debugger/media/snapshot-troubleshooting-symbol-settings.png "sembol ayarları")

- Kuruluşunuz bir sembol sunucusu kullanıyorsa ya da farklı bir yolda sembolleri bıraktığı alternatif olarak, dağıtımınız için doğru sembolleri yüklemek üzere sembol Ayarları'nı kullanın.

## <a name="issue-i-cannot-see-the-attach-snapshot-debugger-option-in-the-cloud-explorer"></a>Sorun: "Snapshot Debugger Ekle" seçeneğini bulut Gezgini'nde göremiyorum

Aşağıdaki adımları gerçekleştirin:

- Anlık görüntü hata ayıklayıcı bileşeni yüklü olduğundan emin olun. Visual Studio Yükleyicisi'ni açın ve kontrol **Snapshot Debugger** Azure iş yükü bileşeni.
::: moniker range="< vs-2019"
- Uygulamanızın desteklenen emin olun. Şu anda, yalnızca ASP.NET (4.6.1+) ve ASP.NET Core (2.0 +) uygulamalarını Azure App Services'a dağıtılmış desteklenir.
::: moniker-end
::: moniker range=">= vs-2019"
- Uygulamanızın desteklenen emin olun:
  - Azure uygulama hizmetleri - .NET Framework 4.6.1 üzerinde çalışan ASP.NET uygulamalarından veya üzeri.
  - Azure uygulama hizmetleri - .NET Core 2.0 veya daha sonra Windows üzerinde çalışan ASP.NET Core uygulamaları.
  - Azure sanal makineler (ve sanal makine ölçek kümesi) - .NET Framework 4.6.1 üzerinde çalışan ASP.NET uygulamalarından veya üzeri.
  - Azure sanal makineler (ve sanal makine ölçek kümesi) - .NET Core 2.0 veya daha sonra Windows üzerinde çalışan ASP.NET Core uygulamaları.
  - Azure Kubernetes Hizmetleri - .NET Core 2.2 veya sonraki Debian 9 üzerinde çalışan ASP.NET Core uygulamaları.
  - Azure Kubernetes Hizmetleri - .NET Core 2.2 veya sonraki Alpine 3.8 üzerinde çalışan ASP.NET Core uygulamaları.
  - Azure Kubernetes Hizmetleri - .NET Core 2.2 veya sonraki Ubuntu 18.04 üzerinde çalışan ASP.NET Core uygulamaları.
::: moniker-end

## <a name="issue-i-only-see-throttled-snapshots-in-the-diagnostic-tools"></a>Sorun: Tanılama araçları kısıtlanmış anlık görüntü yalnızca görüyorum

![Kısıtlı anlık görüntü noktası](../debugger/media/snapshot-troubleshooting-throttled-snapshots.png "kısıtlanmış anlık görüntü noktası")

Aşağıdaki adımları gerçekleştirin:

- Anlık görüntüleri küçük bellek alanı dolduracaktır, ancak bir işleme ücrete tabi. Snapshot Debugger, yoğun bellek yükü altında sunucunuzdur algılarsa, anlık görüntüler olmayacaktır. Snapshot Debugger oturumu durdurma ve yeniden deneyerek zaten yakalanan anlık görüntülerini silebilirsiniz.

::: moniker range=">= vs-2019"
## <a name="issue-snapshot-debugging-with-multiple-versions-of-the-visual-studio-gives-me-errors"></a>Sorun: Visual Studio'nun birden çok sürümü olan anlık görüntü hata ayıklama bana hata veriyor

Visual Studio 2019 Snapshot Debugger site uzantısını Azure App Service üzerinde daha yeni bir sürümü gerektirir.  Bu sürüm Visual Studio 2017 tarafından kullanılan Snapshot Debugger site uzantısını daha eski bir sürümüyle uyumlu değil.  Daha önce Visual Studio 2017'de anlık görüntü hata ayıklayıcı tarafından hata, bir Azure uygulama hizmeti için anlık görüntü hata ayıklayıcı Visual Studio 2019'eklemeye çalışırsanız aşağıdaki hatayı alırsınız:

![Uyumsuz Snapshot Debugger site uzantısını Visual Studio 2019](../debugger/media/snapshot-troubleshooting-incompatible-vs2019.png "uyumsuz Snapshot Debugger site uzantısını Visual Studio 2019")

Buna karşılık, daha önce Visual Studio 2019'de anlık görüntü hata ayıklayıcı tarafından hata, bir Azure uygulama hizmeti için Snapshot Debugger iliştirebilmek için Visual Studio 2017'yi kullanıyorsanız, şu hatayı alırsınız:

![Uyumsuz Snapshot Debugger site uzantısını Visual Studio 2017](../debugger/media/snapshot-troubleshooting-incompatible-vs2017.png "uyumsuz Snapshot Debugger site uzantısını Visual Studio 2017")

Bu sorunu gidermek için Azure portalında aşağıdaki uygulama ayarlarını silin ve yeniden Snapshot Debugger iliştirebilmek:

- INSTRUMENTATIONENGINE_EXTENSION_VERSION
- SNAPSHOTDEBUGGER_EXTENSION_VERSION
::: moniker-end

## <a name="issue-i-am-having-problems-snapshot-debugging-and-i-need-to-enable-more-logging"></a>Sorun: Anlık görüntü hata ayıklama ilgili sorunlar yaşıyorum ve daha fazla günlük kaydını etkinleştirmek istiyorum

### <a name="enable-agent-logs"></a>Aracı günlüklerini etkinleştirme

Oturum Aç Visual Studio aracısını etkinleştirme ve devre dışı bırakma gidin *Araçlar > Seçenekler > anlık görüntü hata ayıklayıcısı > günlüğü etkinleştir aracı*. Not *silme eski aracı günlüklerini oturumu Başlat menüsünde* olduğunu da etkinleştirilmişse, her başarılı Visual Studio ekleme olacak önceki Aracısı günlükleri silin.

Aracı günlükleri aşağıdaki konumlarda bulunabilir:

- Uygulama Hizmetleri:
  - Uygulama hizmetinizin Kudu sitesine gidin (diğer bir deyişle, yourappservice. **SCM**. azurewebsites.net) ve hata ayıklama konsoluna gidin.
  - Aracı günlükleri şu dizinde depolanır:  D:\home\LogFiles\SiteExtensions\DiagnosticsAgentLogs\
- VM/VMSS:
  - Aracısı günlükleri şu şekilde depolanır, VM için oturum açın:  C:\WindowsAzure\Logs\Plugins\Microsoft.Azure.Diagnostics.IaaSDiagnostics\<sürüm > \SnapshotDebuggerAgent_*.txt
- AKS
  - Aşağıdaki dizine gidin: / tmp/diag/AgentLogs / *

### <a name="enable-profilerinstrumentation-logs"></a>Profiler/izleme günlüklerini etkinleştirme

İzleme günlükleri aşağıdaki konumlarda bulunabilir:

- Uygulama Hizmetleri:
  - Hata günlüğü D:\Home\LogFiles\eventlog.xml için otomatik olarak gönderilir, olayları ile işaretlenir `<Provider Name="Instrumentation Engine" />` veya "Üretim kesme noktaları"
- VM/VMSS:
  - Sanal makinenizde oturum açın ve Olay Görüntüleyicisi'ni açın.
  - Aşağıdaki görünümü açın: *Windows Günlükleri > Uygulama*.
  - *Geçerli günlüğü Filtrele* tarafından *olay kaynağı* kullanarak *üretim kesme noktaları* veya *izleme altyapısı*.
- AKS
  - İzleme altyapısının günlük kaydı /tmp/diag/log.txt (DockerFile içinde MicrosoftInstrumentationEngine_FileLogPath ayarlanır)
  - /Tmp/diag/shLog.txt ProductionBreakpoint günlük kaydı

## <a name="known-issues"></a>Bilinen Sorunlar

- Aynı App Service karşı birden fazla Visual Studio istemcilerle anlık görüntü hata ayıklama şu anda desteklenmiyor.
- Roslyn IL en iyi duruma getirme, tam olarak ASP.NET Core projelerinde desteklenmez. Bazı ASP.NET Core projeleri için bkz. bazı değişkenleri veya bazı değişkenler koşullu Deyimlerinizde kullanın mümkün olmayabilir.
- Özel değişkenler gibi *$FUNCTION* veya *$CALLER*, günlüğe kaydetme noktaları ASP.NET Core projeleri için de koşullu ifadeler değerlendirilemez.
- Anlık görüntü hata ayıklama sahip uygulama hizmetleri çalışmıyor [yerel önbelleğe alma](/azure/app-service/app-service-local-cache) açık.
- API Apps hata ayıklama anlık görüntü şu anda desteklenmiyor.

## <a name="site-extension-upgrade"></a>Site uzantısı yükseltme

Anlık görüntü hata ayıklama ve Application Insights site işleme yükler ve dosya kilitleme sorunları yükseltme sırasında neden olan bir ICorProfiler bağlıdır. Üretim sitenizi hiç kapalı kalma süresini olduğundan emin olmak için bu işlemi öneririz.

- Oluşturma bir [dağıtım yuvası](/azure/app-service/web-sites-staged-publishing) , App Service içinde ve sitenizi yuvaya dağıtın.
- Visual Studio'daki bulut Gezgini'nde veya Azure portalından üretim yuvasıyla takas.
- Yuva sitesini durdurun. Bu site w3wp.exe işlemi kaldırılarak devre dışı sonlandırmak için birkaç saniye sürer.
- Yuva site uzantısı Kudu sitesi veya Azure portalından yükseltme (*App Service dikey penceresi > Geliştirme araçları > uzantılar > güncelleştirme*).
- Yuva sitesini başlatın. Yeniden Isınma sitesinden öneririz.
- Üretim yuvasıyla takas etme.

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio’da hata ayıklama](../debugger/index.md)
- [Snapshot Debugger'ı kullanarak canlı ASP.NET uygulamalarının hatalarını ayıklama](../debugger/debug-live-azure-applications.md)
- [Canlı ASP.NET Azure sanal Machines\Virtual makineler ölçek Snapshot Debugger'ı kullanarak kümeleri hata ayıklama](../debugger/debug-live-azure-virtual-machines.md)
- [Snapshot Debugger'ı kullanarak canlı ASP.NET Azure Kubernetes hata ayıklama](../debugger/debug-live-azure-kubernetes.md)
- [Anlık görüntü hatalarını ayıklama hakkında SSS](../debugger/debug-live-azure-apps-faq.md)
