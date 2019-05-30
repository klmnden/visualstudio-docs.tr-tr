---
title: Profil oluşturucu komut satırını kullanarak ASP.NET web uygulaması bellek veri alma
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- .NET memory profiling method
- profiling tools,.NET memory method
ms.assetid: 57acf2b0-327a-4c0e-8078-ac2f6d99457d
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- aspnet
ms.openlocfilehash: 03851869b2067efd014752ab854f30c2d4874711
ms.sourcegitcommit: 117ece52507e86c957a5fd4f28d48a0057e1f581
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/28/2019
ms.locfileid: "66263534"
---
# <a name="collect-memory-data-from-an-aspnet-web-application-by-using-the-profiler-command-line"></a>Profil oluşturucu komut satırını kullanarak bir ASP.NET web uygulamasından bellek verileri toplama
Bu bölümde kullanarak bir ASP.NET Web uygulaması için bellek ayırma ve nesne yaşam verisi toplamak için seçenekleri ve yordamları açıklanmaktadır **VSPerfCmd** komut satırı aracı.

> [!NOTE]
> **VSPerfCmd** aracı profil oluşturma araçları işlevselliği, duraklatma ve profil oluşturma ve ek veri işlemci ve Windows performans sayaçlarını toplamayı yeniden başlatma da dahil olmak üzere tam erişimle, sağlar. Ayrıca **VSPerfASPNETCmd** bu işlevselliği gerekmediğinde komut satırı aracı. İle karşılaştırıldığında [VSPerfCmd](../profiling/vsperfcmd.md) komut satırı aracını hiçbir ortam değişkenleri ayarlamanız gerekir ve bilgisayarın yeniden başlatılması gerekli değildir. Daha fazla bilgi için [VSPerfASPNETCmd ile hızlı web sitesi profili oluşturma](../profiling/rapid-web-site-profiling-with-vsperfaspnetcmd.md).

## <a name="common-tasks"></a>Ortak görevler

|Görev|İlgili içerik|
|----------|---------------------|
|**Çalışan bir ASP.NET uygulamasına profil oluşturucu ekleme**|-   [Nasıl Yapılır: Bellek verileri toplamak için bir ASP.NET web uygulamasına profil oluşturucu ekleme](../profiling/how-to-attach-the-profiler-to-an-aspnet-web-application-to-collect-memory-data-by-using-the-command-line.md)|
|**Gereç statik olarak derlenmiş ikili dosyaları**|-   [Nasıl Yapılır: Statik olarak derlenmiş bir ASP.NET uygulamasını izleme ve bellek verileri toplama](../profiling/how-to-instrument-a-statically-compiled-aspnet-app-and-collect-memory-data.md)|
|**Gereç dinamik olarak derlenmiş ikili dosyaları**|-   [Nasıl Yapılır: Dinamik olarak derlenmiş bir ASP.NET uygulamasını izleme ve bellek verileri toplama](../profiling/how-to-instrument-a-dynamically-compiled-aspnet-web-application-and-collect-memory-data.md)|

## <a name="related-tasks"></a>İlişkili görevler

### <a name="profile-aspnet-web-applications"></a>Profil ASP.NET web uygulamaları

|Görev|İlgili içerik|
|----------|---------------------|
|**Örnekleme yöntemiyle profili**|-   [Örnekleme kullanarak uygulama istatistikleri toplama](../profiling/collecting-application-statistics-for-aspnet-using-the-profiler-sampling-method.md)|
|**İzleme metodunu kullanarak profili**|-   [İzleme kullanarak ayrıntılı zamanlama verileri toplama](../profiling/collecting-detailed-timing-data-aspnet-profiler-instrumentation-method.md)|
|**Kaynak çakışması ve iş parçacığı etkinliği profil**|-   [Eşzamanlılık verileri toplama](../profiling/collecting-concurrency-data-for-an-aspnet-web-application.md)|

### <a name="profile-net-framework-memory-data"></a>Profili .NET Framework bellek verileri

|Görev|İlgili içerik|
|----------|---------------------|
|**(İstemci) tek başına uygulamaların profilini oluşturma**|-   [.NET Framework bellek verileri toplama](../profiling/collecting-dotnet-framework-memory-data-for-stand-alone-applications.md)|
|**Profil hizmetler**|-   [.NET bellek verileri toplama](../profiling/collecting-memory-data-from-dotnet-framework-services-by-using-the-profiler-command-line.md)|

### <a name="analyze-net-memory-data-views-and-reports"></a>.NET bellek verisi görünümleri ve raporları analiz edin
- [.NET bellek verisi görünümleri](../profiling/dotnet-memory-data-views.md)

## <a name="reference"></a>Başvuru
- [Komut satırı profil oluşturma araçları başvurusu](../profiling/command-line-profiling-tools-reference.md)