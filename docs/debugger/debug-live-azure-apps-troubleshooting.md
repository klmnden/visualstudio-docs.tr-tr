---
title: Anlık görüntü hata ayıklama sorunlarını giderme | Microsoft Docs
ms.custom: seodec18
ms.date: 11/07/2018
ms.topic: troubleshooting
helpviewer_keywords:
- debugger
ms.assetid: 511a0697-c68a-4988-9e29-8d0166ca044a
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 7b7916cbd3a7faa633baf53a18686779dc2b386c
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58857768"
---
# <a name="troubleshooting-and-known-issues-for-snapshot-debugging-in-visual-studio"></a>Visual Studio'da anlık görüntü hata ayıklama için sorun giderme ve bilinen sorunlar

Bu makalede açıklanan adımlar sorunu çözmezse, kişi snaphelp@microsoft.com.

## <a name="issue-snappoint-does-not-turn-on"></a>Sorun: Anlık görüntü noktası açılmıyor

Bir uyarı simgesi görürseniz ![anlık görüntü noktası uyarı simgesi](../debugger/media/snapshot-troubleshooting-snappoint-warning-icon.png "anlık görüntü noktası uyarı simgesi") , anlık görüntü noktası ile yerine normal bir anlık görüntü noktası simgesi, sonra anlık görüntü noktası açık değil.

![Anlık görüntü noktası olmayan açma](../debugger/media/snapshot-troubleshooting-dont-turn-on.png "anlık görüntü noktası olmayan Aç")

Aşağıdaki adımları gerçekleştirin:

1. Derleme ve dağıtma, app.isua1 için kullanılan kaynak kodu aynı sürümüne sahip olduğunuzdan emin olun. Dağıtımınız için doğru semboller yükleniyor emin olun. Bunu yapmak için görüntüleme **modülleri** penceresi açıkken anlık görüntü hata ayıklama ve sembol dosyası sütun .pdb dosyasını ayıkladığınız modül için yüklenmiş görüntülendiğini doğrulama. Snapshot Debugger otomatik olarak indirmeyi ve dağıtımınız için semboller kullanın dener.

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

## <a name="issue-snapshot-debugging-with-multiple-versions-of-the-visual-studio-gives-me-errors"></a>Sorun: Visual Studio'nun birden çok sürümü olan anlık görüntü hata ayıklama bana hata veriyor

VS 2019 Snapshot Debugger site uzantısını Azure App Service üzerinde daha yeni bir sürümü gerektirir.  Bu sürüm, VS 2017 tarafından kullanılan Snapshot Debugger site uzantısını daha eski bir sürümüyle uyumlu değil.  Daha önce VS 2017'de anlık görüntü hata ayıklayıcı tarafından hata, bir Azure uygulama hizmeti için anlık görüntü hata ayıklayıcı VS 2019'eklemeye çalışırsanız aşağıdaki hatayı alırsınız:

![Uyumsuz Snapshot Debugger site uzantısını VS 2019](../debugger/media/snapshot-troubleshooting-incompatible-vs2019.png "uyumsuz Snapshot Debugger site uzantısını VS 2019")

Buna karşılık, daha önce anlık görüntü hata ayıklayıcı VS 2019'tarafından hata, bir Azure uygulama hizmeti için Snapshot Debugger iliştirebilmek için VS 2017 kullanırsanız, şu hatayı alırsınız:

![Uyumsuz Snapshot Debugger site uzantısını VS 2017](../debugger/media/snapshot-troubleshooting-incompatible-vs2017.png "uyumsuz Snapshot Debugger site uzantısını VS2017")

Bu sorunu gidermek için Azure portalında aşağıdaki uygulama ayarlarını silin ve yeniden Snapshot Debugger iliştirebilmek:

- INSTRUMENTATIONENGINE_EXTENSION_VERSION
- SNAPSHOTDEBUGGER_EXTENSION_VERSION

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
  - Hata günlüğü D:\Home\LogFiles\eventlog.xml için otomatik olarak gönderilir, olayları ile işaretlenir << sağlayıcı adı = "İzleme altyapısı" / / >> veya "Üretim kesme noktaları"
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