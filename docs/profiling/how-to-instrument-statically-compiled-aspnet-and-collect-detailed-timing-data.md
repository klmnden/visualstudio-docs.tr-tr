---
title: 'Profiler komut satırı: Statik bir ASP.NET uygulamasını izleme, zamanlama verileri Al'
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: b260ce68-76e6-4c3b-8062-3c00bd5cf7b8
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- aspnet
ms.openlocfilehash: 9e66eedf0de32e0af6f387a755b5e439a2b2e5e1
ms.sourcegitcommit: 91c7f1b525e0c22d938bc4080ba4ceac2483474f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/12/2019
ms.locfileid: "67032981"
---
# <a name="how-to-instrument-a-statically-compiled-aspnet-web-application-and-collect-detailed-timing-data-with-the-profiler-by-using-the-command-line"></a>Nasıl yapılır: Gereç statik olarak derlenmiş bir ASP.NET web uygulaması ve komut satırını kullanarak profil oluşturucu ile toplama ayrıntılı zamanlama verileri
Bu makalede nasıl kullanılacağını [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] önceden derlenmiş bir araç haline getirmek için profil oluşturma araçları komut satırı araçlarının [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] web bileşeni veya web sitesi ve ayrıntılı zamanlama verileri toplama.

> [!NOTE]
> Profil oluşturma araçları için olan yolu almak için bkz: [komut satırı araçları yolunu belirtin](../profiling/specifying-the-path-to-profiling-tools-command-line-tools.md). 64-bit bilgisayarlarda araçların 64-bit hem 32-bit sürümleri kullanılabilir. Profil oluşturucu komut satırı araçlarını kullanmak için Araçlar yolunu komut istemi penceresinin PATH ortam değişkenine ekleyin veya komutun kendisine eklemeniz gerekir.
>
> Bir profil oluşturma yürütmesine katman etkileşim verileri ekleme, komut satırı profil araçlarıyla özel yordamlar gerektirir. Bkz: [katman etkileşim verileri toplama](../profiling/adding-tier-interaction-data-from-the-command-line.md).

 Ayrıntılı zamanlama verileri toplamak için bir [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] izleme metodunu kullanarak Web bileşeni kullandığınız [VSInstr.exe](../profiling/vsinstr.md) aracını bileşenin belgelenmiş bir sürümünü oluşturmak için. Bileşeni barındıran bilgisayarda, izleme eklenmiş sürümüyle değiştirirsiniz bileşenin sürümünü değiştirin. Daha sonra [VSPerfCLREnv.cmd](../profiling/vsperfclrenv.md) aracı genel profil oluşturma ortamı değişkenlerini başlatmak ve ana bilgisayar yeniden başlatılır. Ardından profil oluşturucuyu başlatın.

 Araçlı bileşen yürütüldüğünde, zamanlama verileri bir veri dosyasına otomatik olarak toplanır. Duraklatma ve profil oluşturma oturumu sırasında veri koleksiyonu devam ettirin.

 Profil oluşturma oturumunu sona erdirmek için kapatma [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] çalışan işlemini bileşeni barındıran ve profil oluşturucuyu açıkça kapatın. Çoğu durumda, bir oturumun sonunda profil oluşturma ortam değişkenlerini temizlemenizi öneririz.

## <a name="start-to-profile"></a>Profile Başlat

#### <a name="to-instrument-an-aspnet-web-component-and-start-profiling"></a>Bir ASP.NET web bileşenini izleme ve profil oluşturmayı başlatmak için

1. Bir komut istemi penceresi açın.

2. Kullanım **Vsınstr** aracı hedef uygulamanın belgelenmiş bir sürümünü oluşturmak için. Gerekirse, ASP.NET ana bilgisayarda uygulama ikili dosyalarını Araçlı ikililerle değiştirin.

3. .NET profil oluşturma ortamı değişkenlerini başlatın. Komut İstemi penceresinde yazın:

    **VSPerfClrEnv /globaltraceon**

4. Bilgisayarı yeniden başlatın.

5. Bir komut istemi penceresi açın. Gerekirse, profil oluşturucu araçları yolunu ayarlayın.

6. Profil oluşturucuyu başlatın. Tür:

    **VSPerfCmd çalıştığından/Output:** `OutputFile` [`Options`]

   - [/Start](../profiling/start.md) **: izleme** seçeneği profil oluşturucuyu başlatır.

   - [/Output](../profiling/output.md) **:** `OutputFile` ile seçeneği gereklidir **/start**. `OutputFile` Profil oluşturma veri (.vsp) dosyasının konumunu ve adını belirtir.

     Aşağıdaki seçeneklerle dilediğinizi kullanabilirsiniz **çalıştığından** seçeneği.

   > [!NOTE]
   > **/User** ve **/crosssession** seçenekleri genellikle ASP.NET uygulamaları için gereklidir.

   | Seçenek | Açıklama |
   | - | - |
   | [/ User](../profiling/user-vsperfcmd.md) **:** [`Domain` **\\** ]`UserName` | ASP.NET çalışan işlemine sahip hesabın etki alanı ve kullanıcı adını belirtir. Bu seçenek, oturum açan kullanıcının farklı bir kullanıcı olarak işlem çalışıyorsa gereklidir. İşlem sahibi listelenen **kullanıcı adı** sütunu **işlemleri** Windows Görev Yöneticisi'nin sekmesinde. |
   | [/ crosssession](../profiling/crosssession.md) | Etkinleştirir işlemleri diğer oturum açılışlarında profil oluşturma. ASP.NET uygulaması başka bir oturumda çalışıyorsa bu seçenek gereklidir. Oturum tanımlayıcısı oturum kimliği sütununda listelenir **işlemleri** Windows Görev Yöneticisi'nin sekmesinde. **/CS** için bir kısaltma olarak belirtilebilir **/crosssession**. |
   | [/wincounter](../profiling/wincounter.md) **:** `WinCounterPath` | Profil oluşturma sırasında Tahsil edilecek Windows performans sayacı belirtir. |
   | [/automark](../profiling/automark.md) **:** `Interval` | İle kullanma **/wincounter** yalnızca. Windows performans sayacı toplama olayları arasındaki milisaniye sayısını belirtir. 500 ms varsayılandır. |
   | [/Events](../profiling/events-vsperfcmd.md) **:** `Config` | Profil oluşturma sırasında Tahsil edilecek bir olay izleme için Windows (ETW) olayı belirtir. Ayrı bir toplanan ETW olayları (. *etl*) dosyası. |
   | [/globaloff](../profiling/globalon-and-globaloff.md) | Profil Oluşturucu veri toplamayı başlatmak için duraklatıldı, ekleme **/globaloff** seçeneğini **/start** komut satırı. Kullanım **/globalon** profil oluşturmayı devam ettirmek için. |

7. İzleme eklenmiş bileşeni içeren Web sitesini açın.

## <a name="control-data-collection"></a>Veri toplamayı denetleme
 Hedef uygulama çalışırken kullanarak verinin yazılmasını durdurmayla ve veri toplamayı kontrol edebilirsiniz *VSPerfCmd.exe* seçenekleri. Veri toplama denetimi uygulamayı kapatma veya başlatma gibi program yürütmenin özel bir bölümü için veri toplamanızı sağlar.

#### <a name="to-start-and-stop-data-collection"></a>Veri toplamayı durdurmak ve başlatmak

- Aşağıdaki seçenekleri çiftlerini başlatın ve veri toplama işlemini durdurun. Her seçeneği ayrı bir komut satırında belirtin. Veri Toplama'ı, birden çok kez açıp kapatabilirsiniz.

    |Seçenek|Açıklama|
    |------------|-----------------|
    |[/ globalon /globaloff](../profiling/globalon-and-globaloff.md)|Başlar ( **/globalon**) veya durdurur ( **/globaloff**) tüm işlemler için veri toplama.|
    |[/processon](../profiling/processon-and-processoff.md) **:** `PID` [/processoff](../profiling/processon-and-processoff.md) **:** `PID`|Başlar ( **/processon**) veya durdurur ( **/processoff**) işlem kimliği tarafından belirtilen işlem için veri toplama (`PID`).|
    |[/threadon](../profiling/threadon-and-threadoff.md) **:** `TID` [/threadoff](../profiling/threadon-and-threadoff.md) **:** `TID`|Başlar ( **/threadon**) veya durdurur ( **/threadoff**) veri toplama iş parçacığı kimliği tarafından belirtilen iş parçacığı için (`TID`).|

## <a name="end-the-profiling-session"></a>Profil oluşturma oturumunu sona erdirme
 Profil oluşturma oturumunu sona erdirmek için kapatma [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] Web uygulamasını ve ardından Internet Information Services (IIS) **IISReset** kapatmak için komut [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] çalışan işlemi. Çağrı **VSPerfCmd** [/shutdown](../profiling/shutdown.md) profil oluşturucuyu devre dışı bırakırsınız ve profil oluşturma veri dosyasını kapatırsınız.

 **VSPerfClrEnv /globaloff** komutu profil oluşturma ortam değişkenlerini temizler. Yeni ortam ayarlarının uygulanması için bilgisayarı yeniden başlatmanız gerekir.

#### <a name="to-end-a-profiling-session"></a>Profil oluşturma oturumunu sona erdirmek için

1. Kapat [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] Web uygulaması.

2. Kapat [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] çalışan işlemi. Tür:

    **IISReset/stop**

3. Profil oluşturucuyu kapatın. Tür:

    **VSPerfCmd/Shutdown**

4. (İsteğe bağlı). Profil oluşturma ortam değişkenlerini temizleyin. Tür:

    **VSPerfCmd /globaloff**

5. Bilgisayarı yeniden başlatın.

## <a name="see-also"></a>Ayrıca bkz.
- [Profil ASP.NET web uygulamaları](../profiling/command-line-profiling-of-aspnet-web-applications.md)
- [İzleme metodu veri görünümleri](../profiling/instrumentation-method-data-views.md)