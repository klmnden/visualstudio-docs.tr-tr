---
title: Toplama ayrıntılı zamanlama verileri komut satırından Profiler izleme metodunu kullanarak bir ASP.NET Web uygulaması için | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- profiling tools,instrumentation method
- instrumentation profiling method
ms.assetid: 29f2fc55-aaf7-4e18-a672-8815455fba73
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- aspnet
ms.openlocfilehash: 79e8ad7842070d13941ad921ccb25ba502209eb0
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63405952"
---
# <a name="collect-detailed-timing-data-for-an-aspnet-web-application-using-the-profiler-instrumentation-method-from-the-command-line"></a>Komut satırından profil oluşturucu izleme metodunu kullanarak bir ASP.NET web uygulaması için ayrıntılı zamanlama verileri toplama
Bu bölümde ayrıntılı performans toplama seçeneklerini ve yordamlar açıklanmaktadır. verileri bir [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] Web uygulamasını kullanarak **VSPerfCmd** komut satırı aracı ve araç haline getirme yöntemi.

> [!NOTE]
> **VSPerfCmd** aracı profil oluşturma araçları işlevselliği, duraklatma ve profil oluşturma ve ek veri işlemci ve Windows performans sayaçlarını toplamayı yeniden başlatma da dahil olmak üzere tam erişimle, sağlar. Ayrıca **VSPerfASPNETCmd** bu işlevselliği gerekmediğinde komut satırı aracı. Comparison için [VSPerfCmd](../profiling/vsperfcmd.md) komut satırı aracı, hiçbir ortam değişkenlerini ayarlamak sahip ve bilgisayarın yeniden başlatılması gerekli değildir. Daha fazla bilgi için [VSPerfASPNETCmd ile hızlı web sitesi profili oluşturma](../profiling/rapid-web-site-profiling-with-vsperfaspnetcmd.md).

## <a name="common-tasks"></a>Ortak görevler

|Görev|İlgili içerik|
|----------|---------------------|
|**Statik olarak derlenmiş ikili dosyaları profili**|-   [Nasıl Yapılır: Statik olarak derlenmiş bir ASP.NET uygulamasın izleme ve ayrıntılı zamanlama verileri toplama](../profiling/how-to-instrument-statically-compiled-aspnet-and-collect-detailed-timing-data.md)|
|**Dinamik olarak derlenmiş ikili dosyaları profili**|-   [Nasıl Yapılır: Dinamik olarak derlenmiş bir ASP.NET uygulamasını izleme ve ayrıntılı zamanlama verileri toplama](../profiling/how-to-instrument-a-dynamically-compiled-aspnet-app-and-collect-timing-data.md)|

## <a name="related-tasks"></a>İlişkili görevler

### <a name="profile-aspnet-web-applications"></a>Profil ASP.NET web uygulamaları

|Görev|İlgili içerik|
|----------|---------------------|
|**Örnekleme yöntemiyle profili**|-   [Örnekleme kullanarak uygulama istatistikleri toplama](../profiling/collecting-application-statistics-for-aspnet-using-the-profiler-sampling-method.md)|
|**Bellek ayırma ve atık koleksiyon profili**|-   [Bellek verileri toplama](../profiling/collecting-memory-data-from-an-aspnet-web-application.md)|
|**Kaynak çakışması ve iş parçacığı etkinliği profil**|-   [Eşzamanlılık verileri toplama](../profiling/collecting-concurrency-data-for-an-aspnet-web-application.md)|

### <a name="profile-by-using-the-instrumentation-method"></a>İzleme metodunu kullanarak profili

|Görev|İlgili içerik|
|----------|---------------------|
|**(İstemci) tek başına uygulamaların profilini oluşturma**|-   [İzleme kullanarak ayrıntılı zamanlama verileri toplama](../profiling/collecting-detailed-timing-data-for-a-stand-alone-application.md)|
|**Profil hizmetler**|-   [İzleme kullanarak ayrıntılı zamanlama verileri toplama](../profiling/collecting-detailed-timing-data-for-services-by-using-the-instrumentation-method.md)|

### <a name="analyze-instrumentation-data-views-and-reports"></a>İzleme veri görünümleri ve raporları analiz edin
- [İzleme metodu veri görünümleri](../profiling/instrumentation-method-data-views.md)