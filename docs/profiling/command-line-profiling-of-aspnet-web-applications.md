---
title: ASP.NET Web uygulamalarının komut satırı profili oluşturma | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- profiling ASP.NET applications
- profling tools,ASP.NET applications
ms.assetid: 897c00d5-5767-433b-a960-4a29c6023ede
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- aspnet
ms.openlocfilehash: a174f3b428f0a4c7713fa8b368d521c9f826b605
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/17/2019
ms.locfileid: "59648347"
---
# <a name="command-line-profiling-of-aspnet-web-applications"></a>ASP.NET web uygulamalarının komut satırı profili oluşturma
Bu bölümde yordamları ve performans verilerini toplamak için seçenekleri açıklar [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] Web uygulamaları kullanarak [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] komut satırından profil oluşturma araçları.

> [!NOTE]
>  Windows 8 ve Windows Server 2012'deki Gelişmiş güvenlik özellikleri Visual Studio profil oluşturucu bu platformlarda veri toplayan bir şekilde önemli değişiklikler gerekmiştir. UWP uygulamaları, ayrıca yeni toplama teknikleri gerektirir. Bkz: [Windows 8 ve Windows Server 2012 uygulamalarında performans araçları](../profiling/performance-tools-on-windows-8-and-windows-server-2012-applications.md).

## <a name="common-tasks"></a>Ortak görevler

| Görev | İlgili içerik |
| - | - |
| **Temel ASP.NET profil oluşturma verilerini kolayca toplayın:** Kullanım **VSPerfASPNETCmd** örnekleme, izleme, .NET bellek, çekişmeyi toplamak veya yapılandırma gereksinimleri ve gerekli olan Internet Information Services (IIS) yeniden başlatma olmadan etkileşim veri katmanı için aracı için **VSPerfCmd**. **VSPerfASPNETCmd** ek veri toplamak için veya veri toplamayı denetlemek için izin vermez. **Not:**  **VSPerfASPNETCmd** kullanmayı tercih edilen araç bağımsız profil oluşturucu profil ASP.NET Web siteleri için kullanın. | -   [Profil oluşturma VSPerfASPNETCmd ile hızlı web sitesi](../profiling/rapid-web-site-profiling-with-vsperfaspnetcmd.md) |
| **Uygulama istatistikleri toplamak:** Performans istatistikleri toplamak için örnekleme yöntemini kullanın. Veri örnekleme, CPU kullanım sorunlarını analiz etmek için ve bir uygulamanın genel performans özelliklerini anlamak için kullanışlıdır. | -   [Örnekleme kullanarak uygulama istatistikleri toplama](../profiling/collecting-application-statistics-for-aspnet-using-the-profiler-sampling-method.md) |
| **Ayrıntılı zamanlama verileri toplama:** Ayrıntılı zamanlama bilgilerini toplamak için izleme metodunu kullanın. Ölçümlü izleme verileri ayrıntılı analiz uygulama senaryoları biri için g/ç sorunlarını analiz etmek için yararlı olacaktır. | -   [İzleme kullanarak ayrıntılı zamanlama verileri toplama](../profiling/collecting-detailed-timing-data-aspnet-profiler-instrumentation-method.md) |
| **.NET bellek verileri toplamak:** Ayrılmış nesnelerin sayısı ve boyutu gösteren .NET bellek ayırma verilerini toplamak için örnekleme veya Araçlar'ı kullanın. Her çöp toplama nesildeki kazanılır nesnelerinin sayısı ve boyutu gösteren nesne yaşam süresi verilerini de toplayabilirsiniz. | -   [Bellek verileri toplama](../profiling/collecting-memory-data-from-an-aspnet-web-application.md) |
| **Eşzamanlılık verileri toplamak:** Kaynak çekişmesi verisini toplamak için eşzamanlılık yöntemi kullanın. **Not:**  İş parçacığı etkinliği ve görselleştirme verilerini toplamak için Web uygulamaları desteklenmez. | -   [Eşzamanlılık verileri toplama](../profiling/collecting-concurrency-data-for-an-aspnet-web-application.md) |
| **Katman etkileşim verileri ekleyin:** Zaman uyumlu ilişkin performans verilerini ekleyebilirsiniz [!INCLUDE[vstecado](../data-tools/includes/vstecado_md.md)] çağrılarının [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] Web uygulaması için bir Microsoft yapar [!INCLUDE[ssNoVersion](../data-tools/includes/ssnoversion_md.md)] veritabanı. | -   [Katman etkileşim verileri toplama](../profiling/adding-tier-interaction-data-from-the-command-line.md) |

## <a name="related-tasks"></a>İlişkili görevler

|Görev|İlgili içerik|
|----------|---------------------|
|**(İstemci) tek başına uygulamaların profilini oluşturma**|-   [Bağımsız uygulamalar profili](../profiling/command-line-profiling-of-stand-alone-applications.md)|
|**Profil hizmetler**|-   [Profil hizmetler](../profiling/command-line-profiling-of-services.md)|