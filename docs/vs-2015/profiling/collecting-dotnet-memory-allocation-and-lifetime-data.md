---
title: .NET bellek ayırma ve yaşam süresi verilerini toplama | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
helpviewer_keywords:
- .NET memory profiling method
- Profiling Tools,.NET memory method
ms.assetid: 62a6dd5f-db66-4456-9d57-f8913dbfe4d5
caps.latest.revision: 23
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: c40c2f824518ed00dacc41094c1b567f5de248ae
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60112825"
---
# <a name="collecting-net-memory-allocation-and-lifetime-data"></a>.NET Bellek Ayırma ve Yaşam Süresi Verilerini Toplama
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

[!INCLUDE[vsprvs](../includes/vsprvs-md.md)] .NET bellek ayırma koleksiyonunu destek profil oluşturma araçları ve yardımcı olan nesne yaşam verisi uygulamanızda bellekle ilgili performans sorunlarını algılama.  
  
- Ayrılan .NET Framework bellek nesnelerinin sayısı ve boyutu .NET bellek ayırma hakkındaki verileri içerir.  
  
- Nesne yaşam verisi üç çöp toplama kuşakları geri kazanılan .NET Framework bellek nesnelerinin sayısı ve boyutu içerir.  
  
  **Gereksinimler**  
  
- [!INCLUDE[vsUltLong](../includes/vsultlong-md.md)], [!INCLUDE[vsPreLong](../includes/vsprelong-md.md)], [!INCLUDE[vsPro](../includes/vspro-md.md)]  
  
> [!NOTE]
>  Windows 8 ve Windows Server 2012'deki Gelişmiş güvenlik özellikleri Visual Studio profil oluşturucu bu platformlarda veri toplayan bir şekilde önemli değişiklikler gerekmiştir. Windows Store apps ayrıca yeni toplama teknikleri gerektirir. Bkz: [Windows 8 ve Windows Server 2012 uygulamalarında performans araçları](../profiling/performance-tools-on-windows-8-and-windows-server-2012-applications.md).  
  
 Örnekleme veya yöntemi profil oluşturma Araçları'nı kullanarak veri toplayabilir.  
  
- Örnekleme yöntemini kullandığınızda, profil oluşturucu tüm .NET bellek ayırma ve kullanmaya veya bağlı işlem tarafından oluşturulan nesneleri izler.  
  
- Araçlar yöntemini kullandığınızda, profil oluşturucu yalnızca .NET bellek ayırma ve izleme eklenmiş modülleri tarafından oluşturulan nesneleri izler.  
  
> [!IMPORTANT]
>  .NET bellek verileri (ayırma, nesne kullanım ömrü veya her ikisi de) örnekleme yöntemini kullanarak topladığınız, tüm kullanıcı tarafından belirtilen örnekleme olayları göz ardı edilir ve uygun bir bellek ayırma olayları toplamak için kullanılır.  
  
 Profil oluşturma of.NET bellek ayırma etkinleştirirseniz, ayrıca ayırma görünümü sağlar. Profil oluşturma .NET yaşam süresi verilerini etkinleştirirseniz, ayrıca nesne ömrü görünümü sağlar. Daha fazla bilgi için [ayırma görünümü](../profiling/dotnet-memory-allocations-view.md) ve [nesne ömrü görünümü](../profiling/object-lifetime-view.md).  
  
 Profil Araçları komut satırı araçları kullanarak .NET bellek verileri toplamak nasıl hakkında daha fazla bilgi için bkz: kullanarak .NET bellek yöntemleri toplamak bellek ayırma ve nesne yaşam verisi [profil oluşturma yöntemleri gelen komut satırını kullanarak](../profiling/using-profiling-methods-to-collect-performance-data-from-the-command-line.md).  
  
### <a name="to-collect-net-memory-data"></a>.NET bellek verileri toplamak için  
  
1. İçinde **performans Gezgini**performans oturumu sağ tıklayın ve ardından **özellikleri**.  
  
2. Üzerinde _performans oturumu_**özellik sayfaları** iletişim kutusu, tıklayın **genel** sekmesine tıklayın ve **toplamak .NET nesnesi ayırma bilgilerini** onay kutusu.  
  
3. .NET nesnesi ömür verilerini toplamak için seçin **ayrıca .NET nesnesi ömür bilgilerini toplayın** onay kutusu.  
  
## <a name="common-tasks"></a>Ortak Görevler  
 Ek seçenekler belirtebilirsiniz _performans oturumu_**özellik sayfaları** performans oturumunun iletişim kutusu. Bu iletişim kutusunu açmak için:  
  
- İçinde **performans Gezgini**performans oturumu adına sağ tıklayın ve ardından **özellikleri**.  
  
  Aşağıdaki tabloda görevler belirleyebilirsiniz seçenekleri açıklanmıştır _performans oturumu_**özellik sayfaları** .NET bellek verileri toplamak için iletişim kutusuna.  
  
|Görev|İlgili içerik|  
|----------|---------------------|  
|Üzerinde **genel** sayfasında, oluşturulan profil oluşturma veri (.vsp) dosyasının adlandırma ayrıntıları belirtin.|-   [.NET bellek ayırma ve yaşam süresi verilerini toplama](../profiling/collecting-dotnet-memory-allocation-and-lifetime-data.md)<br />-   [Nasıl Yapılır: Performans Veri Dosyası Adlandırma Seçeneklerini Ayarlama](../profiling/how-to-set-performance-data-file-name-options.md)|  
|Üzerinde **başlatma** kod çözümünüz içinde birden çok .exe projeniz varsa başlatılacak uygulamayı seçin.|-   [Katman etkileşim verileri toplama](../profiling/collecting-tier-interaction-data.md)|  
|Üzerinde **katman etkileşim** sayfasında, profil oluşturma çalışması için ADO.NET çağrı veri ekleyin.|-   [Katman etkileşim verileri toplama](../profiling/collecting-tier-interaction-data.md)|  
|Üzerinde **Windows olayları** sayfasında, bir veya daha fazla olay izleme için Windows (ETW) olayları, örnekleme verileri toplama belirtin.|-   [Nasıl Yapılır: Windows İçin Olay İzleme (ETW) Verileri Toplama](../profiling/how-to-collect-event-tracing-for-windows-etw-data.md)|  
|Üzerinde **Windows sayaçları** sayfasında işaretleri olarak profil oluşturma verilerini eklemek için bir veya daha fazla işletim sistemi performans sayaçları belirtin.|-   [Nasıl Yapılır: Windows Sayaç Verileri Toplama](../profiling/how-to-collect-windows-counter-data.md)|  
|Üzerinde **Gelişmiş** sayfasında, uygulama modüllerinizi birden çok sürümü kullanırsanız profili .NET Framework çalışma zamanının sürümünü belirtin. Varsayılan olarak yüklenen ilk sürüm profil oluşturulan.|-   [Nasıl Yapılır: .NET Framework Çalışma Zamanını Belirtme](../profiling/how-to-specify-the-dotnet-framework-runtime.md)|  
  
## <a name="instrumentation-tasks"></a>Görevleri izleme  
 Seçenekler aşağıdaki tabloda görevlerdir **özellik sayfaları** cihaz atama yöntemi ile profil oluşturma için belirli bir iletişim kutusu.  
  
|Görev|İlgili içerik|  
|----------|---------------------|  
|Üzerinde **ikili dosyaları** sayfasında, modüller için izleme eklenmiş kopyalar konumunu belirtin. Varsayılan olarak, orijinal ikililerin bir yedekleme klasörüne taşınır.|-   [Nasıl Yapılır: İşaretlenmiş İkili Dosyaları Yeniden Yerleştirme](../profiling/how-to-relocate-instrumented-binaries.md)|  
|Üzerinde **izleme** öncesinde ve sonrasında bir komut isteminde çalıştırmak için komutları belirtin sayfasında ve ek yükü, profil oluşturma profili ASP.NET Web sayfalarında JavaScript kodu azaltmak için profil küçük işlevleri Dışla izleme işlemi.|-   [Nasıl Yapılır: Kısa İşlevleri İzlemeden Hariç Tutma veya İzlemeye Dahil Etme](../profiling/how-to-exclude-or-include-short-functions-from-instrumentation.md)<br />-   [Nasıl Yapılır: Web Sayfalarında JavaScript Kodunun Profilini Oluşturma](../profiling/how-to-profile-javascript-code-in-web-pages.md)<br />-   [Nasıl Yapılır: Ön ve Son İzleme Komutlarını Belirtme](../profiling/how-to-specify-pre-and-post-instrument-commands.md)|  
|Üzerinde **CPU sayaçları** sayfasında, profil oluşturma verileri eklemek için bir veya daha fazla işlemci performans sayaçları belirtin.|-   [Nasıl Yapılır: CPU Sayaç Verileri Toplama](../profiling/how-to-collect-cpu-counter-data.md)|  
|Üzerinde **Gelişmiş** sayfasında, herhangi bir ek VSInstr.exe, dahil etmek veya belirli işlevleri hariç tutmak için seçenekleri gibi istediğiniz seçenekleri belirtin. Vsınstr seçenekleri hakkında daha fazla bilgi için bkz. [Vsınstr](../profiling/vsinstr.md)|-   [Nasıl Yapılır: Ek İzleme Seçeneklerini Belirtme](../profiling/how-to-specify-additional-instrumentation-options.md)<br />-   [Nasıl Yapılır: İzlemeyi Belirli Araçlarla Sınırlama](../profiling/how-to-limit-instrumentation-to-specific-functions.md)|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Performans oturumlarını yapılandırma](../profiling/configuring-performance-sessions.md)   
 [Nasıl yapılır: Koleksiyon metotları seçme](../profiling/how-to-choose-collection-methods.md)   
 [Performans Oturumu Özellikleri](../profiling/performance-session-properties.md)
