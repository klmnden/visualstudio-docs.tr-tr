---
title: Toplama istatistiklerini ASP.NET web uygulamaları | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- profiling tools, sampling method
- sampling profling method
ms.assetid: f8383ab1-eb49-4d3f-8608-d8b4d51a81be
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- aspnet
ms.openlocfilehash: f8fd108e71a49e8860a0fd4fec8751da4bc81644
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56638848"
---
# <a name="collect-statistics-for-aspnet-web-apps"></a>ASP.NET web uygulamaları için istatistikleri toplama

Bu bölümdeki yordamları ve kullanarak bir ASP.NET Web uygulaması için performans istatistikleri toplama seçeneklerini açıklar **VSPerfASPNETCmd** ve **VSPerfCmd** komut satırı aracı ve örnekleme profili oluşturma yöntemi.

> [!NOTE]
>  Windows 8 ve Windows Server 2012'deki Gelişmiş güvenlik özellikleri Visual Studio profil oluşturucu bu platformlarda veri toplayan bir şekilde önemli değişiklikler gerekmiştir. UWP uygulamaları, ayrıca yeni toplama teknikleri gerektirir. Bkz: [Windows 8 ve Windows Server 2012 uygulamalarında performans araçları](../profiling/performance-tools-on-windows-8-and-windows-server-2012-applications.md).

> [!NOTE]
>  Ancak **VSPerfCmd** aracı, size tam erişim duraklatma ve profil oluşturma, yeniden başlatma da dahil olmak üzere profil oluşturma araçları işlevsellik ve ek veri işlemci ve Windows performans sayaçlarından toplanan kullanmanız gerekir **VSPerfASPNETCmd** bu işlevselliği gerekmediğinde komut satırı aracı. **VSPerfASPNETCmd** komut satırı aracı, tercih edilen yöntem, olduğunuz bağımsız profil oluşturucuyu kullanarak ASP.NET Web sitesi profili oluşturma. İle karşılaştırıldığında [VSPerfCmd](../profiling/vsperfcmd.md) komut satırı aracını hiçbir ortam değişkenleri ayarlamanız gerekir ve bilgisayarın yeniden başlatılması gerekli değildir. Daha fazla bilgi için [VSPerfASPNETCmd ile hızlı web sitesi profili oluşturma](../profiling/rapid-web-site-profiling-with-vsperfaspnetcmd.md).

## <a name="common-tasks"></a>Ortak görevler

|Görev|İlgili içerik|
|----------|---------------------|
|**Bir ASP.NET uygulamasına profil oluşturucu ekleme**|-   [Nasıl Yapılır: Uygulama istatistikleri toplamak için bir ASP.NET web uygulamasına profil oluşturucu ekleme](../profiling/how-to-attach-the-profiler-to-an-aspnet-web-application-to-collect-application-statistics-by-using-the-command-line.md)|

## <a name="related-tasks"></a>İlişkili görevler

### <a name="profile-aspnet-web-applications"></a>Profil ASP.NET web uygulamaları

|Görev|İlgili içerik|
|----------|---------------------|
|**İzleme metodunu kullanarak profili**|-   [İzleme kullanarak ayrıntılı zamanlama verileri toplama](../profiling/collecting-detailed-timing-data-aspnet-profiler-instrumentation-method.md)|
|**Bellek ayırma ve atık koleksiyon profili**|-   [Bellek verileri toplama](../profiling/collecting-memory-data-from-an-aspnet-web-application.md)|
|**Kaynak çakışması ve iş parçacığı etkinliği profil**|-   [Eşzamanlılık verileri toplama](../profiling/collecting-concurrency-data-for-an-aspnet-web-application.md)|

### <a name="sample-method"></a>Örnek yöntemi

|Görev|İlgili içerik|
|----------|---------------------|
|**(İstemci) tek başına uygulamaların profilini oluşturma**|-   [Örnekleme kullanarak uygulama istatistikleri toplama](../profiling/collecting-application-statistics-for-stand-alone-applications.md)|
|-   **Profil hizmetler**|-   [Örnekleme kullanarak uygulama istatistikleri toplama](../profiling/collecting-application-statistics-for-services-by-using-the-profiler-sampling-method.md)|

### <a name="analyze-sampling-data-views-and-reports"></a>Örnekleme veri görünümleri ve raporları analiz edin
- [Örnekleme yöntemi veri görünümleri](../profiling/profiler-sampling-method-data-views.md)