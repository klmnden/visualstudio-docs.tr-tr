---
title: Profiler komut satırını kullanarak bağımsız uygulamalar için uygulama istatistikleri toplama | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- sampling profiling method
- profilng tools,sampling method
ms.assetid: be2dbdd0-fc88-45f9-a1d5-bcb4f64e17ad
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 233934f9206e71a4051dbbcd17efc6001656ddfe
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63440229"
---
# <a name="collect-application-statistics-for-stand-alone-applications-by-using-the-profiler-command-line"></a>Profil oluşturucu komut satırını kullanarak bağımsız uygulamalar için uygulama istatistikleri toplama
Bu bölümde, yordamları ve komut satırından örnekleme yöntemini kullanarak bir istemci (tek başına) uygulaması için performans istatistikleri toplama seçeneklerini açıklar.

> [!NOTE]
> Windows 8 ve Windows Server 2012'deki Gelişmiş güvenlik özellikleri Visual Studio profil oluşturucu bu platformlarda veri toplayan bir şekilde önemli değişiklikler gerekmiştir. UWP uygulamaları, ayrıca yeni toplama teknikleri gerektirir. Bkz: [Windows 8 ve Windows Server 2012 uygulamalarında performans araçları](../profiling/performance-tools-on-windows-8-and-windows-server-2012-applications.md).

## <a name="common-tasks"></a>Ortak görevler

|Görev|İlgili içerik|
|----------|---------------------|
|**Profil oluşturma'ı kullanarak bir uygulama başlatın**|-   [Nasıl Yapılır: Bağımsız bir uygulama başlatma ve uygulama istatistikleri toplama](../profiling/how-to-launch-a-stand-alone-app-and-collect-application-statistics.md)|
|**Çalışan bir .NET Framework uygulamasına profil oluşturucu ekleme**|-   [Nasıl Yapılır: Profil oluşturucuyu bir .NET Framework uygulamasına ekleme ve uygulama istatistikleri toplama](../profiling/how-to-attach-the-profiler-to-a-dotnet-app-and-collect-application-statistics.md)|
|**Çalışan bir C/C++ uygulamasına profil oluşturucu ekleme**|-   [Nasıl Yapılır: Yerel bir uygulamaya profil oluşturucu ekleme ve uygulama istatistikleri toplama](../profiling/how-to-attach-the-profiler-to-a-native-app-and-collect-application-statistics.md)|
|**Katman etkileşim verileri ekleme**|-   [Katman etkileşim verileri toplama](../profiling/adding-tier-interaction-data-from-the-command-line.md)|

## <a name="related-tasks"></a>İlişkili görevler

### <a name="profile-stand-alone-applications"></a>Bağımsız uygulamalar profili

|Görev|İlgili içerik|
|----------|---------------------|
|**Bir uygulamayı izleme**|-   [İzleme kullanarak ayrıntılı zamanlama verileri toplama](../profiling/collecting-detailed-timing-data-for-a-stand-alone-application.md)|
|**.NET bellek ayırma ve atık koleksiyon verisi toplama**|-   [.NET Framework bellek verileri toplama](../profiling/collecting-dotnet-framework-memory-data-for-stand-alone-applications.md)|
|**Kaynak çakışması ve iş parçacığı yürütme verileri topla**|-   [Eşzamanlılık verileri toplama](../profiling/collecting-concurrency-data-for-stand-alone-applications.md)|

### <a name="profile-by-using-the-sampling-method"></a>Örnekleme yöntemiyle profili

|Görev|İlgili içerik|
|----------|---------------------|
|**Profil ASP.NET web uygulamaları**|-   [Örnekleme kullanarak uygulama istatistikleri toplama](../profiling/collecting-application-statistics-for-aspnet-using-the-profiler-sampling-method.md)|
|**Profil hizmetler**|-   [Örnekleme kullanarak uygulama istatistikleri toplamak](../profiling/collecting-application-statistics-for-services-by-using-the-profiler-sampling-method.md). Örnekleme yöntemini kullanarak, Windows Hizmetleri'nden performans istatistikleri toplamak nasıl açıklar.|

### <a name="analyze-sampling-data-views-and-reports"></a>Örnekleme veri görünümleri ve raporları analiz edin
- [Örnekleme yöntemi veri görünümleri](../profiling/profiler-sampling-method-data-views.md)
