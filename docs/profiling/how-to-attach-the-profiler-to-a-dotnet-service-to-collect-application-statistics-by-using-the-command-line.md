---
title: Uygulama istatistikleri toplamak için .NET hizmetine profil oluşturucu ekleme
ms.custom: seodec18
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: a0046c47-26c8-4bec-96a0-81da05e5104a
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- dotnet
ms.openlocfilehash: 32aa82654d55496c3d407f59712a8b7adba56b9a
ms.sourcegitcommit: 117ece52507e86c957a5fd4f28d48a0057e1f581
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/28/2019
ms.locfileid: "66261557"
---
# <a name="how-to-attach-the-profiler-to-a-net-service-to-collect-application-statistics-by-using-the-command-line"></a>Nasıl yapılır: Komut satırını kullanarak uygulama istatistikleri toplamak için bir .NET hizmetine profil oluşturucu ekleme
Bu makalede nasıl kullanılacağını [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] Profil Araçları komut satırı araçlarının profil oluşturucuyu bir .NET Framework eklemek, hizmet ve örnekleme yöntemini kullanarak performans istatistikleri toplama.

> [!NOTE]
> Windows 8 ve Windows Server 2012'deki Gelişmiş güvenlik özellikleri Visual Studio profil oluşturucu bu platformlarda veri toplayan bir şekilde önemli değişiklikler gerekmiştir. UWP uygulamaları, ayrıca yeni toplama teknikleri gerektirir. Bkz: [Windows 8 ve Windows Server 2012 uygulamalarında performans araçları](../profiling/performance-tools-on-windows-8-and-windows-server-2012-applications.md).
>
> Profil oluşturma araçları için olan yolu almak için bkz: [komut satırı araçları yolunu belirtin](../profiling/specifying-the-path-to-profiling-tools-command-line-tools.md). 64-bit bilgisayarlarda araçların 64-bit hem 32-bit sürümleri kullanılabilir. Profil oluşturucu komut satırı araçlarını kullanmak için Araçlar yolunu komut istemi penceresinin PATH ortam değişkenine ekleyin veya komutun kendisine eklemeniz gerekir.
>
> Bir profil oluşturma yürütmesine katman etkileşim verileri ekleme, komut satırı profil araçlarıyla özel yordamlar gerektirir. Bkz: [katman etkileşim verileri toplama](../profiling/adding-tier-interaction-data-from-the-command-line.md).

 .NET Framework hizmetinden performans verilerini toplamak için kullanmanız gerekir [VSPerfCLREnv.cmd](../profiling/vsperfclrenv.md) uygun ortam değişkenlerini başlatmak üzere. Sonra hizmeti barındıran bilgisayarı yeniden başlatın ve profil oluşturma için o bilgisayarın yapılandırmanız gerekir. Daha sonra profil oluşturucuyu hizmet işlemine iliştirin. Hizmete profil oluşturucu eklendiğinde, duraklatma ve veri koleksiyonu devam ettirin.

 Profil oluşturma oturumunu sonlandırmak için, profil oluşturucunun hizmetten ayrılması ve ve açıkça kapatılması gerekir. Çoğu durumda, bir oturumun sonunda profil oluşturma ortam değişkenlerini temizlemenizi öneririz.

## <a name="attach-the-profiler"></a>Profil Oluşturucu ekleme

#### <a name="to-attach-the-profiler-to-a-net-framework-service"></a>Profil oluşturucuyu bir .NET Framework servisine eklemek

1. Hizmetini yükleyin.

2. Bir komut istemi penceresi açın.

3. Profil oluşturma ortamı değişkenlerini başlatın. Tür:

    **VSPerfClrEnv /globalsampleon** [**/samplelineoff**]

   - **/globalsampleon** örnekleme sağlar.

   - **/samplelineoff** toplanan verilerin belirli kaynak kod satırlarına atamayı devre dışı bırakır. Bu seçenek belirtildiğinde, veriler yalnızca işlevlere atanır.

4. Bilgisayarı yeniden başlatın.

5. Bir komut istemi penceresi açın.

6. Profil oluşturucuyu başlatın. Tür:

    **VSPerfCmd**[/start](../profiling/start.md) **: örnek**[/output](../profiling/output.md) **:** `OutputFile` [`Options`]    

   - **/Start:sample** seçeneği profil oluşturucuyu başlatır.

   - **/Output:** `OutputFile` ile seçeneği gereklidir **/start**. `OutputFile` Profil oluşturma veri (.vsp) dosyasının konumunu ve adını belirtir.

     Aşağıdaki seçeneklerle dilediğinizi kullanabilirsiniz **/start:sample** seçeneği.

   > [!NOTE]
   > **/User** ve **/crosssession** seçenekleri genellikle hizmetler için gereklidir.

   | Seçenek | Açıklama |
   | - | - |
   | [/ User](../profiling/user-vsperfcmd.md) **:**[`Domain`**\\**]`UserName` | Profilli işlemin sahibi olan hesabının etki alanı ve kullanıcı adını belirtir. Bu seçenek, yalnızca oturum açan kullanıcının farklı bir kullanıcı olarak işlem çalışıyorsa gereklidir. İşlem sahibi, Windows Görev Yöneticisi'nin İşlemler sekmesinde kullanıcı adı sütununda listelenir. |
   | [/ crosssession](../profiling/crosssession.md) | Etkinleştirir, diğer oturumlarda işlemleri profil oluşturma. Bu seçenek, başka bir oturumda hizmet çalışıyorsa gereklidir. Oturum kimliği, Windows Görev Yöneticisi'nin İşlemler sekmesinde oturum kimliği sütununda listelenir. **/CS** için bir kısaltma olarak belirtilebilir **/crosssession**. |
   | [/wincounter](../profiling/wincounter.md) **:** `WinCounterPath` | Profil oluşturma sırasında Tahsil edilecek Windows performans sayacı belirtir. |
   | [/automark](../profiling/automark.md) **:** `Interval` | İle kullanma **/wincounter** yalnızca. Windows performans sayacı toplama olayları arasındaki milisaniye sayısını belirtir. 500 ms varsayılandır. |
   | [/Events](../profiling/events-vsperfcmd.md) **:** `Config` | Profil oluşturma sırasında Tahsil edilecek bir olay izleme için Windows (ETW) olayı belirtir. ETW olayları ayrı (.etl) dosyasında toplanır. |

7. Gerekirse, hizmeti başlatın.

8. Hizmete profil oluşturucu iliştirin. Tür:

    **VSPerfCmd**[/ ekleme](../profiling/attach.md) **:** {`PID`&#124;`ProcName`} [`Sample Event`] [[/targetclr](../profiling/targetclr.md)**:**`Version`]  

   - İşlem kimliği belirtin (`PID`) veya hizmetin işlem adı (ProcName). Windows Görev Yöneticisi'nde, işlem kimliklerini ve isimlerini çalışan tüm işlemlerin görüntüleyebilirsiniz.

     Varsayılan olarak, performans verisi her 10.000.000 durdurulmamış işlemci saat örneklenen döngüsü. Saniyede bir adet 1GH işlemcide yaklaşık 100 örnek budur. Saat döngüsü aralığı değiştirmek veya farklı örnekleme olayı belirtmek için aşağıdaki seçeneklerden birini belirtebilirsiniz.

   |Örnek olay|Açıklama|
   |------------------|-----------------|
   |[/ Timer](../profiling/timer.md) **:** `Interval`|Örnekleme aralığı tarafından belirtilen durdurulmamış saati döngüleri sayısını değiştirir `Interval`.|
   |[/PF](../profiling/pf.md)[**:**`Interval`]|Örnekleme olay sayfa hataları değiştirir. Varsa `Interval` belirtilmemişse, örnekler arasında sayfa hatalarının sayısını ayarlar. Varsayılan 10'dur.|
   |[/ sys](../profiling/sys-vsperfcmd.md)[`:``Interval`]|Örnekleme olayını, işletim sisteminin çekirdeğine (syscalls) işlemden sisteme çağrı yapmak değiştirir. Varsa `Interval` belirtilmemişse, örnekler arasındaki çağrıların sayısını ayarlar. Varsayılan 10'dur.|
   |[/ Sayaç](../profiling/counter.md) **:** `Config`|İşlemci performans sayacı ve belirtilen aralık için örnekleme olay ve aralığını değiştirir `Config`.|

   - **targetclr:** `Version` bir uygulamada birden fazla çalışma zamanı sürümü yüklendiğinde profiline ortak dil çalışma zamanı (CLR) sürümünü belirtir. İsteğe bağlı.

## <a name="control-data-collection"></a>Veri toplamayı denetleme
 Hizmet çalışırken kullanabileceğiniz *VSPerfCmd.exe* Profil Oluşturucu veri dosyasına verilerin yazılmasını başlatıp için Seçenekler. Veri toplama denetimi uygulamayı kapatma veya başlatma gibi program yürütmenin özel bir bölümü için veri toplamanızı sağlar.

#### <a name="to-start-and-stop-data-collection"></a>Veri toplamayı durdurmak ve başlatmak

- Aşağıdaki çiftleri **VSPerfCmd** seçenekleri başlatın ve veri toplamayı durdurun. Her seçeneği ayrı bir komut satırında belirtin. Veri Toplama'ı, birden çok kez açıp kapatabilirsiniz.

    |Seçenek|Açıklama|
    |------------|-----------------|
    |[/ globalon /globaloff](../profiling/globalon-and-globaloff.md)|Başlar (**/globalon**) veya durdurur (**/globaloff**) tüm işlemler için veri toplama.|
    |[/processon](../profiling/processon-and-processoff.md) **:** `PID` [/processoff](../profiling/processon-and-processoff.md) **:** `PID`|Başlar (**/processon**) veya durdurur (**/processoff**) işlem kimliği tarafından belirtilen işlem için veri toplama (`PID`).|
    |**/ ekleme:**{`PID`&#124;`ProcName`} [/ detach](../profiling/detach.md)[: {`PID`&#124;`ProcName`}]|**/ ekleme** işlem kimliği veya işlem adı tarafından belirtilen işlem için veri toplamaya başlar. **/ detach** belirli bir işlem belirtilmezse, belirtilen işlem için veya tüm işlemler için veri toplamayı durdurur.|

## <a name="end-the-profiling-session"></a>Profil oluşturma oturumunu sona erdirme
 Profil oluşturma oturumunu sona erdirmek için profil oluşturucu oluşturulmuş tüm işlemlerden ayrılması ve profil oluşturucu açıkça kapatılmalıdır. Bunu ayırabilirsiniz uygulamayı kapatarak veya çağırarak örnekleme yöntemiyle profili oluşturulmuş bir uygulamadan **VSPerfCmd / detach** seçeneği. Ardından çağırın **VSPerfCmd/shutdown** profil oluşturucuyu kapatmak ve profil oluşturma veri dosyasını kapatırsınız.

 **VSPerfClrEnv /globaloff** komutu profil oluşturma ortam değişkenlerini temizler, ancak bilgisayar yeniden başlatılana kadar sistem yapılandırması sıfırlanmaz.

#### <a name="to-end-a-profiling-session"></a>Profil oluşturma oturumunu sona erdirmek için

1. Hedef uygulamadaki profil oluşturucuyu ayırmak için aşağıdakilerden birini yapın:

    - Hizmeti durdurun.

         veya

    - Tür **VSPerfCmd / detach**

2. Profil oluşturucuyu kapatın. Tür:

     **VSPerfCmd/Shutdown**

3. (İsteğe bağlı) Profil oluşturma ortam değişkenlerini temizleyin. Tür:

     **VSPerfClrEnv /globaloff**

4. Bilgisayarı yeniden başlatın.

## <a name="see-also"></a>Ayrıca bkz.
- [Profil hizmetler](../profiling/command-line-profiling-of-services.md)
- [Örnekleme yöntemi veri görünümleri](../profiling/profiler-sampling-method-data-views.md)