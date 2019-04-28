---
title: Performans oturumlarını yapılandırma | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- common tasks, performance
- common tasks, profiling tools
- profiling tools, common tasks
- performance, gathering data
ms.assetid: e1c3ba41-ffca-4edf-9a7f-8a5a9244ef9b
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 4a36486816d9b6bdc160616b893c6d7a79dfad58
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63405775"
---
# <a name="configure-performance-sessions"></a>Performans oturumlarını yapılandırma
Kullanarak [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] profil oluşturma araçları, çok çeşitli çok sayıda uygulama türleri için performans verilerini toplayabilir. Bu bölümde, ilginizi çeken verileri toplamak için profil oluşturma Araçları'nı yapılandırmak için performans oturumu ve hedef ikili performans Wizardand özelliklerini kullanmayı gösterir. Profil oluşturma araçları yapılandırma özellikleri de içinde profil oluşturma yürütmesine toplanan veri miktarını denetlemek için kullanılabilir. Daha fazla bilgi için [veri toplamayı kontrol](../profiling/controlling-data-collection.md).

> [!NOTE]
> Çoğu durumda, varsayılan özellikleri ve performans Sihirbazı kullanarak profil oluşturma verilerinin toplanması etkili bir yoludur. Daha fazla bilgi için [yeni başlayanlar için performans profili oluşturma Kılavuzu](../profiling/beginners-guide-to-performance-profiling.md) ve [Başlarken](../profiling/getting-started-with-performance-tools.md).

## <a name="common-tasks"></a>Ortak görevler

| Görev | İlgili içerik |
| - | - |
| **Temel profil oluşturma seçenekleri ayarlayın:** Yapılandırmanız gereken [!INCLUDE[vs_current_short](../code-quality/includes/vs_current_short_md.md)] Microsoft sembol sunucusu kullanmak için. Bu, Windows ve diğer Microsoft uygulamaları geçerli sürümü için işlevi ve parametre adları gibi semboller erişebildiğinizden emin yapar. Profil oluşturma araçları ve profil oluşturma veri dosyalarıyla adları sistem izinleri gibi profil oluşturma oturumu başlamadan önce diğer genel seçenekleri de belirtebilirsiniz. | -   [Nasıl Yapılır: Başvuru Windows sembol bilgileri](../profiling/how-to-reference-windows-symbol-information.md)<br />-   [Nasıl Yapılır: Sembol bilgilerini seri hale getirme](../profiling/how-to-serialize-symbol-information.md)<br />-   [Nasıl Yapılır: Geçerli oturumu ayarlama](../profiling/how-to-set-the-current-session.md)<br />-   [Nasıl Yapılır: İzinleri ayarlama](../profiling/how-to-set-permissions.md)<br />-   [Nasıl Yapılır: Performans veri dosyası adlandırma seçeneklerini ayarlama](../profiling/how-to-set-performance-data-file-name-options.md) |
| **Toplamak istediğiniz verileri belirtin:** Profil oluşturma oturumunu yapılandırmak için kullandığınız yordam, profil oluşturmak istediğiniz hedef uygulama türü ve toplamak istediğiniz performans veri türüne bağlıdır. | -   [Nasıl Yapılır: Koleksiyon metotları seçme](../profiling/how-to-choose-collection-methods.md)<br />-   [Örnekleme kullanarak performans istatistikleri toplama](../profiling/collecting-performance-statistics-by-using-sampling.md)<br />-   [.NET bellek ayırma ve yaşam süresi verilerini toplama](../profiling/collecting-dotnet-memory-allocation-and-lifetime-data.md)<br />-   [İzleme kullanarak ayrıntılı zamanlama verileri toplama](../profiling/collecting-detailed-timing-data-by-using-instrumentation.md)<br />-   [Nasıl Yapılır: Web sayfalarında JavaScript kodu profili](../profiling/how-to-profile-javascript-code-in-web-pages.md)<br />-   [İş parçacığı ve işlem eşzamanlılık verileri toplama](../profiling/collecting-thread-and-process-concurrency-data.md)<br />-   [Ek performans verileri toplama](../profiling/collecting-additional-performance-data.md) |
| **Gelişmiş yapılandırma seçenekleri ayarlayın:** Birden çok ortak dil çalışma zamanı (CLR) sürümünü yükleyin ve .NET Framework uygulamaları profil, hangi sürümünün profilinin belirtebilirsiniz. Performans oturumu içinde birden fazla .exe dosyası varsa, ikili dosyalarının başlatma sırasını ayarlayabilirsiniz. | -   [Nasıl Yapılır: .NET Framework çalışma zamanını belirtin](../profiling/how-to-specify-the-dotnet-framework-runtime.md)<br />-   [Nasıl Yapılır: Başlamak için ikili dosya belirtme](../profiling/how-to-specify-the-binary-to-start.md) |

## <a name="related-sections"></a>İlgili bölümler
- [Veri toplamayı denetleme](../profiling/controlling-data-collection.md)

## <a name="see-also"></a>Ayrıca bkz.
- [Performans Gezgini](../profiling/performance-explorer.md)