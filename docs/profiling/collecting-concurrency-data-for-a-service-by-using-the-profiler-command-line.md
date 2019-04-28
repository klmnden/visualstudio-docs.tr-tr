---
title: Profiler komut satırını kullanarak bir hizmet için eşzamanlılık verileri toplama | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 275aacba-b2af-4d34-8931-ee30d777a256
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 5df8fa1b0e0d9c76595c29958641de628e5e8b78
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63440217"
---
# <a name="collect-concurrency-data-for-a-service-by-using-the-profiler-command-line"></a>Profil oluşturucu komut satırını kullanarak bir hizmet için eşzamanlılık verileri toplama
Eşzamanlılık yöntemi [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] profil oluşturma araçları, kaynak Çekişme verisi ve gösterir, CPU kullanımı, iş parçacığı Çekişme, iş parçacığı geçişi, eşitleme gecikmeleri, çakışan g/ç ve diğer alanlar, iş parçacığı etkinlik verileri toplamanıza olanak sağlar sistem olayları.

> [!NOTE]
> Windows 8 ve Windows Server 2012'deki Gelişmiş güvenlik özellikleri Visual Studio profil oluşturucu bu platformlarda veri toplayan bir şekilde önemli değişiklikler gerekmiştir. UWP uygulamaları, ayrıca yeni toplama teknikleri gerektirir. Bkz: [Windows 8 ve Windows Server 2012 uygulamalarında performans araçları](../profiling/performance-tools-on-windows-8-and-windows-server-2012-applications.md).

## <a name="common-tasks"></a>Ortak görevler

|Görev|İlgili içerik|
|----------|---------------------|
|**Çalışan bir .NET hizmetine ekleme**|-   [Nasıl Yapılır: Eşzamanlılık verileri toplamak için bir .NET hizmetine profil oluşturucu ekleme](../profiling/how-to-attach-the-profiler-to-a-dotnet-service-to-collect-concurrency-data-by-using-the-command-line.md)|
|**Katman etkileşim verileri ekleme**|-   [Katman etkileşim verileri toplama](../profiling/adding-tier-interaction-data-from-the-command-line.md)|
|**Çalışan bir C/C++ hizmetine ekleme**|-   [Nasıl Yapılır: Eşzamanlılık verileri toplamak için bir yerel hizmete profil oluşturucu ekleme](../profiling/how-to-attach-the-profiler-to-a-native-service-to-collect-concurrency-data-by-using-the-command-line.md)|

## <a name="related-tasks"></a>İlişkili görevler

### <a name="profile-windows-services"></a>Windows Hizmetleri profil

|Görev|İlgili içerik|
|----------|---------------------|
|**Örnekleme yöntemiyle profili**|-   [Örnekleme kullanarak uygulama istatistikleri toplama](../profiling/collecting-application-statistics-for-services-by-using-the-profiler-sampling-method.md)|
|**İzleme metodunu kullanarak profili**|-   [İzleme kullanarak ayrıntılı zamanlama verileri toplama](../profiling/collecting-detailed-timing-data-for-services-by-using-the-instrumentation-method.md)|
|**Profile.NET bellek ayırma ve atık toplama**|-   [.NET bellek verileri toplama](../profiling/collecting-memory-data-from-dotnet-framework-services-by-using-the-profiler-command-line.md)|

### <a name="profile-concurrency-data"></a>Profil eşzamanlılık verileri

|Görev|İlgili içerik|
|----------|---------------------|
|**Bağımsız uygulamalar profili**|-   [Eşzamanlılık verileri toplama](../profiling/collecting-concurrency-data-for-stand-alone-applications.md)|
|**ASP.NET Web uygulamalarının profilini oluşturma**|-   [Eşzamanlılık verileri toplama](../profiling/collecting-concurrency-data-for-an-aspnet-web-application.md)|

### <a name="analyze-concurrency-data-views-and-reports"></a>Eşzamanlılık veri görünümleri ve raporları analiz edin
- [Kaynak çakışması veri görünümleri](../profiling/resource-contention-data-views.md)

- [Eşzamanlılık görselleştiricisi](../profiling/concurrency-visualizer.md)

## <a name="reference"></a>Başvuru
- [Komut satırı profil oluşturma araçları başvurusu](../profiling/command-line-profiling-tools-reference.md)