---
title: Profiler komut satırını kullanarak bir ASP.NET Web uygulamasından bellek verileri toplama | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
helpviewer_keywords:
- .NET memory profiling method
- profiling tools,.NET memory method
ms.assetid: 57acf2b0-327a-4c0e-8078-ac2f6d99457d
caps.latest.revision: 18
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 373e20ba3130cc5b5c633ef58f104d8cb8112ae3
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54758541"
---
# <a name="collecting-memory-data-from-an-aspnet-web-application-by-using-the-profiler-command-line"></a>Profil Oluşturucu Komut Satırını Kullanarak bir ASP.NET Web Uygulamasından Bellek Verileri Toplama
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bu bölümde kullanarak bir ASP.NET Web uygulaması için bellek ayırma ve nesne yaşam verisi toplamak için seçenekleri ve yordamları açıklanmaktadır **VSPerfCmd** komut satırı aracı.  
  
> [!NOTE]
>  **VSPerfCmd** aracı profil oluşturma araçları işlevselliği, duraklatma ve profil oluşturma ve ek veri işlemci ve Windows performans sayaçlarını toplamayı yeniden başlatma da dahil olmak üzere tam erişimle, sağlar. Ayrıca **VSPerfASPNETCmd** bu işlevselliği gerekmediğinde komut satırı aracı. İle karşılaştırıldığında [VSPerfCmd](../profiling/vsperfcmd.md) komut satırı aracını hiçbir ortam değişkenleri ayarlamanız gerekir ve bilgisayarın yeniden başlatılması gerekli değildir. Daha fazla bilgi için [VSPerfASPNETCmd ile Hızlı Web sitesi profil](../profiling/rapid-web-site-profiling-with-vsperfaspnetcmd.md).  
  
## <a name="common-tasks"></a>Ortak Görevler  
  
|Görev|İlgili içerik|  
|----------|---------------------|  
|**Çalışan bir ASP.NET uygulamasına profil oluşturucu ekleme**|-   [Nasıl Yapılır: Bellek Verileri Toplamak için ASP.NET Web Uygulamasına Profil Oluşturucu Ekleme](../profiling/how-to-attach-the-profiler-to-an-aspnet-web-application-to-collect-memory-data-by-using-the-command-line.md)|  
|**Gereç statik olarak derlenmiş ikili dosyaları**|-   [Nasıl Yapılır: Statik Olarak Derlenmiş Bir ASP.NET Uygulamasını İzleme ve Bellek Verileri Toplama](../profiling/how-to-instrument-a-statically-compiled-aspnet-web-application-and-collect-memory-data-by-using-the-profiler-command-line.md)|  
|**Gereç dinamik olarak derlenmiş ikili dosyaları**|-   [Nasıl Yapılır: Dinamik Olarak Derlenmiş Bir ASP.NET Uygulamasını İzleme ve Bellek Verileri Toplama](../profiling/how-to-instrument-a-dynamically-compiled-aspnet-web-application-and-collect-memory-data-by-using-the-profiler-command-line.md)|  
  
## <a name="related-tasks"></a>İlişkili görevler  
  
### <a name="profiling-aspnet-web-applications"></a>ASP.NET Web Uygulamalarında Profil Oluşturma  
  
|Görev|İlgili içerik|  
|----------|---------------------|  
|**Örnekleme yöntemiyle profili**|-   [Örnekleme kullanarak uygulama istatistikleri toplama](../profiling/collecting-application-statistics-for-aspnet-web-applications-using-the-profiler-sampling-method-from-the-command-line.md)|  
|**İzleme metodunu kullanarak profili**|-   [İzleme kullanarak ayrıntılı zamanlama verileri toplama](/visualstudio/profiling/collecting-detailed-timing-data-aspnet-profiler-instrumentation-method?view=vs-2015)|  
|**Kaynak çakışması ve iş parçacığı etkinliği profil**|-   [Eşzamanlılık verileri toplama](../profiling/collecting-concurrency-data-for-an-aspnet-web-application-using-the-profiler-command-line.md)|  
  
### <a name="profiling-net-framework-memory-data"></a>.NET Framework bellek verileri profil oluşturma  
  
|Görev|İlgili içerik|  
|----------|---------------------|  
|**(İstemci) tek başına uygulamaların profilini oluşturma**|-   [.NET Framework bellek verileri toplama](../profiling/collecting-dotnet-framework-memory-data-for-stand-alone-applications-by-using-the-profiler-command-line.md)|  
|**Profil hizmetler**|-   [.NET bellek verileri toplama](../profiling/collecting-memory-data-from-dotnet-framework-services-by-using-the-profiler-command-line.md)|  
  
### <a name="analyzing-net-memory-data-views-and-reports"></a>.NET bellek verileri analiz etme, görünümleri ve raporlar  
 [.NET Bellek Verisi Görünümleri](../profiling/dotnet-memory-data-views.md)  
  
## <a name="reference"></a>Başvuru  
 [Komut Satırı Profil Oluşturma Araçları Başvurusu](../profiling/command-line-profiling-tools-reference.md)
