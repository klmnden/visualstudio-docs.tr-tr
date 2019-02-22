---
title: Tek başına uygulamaların komut satırı profili oluşturma | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- profillng tools,stand-alone applications
- profling stand-alone applications
ms.assetid: a47f2bf2-186d-4120-bb79-34e2f3a1ee42
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: bcd48f421dcae74e82b0d9249a958f2a834f0a45
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56603293"
---
# <a name="command-line-profiling-of-stand-alone-applications"></a>Komut satırından tek başına uygulamaların profilini oluşturma
Bu bölümde kullanarak tek başına (istemci) uygulamaları için performans verilerini toplamak için seçenekleri ve yordamları açıklanmaktadır [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] komut satırından profil oluşturma araçları.

## <a name="common-tasks"></a>Ortak görevler

| Görev | İlgili içerik |
| - | - |
| **Uygulama istatistikleri toplamak:** Performans istatistikleri toplamak için örnekleme yöntemini kullanın. Veri örnekleme, CPU kullanımı sorunlarını analiz etmek için ve bir uygulamanın genel performans özelliklerini anlamak için kullanışlıdır. | -   [Örnekleme kullanarak uygulama istatistikleri toplama](../profiling/collecting-application-statistics-for-stand-alone-applications.md) |
| **Ayrıntılı zamanlama verileri toplama:** Ayrıntılı zamanlama bilgilerini toplamak için izleme metodunu kullanın. Ölçümlü izleme verileri ayrıntılı analiz uygulama senaryoları biri için g/ç sorunlarını analiz etmek için yararlı olacaktır. | -   [İzleme kullanarak ayrıntılı zamanlama verileri toplama](../profiling/collecting-detailed-timing-data-for-a-stand-alone-application.md) |
| **.NET bellek verileri toplamak:** Ayrılmış nesnelerin sayısı ve boyutu gösteren .NET bellek ayırma verilerini toplamak için örnekleme veya Araçlar'ı kullanın. Her çöp toplama nesildeki kazanılır nesnelerinin sayısı ve boyutu gösteren nesne yaşam süresi verilerini de toplayabilirsiniz. | -   [.NET Framework bellek verileri toplama](../profiling/collecting-dotnet-framework-memory-data-for-stand-alone-applications.md) |
| **Eşzamanlılık verileri toplamak:** Kaynak Çekişme verisi ve CPU kullanımı, iş parçacığı Çekişme, iş parçacığı geçişi, eşitleme gecikmeleri, çakışan I/O alanları ve diğer sistem olaylarıdır gösteren iş parçacığı etkinlik verilerini toplamak için eşzamanlılık yöntemi kullanın. | -   [Eşzamanlılık verileri toplama](../profiling/collecting-concurrency-data-for-stand-alone-applications.md) |
| **Katman etkileşim verileri ekleyin:** Zaman uyumlu ADO.NET ilişkin performans verilerini çağırır, Microsoft yapılan uygulama ekleyebileceğiniz [!INCLUDE[ssNoVersion](../data-tools/includes/ssnoversion_md.md)] veritabanı. Bir profil oluşturma yürütmesine katman etkileşim verileri ekleme, komut satırı profil araçlarıyla özel yordamlar gerektirir. | -   [Katman etkileşim verileri toplama](../profiling/adding-tier-interaction-data-from-the-command-line.md) |
| **Deneyin:** Örnek istemci uygulaması örnekleme veya Araçlar yöntemini kullanarak profil için adım adım yordamları kullanın. | -   [İzlenecek yol: Komut satırı kullanarak örnekleme profili oluşturma](../profiling/walkthrough-command-line-profiling-using-sampling.md)<br />-   [İzlenecek yol: Komut satırı araçları kullanarak profil oluşturma](/visualstudio/profiling/command-line-profiling-of-stand-alone-applications) |

## <a name="related-tasks"></a>İlişkili görevler

|Görev|İlgili içerik|
|----------|---------------------|
|**Profil ASP.NET uygulamaları**|-   [Profil ASP.NET web uygulamaları](../profiling/command-line-profiling-of-aspnet-web-applications.md)|
|**Profil hizmetler**|-   [Profil hizmetler](../profiling/command-line-profiling-of-services.md)|