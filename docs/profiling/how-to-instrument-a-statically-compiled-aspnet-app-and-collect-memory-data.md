---
title: 'Nasıl Yapılır: Aracı bir statik olarak derlenmiş ASP.NET Web uygulaması ve Profiler komut satırını kullanarak bellek verilerini toplamak | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: ea1dcb7c-1dc3-49ff-9418-8795b5b3d3bc
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: d37df1d22f42e3046960c81b1cd75d6c6ae0898f
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53850602"
---
# <a name="how-to-instrument-a-statically-compiled-aspnet-web-application-and-collect-memory-data-by-using-the-profiler-command-line"></a>Nasıl Yapılır: Gereç statik olarak derlenmiş bir ASP.NET web uygulamasını ve profil oluşturucu komut satırını kullanarak bellek verilerini toplamak
Bu makalede nasıl kullanılacağını [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] önceden derlenmiş bir araç haline getirmek için profil oluşturma araçları komut satırı araçlarının [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] web bileşeni veya web sitesi ve toplama .NET bellek ayırma, nesne ömrü ve ayrıntılı zamanlama verileri.  

> [!NOTE]
>  Profil oluşturma araçları için olan yolu almak için bkz: [komut satırı araçları yolunu belirtin](../profiling/specifying-the-path-to-profiling-tools-command-line-tools.md). 64-bit bilgisayarlarda araçların 64-bit hem 32-bit sürümleri kullanılabilir. Profil oluşturucu komut satırı araçlarını kullanmak için Araçlar yolunu komut istemi penceresinin PATH ortam değişkenine ekleyin veya komutun kendisine eklemeniz gerekir.

 Verileri toplamak için bir [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] izleme metodunu kullanarak Web bileşeni kullandığınız [VSInstr.exe](../profiling/vsinstr.md) aracını bileşenin belgelenmiş bir sürümünü oluşturmak için. Bileşeni barındıran bilgisayarda, bileşenin eklenmemiş sürümünü izleme eklenmiş sürümüyle değiştirin. Daha sonra [VSPerfCLREnv.cmd](../profiling/vsperfclrenv.md) aracı genel profil oluşturma ortamı değişkenlerini başlatmak ve ana bilgisayar yeniden başlatılır. Ardından profil oluşturucuyu başlatın.  

 Araçlı bileşen yürütüldüğünde, zamanlama verileri bir veri dosyasına otomatik olarak toplanır. Duraklatma ve profil oluşturma oturumu sırasında veri koleksiyonu devam ettirin.  

 Profil oluşturma oturumunu sona erdirmek için kapatma [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] çalışan işlemini bileşeni barındıran ve profil oluşturucuyu açıkça kapatın. Çoğu durumda, bir oturumun sonunda profil oluşturma ortam değişkenlerini temizlemenizi öneririz.  

## <a name="start-to-profile"></a>Profile Başlat  

#### <a name="to-instrument-an-aspnet-web-component-and-start-profiling"></a>Bir ASP.NET Web bileşenini izleme ve profil oluşturmayı başlatmak için  

1. Kullanım **Vsınstr** aracı hedef uygulamanın belgelenmiş bir sürümünü oluşturmak için. Gerekirse, ASP.NET ana bilgisayarda uygulama ikili dosyalarını Araçlı ikililerle değiştirin.  

2. Bir komut istemi penceresi açın  

3. .NET profil oluşturma ortamı değişkenlerini başlatın. Bir komut istemi penceresinde yazın:  

    **VSPerfClrEnv /globaltracegc**  

    -veya-  

    **VSPerfClrEnv /globaltracegclife**  

   -   **/globaltracegc** .NET bellek ayırma ve zamanlama verilerini toplar.  

   -   **/globaltracegclife** toplar .NET bellek ayırma, nesne ömrü ve ayrıntılı zamanlama verileri.  

4. Bilgisayarı yeniden başlatın.  

5. Bir komut istemi penceresi açın.  

6. Profil oluşturucuyu başlatın. Bir komut istemi penceresinde yazın:  

    **VSPerfCmd çalıştığından/Output:** `OutputFile` [`Options`]  

   - [/Start](../profiling/start.md)**: izleme** seçeneği profil oluşturucuyu başlatır.  

   - [/Output](../profiling/output.md)**:** `OutputFile` ile seçeneği gereklidir **/start**. `OutputFile` Profil oluşturma veri (.vsp) dosyasının konumunu ve adını belirtir.  

     Aşağıdaki seçeneklerle dilediğinizi kullanabilirsiniz **çalıştığından** seçeneği.  

   > [!NOTE]
   >  **/User** ve **/crosssession** seçenekleri genellikle ASP.NET uygulamaları için gereklidir.  

   | Seçenek | Açıklama |
   | - | - |
   | [/ User](../profiling/user-vsperfcmd.md) **:**[`Domain`**\\**]`UserName` | ASP.NET çalışan işlemine sahip hesabın kullanıcı adını ve isteğe bağlı etki alanını belirtir. Bu seçenek, oturum açan kullanıcının farklı bir kullanıcı olarak işlem çalışıyorsa gereklidir. Adı listelenir **kullanıcı adı** sütunu **işlemleri** Windows Görev Yöneticisi'nin sekmesinde. |
   | [/ crosssession](../profiling/crosssession.md) | Etkinleştirir, diğer oturumlarda işlemleri profil oluşturma. Bu seçenek, başka bir oturumda uygulama çalışıyorsa gereklidir. Oturum kimliği oturum kimliği sütununda listelenir **işlemleri** Windows Görev Yöneticisi'nin sekmesinde. **/CS** için bir kısaltma olarak belirtilebilir **/crosssession**. |
   | [/wincounter](../profiling/wincounter.md) **:** `WinCounterPath` | Profil oluşturma sırasında Tahsil edilecek Windows performans sayacı belirtir. |
   | [/automark](../profiling/automark.md) **:** `Interval` | İle kullanma **/wincounter** yalnızca. Windows performans sayacı toplama olayları arasındaki milisaniye sayısını belirtir. 500 ms varsayılandır. |
   | [/Events](../profiling/events-vsperfcmd.md) **:** `Config` | Profil oluşturma sırasında Tahsil edilecek bir olay izleme için Windows (ETW) olayı belirtir. ETW olayları ayrı (.etl) dosyasında toplanır. |
   | [/globaloff](../profiling/globalon-and-globaloff.md) | Profil Oluşturucu veri toplamayı başlatmak için duraklatıldı, ekleme **/globaloff** seçeneğini **/start** komut satırı. Kullanım **/globalon** profil oluşturmayı devam ettirmek için. |


7. İzleme eklenmiş bileşeni içeren web sitesini açın.  

## <a name="control-data-collection"></a>Veri toplamayı denetleme  
 Hedef uygulama çalışırken, kullanarak verinin yazılmasını durdurmayla ve veri toplamayı kontrol edebilirsiniz *VSPerfCmd.exe* seçenekleri. Veri toplama denetimi uygulamayı kapatma veya başlatma gibi program yürütmenin özel bir bölümü için veri toplamanızı sağlar.  

#### <a name="to-start-and-stop-data-collection"></a>Veri toplamayı durdurmak ve başlatmak  

-   Aşağıdaki seçenekleri çiftlerini başlatın ve veri toplama işlemini durdurun. Her seçeneği ayrı bir komut satırında belirtin. Veri Toplama'ı, birden çok kez açıp kapatabilirsiniz.  

    |Seçenek|Açıklama|  
    |------------|-----------------|  
    |[/ globalon /globaloff](../profiling/globalon-and-globaloff.md)|Başlar (**/globalon**) veya durdurur (**/globaloff**) tüm işlemler için veri toplama.|  
    |[/processon](../profiling/processon-and-processoff.md) **:** `PID` [/processoff](../profiling/processon-and-processoff.md) **:** `PID`|Başlar (**/processon**) veya durdurur (**/processoff**) işlem kimliği tarafından belirtilen işlem için veri toplama (`PID`).|  
    |[/threadon](../profiling/threadon-and-threadoff.md) **:** `TID` [/threadoff](../profiling/threadon-and-threadoff.md) **:** `TID`|Başlar (**/threadon**) veya durdurur (**/threadoff**) veri toplama iş parçacığı kimliği tarafından belirtilen iş parçacığı için (`TID`).|  

## <a name="end-the-profiling-session"></a>Profil oluşturma oturumunu sona erdirme  
 Profil oluşturma oturumunu sona erdirmek için kapatma [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] web uygulamasını ve ardından Internet Information Services (IIS) **IISReset** kapatmak için komut [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] çalışan işlemi. Çağrı **VSPerfCmd** [/shutdown](../profiling/shutdown.md) profil oluşturucuyu kapatmak ve profil oluşturma veri dosyasını kapatırsınız. **VSPerfClrEnv /globaloff** komutu profil oluşturma ortam değişkenlerini temizler. Yeni ortam ayarlarının uygulanması için bilgisayarı yeniden başlatmanız gerekir.  

#### <a name="to-end-a-profiling-session"></a>Profil oluşturma oturumunu sona erdirmek için  

1. Kapat [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] web uygulaması.  

2. Kapat [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] çalışan işlemi. Tür:  

    **IISReset/stop**  

3. Profil oluşturucuyu kapatın. Tür:  

    **VSPerfCmd/Shutdown**  

4. (İsteğe bağlı). Profil oluşturma ortam değişkenlerini temizleyin. Tür:  

    **VSPerfCmd /globaloff**  

5. Bilgisayarı yeniden başlatın. Gerekirse, IIS'yi yeniden başlatın. Tür:  

    **IISReset/Start**  

## <a name="see-also"></a>Ayrıca bkz.  
 [Profil ASP.NET web uygulamaları](../profiling/command-line-profiling-of-aspnet-web-applications.md)   
 [.NET bellek verisi görünümleri](../profiling/dotnet-memory-data-views.md)