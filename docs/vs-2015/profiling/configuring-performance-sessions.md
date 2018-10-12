---
title: Performans oturumlarını yapılandırma | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- common tasks, performance
- common tasks, profiling tools
- profiling tools, common tasks
- performance, gathering data
ms.assetid: e1c3ba41-ffca-4edf-9a7f-8a5a9244ef9b
caps.latest.revision: 41
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 6b858d7a521f53876e185d8d4deb2b3467833d02
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49285343"
---
# <a name="configuring-performance-sessions"></a>Performans Oturumlarını Yapılandırma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Kullanarak [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] profil oluşturma araçları, çok çeşitli çok sayıda uygulama türleri için performans verilerini toplayabilir. Bu bölümde, ilginizi çeken verileri toplamak için profil oluşturma Araçları'nı yapılandırmak için performans oturumu ve hedef ikili performans Wizardand özelliklerini kullanmayı gösterir. Profil oluşturma araçları yapılandırma özellikleri de içinde profil oluşturma yürütmesine toplanan veri miktarını denetlemek için kullanılabilir. Daha fazla bilgi için [veri toplamayı denetleme](../profiling/controlling-data-collection.md).  
  
> [!NOTE]
>  Çoğu durumda, varsayılan özellikleri ve performans Sihirbazı kullanarak profil oluşturma verilerinin toplanması etkili bir yoludur. Daha fazla bilgi için [performans profili oluşturma Başlangıç Kılavuzu](../profiling/beginners-guide-to-performance-profiling.md) ve [Başlarken](../profiling/getting-started-with-performance-tools.md).  
  
## <a name="common-tasks"></a>Ortak Görevler  
  
|Görev|İlgili içerik|  
|----------|---------------------|  
|**Temel profil oluşturma seçenekleri ayarlayın:** yapılandırmanız gereken [!INCLUDE[vs_current_short](../includes/vs-current-short-md.md)] Microsoft sembol sunucusu kullanmak için. Bu, Windows ve diğer Microsoft uygulamaları geçerli sürümü için işlevi ve parametre adları gibi semboller erişebildiğinizden emin yapar. Profil oluşturma araçları ve profil oluşturma veri dosyalarıyla adları sistem izinleri gibi profil oluşturma oturumu başlamadan önce diğer genel seçenekleri de belirtebilirsiniz.|-   [Nasıl yapılır: başvuru Windows sembol bilgileri](../profiling/how-to-reference-windows-symbol-information.md)<br />-   [Nasıl yapılır: sembol bilgilerini seri hale getirme](../profiling/how-to-serialize-symbol-information.md)<br />-   [Nasıl yapılır: geçerli oturumu ayarlama](../profiling/how-to-set-the-current-session.md)<br />-   [Nasıl yapılır: izinleri ayarlama](../profiling/how-to-set-permissions.md)<br />-   [Nasıl yapılır: performans veri dosyası adlandırma seçeneklerini ayarlama](../profiling/how-to-set-performance-data-file-name-options.md)|  
|**Toplamak istediğiniz verileri belirtin:** profil oluşturma oturumunu yapılandırmak için kullandığınız yordam profil oluşturmak istediğiniz hedef uygulama türü ve toplamak istediğiniz performans veri türüne bağlıdır.|-   [Nasıl yapılır: Koleksiyon metotları seçme](../profiling/how-to-choose-collection-methods.md)<br />-   [Örnekleme kullanarak performans istatistikleri toplama](../profiling/collecting-performance-statistics-by-using-sampling.md)<br />-   [.NET bellek ayırma ve yaşam süresi verilerini toplama](../profiling/collecting-dotnet-memory-allocation-and-lifetime-data.md)<br />-   [İzleme kullanarak ayrıntılı zamanlama verileri toplama](../profiling/collecting-detailed-timing-data-by-using-instrumentation.md)<br />-   [Nasıl yapılır: Web sayfalarında JavaScript kodu profili](../profiling/how-to-profile-javascript-code-in-web-pages.md)<br />-   [İş parçacığı ve işlem eşzamanlılık verileri toplama](../profiling/collecting-thread-and-process-concurrency-data.md)<br />-   [Ek performans verileri toplama](../profiling/collecting-additional-performance-data.md)|  
|**Gelişmiş yapılandırma seçenekleri ayarlayın:** birden çok ortak dil çalışma zamanı (CLR) sürümünü yükleyin ve .NET Framework uygulamaları profili oluşturduğunuzda, hangi sürümünün profilinin belirtebilirsiniz. Performans oturumu içinde birden fazla .exe dosyası varsa, ikili dosyalarının başlatma sırasını ayarlayabilirsiniz.|-   [Nasıl yapılır: .NET Framework çalışma zamanını belirtin](../profiling/how-to-specify-the-dotnet-framework-runtime.md)<br />-   [Nasıl yapılır: başlatma için ikili dosya belirtme](../profiling/how-to-specify-the-binary-to-start.md)|  
  
## <a name="related-sections"></a>İlgili Bölümler  
 [Veri Koleksiyonunu Denetleme](../profiling/controlling-data-collection.md)  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Performans Gezgini](../profiling/performance-explorer.md)



