---
title: Örnekleme kullanarak performans istatistikleri toplama | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- Profiling Tools,sampling
- sampling profiling method
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 97644776f4197e2f3286d29cbd3f746f7ecd0b15
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62809658"
---
# <a name="collect-performance-statistics-by-using-sampling"></a>Örnekleme kullanarak performans istatistikleri toplama

Varsayılan olarak, Visual Studio profil oluşturma araçları örnekleme profil bilgilerini her 10.000.000 işlemci döngülerinin (yaklaşık olarak her bir yüzde değerini saniyenin 1 GHz bilgisayarda) toplar. Örnekleme yöntemi çoğu performans araştırmalar başlangıç için önerilen yöntem ve işlemci kullanım sorunları bulmak için kullanışlıdır.

> [!NOTE]
> Windows 8 ve Windows Server 2012'deki Gelişmiş güvenlik özellikleri Visual Studio profil oluşturucu bu platformlarda veri toplayan bir şekilde önemli değişiklikler gerekmiştir. UWP uygulamaları, ayrıca yeni toplama teknikleri gerektirir. Bkz: [Windows 8 ve Windows Server 2012 uygulamalarında performans araçları](../profiling/performance-tools-on-windows-8-and-windows-server-2012-applications.md).

Örnekleme yöntemi, aşağıdaki yordamlardan birini kullanarak belirtebilirsiniz:

- Profil Oluşturma Sihirbazı'nın ilk sayfasında, tıklayın **CPU örnekleme (önerilir)**.
- Üzerinde **performans Gezgini** araç penceresindeki **yöntemi** listesinde **örnekleme**.
- Üzerinde **genel** sayfası için performans oturumu Özellikleri iletişim kutusu tıklayın **örnekleme**.

## <a name="common-tasks"></a>Ortak görevler

Ek seçenekler belirtebilirsiniz _performans oturumu_**özellik sayfaları** performans oturumunun iletişim kutusu. Bu iletişim kutusunu açmak için:

- İçinde **performans Gezgini**performans oturumu adına sağ tıklayın ve ardından **özellikleri**.

  Aşağıdaki tabloda görevler belirleyebilirsiniz seçenekleri açıklanmıştır _performans oturumu_**özellik sayfaları** iletişim kutusuna örnekleme yöntemiyle profili.

|Görev|İlgili içerik|
|----------|---------------------|
|Üzerinde **genel** sayfasında .NET bellek ayırma ve yaşam süresi verilerini toplama ekleyin ve oluşturulan profil oluşturma veri (.vsp) dosyasının adlandırma ayrıntılarını belirtin.|- [.NET bellek ayırma ve yaşam süresi verilerini toplama](../profiling/collecting-dotnet-memory-allocation-and-lifetime-data.md)<br />- [Nasıl Yapılır: Performans Veri Dosyası Adlandırma Seçeneklerini Ayarlama](../profiling/how-to-set-performance-data-file-name-options.md)|
|Üzerinde **örnekleme** sayfasında, örnekleme hızını değiştirmek, örnekleme olay işlemci saat döngülerini başka bir işlemci performans sayacı değiştirme veya her ikisini de değiştirin...|- [Nasıl Yapılır: Örnekleme Olaylarını Seçme](../profiling/how-to-choose-sampling-events.md)|
|Üzerinde **başlatma** sayfasında, uygulamayı başlatmak için başlangıç sipariş kod çözümünüzde birden fazla .exe projeler varsa belirtin.|- [Katman etkileşim verileri toplama](../profiling/collecting-tier-interaction-data.md)|
|Üzerinde **katman etkileşim** sayfasında, theprofiling çalıştırın toplanan veriler ADO.NET çağrı bilgilerini ekleyin.|- [Katman etkileşim verileri toplama](../profiling/collecting-tier-interaction-data.md)|
|Üzerinde **Windows olayları** sayfasında, bir veya daha fazla olay izleme için Windows (ETW) olayları, örnekleme verileri toplama belirtin.|- [Nasıl Yapılır: Windows İçin Olay İzleme (ETW) Verileri Toplama](../profiling/how-to-collect-event-tracing-for-windows-etw-data.md)|
|Üzerinde **Windows sayaçları** sayfasında işaretleri olarak profil oluşturma verilerini eklemek için bir veya daha fazla işletim sistemi performans sayaçları belirtin.|- [Nasıl Yapılır: Windows Sayaç Verileri Toplama](../profiling/how-to-collect-windows-counter-data.md)|
|Üzerinde **Gelişmiş** sayfasında, uygulama modüllerinizi birden çok sürümü kullanırsanız profili .NET Framework çalışma zamanının sürümünü belirtin. Varsayılan olarak yüklenen ilk sürüm profil oluşturulan.|- [Nasıl Yapılır: .NET Framework Çalışma Zamanını Belirtme](../profiling/how-to-specify-the-dotnet-framework-runtime.md)|