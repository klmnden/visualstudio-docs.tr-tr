---
title: Performans oturumlarını yapılandırma | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
helpviewer_keywords:
- common tasks, performance
- common tasks, profiling tools
- profiling tools, common tasks
- performance, gathering data
ms.assetid: e1c3ba41-ffca-4edf-9a7f-8a5a9244ef9b
caps.latest.revision: 41
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: d67801cedded1ccf66544e21257866feda828e31
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63434325"
---
# <a name="configuring-performance-sessions"></a>Performans Oturumlarını Yapılandırma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Kullanarak [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] profil oluşturma araçları, çok çeşitli çok sayıda uygulama türleri için performans verilerini toplayabilir. Bu bölümde, ilginizi çeken verileri toplamak için profil oluşturma Araçları'nı yapılandırmak için performans oturumu ve hedef ikili performans Wizardand özelliklerini kullanmayı gösterir. Profil oluşturma araçları yapılandırma özellikleri de içinde profil oluşturma yürütmesine toplanan veri miktarını denetlemek için kullanılabilir. Daha fazla bilgi için [veri toplamayı denetleme](../profiling/controlling-data-collection.md).  
  
> [!NOTE]
> Çoğu durumda, varsayılan özellikleri ve performans Sihirbazı kullanarak profil oluşturma verilerinin toplanması etkili bir yoludur. Daha fazla bilgi için [performans profili oluşturma Başlangıç Kılavuzu](../profiling/beginners-guide-to-performance-profiling.md) ve [Başlarken](../profiling/getting-started-with-performance-tools.md).  
  
## <a name="common-tasks"></a>Ortak Görevler  
  
|Görev|İlgili içerik|  
|----------|---------------------|  
|**Temel profil oluşturma seçenekleri ayarlayın:** Yapılandırmanız gereken [!INCLUDE[vs_current_short](../includes/vs-current-short-md.md)] Microsoft sembol sunucusu kullanmak için. Bu, Windows ve diğer Microsoft uygulamaları geçerli sürümü için işlevi ve parametre adları gibi semboller erişebildiğinizden emin yapar. Profil oluşturma araçları ve profil oluşturma veri dosyalarıyla adları sistem izinleri gibi profil oluşturma oturumu başlamadan önce diğer genel seçenekleri de belirtebilirsiniz.|-   [Nasıl Yapılır: Başvuru Pencereleri Sembol Bilgileri](../profiling/how-to-reference-windows-symbol-information.md)<br />-   [Nasıl Yapılır: Sembol Bilgilerini Seri Hale Getirme](../profiling/how-to-serialize-symbol-information.md)<br />-   [Nasıl Yapılır: Geçerli Oturumu Ayarlama](../profiling/how-to-set-the-current-session.md)<br />-   [Nasıl Yapılır: İzinleri Ayarlama](../profiling/how-to-set-permissions.md)<br />-   [Nasıl Yapılır: Performans Veri Dosyası Adlandırma Seçeneklerini Ayarlama](../profiling/how-to-set-performance-data-file-name-options.md)|  
|**Toplamak istediğiniz verileri belirtin:** Profil oluşturma oturumunu yapılandırmak için kullandığınız yordam, profil oluşturmak istediğiniz hedef uygulama türü ve toplamak istediğiniz performans veri türüne bağlıdır.|-   [Nasıl Yapılır: Toplama Yöntemlerini Seçme](../profiling/how-to-choose-collection-methods.md)<br />-   [Örnekleme kullanarak performans istatistikleri toplama](../profiling/collecting-performance-statistics-by-using-sampling.md)<br />-   [.NET bellek ayırma ve yaşam süresi verilerini toplama](../profiling/collecting-dotnet-memory-allocation-and-lifetime-data.md)<br />-   [İzleme kullanarak ayrıntılı zamanlama verileri toplama](../profiling/collecting-detailed-timing-data-by-using-instrumentation.md)<br />-   [Nasıl Yapılır: Web Sayfalarında JavaScript Kodunun Profilini Oluşturma](../profiling/how-to-profile-javascript-code-in-web-pages.md)<br />-   [İş parçacığı ve işlem eşzamanlılık verileri toplama](../profiling/collecting-thread-and-process-concurrency-data.md)<br />-   [Ek performans verileri toplama](../profiling/collecting-additional-performance-data.md)|  
|**Gelişmiş yapılandırma seçenekleri ayarlayın:** Birden çok ortak dil çalışma zamanı (CLR) sürümünü yükleyin ve .NET Framework uygulamaları profil, hangi sürümünün profilinin belirtebilirsiniz. Performans oturumu içinde birden fazla .exe dosyası varsa, ikili dosyalarının başlatma sırasını ayarlayabilirsiniz.|-   [Nasıl Yapılır: .NET Framework Çalışma Zamanını Belirtme](../profiling/how-to-specify-the-dotnet-framework-runtime.md)<br />-   [Nasıl Yapılır: Başlatma İçin İkili Dosya Belirtme](../profiling/how-to-specify-the-binary-to-start.md)|  
  
## <a name="related-sections"></a>İlgili Bölümler  
 [Veri Koleksiyonunu Denetleme](../profiling/controlling-data-collection.md)  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Performans Gezgini](../profiling/performance-explorer.md)
