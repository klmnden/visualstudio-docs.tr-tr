---
title: Profiler komut satırını kullanarak bağımsız uygulamalar için uygulama istatistikleri toplama | Microsoft Docs
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
- sampling profiling method
- profilng tools,sampling method
ms.assetid: be2dbdd0-fc88-45f9-a1d5-bcb4f64e17ad
caps.latest.revision: 24
author: MikeJo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: da0fb80c6787d13b1c30fc13081264736030add0
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53867702"
---
# <a name="collecting-application-statistics-for-stand-alone-applications-by-using-the-profiler-command-line"></a>Profil Oluşturucu Komut Satırını Kullanarak Bağımsız Uygulamalar için Uygulama İstatistikleri Toplama
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bu bölümde, yordamları ve komut satırından örnekleme yöntemini kullanarak bir istemci (tek başına) uygulaması için performans istatistikleri toplama seçeneklerini açıklar.  
  
> [!NOTE]
>  Windows 8 ve Windows Server 2012'deki Gelişmiş güvenlik özellikleri Visual Studio profil oluşturucu bu platformlarda veri toplayan bir şekilde önemli değişiklikler gerekmiştir. Windows Store apps ayrıca yeni toplama teknikleri gerektirir. Bkz: [Windows 8 ve Windows Server 2012 uygulamalarında performans araçları](../profiling/performance-tools-on-windows-8-and-windows-server-2012-applications.md).  
  
## <a name="common-tasks"></a>Ortak Görevler  
  
|Görev|İlgili içerik|  
|----------|---------------------|  
|**Profil oluşturma'ı kullanarak bir uygulama başlatın**|-   [Nasıl Yapılır: Bağımsız bir uygulama başlatma ve uygulama istatistikleri toplama](../profiling/how-to-launch-a-stand-alone-application-with-the-profiler-and-collect-application-statistics-by-using-the-command-line.md)|  
|**Çalışan bir .NET Framework uygulamasına profil oluşturucu ekleme**|-   [Nasıl Yapılır: Profiler'ı bir .NET Framework uygulamasına ekleme ve uygulama istatistikleri toplama](../profiling/how-to-attach-the-profiler-to-a-dotnet-framework-stand-alone-application-and-collect-application-statistics-by-using-the-command-line.md)|  
|**Çalışan bir C/C++ uygulamasına profil oluşturucu ekleme**|-   [Nasıl Yapılır: Profiler bir yerel uygulamaya profil oluşturucu ekleme ve uygulama istatistikleri toplama](../profiling/how-to-attach-the-profiler-to-a-native-stand-alone-application-and-collect-application-statistics-by-using-the-command-line.md)|  
|**Katman etkileşim verileri ekleme**|-   [Katman etkileşim verileri toplama](../profiling/adding-tier-interaction-data-from-the-command-line.md)|  
  
## <a name="related-tasks"></a>İlişkili görevler  
  
### <a name="profiling-stand-alone-applications"></a>Bağımsız Uygulamaların Profilini Oluşturma  
  
|Görev|İlgili içerik|  
|----------|---------------------|  
|**Bir uygulamayı izleme**|-   [İzleme kullanarak ayrıntılı zamanlama verileri toplama](../profiling/collecting-detailed-timing-data-for-a-stand-alone-application-by-using-the-profiler-command-line.md)|  
|**.NET bellek ayırma ve atık koleksiyon verisi toplama**|-   [.NET Framework bellek verileri toplama](../profiling/collecting-dotnet-framework-memory-data-for-stand-alone-applications-by-using-the-profiler-command-line.md)|  
|**Kaynak çakışması ve iş parçacığı yürütme verileri topla**|-   [Eşzamanlılık verileri toplama](../profiling/collecting-concurrency-data-for-stand-alone-applications-by-using-the-profiler-command-line.md)|  
  
### <a name="profiling-by-using-the-sampling-method"></a>Örnekleme yöntemiyle profili oluşturma  
  
|Görev|İlgili içerik|  
|----------|---------------------|  
|**ASP.NET Web uygulamalarının profilini oluşturma**|-   [Örnekleme kullanarak uygulama istatistikleri toplama](/visualstudio/profiling/collecting-concurrency-data-for-an-aspnet-web-application?view=vs-2015)|  
|**Profil hizmetler**|-   [Örnekleme kullanarak uygulama istatistikleri toplama](../profiling/collecting-application-statistics-for-services-by-using-the-profiler-sampling-method.md). Örnekleme yöntemini kullanarak, Windows Hizmetleri'nden performans istatistikleri toplamak nasıl açıklar.|  
  
### <a name="analyzing-sampling-data-views-and-reports"></a>Görünümleri ve raporları örnekleme verileri analiz etme  
 [Örnekleme Yöntemi Veri Görünümleri](../profiling/profiler-sampling-method-data-views.md)



