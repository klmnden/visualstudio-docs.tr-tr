---
title: Profiler örnekleme yöntemini kullanarak hizmetler için uygulama istatistikleri toplama | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
ms.assetid: 07840ab2-3a92-4744-ac87-48b19e0ceecd
caps.latest.revision: 19
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: f3f556a039ab131a563a90010112009b39f4c981
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63445765"
---
# <a name="collecting-application-statistics-for-services-by-using-the-profiler-sampling-method"></a>Profil Oluşturucu Örnekleme Yöntemini Kullanarak Hizmetler için Uygulama İstatistikleri Toplama
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bu bölümde, Windows Hizmetleri komut satırından örnekleme yöntemini kullanarak performans istatistikleri toplama seçeneklerini ve yordamlar açıklanmaktadır.  
  
> [!NOTE]
> Windows 8 ve Windows Server 2012'deki Gelişmiş güvenlik özellikleri Visual Studio profil oluşturucu bu platformlarda veri toplayan bir şekilde önemli değişiklikler gerekmiştir. Windows Store apps ayrıca yeni toplama teknikleri gerektirir. Bkz: [Windows 8 ve Windows Server 2012 uygulamalarında performans araçları](../profiling/performance-tools-on-windows-8-and-windows-server-2012-applications.md).  
  
## <a name="common-tasks"></a>Ortak Görevler  
  
|Görev|İlgili içerik|  
|----------|---------------------|  
|**Bir .NET hizmetine profil oluşturucu ekleme**|-   [Nasıl Yapılır: Uygulama İstatistikleri Toplamak için Bir .NET Hizmetine Profil Oluşturucu Ekleme](../profiling/how-to-attach-the-profiler-to-a-dotnet-service-to-collect-application-statistics-by-using-the-command-line.md)|  
|**Katman etkileşim verileri ekleme**|-   [Katman etkileşim verileri toplama](../profiling/adding-tier-interaction-data-from-the-command-line.md)|  
|**C/C++ hizmete profil oluşturucu ekleme**|-   [Nasıl Yapılır: Uygulama İstatistikleri Toplamak için Yerel Hizmete Profil Oluşturucu Ekleme](../profiling/how-to-attach-the-profiler-to-a-native-service-to-collect-application-statistics-by-using-the-command-line.md)|  
  
## <a name="related-tasks"></a>İlişkili görevler  
  
### <a name="profiling-windows-services"></a>Windows Hizmetleri profil oluşturma  
  
|Görev|İlgili içerik|  
|----------|---------------------|  
|**İzleme metodunu kullanarak profili**|-   [İzleme kullanarak ayrıntılı zamanlama verileri toplama](../profiling/collecting-detailed-timing-data-for-services-by-using-the-instrumentation-method-from-the-profiler-command-line.md)|  
|**.NET bellek ayırma ve atık koleksiyon profili**|-   [.NET bellek verileri toplama](../profiling/collecting-memory-data-from-dotnet-framework-services-by-using-the-profiler-command-line.md)|  
|**Kaynak çakışması ve iş parçacığı etkinliği profil**|-   [Eşzamanlılık verileri toplama](../profiling/collecting-concurrency-data-for-a-service-by-using-the-profiler-command-line.md)|  
  
### <a name="profiling-by-using-the-sampling-method"></a>Örnekleme yöntemiyle profili oluşturma  
  
|Görev|İlgili içerik|  
|----------|---------------------|  
|**(İstemci) tek başına uygulamaların profilini oluşturma**|-   [Örnekleme kullanarak uygulama istatistikleri toplama](../profiling/collecting-application-statistics-for-stand-alone-applications-by-using-the-profiler-command-line.md)|  
|**ASP.NET Web uygulamalarının profilini oluşturma**|-   [Örnekleme kullanarak uygulama istatistikleri toplama](/visualstudio/profiling/collecting-concurrency-data-for-an-aspnet-web-application?view=vs-2015)|  
  
### <a name="analyzing-sampling-data-views-and-reports"></a>Görünümleri ve raporları örnekleme verileri analiz etme  
 [Örnekleme Yöntemi Veri Görünümleri](../profiling/profiler-sampling-method-data-views.md)
