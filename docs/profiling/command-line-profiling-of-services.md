---
title: Komut satırından hizmetler profili oluşturma | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- profiling toos,services
- profiling services
ms.assetid: f0d62318-b0e8-49c6-9a30-9f7a6adef2f6
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: fde17ace877d9c2fe0ce6c98a64963d82550c3ae
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63405693"
---
# <a name="command-line-profiling-of-services"></a>Komut satırından hizmetler profili oluşturma
Bu bölümde kullanarak Windows Hizmetleri için performans verilerini toplamak için seçenekleri ve yordamları açıklanmaktadır [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] komut satırından profil oluşturma araçları.

> [!NOTE]
> Windows 8 ve Windows Server 2012'deki Gelişmiş güvenlik özellikleri Visual Studio profil oluşturucu bu platformlarda veri toplayan bir şekilde önemli değişiklikler gerekmiştir. UWP uygulamaları, ayrıca yeni toplama teknikleri gerektirir. Bkz: [Windows 8 ve Windows Server 2012 uygulamalarında performans araçları](../profiling/performance-tools-on-windows-8-and-windows-server-2012-applications.md).

## <a name="common-tasks"></a>Ortak görevler

| Görev | İlgili içerik |
| - | - |
| **Uygulama istatistikleri toplamak:** Performans istatistikleri toplamak için örnekleme yöntemini kullanın. Veri örnekleme, CPU kullanımı sorunlarını analiz etmek için ve bir uygulamanın genel performans özelliklerini anlamak için kullanışlıdır. | -   [Örnekleme kullanarak uygulama istatistikleri toplama](../profiling/collecting-application-statistics-for-services-by-using-the-profiler-sampling-method.md) |
| **Ayrıntılı zamanlama verileri toplama:** Ayrıntılı zamanlama bilgilerini toplamak için izleme metodunu kullanın. Ölçümlü izleme verileri ayrıntılı analiz uygulama senaryoları biri için g/ç sorunlarını analiz etmek için yararlı olacaktır. | -   [İzleme kullanarak ayrıntılı zamanlama verileri toplama](../profiling/collecting-detailed-timing-data-for-services-by-using-the-instrumentation-method.md) |
| **.NET bellek verileri toplamak:** Ayrılmış nesnelerin sayısı ve boyutu gösteren .NET bellek ayırma verilerini toplamak için örnekleme veya Araçlar'ı kullanın. Her çöp toplama nesildeki kazanılır nesnelerinin sayısı ve boyutu gösteren nesne yaşam süresi verilerini de toplayabilirsiniz. | -   [.NET bellek verileri toplama](../profiling/collecting-memory-data-from-dotnet-framework-services-by-using-the-profiler-command-line.md) |
| **Eşzamanlılık verileri toplamak:** Kaynak Çekişme verisi ve CPU kullanımı, iş parçacığı Çekişme, iş parçacığı geçişi, eşitleme gecikmeleri, alanları çakışan g/ç ve diğer sistem olaylarıdır gösteren iş parçacığı etkinlik verilerini toplamak için eşzamanlılık yöntemi kullanın. | -   [Eşzamanlılık verileri toplama](../profiling/collecting-concurrency-data-for-a-service-by-using-the-profiler-command-line.md) |
| **Katman etkileşim verileri ekleyin:** Zaman uyumlu ADO.NET ilişkin performans verilerini çağırır, yapılan bir Microsoft hizmeti ekleyebilirsiniz [!INCLUDE[ssNoVersion](../data-tools/includes/ssnoversion_md.md)] veritabanı. | -   [Katman etkileşim verileri toplama](../profiling/adding-tier-interaction-data-from-the-command-line.md) |

## <a name="related-tasks"></a>İlişkili görevler

|Görev|İlgili içerik|
|----------|---------------------|
|**(İstemci) tek başına uygulamaların profilini oluşturma**|-   [Bağımsız uygulamalar profili](../profiling/command-line-profiling-of-stand-alone-applications.md)|
|**Profil ASP.NET uygulamaları**|-   [Profil ASP.NET web uygulamaları](../profiling/command-line-profiling-of-aspnet-web-applications.md)|