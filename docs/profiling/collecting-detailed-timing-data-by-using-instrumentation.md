---
title: Toplama ayrıntılı zamanlama verileri araçları kullanarak | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- Profiling Tools,instrumentation method
- instrumentation profiling method
ms.assetid: e9deb370-c459-45ac-84d3-14d646590d05
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: f8812db301b4e58b89ac8ab879625b7cf101ad94
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53913974"
---
# <a name="collect-detailed-timing-data-by-using-instrumentation"></a>İzleme kullanarak ayrıntılı zamanlama verileri toplama
[!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] Profil oluşturma araçları araç haline getirme yöntemi, bir modülün bir kopyasını profil oluşturma kodu ekler. Kodun her giriş, çıkış ve işlevlerin işlev çağrısı modülünde bir profil oluşturma sırasında kaydeder. Araçlar yöntemini giriş ve çıkış işlemleri uygulama performansı üzerindeki etkisini anlamak için kodun bir bölümünü hakkında ayrıntılı zamanlama bilgileri toplamak için yararlı olacaktır.  
  
 Araçlar yöntemini aşağıdaki yordamlardan birini kullanarak belirtebilirsiniz:  
  
-   Profil Oluşturma Sihirbazı'nın ilk sayfasında, seçin **izleme**.  
  
-   Üzerinde **performans Gezgini** araç penceresindeki **yöntemi** listesinde **izleme**.  
  
-   Üzerinde **genel** sayfa seçin performans oturumu Özellikleri iletişim kutusunun **izleme**.  
  
## <a name="common-tasks"></a>Ortak görevler
 Ek seçenekler belirtebilirsiniz _performans oturumu_**özellik sayfaları** performans oturumunun iletişim kutusu. Bu iletişim kutusunu açmak için:  
  
- İçinde **performans Gezgini**performans oturumu adına sağ tıklayın ve ardından **özellikleri**.  
  
  Aşağıdaki tabloda görevler belirleyebilirsiniz seçenekleri açıklanmıştır _performans oturumu_**özellik sayfaları** iletişim kutusuna izleme metodunu kullanarak profili.  
  
|Görev|İlgili içerik|  
|----------|---------------------|  
|Üzerinde **genel** sayfasında .NET bellek ayırma ve yaşam süresi verilerini ekleyin ve oluşturulan profil oluşturma veri (.vsp) dosyasının adlandırma ayrıntılarını belirtin.|-   [.NET bellek ayırma ve yaşam süresi verilerini toplama](../profiling/collecting-dotnet-memory-allocation-and-lifetime-data.md)<br />-   [Nasıl Yapılır: Performans veri dosyası adlandırma seçeneklerini ayarlama](../profiling/how-to-set-performance-data-file-name-options.md)|  
|Üzerinde **başlatma** , solution.specify içinde birden çok .exe proje başlatmak için uygulama ve bunların başlatma sırasını varsa, sayfa.|-   [Nasıl Yapılır: Başlamak için ikili dosya belirtme](../profiling/how-to-specify-the-binary-to-start.md)|  
|Üzerinde **ikili dosyaları** sayfasında, modüller için izleme eklenmiş kopyalar konumunu belirtin. Varsayılan olarak, orijinal ikililerin bir yedekleme klasörüne taşınır.|-   [Nasıl Yapılır: İşaretlenmiş ikilileri yeniden Yerleştir](../profiling/how-to-relocate-instrumented-binaries.md)|  
|Üzerinde **katman etkileşim** sayfasında, profil oluşturma çalışması için ADO.NET çağrı veri ekleyin.|-   [Katman etkileşim verileri toplama](../profiling/collecting-tier-interaction-data.md)|  
|Üzerinde **izleme** öncesinde ve sonrasında bir komut isteminde çalıştırmak için komutları belirtin sayfasında ve ek yükü, profil oluşturma profili ASP.NET Web sayfalarında JavaScript kodu azaltmak için profil küçük işlevleri Dışla izleme işlemi.|-   [Nasıl Yapılır: Hariç tutma veya kısa işlevleri izlemeden içerir](../profiling/how-to-exclude-or-include-short-functions-from-instrumentation.md)<br />-   [Nasıl Yapılır: Web sayfalarında JavaScript kodu profili](../profiling/how-to-profile-javascript-code-in-web-pages.md)<br />-   [Nasıl Yapılır: Ön ve son izleme komutları belirtme](../profiling/how-to-specify-pre-and-post-instrument-commands.md)|  
|Üzerinde **CPU sayaçları** sayfasında, profil oluşturma verileri eklemek için bir veya daha fazla işlemci performans sayaçları belirtin.|-   [Nasıl yapılır: CPU sayaç verileri toplama](../profiling/how-to-collect-cpu-counter-data.md)|  
|Üzerinde **Windows olayları** sayfasında, örnekleme verileri toplama için bir veya daha fazla olay izleme için Windows (ETW) olayları seçin.|-   [Nasıl Yapılır: Olay izleme için Windows (ETW) verileri toplama](../profiling/how-to-collect-event-tracing-for-windows-etw-data.md)|  
|Üzerinde **Windows sayaçları** sayfasında işaretleri olarak profil oluşturma verilerini eklemek için bir veya daha fazla işletim sistemi performans sayaçları belirtin.|-   [Nasıl Yapılır: Windows sayaç verileri toplama](../profiling/how-to-collect-windows-counter-data.md)|  
|Üzerinde **Gelişmiş** sayfasında, Vsınstr izleme programa dahil etmek veya belirli işlevleri hariç tutmak için seçenekleri gibi geçirmek istediğiniz ek seçenekleri belirtin.|-   [Nasıl Yapılır: Ek izleme seçeneklerini belirtme](../profiling/how-to-specify-additional-instrumentation-options.md)<br />-   [Nasıl Yapılır: Belirli işlevler için izlemeyi sınırı](../profiling/how-to-limit-instrumentation-to-specific-functions.md)<br />-   [Vsınstr](../profiling/vsinstr.md)|