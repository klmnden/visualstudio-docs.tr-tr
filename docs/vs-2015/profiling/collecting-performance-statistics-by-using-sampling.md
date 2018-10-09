---
title: Örnekleme kullanarak performans istatistikleri toplama | Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- Profiling Tools,sampling
- sampling profiling method
ms.assetid: 8e36361b-bb3d-40c6-b286-0e68c0ecb915
caps.latest.revision: 26
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: ce6a9fed51e4c5dc93fca406dbb43787700d83d2
ms.sourcegitcommit: 71218ffc33da325cc1b886f69ff2ca50d44f5f33
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/09/2018
ms.locfileid: "48880415"
---
# <a name="collecting-performance-statistics-by-using-sampling"></a>Örnekleme Kullanarak Performans İstatistikleri Toplama
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bu konuda en son sürümünü şu yolda bulunabilir: [tarafından örnekleme kullanarak performans istatistikleri toplama](https://docs.microsoft.com/visualstudio/profiling/collecting-performance-statistics-by-using-sampling).  
  
Varsayılan olarak, [!INCLUDE[vsPreShort](../includes/vspreshort-md.md)] profil oluşturma araçları örnekleme profil bilgilerini her 10.000.000 işlemci döngülerinin (yaklaşık olarak her bir yüzde değerini saniyenin 1 GHz bilgisayarda) toplar. Örnekleme yöntemi çoğu performans araştırmalar başlangıç için önerilen yöntem ve işlemci kullanım sorunları bulmak için kullanışlıdır.  
  
 **Gereksinimler**  
  
-   [!INCLUDE[vsUltLong](../includes/vsultlong-md.md)], [!INCLUDE[vsPreLong](../includes/vsprelong-md.md)], [!INCLUDE[vsPro](../includes/vspro-md.md)]  
  
> [!NOTE]
>  Windows 8 ve Windows Server 2012'deki Gelişmiş güvenlik özellikleri Visual Studio profil oluşturucu bu platformlarda veri toplayan bir şekilde önemli değişiklikler gerekmiştir. Windows Store apps ayrıca yeni toplama teknikleri gerektirir. Bkz: [Windows 8 ve Windows Server 2012 uygulamalarında performans araçları](../profiling/performance-tools-on-windows-8-and-windows-server-2012-applications.md).  
  
 Örnekleme yöntemi, aşağıdaki yordamlardan birini kullanarak belirtebilirsiniz:  
  
-   Profil Oluşturma Sihirbazı'nın ilk sayfasında, tıklayın **CPU örnekleme (önerilir)**.  
  
-   Üzerinde **performans Gezgini** araç penceresindeki **yöntemi** listesinde **örnekleme**.  
  
-   Üzerinde **genel** sayfası için performans oturumu Özellikleri iletişim kutusu tıklayın **örnekleme**.  
  
## <a name="common-tasks"></a>Ortak Görevler  
 Ek seçenekler belirtebilirsiniz _performans oturumu_**özellik sayfaları** performans oturumunun iletişim kutusu. Bu iletişim kutusunu açmak için:  
  
-   İçinde **performans Gezgini**performans oturumu adına sağ tıklayın ve ardından **özellikleri**.  
  
 Aşağıdaki tabloda görevler belirleyebilirsiniz seçenekleri açıklanmıştır _performans oturumu_**özellik sayfaları** iletişim kutusuna örnekleme yöntemiyle profili.  
  
|Görev|İlgili içerik|  
|----------|---------------------|  
|Üzerinde **genel** sayfasında .NET bellek ayırma ve yaşam süresi verilerini toplama ekleyin ve oluşturulan profil oluşturma veri (.vsp) dosyasının adlandırma ayrıntılarını belirtin.|-   [.NET bellek ayırma ve yaşam süresi verilerini toplama](../profiling/collecting-dotnet-memory-allocation-and-lifetime-data.md)<br />-   [Nasıl yapılır: performans veri dosyası adlandırma seçeneklerini ayarlama](../profiling/how-to-set-performance-data-file-name-options.md)|  
|Üzerinde **örnekleme** sayfasında, örnekleme hızını değiştirmek, örnekleme olay işlemci saat döngülerini başka bir işlemci performans sayacı değiştirme veya her ikisini de değiştirin...|-   [Nasıl yapılır: örnekleme olayları seçme](../profiling/how-to-choose-sampling-events.md)|  
|Üzerinde **başlatma** sayfasında, uygulamayı başlatmak için başlangıç sipariş kod çözümünüzde birden fazla .exe projeler varsa belirtin.|-   [Katman etkileşim verileri toplama](../profiling/collecting-tier-interaction-data.md)|  
|Üzerinde **katman etkileşim** sayfasında, theprofiling çalıştırın toplanan veriler ADO.NET çağrı bilgilerini ekleyin.|-   [Katman etkileşim verileri toplama](../profiling/collecting-tier-interaction-data.md)|  
|Üzerinde **Windows olayları** sayfasında, bir veya daha fazla olay izleme için Windows (ETW) olayları, örnekleme verileri toplama belirtin.|-   [Nasıl yapılır: olay izleme için Windows (ETW) verilerini toplama](../profiling/how-to-collect-event-tracing-for-windows-etw-data.md)|  
|Üzerinde **Windows sayaçları** sayfasında işaretleri olarak profil oluşturma verilerini eklemek için bir veya daha fazla işletim sistemi performans sayaçları belirtin.|-   [Nasıl yapılır: Windows sayaç verileri toplama](../profiling/how-to-collect-windows-counter-data.md)|  
|Üzerinde **Gelişmiş** sayfasında, uygulama modüllerinizi birden çok sürümü kullanırsanız profili .NET Framework çalışma zamanının sürümünü belirtin. Varsayılan olarak yüklenen ilk sürüm profil oluşturulan.|-   [Nasıl yapılır: .NET Framework çalışma zamanını belirtin](../profiling/how-to-specify-the-dotnet-framework-runtime.md)|



