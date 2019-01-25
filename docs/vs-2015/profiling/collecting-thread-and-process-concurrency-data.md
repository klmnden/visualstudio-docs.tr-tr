---
title: İş parçacığı ve işlem eşzamanlılık verileri toplama | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
helpviewer_keywords:
- concurrency profiling method
- Profiling Tools, concurrency method
ms.assetid: fa03d381-a9ee-408c-876d-05111e29225b
caps.latest.revision: 19
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: cf8a9de5f2a7e520a745fab81197016d6e1bd15d
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54777018"
---
# <a name="collecting-thread-and-process-concurrency-data"></a>İş Parçacığı ve İşlem Eşzamanlılık Verileri Toplama
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

[!INCLUDE[vsprvs](../includes/vsprvs-md.md)] Profil oluşturma araçları eşzamanlılık profili oluşturma yöntemi, bir işlev bir kaynağa erişim için beklenecek profillenen uygulamanın neden olan her eşitleme olay hakkında bilgiler içeren kaynak çekişmesi verisini toplamak olanak tanır.  
  
 **Gereksinimler**  
  
- [!INCLUDE[vsUltLong](../includes/vsultlong-md.md)], [!INCLUDE[vsPreLong](../includes/vsprelong-md.md)], [!INCLUDE[vsPro](../includes/vspro-md.md)]  
  
  Aşağıdaki yordamlardan birini kullanarak profili oluşturma yöntemi eşzamanlılık belirtebilirsiniz:  
  
- Profil Oluşturma Sihirbazı'nın ilk sayfasında, tıklayın **eşzamanlılık**  
  
- Üzerinde **genel** sayfası için performans oturumu Özellikleri iletişim kutusu tıklayın **eşzamanlılık**.  
  
- Üzerinde **performans Gezgini** araç penceresindeki **yöntemi** listesinde **eşzamanlılık**.  
  
## <a name="common-tasks"></a>Ortak Görevler  
 Ek seçenekler belirtebilirsiniz _performans oturumu_**özellik sayfaları** performans oturumunun iletişim kutusu. Bu iletişim kutusunu açmak için:  
  
- İçinde **performans Gezgini**performans oturumu adına sağ tıklayın ve ardından **özellikleri**.  
  
  Aşağıdaki tabloda görevler belirleyebilirsiniz seçenekleri açıklanmıştır _performans oturumu_**özellik sayfaları** eşzamanlılık metodu kullanarak profil olduğunda iletişim kutusu.  
  
|Görev|İlgili içerik|  
|----------|---------------------|  
|Üzerinde **genel** sayfasında, oluşturulan profil oluşturma veri (.vsp) dosyasının adlandırma ayrıntıları belirtin.|-   [Nasıl Yapılır: Performans Veri Dosyası Adlandırma Seçeneklerini Ayarlama](../profiling/how-to-set-performance-data-file-name-options.md)|  
|Üzerinde **başlatma** sayfasında, kod çözümünüz içinde birden çok .exe projeniz varsa başlatmak için bir uygulama belirtin.|-   [Nasıl Yapılır: Başlatma İçin İkili Dosya Belirtme](../profiling/how-to-specify-the-binary-to-start.md)|  
|Üzerinde **katman etkileşim** sayfasında, profil oluşturma çalışması için ADO.NET çağrı veri ekleyin.|-   [Katman etkileşim verileri toplama](../profiling/collecting-tier-interaction-data.md)|  
|Üzerinde **Windows sayaçları** sayfasında işaretleri olarak profil oluşturma verilerini eklemek için bir veya daha fazla işletim sistemi performans sayaçları belirtin.|-   [Nasıl Yapılır: Windows Sayaç Verileri Toplama](../profiling/how-to-collect-windows-counter-data.md)|  
|Üzerinde **Gelişmiş** sayfasında, uygulama modüllerinizi birden çok sürümü kullanıyorsanız, .NET Framework çalışma zamanı profili sürümünü belirtin. Varsayılan olarak yüklenen ilk sürüm profil oluşturulan.|-   [Nasıl Yapılır: .NET Framework Çalışma Zamanını Belirtme](../profiling/how-to-specify-the-dotnet-framework-runtime.md)|
