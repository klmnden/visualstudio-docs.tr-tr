---
title: VSPerfASPNETCmd ile hızlı web sitesi profili oluşturma | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- proflilng tools,VSPerfASPNETCmd
- VSPerfASPNETCmd
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 5f86ae2e14067a645bb39a1c8fdc0421f415a9e6
ms.sourcegitcommit: 5694c5236fa32ba7f5bc1236a853f725ec7557e9
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/31/2019
ms.locfileid: "68681131"
---
# <a name="rapid-web-site-profiling-with-vsperfaspnetcmd"></a>VSPerfASPNETCmd ile hızlı web sitesi profili oluşturma

**VSPerfASPNETCmd** komut satırı aracı, Web uygulamalarını kolayca profillemenize [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] olanak sağlar. [VSPerfCmd](../profiling/vsperfcmd.md) komut satırı aracına kıyasla, seçenekler azalır, hiçbir ortam değişkeni ayarlanamaz ve bilgisayarın yeniden başlatılması gerekli değildir. **VSPerfASPNETCmd** kullanmak, tek başına profil Oluşturucu ile profil oluşturma için tercih edilen yöntemdir. Daha fazla bilgi için [nasıl yapılır: Tek başına profil oluşturucuyu](../profiling/how-to-install-the-stand-alone-profiler.md)yükler.

> [!NOTE]
> Windows 8 ve Windows Server 2012'deki Gelişmiş güvenlik özellikleri Visual Studio profil oluşturucu bu platformlarda veri toplayan bir şekilde önemli değişiklikler gerekmiştir. UWP uygulamaları, ayrıca yeni toplama teknikleri gerektirir. Bkz. [Windows 8 ve Windows Server 2012 uygulamalarında performans araçları](../profiling/performance-tools-on-windows-8-and-windows-server-2012-applications.md).

 Eşzamanlılık verileri toplama veya profil oluşturmayı duraklatma ve sürdürme gibi bazı senaryolarda, **VSPerfCmd** kullanılması tercih edilen profil oluşturma yöntemidir.

> [!NOTE]
> Profil oluşturma araçlarının yolunu almak için, bkz. [komut satırı araçlarının yolunu belirtme](../profiling/specifying-the-path-to-profiling-tools-command-line-tools.md). 64-bit bilgisayarlarda araçların 64-bit hem 32-bit sürümleri kullanılabilir. Profil oluşturucu komut satırı araçlarını kullanmak için Araçlar yolunu komut istemi penceresinin PATH ortam değişkenine ekleyin veya komutun kendisine eklemeniz gerekir.

## <a name="profile-an-aspnet-application"></a>ASP.NET uygulaması profili oluşturma

Bir [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] Web uygulaması profili eklemek için aşağıdaki bölümlerde açıklanan komutlardan birini yazın. Web sitesi başlatılır ve profil oluşturucu veri toplamaya başlar. Uygulamanızı alıştırma yapın ve ardından tarayıcıyı kapatın. Profil oluşturmayı durdurmak için komut istemi penceresindeki **ENTER** tuşuna basın.

> [!NOTE]
> Varsayılan olarak, komut istemi bir **VSPerfASPNETCmd** komutundan sonra döndürmez. Komut istemi 'ni döndürmesini zorlamak için **/nowait** seçeneğini kullanabilirsiniz. Bkz. [/NoWait seçeneğini kullanma](#use-the-nowait-option).

## <a name="to-collect-application-statistics-by-using-the-sampling-method"></a>Örnekleme yöntemini kullanarak uygulama istatistikleri toplamak için
 Örnekleme, **VSPerfASPNETCmd** aracının varsayılan profil oluşturma yöntemidir ve komut satırında belirtilmesi gerekmez. Aşağıdaki komut satırı, belirtilen Web uygulamasından uygulama istatistiklerini toplar:

 **vsperfaspnetcmd**  *websiteUrl*

 Yerel sunucu tarafından barındırılan bir *WebSiteUrl 'si* *http://localhost/MySite/default.aspx* örneği olabilir. Dış siteye *http://www.contoso.com* bir örnek. Daha fazla bilgi için, [Visual Studio 'da bir proje açmadan bir Web sitesi profili oluşturma](how-to-collect-performance-data-for-a-web-site.md#to-profile-a-web-site-without-opening-a-project-in-visual-studio)' daki örnek URL 'ler bölümüne bakın.

## <a name="to-collect-detailed-timing-data-by-using-the-instrumentation-method"></a>İzleme yöntemini kullanarak ayrıntılı zamanlama verileri toplama

Dinamik olarak derlenen [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] bir Web uygulamasından ayrıntılı zamanlama verileri toplamak için aşağıdaki komut satırını kullanın:

**vsperfaspnetcmd/Trace**  *websiteUrl*

Statik olarak derlenen profil eklemek istiyorsanız. *DLL* dosyaları Web uygulamanızda, [VSInstr](../profiling/vsinstr.md) komut satırı aracını kullanarak dosyaları seçmeniz gerekir. VSPerfASPNETCmd/Trace komutu, Araçlı dosyalardaki verileri içerir.

## <a name="to-collect-net-memory-data"></a>.NET bellek verileri toplamak için

**/Memory** seçeneği, .net bellekte nesnelerin ayrılması hakkındaki verileri toplar ve bu nesnelerin yaşam süresi hakkında veri toplayabilir. Ayırma verisi toplama, **/Memory** veri seçeneğinin varsayılan modudur ve komut satırında belirtilmesi gerekmez.

 **VSPerfASPNETCmd/Memory** *WebSiteUrl 'si*

 Ayırma verilerine ek olarak nesne yaşam süresi verilerini toplamak için **ömür** parametresini kullanın:

 **VSPerfASPNETCmd/Memory: ömür** *WebSiteUrl 'si*

 .NET bellek verileriyle ayrıntılı zamanlama bilgilerini eklemek için **/Trace** seçeneğini de kullanabilirsiniz:

 **VSPerfASPNETCmd/Memory** [ **: Lifetime**] **/Trace**`websiteUrl`

## <a name="to-collect-tier-interaction-data"></a>Katman etkileşim verilerini toplamak için

> [!WARNING]
> Katman etkileşimi profil oluşturma (tıp) verileri, herhangi bir Visual Studio sürümü kullanılarak toplanabilir. Ancak, katman etkileşimi profil oluşturma verileri yalnızca Visual Studio Enterprise görüntülenebilir.
>
> Windows 8 veya Windows Server 2012 ' de tıp verisi toplamak için, izleme ( **/Trace**) seçeneğini kullanmanız gerekir.

Örnekleme verileriyle katman etkileşim verileri toplamak için:

**VSPerfASPNETCmd/tip**`websiteUrl`

Katman etkileşimi verilerini izleme verileriyle toplamak için:

**VSPerfASPNETCmd/Trace/tip** *WebSiteUrl 'si*

.NET bellek verileriyle katman etkileşim verileri toplamak için:

**VSPerfASPNETCmd/Memory** [ **: Lifetime**] **/tip** _WebSiteUrl 'si_

## <a name="use-the-nowait-option"></a>/NoWait seçeneğini kullanın

Varsayılan olarak, komut istemi bir **VSPerfASPNETCmd** komutundan sonra döndürmez. Komut istemi 'ni döndürmesini zorlamak için aşağıdaki söz dizimi seçeneğini kullanabilirsiniz. Daha sonra komut istemi penceresinde başka işlemler gerçekleştirebilirsiniz. Profil oluşturmayı sonlandırmak için, **/Shutdown** seçeneğini ayrı bir **VSPerfASPNETCmd** komutunda kullanın.

Profil oluşturmaya başlamak için:

**VSPerfASPNETCmd** [ */Options*] **/nowait** _WebSiteUrl 'si_

Profil oluşturmayı sonlandırmak için:

**VSPerfASPNETCmd/Shutdown** *WebSiteUrl 'si*

## <a name="additional-options"></a>Ek seçenekler

Aşağıdaki seçeneklerden herhangi birini, **VSPerfASPNETCmd/Shutdown** komutu hariç, bu bölümün önceki kısımlarında listelenen komutlara ekleyebilirsiniz.

|Seçenek|Açıklama|
|------------|-----------------|
|**/Output:** `VspFile`|Varsayılan olarak, profil oluşturma verileri (. *VSP*) dosyası, geçerli dizinde, bu dosya adı **PerformanceReport. vsp**olarak oluşturulur. Farklı bir konum, dosya adı veya her ikisini de belirtmek için/output seçeneğini kullanın.|
|**/PackSymbols: kapalı**|Varsayılan olarak, VsPerfASPNETCmd, içindeki sembolleri (işlev ve parametre adları vb.) katıştırır. *VSP* dosyası. Sembolleri katıştırmak, profil oluşturma veri dosyasını çok büyük hale getirir. Öğesine erişiminiz varsa. sembolleri içeren *pdb* dosyaları verileri çözümlediğinizde, sembollerin gömülmesini devre dışı bırakmak için/packsymbols: off seçeneğini kullanın.|
