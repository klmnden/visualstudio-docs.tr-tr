---
title: .NET bellek ayırma ve yaşam süresi verilerini toplama | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- .NET memory profiling method
- Profiling Tools,.NET memory method
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- dotnet
ms.openlocfilehash: dbdc92ff0d8a4020c664de527b60e95ed6113329
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62535469"
---
# <a name="collect-net-memory-allocation-and-lifetime-data"></a>.NET bellek ayırma ve yaşam süresi verilerini toplama

Visual Studio profil oluşturma araçları, .NET bellek ayırma koleksiyonunu destekleyen ve yardımcı olan nesne yaşam verisi uygulamanızda bellekle ilgili performans sorunları algılayın.

- Ayrılan .NET Framework bellek nesnelerinin sayısı ve boyutu .NET bellek ayırma hakkındaki verileri içerir.

- Nesne yaşam verisi üç çöp toplama kuşakları geri kazanılan .NET Framework bellek nesnelerinin sayısı ve boyutu içerir.

> [!NOTE]
> Windows 8 ve Windows Server 2012'deki Gelişmiş güvenlik özellikleri Visual Studio profil oluşturucu bu platformlarda veri toplayan bir şekilde önemli değişiklikler gerekmiştir. UWP uygulamaları, ayrıca yeni toplama teknikleri gerektirir. Bkz: [Windows 8 ve Windows Server 2012 uygulamalarında performans araçları](../profiling/performance-tools-on-windows-8-and-windows-server-2012-applications.md).

Örnekleme veya yöntemi profil oluşturma Araçları'nı kullanarak veri toplayabilir.

- Örnekleme yöntemini kullandığınızda, profil oluşturucu tüm .NET bellek ayırma ve kullanmaya veya bağlı işlem tarafından oluşturulan nesneleri izler.

- Araçlar yöntemini kullandığınızda, profil oluşturucu yalnızca .NET bellek ayırma ve izleme eklenmiş modülleri tarafından oluşturulan nesneleri izler.

> [!IMPORTANT]
> .NET bellek verileri (ayırma, nesne kullanım ömrü veya her ikisi de) örnekleme yöntemini kullanarak topladığınız, tüm kullanıcı tarafından belirtilen örnekleme olayları göz ardı edilir ve uygun bir bellek ayırma olayları toplamak için kullanılır.

Profil oluşturma of.NET bellek ayırma etkinleştirirseniz, ayrıca ayırma görünümü sağlar. Profil oluşturma .NET yaşam süresi verilerini etkinleştirirseniz, ayrıca nesne ömrü görünümü sağlar. Daha fazla bilgi için [ayırma görünümü](../profiling/dotnet-memory-allocations-view.md) ve [nesne ömrü görünümü](../profiling/object-lifetime-view.md).

Profil Araçları komut satırı araçları kullanarak .NET bellek verileri toplamak nasıl hakkında daha fazla bilgi için bkz: kullanarak .NET bellek yöntemleri toplamak bellek ayırma ve nesne yaşam verisi [profil oluşturma yöntemleri gelen komut satırını kullanarak](../profiling/using-profiling-methods-to-collect-performance-data-from-the-command-line.md).

## <a name="to-collect-net-memory-data"></a>.NET bellek verileri toplamak için

1. İçinde **performans Gezgini**performans oturumu sağ tıklayın ve ardından **özellikleri**.

2. Üzerinde *performans oturumu* **özellik sayfaları** iletişim kutusu, tıklayın **genel** sekmesine tıklayın ve **toplamak .NET nesnesi ayırma bilgilerini** onay kutusu.

3. .NET nesnesi ömür verilerini toplamak için seçin **ayrıca .NET nesnesi ömür bilgilerini toplayın** onay kutusu.

## <a name="common-tasks"></a>Ortak görevler

Ek seçenekler belirtebilirsiniz _performans oturumu_**özellik sayfaları** performans oturumunun iletişim kutusu. Bu iletişim kutusunu açmak için:

- İçinde **performans Gezgini**performans oturumu adına sağ tıklayın ve ardından **özellikleri**.

Aşağıdaki tabloda görevler belirleyebilirsiniz seçenekleri açıklanmıştır _performans oturumu_**özellik sayfaları** .NET bellek verileri toplamak için iletişim kutusuna.

|Görev|İlgili içerik|
|----------|---------------------|
|Üzerinde **genel** sayfasında, oluşturulan profil oluşturma veri (.vsp) dosyasının adlandırma ayrıntıları belirtin.|- [.NET bellek ayırma ve yaşam süresi verilerini toplama](../profiling/collecting-dotnet-memory-allocation-and-lifetime-data.md)<br />- [Nasıl Yapılır: Performans veri dosyası adlandırma seçeneklerini ayarlama](../profiling/how-to-set-performance-data-file-name-options.md)|
|Üzerinde **başlatma** kod çözümünüz içinde birden çok .exe projeniz varsa başlatılacak uygulamayı seçin.|- [Katman etkileşim verileri toplama](../profiling/collecting-tier-interaction-data.md)|
|Üzerinde **katman etkileşim** sayfasında, profil oluşturma çalışması için ADO.NET çağrı veri ekleyin.|- [Katman etkileşim verileri toplama](../profiling/collecting-tier-interaction-data.md)|
|Üzerinde **Windows olayları** sayfasında, bir veya daha fazla olay izleme için Windows (ETW) olayları, örnekleme verileri toplama belirtin.|- [Nasıl Yapılır: Olay izleme için Windows (ETW) verileri toplama](../profiling/how-to-collect-event-tracing-for-windows-etw-data.md)|
|Üzerinde **Windows sayaçları** sayfasında işaretleri olarak profil oluşturma verilerini eklemek için bir veya daha fazla işletim sistemi performans sayaçları belirtin.|- [Nasıl Yapılır: Windows sayaç verileri toplama](../profiling/how-to-collect-windows-counter-data.md)|
|Üzerinde **Gelişmiş** sayfasında, uygulama modüllerinizi birden çok sürümü kullanırsanız profili .NET Framework çalışma zamanının sürümünü belirtin. Varsayılan olarak yüklenen ilk sürüm profil oluşturulan.|- [Nasıl Yapılır: .NET Framework çalışma zamanını belirtin](../profiling/how-to-specify-the-dotnet-framework-runtime.md)|

## <a name="instrumentation-tasks"></a>Görevleri izleme

Seçenekler aşağıdaki tabloda görevlerdir **özellik sayfaları** cihaz atama yöntemi ile profil oluşturma için belirli bir iletişim kutusu.

|Görev|İlgili içerik|
|----------|---------------------|
|Üzerinde **ikili dosyaları** sayfasında, modüller için izleme eklenmiş kopyalar konumunu belirtin. Varsayılan olarak, orijinal ikililerin bir yedekleme klasörüne taşınır.|- [Nasıl Yapılır: İşaretlenmiş İkili Dosyaları Yeniden Yerleştirme](../profiling/how-to-relocate-instrumented-binaries.md)|
|Üzerinde **izleme** öncesinde ve sonrasında bir komut isteminde çalıştırmak için komutları belirtin sayfasında ve ek yükü, profil oluşturma profili ASP.NET Web sayfalarında JavaScript kodu azaltmak için profil küçük işlevleri Dışla izleme işlemi.|- [Nasıl Yapılır: Hariç tutma veya kısa işlevleri izlemeden içerir](../profiling/how-to-exclude-or-include-short-functions-from-instrumentation.md)<br />- [Nasıl Yapılır: Web Sayfalarında JavaScript Kodunun Profilini Oluşturma](../profiling/how-to-profile-javascript-code-in-web-pages.md)<br />- [Nasıl Yapılır: Ön ve Son İzleme Komutlarını Belirtme](../profiling/how-to-specify-pre-and-post-instrument-commands.md)|
|Üzerinde **CPU sayaçları** sayfasında, profil oluşturma verileri eklemek için bir veya daha fazla işlemci performans sayaçları belirtin.|- [Nasıl Yapılır: CPU Sayaç Verileri Toplama](../profiling/how-to-collect-cpu-counter-data.md)|
|Üzerinde **Gelişmiş** sayfasında, herhangi bir ek VSInstr.exe, dahil etmek veya belirli işlevleri hariç tutmak için seçenekleri gibi istediğiniz seçenekleri belirtin. Vsınstr seçenekleri hakkında daha fazla bilgi için bkz. [Vsınstr](../profiling/vsinstr.md)|- [Nasıl Yapılır: Ek izleme seçeneklerini belirtme](../profiling/how-to-specify-additional-instrumentation-options.md)<br />- [Nasıl Yapılır: Belirli işlevler için izlemeyi sınırı](../profiling/how-to-limit-instrumentation-to-specific-functions.md)|

## <a name="see-also"></a>Ayrıca bkz.

[Performans oturumlarını yapılandırma](../profiling/configuring-performance-sessions.md)
[nasıl yapılır: Koleksiyon metotları seçme](../profiling/how-to-choose-collection-methods.md)
[performans oturumu özellikleri](../profiling/performance-session-properties.md)
