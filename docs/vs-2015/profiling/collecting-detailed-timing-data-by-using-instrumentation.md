---
title: Toplama ayrıntılı zamanlama verileri araçları kullanarak | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
helpviewer_keywords:
- Profiling Tools,instrumentation method
- instrumentation profiling method
ms.assetid: e9deb370-c459-45ac-84d3-14d646590d05
caps.latest.revision: 23
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: c129ddf016e02fe6c29d5cf63fe57ba07fbd4e95
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60087982"
---
# <a name="collecting-detailed-timing-data-by-using-instrumentation"></a>İzleme Kullanarak Ayrıntılı Zamanlama Verileri Toplama
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

[!INCLUDE[vsprvs](../includes/vsprvs-md.md)] Profil oluşturma araçları araç haline getirme yöntemi, bir modülün bir kopyasını profil oluşturma kodu ekler. Kodun her giriş, çıkış ve işlevlerin işlev çağrısı modülünde bir profil oluşturma sırasında kaydeder. Araçlar yöntemini giriş ve çıkış işlemleri uygulama performansı üzerindeki etkisini anlamak için kodun bir bölümünü hakkında ayrıntılı zamanlama bilgileri toplamak için yararlı olacaktır.  
  
 Araçlar yöntemini aşağıdaki yordamlardan birini kullanarak belirtebilirsiniz:  
  
- Profil Oluşturma Sihirbazı'nın ilk sayfasında, seçin **izleme**.  
  
- Üzerinde **performans Gezgini** araç penceresindeki **yöntemi** listesinde **izleme**.  
  
- Üzerinde **genel** sayfa seçin performans oturumu Özellikleri iletişim kutusunun **izleme**.  
  
## <a name="common-tasks"></a>Ortak Görevler  
 Ek seçenekler belirtebilirsiniz _performans oturumu_**özellik sayfaları** performans oturumunun iletişim kutusu. Bu iletişim kutusunu açmak için:  
  
- İçinde **performans Gezgini**performans oturumu adına sağ tıklayın ve ardından **özellikleri**.  
  
  Aşağıdaki tabloda görevler belirleyebilirsiniz seçenekleri açıklanmıştır _performans oturumu_**özellik sayfaları** iletişim kutusuna izleme metodunu kullanarak profili.  
  
|Görev|İlgili içerik|  
|----------|---------------------|  
|Üzerinde **genel** sayfasında .NET bellek ayırma ve yaşam süresi verilerini ekleyin ve oluşturulan profil oluşturma veri (.vsp) dosyasının adlandırma ayrıntılarını belirtin.|-   [.NET bellek ayırma ve yaşam süresi verilerini toplama](../profiling/collecting-dotnet-memory-allocation-and-lifetime-data.md)<br />-   [Nasıl Yapılır: Performans Veri Dosyası Adlandırma Seçeneklerini Ayarlama](../profiling/how-to-set-performance-data-file-name-options.md)|  
|Üzerinde **başlatma** , solution.specify içinde birden çok .exe proje başlatmak için uygulama ve bunların başlatma sırasını varsa, sayfa.|-   [Nasıl Yapılır: Başlatma İçin İkili Dosya Belirtme](../profiling/how-to-specify-the-binary-to-start.md)|  
|Üzerinde **ikili dosyaları** sayfasında, modüller için izleme eklenmiş kopyalar konumunu belirtin. Varsayılan olarak, orijinal ikililerin bir yedekleme klasörüne taşınır.|-   [Nasıl Yapılır: İşaretlenmiş İkili Dosyaları Yeniden Yerleştirme](../profiling/how-to-relocate-instrumented-binaries.md)|  
|Üzerinde **katman etkileşim** sayfasında, profil oluşturma çalışması için ADO.NET çağrı veri ekleyin.|-   [Katman etkileşim verileri toplama](../profiling/collecting-tier-interaction-data.md)|  
|Üzerinde **izleme** öncesinde ve sonrasında bir komut isteminde çalıştırmak için komutları belirtin sayfasında ve ek yükü, profil oluşturma profili ASP.NET Web sayfalarında JavaScript kodu azaltmak için profil küçük işlevleri Dışla izleme işlemi.|-   [Nasıl Yapılır: Kısa İşlevleri İzlemeden Hariç Tutma veya İzlemeye Dahil Etme](../profiling/how-to-exclude-or-include-short-functions-from-instrumentation.md)<br />-   [Nasıl Yapılır: Web Sayfalarında JavaScript Kodunun Profilini Oluşturma](../profiling/how-to-profile-javascript-code-in-web-pages.md)<br />-   [Nasıl Yapılır: Ön ve Son İzleme Komutlarını Belirtme](../profiling/how-to-specify-pre-and-post-instrument-commands.md)|  
|Üzerinde **CPU sayaçları** sayfasında, profil oluşturma verileri eklemek için bir veya daha fazla işlemci performans sayaçları belirtin.|-   [Nasıl Yapılır: CPU Sayaç Verileri Toplama](../profiling/how-to-collect-cpu-counter-data.md)|  
|Üzerinde **Windows olayları** sayfasında, örnekleme verileri toplama için bir veya daha fazla olay izleme için Windows (ETW) olayları seçin.|-   [Nasıl Yapılır: Windows İçin Olay İzleme (ETW) Verileri Toplama](../profiling/how-to-collect-event-tracing-for-windows-etw-data.md)|  
|Üzerinde **Windows sayaçları** sayfasında işaretleri olarak profil oluşturma verilerini eklemek için bir veya daha fazla işletim sistemi performans sayaçları belirtin.|-   [Nasıl Yapılır: Windows Sayaç Verileri Toplama](../profiling/how-to-collect-windows-counter-data.md)|  
|Üzerinde **Gelişmiş** sayfasında, Vsınstr izleme programa dahil etmek veya belirli işlevleri hariç tutmak için seçenekleri gibi geçirmek istediğiniz ek seçenekleri belirtin.|-   [Nasıl Yapılır: Ek İzleme Seçeneklerini Belirtme](../profiling/how-to-specify-additional-instrumentation-options.md)<br />-   [Nasıl Yapılır: İzlemeyi Belirli Araçlarla Sınırlama](../profiling/how-to-limit-instrumentation-to-specific-functions.md)<br />-   [Vsınstr](../profiling/vsinstr.md)|
