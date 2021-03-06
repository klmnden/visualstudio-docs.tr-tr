---
title: 'Profiler komut satırı: .NET hizmetini izleme, zamanlama ayrıntı Al'
ms.date: 11/04/2016
ms.topic: conceptual
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- dotnet
ms.openlocfilehash: 4f3e03a35719e6dd1cbfa7514a304539dc4f0ca1
ms.sourcegitcommit: 91c7f1b525e0c22d938bc4080ba4ceac2483474f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/12/2019
ms.locfileid: "67032053"
---
# <a name="how-to-instrument-a-net-service-and-collect-detailed-timing-data-by-using-the-profiler-command-line"></a>Nasıl yapılır: Profil oluşturucu komut satırını kullanarak bir .NET hizmetini izleme ve ayrıntılı zamanlama verileri toplama

Bu makalede, bir .NET Framework hizmetini izleme ve ayrıntılı zamanlama verileri toplamak için Visual Studio Profil Araçları komut satırı araçlarını kullanmayı açıklar.

> [!NOTE]
> Bilgisayar başlatıldıktan sonra hizmeti yeniden başlatılamıyor ise izleme yöntemi ile bir hizmetin profilini oluşturamazsınız, böyle bir hizmet, yalnızca işletim sistemi başlatıldığında başlar.
>
> Profil oluşturma araçları için olan yolu almak için bkz: [komut satırı araçları yolunu belirtin](../profiling/specifying-the-path-to-profiling-tools-command-line-tools.md). 64-bit bilgisayarlarda araçların 64-bit hem 32-bit sürümleri kullanılabilir. Profil oluşturucu komut satırı araçlarını kullanmak için Araçlar yolunu komut istemi penceresinin PATH ortam değişkenine ekleyin veya komutun kendisine eklemeniz gerekir.
>
> Bir profil oluşturma yürütmesine katman etkileşim verileri ekleme, komut satırı profil oluşturma araçları ile özel yordamlar gerektirir. Bkz: [katman etkileşim verileri toplama](../profiling/adding-tier-interaction-data-from-the-command-line.md).

Araçlar yöntemini kullanarak bir .NET Framework hizmetinden ayrıntılı zamanlama verileri toplamak için kullandığınız [VSInstr.exe](../profiling/vsinstr.md) aracını bileşenin belgelenmiş bir sürümünü oluşturmak için. Hizmet eklenmemiş sürümünü izleme eklenmiş sürümüyle hizmeti el ile başlatmak için yapılandırıldığından emin emin değiştirmeniz. Kullandığınız [VSPerfCLREnv.cmd](../profiling/vsperfclrenv.md) aracı genel profil oluşturma ortamı değişkenlerini başlatmak ve ana bilgisayarı yeniden başlatın. Ardından profil oluşturucuyu başlatın.

Hizmet başlatıldığında, zamanlama verileri bir veri dosyasına otomatik olarak toplanır. Duraklatma ve profil oluşturma oturumu sırasında veri koleksiyonu devam ettirin.

Profil oluşturma oturumunu sona erdirmek için hizmeti kapatmak ve profil oluşturucuyu açıkça kapatın. Çoğu durumda, bir oturumun sonunda profil oluşturma ortam değişkenlerini temizlemenizi öneririz.

## <a name="start-the-application-with-the-profiler"></a>Uygulamayı Profil Oluşturucu ile başlatma

1. Bir komut istemi penceresi açın.

2. Kullanım **Vsınstr** aracını hizmet ikililerinin belgelenmiş bir sürümünü oluşturmak için.

3. Özgün ikiliyi belgelenmiş sürüm ile değiştirin. Windows hizmeti Denetim Yöneticisi'nde hizmet başlangıç türü el ile olarak ayarlanmış olduğundan emin olun.

4. .NET Framework'te profil oluşturma ortamı değişkenlerini başlatın. Tür:

     **VSPerfClrEnv /globaltraceon**

5. Bilgisayarı yeniden başlatın.

6. Bir komut istemi penceresi açın.

7. Profil oluşturucuyu başlatın. Tür:

     **VSPerfCmd çalıştığından/Output:** `OutputFile` [`Options`]

   - [/Start](../profiling/start.md) **: izleme** seçeneği profil oluşturucuyu başlatır.

   - [/Output](../profiling/output.md) **:** `OutputFile` ile seçeneği gereklidir **/start**. `OutputFile` Profil oluşturma verilerinin konumunu ve adını belirtir (. *Vsp*) dosyası.

     Aşağıdaki seçenekler herhangi birini kullanabilirsiniz **çalıştığından** seçeneği.

     > [!NOTE]
     > **/User** ve **/crosssession** seçenekleri genellikle profil oluşturma hizmetleri için gereklidir.

     | Seçenek | Açıklama |
     | - | - |
     | [/ User](../profiling/user-vsperfcmd.md) **:** [`Domain` **\\** ]`UserName` | Profilli işlemin sahibi olan hesabının etki alanı ve kullanıcı adını belirtir. Bu seçenek, yalnızca oturum açan kullanıcının farklı bir kullanıcı olarak işlem çalışıyorsa gereklidir. İşlem sahibi listelenen **kullanıcı adı** sütunu **işlemleri** Windows Görev Yöneticisi'nin sekmesinde. |
     | [/ crosssession](../profiling/crosssession.md) | Etkinleştirir, diğer oturumlarda işlemleri profil oluşturma. Bu seçenek, başka bir oturumda uygulama çalışıyorsa gereklidir. Oturum kimliği listelendiğinden **oturum kimliği** sütunu **işlemleri** Windows Görev Yöneticisi'nin sekmesinde. **/CS** için bir kısaltma olarak belirtilebilir **/crosssession**. |
     | [/waitstart](../profiling/waitstart.md)[ **:** `Interval`] | Profil oluşturucunun hata vermeden önce başlatmak beklenecek saniye sayısını belirtir. Varsa `Interval` belirtilmezse, profil oluşturucu süresiz olarak bekler. Varsayılan olarak, **/start** hemen döndürür. |
     | [/globaloff](../profiling/globalon-and-globaloff.md) | Profil Oluşturucu veri toplamayı başlatmak için duraklatıldı, ekleme **/globaloff** seçeneğini **/start** komut satırı. Kullanım **/globalon** profil oluşturmayı devam ettirmek için. |
     | [/ Sayaç](../profiling/counter.md) **:** `Config` | Sayaç Config içerisinde belirtilen işlemci performans bilgileri toplar. Sayaç bilgileri, her profil oluşturma etkinliğinde toplanan verilere eklenir. |
     | [/wincounter](../profiling/wincounter.md) **:** `WinCounterPath` | Profil oluşturma sırasında Tahsil edilecek Windows performans sayacı belirtir. |
     | [/automark](../profiling/automark.md) **:** `Interval` | İle kullanma **/wincounter** yalnızca. Windows performans sayacı toplama olayları arasındaki milisaniye sayısını belirtir. 500 ms varsayılandır. |
     | [/Events](../profiling/events-vsperfcmd.md) **:** `Config` | Profil oluşturma sırasında Tahsil edilecek bir olay izleme için Windows (ETW) olayı belirtir. Ayrı bir toplanan ETW olayları (. *etl*) dosyası. |

8. Windows servis kontrol yöneticisinden hizmeti başlatın.

## <a name="control-data-collection"></a>Veri toplamayı denetleme

Hizmet çalışırken kullanabileceğiniz *VSPerfCmd.exe* Profil Oluşturucu veri dosyasına verilerin yazılmasını başlatıp için Seçenekler. Veri toplama denetlenmesi size program yürütmenin, hizmeti kapatılıyor veya başlatma gibi özel bir bölümü için veri toplamanızı sağlar.

- Aşağıdaki çiftleri **VSPerfCmd** seçenekleri başlatın ve veri toplamayı durdurun. Her seçeneği ayrı bir komut satırında belirtin. Veri Toplama'ı, birden çok kez açıp kapatabilirsiniz.

    |Seçenek|Açıklama|
    |------------|-----------------|
    |[/ globalon /globaloff](../profiling/globalon-and-globaloff.md)|Başlar ( **/globalon**) veya durdurur ( **/globaloff**) tüm işlemler için veri toplama.|
    |[/processon](../profiling/processon-and-processoff.md) **:** `PID` [/processoff](../profiling/processon-and-processoff.md) **:** `PID`|Başlar ( **/processon**) veya durdurur ( **/processoff**) işlem kimliği tarafından belirtilen işlem için veri toplama (`PID`).|
    |[/threadon](../profiling/threadon-and-threadoff.md) **:** `TID` [/threadoff](../profiling/threadon-and-threadoff.md) **:** `TID`|Başlar ( **/threadon**) veya durdurur ( **/threadoff**) veri toplama iş parçacığı kimliği tarafından belirtilen iş parçacığı için (`TID`).|

## <a name="end-the-profiling-session"></a>Profil oluşturma oturumunu sona erdirme

Profil oluşturma oturumunu sona erdirmek için Araçlı bileşeni çalıştıran hizmetini durdurun ve sonra çağrı **VSPerfCmd** [/shutdown](../profiling/shutdown.md) profil oluşturucuyu kapatmak ve profil oluşturma veri dosyasını kapatırsınız. **VSPerfClrEnv /globaloff** komutu profil oluşturma ortam değişkenlerini temizler.

Yeni ortam ayarlarının uygulanması için bilgisayarı yeniden başlatmanız gerekir.

1. Servis kontrol yöneticisinden hizmeti durdurun.

2. Profil oluşturucuyu kapatın. Tür:

     **VSPerfCmd/Shutdown**

3. Tüm profil oluşturma işlemini tamamladıktan sonra profil oluşturma ortam değişkenlerini temizleyin. Tür:

     **VSPerfClrEnv /globaloff**

4. Belgelenmiş modülü özgün hali ile değiştirin. Gerekirse, hizmetin başlangıç türünü yeniden yapılandırın.

5. Bilgisayarı yeniden başlatın.

## <a name="see-also"></a>Ayrıca bkz.

[Profil Hizmetleri](../profiling/command-line-profiling-of-services.md)
[izleme metodu veri görünümleri](../profiling/instrumentation-method-data-views.md)
