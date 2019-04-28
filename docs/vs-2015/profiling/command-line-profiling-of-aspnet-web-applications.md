---
title: ASP.NET Web uygulamalarının komut satırı profili oluşturma | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
helpviewer_keywords:
- profiling ASP.NET applications
- profling tools,ASP.NET applications
ms.assetid: 897c00d5-5767-433b-a960-4a29c6023ede
caps.latest.revision: 26
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: c93cb4774953f1425ff0330d7f588cbbf0f0b823
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63439020"
---
# <a name="command-line-profiling-of-aspnet-web-applications"></a>ASP.NET Web Uygulamalarının Komut Satırından Profilinin Oluşturulması
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bu bölümde yordamları ve performans verilerini toplamak için seçenekleri açıklar [!INCLUDE[vstecasp](../includes/vstecasp-md.md)] Web uygulamaları kullanarak [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] komut satırından profil oluşturma araçları.  
  
> [!NOTE]
> Windows 8 ve Windows Server 2012'deki Gelişmiş güvenlik özellikleri Visual Studio profil oluşturucu bu platformlarda veri toplayan bir şekilde önemli değişiklikler gerekmiştir. Windows Store apps ayrıca yeni toplama teknikleri gerektirir. Bkz: [Windows 8 ve Windows Server 2012 uygulamalarında performans araçları](../profiling/performance-tools-on-windows-8-and-windows-server-2012-applications.md).  
  
## <a name="common-tasks"></a>Ortak Görevler  
  
|Görev|İlgili içerik|  
|----------|---------------------|  
|**Temel ASP.NET profil oluşturma verilerini kolayca toplayın:** Kullanım **VSPerfASPNETCmd** örnekleme, izleme, .NET bellek, çekişmeyi toplamak veya yapılandırma gereksinimleri ve gerekli olan Internet Information Services (IIS) yeniden başlatma olmadan etkileşim veri katmanı için aracı için **VSPerfCmd**. **VSPerfASPNETCmd** ek veri toplamak için veya veri toplamayı denetlemek için izin vermez. **Not:**  **VSPerfASPNETCmd** kullanmayı tercih edilen araç bağımsız profil oluşturucu profil ASP.NET Web siteleri için kullanın.|-   [Profil oluşturma VSPerfASPNETCmd ile Hızlı Web sitesi](../profiling/rapid-web-site-profiling-with-vsperfaspnetcmd.md)|  
|**Uygulama istatistikleri toplamak:** Performans istatistikleri toplamak için örnekleme yöntemini kullanın. Veri örnekleme, CPU kullanım sorunlarını analiz etmek için ve bir uygulamanın genel performans özelliklerini anlamak için kullanışlıdır.|-   [Örnekleme kullanarak uygulama istatistikleri toplama](../profiling/collecting-application-statistics-for-aspnet-web-applications-using-the-profiler-sampling-method-from-the-command-line.md)|  
|**Ayrıntılı zamanlama verileri toplama:** Ayrıntılı zamanlama bilgilerini toplamak için izleme metodunu kullanın. Ölçümlü izleme verileri ayrıntılı analiz uygulama senaryoları biri için g/ç sorunlarını analiz etmek için yararlı olacaktır.|-   [İzleme kullanarak ayrıntılı zamanlama verileri toplama](/visualstudio/profiling/collecting-detailed-timing-data-aspnet-profiler-instrumentation-method?view=vs-2015)|  
|**.NET bellek verileri toplamak:** Ayrılmış nesnelerin sayısı ve boyutu gösteren .NET bellek ayırma verilerini toplamak için örnekleme veya Araçlar'ı kullanın. Her çöp toplama nesildeki kazanılır nesnelerinin sayısı ve boyutu gösteren nesne yaşam süresi verilerini de toplayabilirsiniz.|-   [Bellek verileri toplama](../profiling/collecting-memory-data-from-an-aspnet-web-application-by-using-the-profiler-command-line.md)|  
|**Eşzamanlılık verileri toplamak:** Kaynak çekişmesi verisini toplamak için eşzamanlılık yöntemi kullanın. **Not:**  İş parçacığı etkinliği ve görselleştirme verilerini toplamak için Web uygulamaları desteklenmez.|-   [Eşzamanlılık verileri toplama](../profiling/collecting-concurrency-data-for-an-aspnet-web-application-using-the-profiler-command-line.md)|  
|**Katman etkileşim verileri ekleyin:** Zaman uyumlu ilişkin performans verilerini ekleyebilirsiniz [!INCLUDE[vstecado](../includes/vstecado-md.md)] çağrılarının [!INCLUDE[vstecasp](../includes/vstecasp-md.md)] Web uygulaması için bir Microsoft yapar [!INCLUDE[ssNoVersion](../includes/ssnoversion-md.md)] veritabanı.|-   [Katman etkileşim verileri toplama](../profiling/adding-tier-interaction-data-from-the-command-line.md)|  
  
## <a name="related-tasks"></a>İlişkili görevler  
  
|Görev|İlgili içerik|  
|----------|---------------------|  
|**(İstemci) tek başına uygulamaların profilini oluşturma**|-   [Bağımsız uygulamaların profilini oluşturma](../profiling/command-line-profiling-of-stand-alone-applications.md)|  
|**Profil hizmetler**|-   [Profil oluşturma hizmetleri](../profiling/command-line-profiling-of-services.md)|
