---
title: Profil Oluşturucu örnekleme metodunu kullanarak uygulama istatistikleri toplama
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 07840ab2-3a92-4744-ac87-48b19e0ceecd
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: f9b2de87e77abc701f14211cb49e82220c4c935d
ms.sourcegitcommit: 117ece52507e86c957a5fd4f28d48a0057e1f581
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/28/2019
ms.locfileid: "66263002"
---
# <a name="collect-application-statistics-for-services-by-using-the-profiler-sampling-method"></a>Profil Oluşturucu örnekleme metodunu kullanarak hizmetler için uygulama istatistikleri toplama
Bu bölümde, Windows Hizmetleri komut satırından örnekleme yöntemini kullanarak performans istatistikleri toplama seçeneklerini ve yordamlar açıklanmaktadır.

> [!NOTE]
> Windows 8 ve Windows Server 2012'deki Gelişmiş güvenlik özellikleri Visual Studio profil oluşturucu bu platformlarda veri toplayan bir şekilde önemli değişiklikler gerekmiştir. UWP uygulamaları, ayrıca yeni toplama teknikleri gerektirir. Bkz: [Windows 8 ve Windows Server 2012 uygulamalarında performans araçları](../profiling/performance-tools-on-windows-8-and-windows-server-2012-applications.md).

## <a name="common-tasks"></a>Ortak görevler

|Görev|İlgili içerik|
|----------|---------------------|
|**Bir .NET hizmetine profil oluşturucu ekleme**|-   [Nasıl Yapılır: Uygulama istatistikleri toplamak için bir .NET hizmetine profil oluşturucu ekleme](../profiling/how-to-attach-the-profiler-to-a-dotnet-service-to-collect-application-statistics-by-using-the-command-line.md)|
|**Katman etkileşim verileri ekleme**|-   [Katman etkileşim verileri toplama](../profiling/adding-tier-interaction-data-from-the-command-line.md)|
|**C/C++ hizmete profil oluşturucu ekleme**|-   [Nasıl Yapılır: Uygulama istatistikleri toplamak için bir yerel hizmete profil oluşturucu ekleme](../profiling/how-to-attach-the-profiler-to-a-native-service-to-collect-application-statistics-by-using-the-command-line.md)|

## <a name="related-tasks"></a>İlişkili görevler

### <a name="profile-windows-services"></a>Windows Hizmetleri profil

|Görev|İlgili içerik|
|----------|---------------------|
|**İzleme metodunu kullanarak profili**|-   [İzleme kullanarak ayrıntılı zamanlama verileri toplama](../profiling/collecting-detailed-timing-data-for-services-by-using-the-instrumentation-method.md)|
|**.NET bellek ayırma ve atık koleksiyon profili**|-   [.NET bellek verileri toplama](../profiling/collecting-memory-data-from-dotnet-framework-services-by-using-the-profiler-command-line.md)|
|**Kaynak çakışması ve iş parçacığı etkinliği profil**|-   [Eşzamanlılık verileri toplama](../profiling/collecting-concurrency-data-for-a-service-by-using-the-profiler-command-line.md)|

### <a name="profile-by-using-the-sampling-method"></a>Örnekleme yöntemiyle profili

|Görev|İlgili içerik|
|----------|---------------------|
|**(İstemci) tek başına uygulamaların profilini oluşturma**|-   [Örnekleme kullanarak uygulama istatistikleri toplama](../profiling/collecting-application-statistics-for-stand-alone-applications.md)|
|**ASP.NET Web uygulamalarının profilini oluşturma**|-   [Örnekleme kullanarak uygulama istatistikleri toplama](../profiling/collecting-application-statistics-for-aspnet-using-the-profiler-sampling-method.md)|

### <a name="analyze-sampling-data-views-and-reports"></a>Örnekleme veri görünümleri ve raporları analiz edin
- [Örnekleme yöntemi veri görünümleri](../profiling/profiler-sampling-method-data-views.md)
