---
title: Tek başına uygulamaların komut satırı profili oluşturma | Microsoft Docs
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
- profillng tools,stand-alone applications
- profling stand-alone applications
ms.assetid: a47f2bf2-186d-4120-bb79-34e2f3a1ee42
caps.latest.revision: 21
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 0eb4f54c562ea9812c2196c53775b0acd872f877
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49252219"
---
# <a name="command-line-profiling-of-stand-alone-applications"></a>Bağımsız Uygulamaların Komut Satırından Profilinin Oluşturulması
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bu bölümde kullanarak tek başına (istemci) uygulamaları için performans verilerini toplamak için seçenekleri ve yordamları açıklanmaktadır [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] komut satırından profil oluşturma araçları.  
  
## <a name="common-tasks"></a>Ortak Görevler  
  
|Görev|İlgili içerik|  
|----------|---------------------|  
|**Uygulama istatistikleri toplamak:** performans istatistikleri toplamak için örnekleme yöntemini kullanın. Veri örnekleme, CPU kullanımı sorunlarını analiz etmek için ve bir uygulamanın genel performans özelliklerini anlamak için kullanışlıdır.|-   [Örnekleme kullanarak uygulama istatistikleri toplama](../profiling/collecting-application-statistics-for-stand-alone-applications-by-using-the-profiler-command-line.md)|  
|**Ayrıntılı zamanlama verileri toplama:** ayrıntılı zamanlama bilgileri toplamak için izleme metodunu kullanın. Ölçümlü izleme verileri ayrıntılı analiz uygulama senaryoları biri için g/ç sorunlarını analiz etmek için yararlı olacaktır.|-   [İzleme kullanarak ayrıntılı zamanlama verileri toplama](../profiling/collecting-detailed-timing-data-for-a-stand-alone-application-by-using-the-profiler-command-line.md)|  
|**.NET bellek verileri toplamak:** kullanım örnekleme veya Araçlar boyutunu ve sayısını gösteren .NET bellek ayırma verilerini toplamak için ayrılan nesneler. Her çöp toplama nesildeki kazanılır nesnelerinin sayısı ve boyutu gösteren nesne yaşam süresi verilerini de toplayabilirsiniz.|-   [.NET Framework bellek verileri toplama](../profiling/collecting-dotnet-framework-memory-data-for-stand-alone-applications-by-using-the-profiler-command-line.md)|  
|**Eşzamanlılık verileri toplamak:** kaynak Çekişme verisi ve, CPU kullanımı, iş parçacığı Çekişme, iş parçacığı geçişi, eşitleme gecikmeleri, çakışan g/ç ve diğer alanları gösteren iş parçacığı etkinlik verilerini toplamak için eşzamanlılık yöntemi kullanın. sistem olayları.|-   [Eşzamanlılık verileri toplama](../profiling/collecting-concurrency-data-for-stand-alone-applications-by-using-the-profiler-command-line.md)|  
|**Katman etkileşim verileri ekleme:** zaman uyumlu ADO.NET ilişkin performans verilerini çağırır, Microsoft yapılan uygulama ekleyebileceğiniz [!INCLUDE[ssNoVersion](../includes/ssnoversion-md.md)] veritabanı. Bir profil oluşturma yürütmesine katman etkileşim verileri ekleme, komut satırı profil araçlarıyla özel yordamlar gerektirir.|-   [Katman etkileşim verileri toplama](../profiling/adding-tier-interaction-data-from-the-command-line.md)|  
|**Deneyin:** örnek istemci uygulaması örnekleme veya Araçlar yöntemini kullanarak profil için adım adım yordamları kullanın.|-   [İzlenecek yol: Örnekleme metodunu kullanarak komut satırı profil](../profiling/walkthrough-command-line-profiling-using-sampling.md)<br />-   [İzlenecek yol: İzleme metodunu kullanarak komut satırı profil](../profiling/walkthrough-command-line-profiling-using-instrumentation.md)|  
  
## <a name="related-tasks"></a>İlişkili görevler  
  
|Görev|İlgili içerik|  
|----------|---------------------|  
|**Profil ASP.NET uygulamaları**|-   [ASP.NET Web uygulamalarında profil oluşturma](../profiling/command-line-profiling-of-aspnet-web-applications.md)|  
|**Profil hizmetler**|-   [Profil oluşturma hizmetleri](../profiling/command-line-profiling-of-services.md)|



