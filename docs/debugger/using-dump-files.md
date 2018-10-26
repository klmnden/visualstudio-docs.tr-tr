---
title: Döküm dosyalarını kullanma | Microsoft Docs
ms.custom: H1HackMay2017
ms.date: 03/08/2017
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.debug.crashdump
dev_langs:
- CSharp
- VB
- FSharp
- C++
- JScript
helpviewer_keywords:
- dumps, about dumps
- crash dumps
- dump files
- dumps
ms.assetid: b71be6dc-57e0-4730-99d2-b540a0863e49
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: c346c74b88f899101d30a0ecfb3a46544093a596
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49847872"
---
# <a name="use-dump-files-with-visual-studio"></a>Döküm dosyalarını Visual Studio ile kullanma
Yığınlar içeren veya içermeyen döküm dosyaları; bir döküm dosyası oluşturma bir döküm dosyasını açın; ikili dosyaları, pdb'ın ve bir döküm dosyası için kaynak dosyasını bulun.

##  <a name="BKMK_What_is_a_dump_file_"></a> Bir döküm dosyası nedir?
 A *döküm dosyasını* dökümün alındığı andaki bir uygulamanın anlık görüntüsüdür. Hangi işlemin yürütülmüş, hangi modüllerin de yüklenmiş olduğunu gösterir. Döküm, yığın bilgileriyle kaydedildiyse, döküm dosyası, zaman içinde o anda uygulamanın belleğinde olanların bir anlık görüntüsünü içerir. Döküm dosyasını Visual Studio'da bir yığın ile açmak, bir hata ayıklama oturumunda kesme noktasında durdurmak gibidir. Yürütme devam edemiyor olsanız da, döküm oluştuğu anda uygulamanın yığınlarını, iş parçacıklarını ve değişken değerlerini inceleyebilirsiniz.

 Dökümler öncelikle Geliştirici erişimi yok makinelerde oluşan sorunların hatalarını ayıklamak için kullanılır. Örneğin, müşterinin kilitlenmesini yeniden oluşturamadığınızda veya makineniz kesintiye bir müşterinin makinesinden döküm dosyasını kullanabilirsiniz. Daha fazla test için test makinesinin kullanılabilmesi amacıyla çökmeyi veya takılma verilerini kaydetmek üzere testçiler tarafından da dökümler oluşturulur. Visual Studio hata ayıklayıcı, yönetilen veya yerel kod için döküm dosyaları kaydedebilir. Hata ayıklayıcı, Visual Studio veya dosyaları kaydeden başka programlar tarafından oluşturulmuş döküm dosyalarını yükleyebilir *mini döküm* biçimi.

##  <a name="BKMK_Dump_files__with_or_without_heaps"></a> Yığınlar içeren veya içermeyen döküm dosyaları
 Yığın bilgileri içeren veya içermeyen döküm dosyaları oluşturabilirsiniz.

-   **Yığınlar içeren döküm dosyaları** uygulamanın bellek anlık görüntüsünü içerir. Bu döküm oluşturulduğundaki değişkenlerin değerlerini içerir. Yığınla kaydedilmiş bir döküm dosyası yüklerseniz, uygulama ikili dosyası bulunamasa bile Visual Studio sembolleri yükleyebilir. Visual Studio ayrıca döküm dosyasında yüklenen yerel modüllerin ikili dosyalarını kaydederek hata ayıklamayı daha da kolaylaştırır.

-   **Yığınlar içermeyen döküm dosyaları** yığın bilgileri içeren daha küçük olur. Ancak hata ayıklayıcısının sembol bilgilerini bulmak için uygulama ikili dosyalarını yüklemesi gerekir. İkili dosyalar, döküm oluşturulduğunda kullanılan ikili dosyalarla tam olarak eşleşen ikili dosyalar olmalıdır. Sadece yığın değişkenlerin değerleri öbek veri olmadan döküm dosyalarına kaydedilir.

##  <a name="BKMK_Requirements_and_limitations"></a> Gereksinimler ve sınırlamalar

-   En iyi duruma getirilmiş kodun döküm dosyalarının hatalarının ayıklanması kafa karıştırıcı olabilir. Örneğin, işlevlerin derleyici içerilmesi, beklenmeyen çağrı yığınlarıyla sonuçlanabilir ve diğer iyileştirmeler, değişkenlerin ömrünü değiştirebilir.

-   64 bit bilgisayarda çalışan bir Visual Studio örneğinde 64 bit makinelerdeki döküm dosyalarının hataları ayıklanmalıdır.

-   Visual Studio'nun VS 2013 öncesi sürümlerinde, 64 bit makinelerde çalıştırılan 32 bit uygulamaların bazı araçlar tarafından toplanan (Görev Yöneticisi ve 64-bit WinDbg) dökümleri Visual Studio'da açılamadı. Bu sınırlama, VS 2013 sürümünde kaldırılmıştır.

-   Visual Studio, ARM cihazlarından yerel uygulamaların döküm dosyalarının hatalarını ayıklayabilir. Visual Studio, ARM cihazlarındaki yönetilen uygulamaların uygulama döküm dosyalarının da hatalarını ayıklayabilir, ancak bunu yalnızca yerel hata ayıklayıcıda yapabilir.

-   Hata ayıklamak için [çekirdek modu](/windows-hardware/drivers/debugger/kernel-mode-dump-files) düküm dosyalarında, parçası olan Windows için hata ayıklama araçlarını indirin [Windows Sürücü Seti'nin (WDK)](/windows-hardware/drivers/download-the-wdk).

-   Visual Studio olarak bilinen eski döküm biçiminde kaydedilen döküm dosyalarının hatalarını ayıklayamaz bir [tam kullanıcı modu dökümü](http://msdn.microsoft.com/library/windows/hardware/ff545506.aspx). Tam kullanıcı modu dökümünün yığını olan bir dökümle aynı olmadığına dikkat edin.

-   İle hata ayıklamak için [SOS.dll (SOS Debugging Extension)](/dotnet/framework/tools/sos-dll-sos-debugging-extension) Visual Studio'da parçası olan Windows için hata ayıklama araçlarını yüklemeniz gerekir [Windows Sürücü Seti'nin (WDK)](/windows-hardware/drivers/download-the-wdk)

##  <a name="BKMK_Create_a_dump_file"></a> Bir döküm dosyası oluşturma
 Visual Studio ile bir döküm dosyası oluşturmak için:

- Visual Studio'daki bir işlemde hata ayıklarken, hata ayıklayıcı kesme noktası veya bir özel durumda durduğunda döküm dosyasını kaydedebilirsiniz. Seçin **hata ayıklama**, ardından **dökümü Farklı Kaydet**, ardından **hata ayıklama**. İçinde **dökümü Farklı Kaydet** iletişim kutusundaki **farklı kaydetme türü** seçebileceğiniz listesinde **mini döküm** veya **yığınlı** (varsayılan).

- İle [tam zamanında hata ayıklama](../debugger/just-in-time-debugging-in-visual-studio.md) etkinleştirildiğinde, hata ayıklayıcının hata ayıklayıcısı dışında çalışan çöken bir işleme ve sonra döküm dosyasını kaydedebilirsiniz. Bkz: [çalıştırma işlemleri iliştirme](../debugger/attach-to-running-processes-with-the-visual-studio-debugger.md)

  Windows mini döküm biçimini destekleyen herhangi bir programla da döküm dosyaları oluşturabilirsiniz. Örneğin, **Procdump** komut satırı yardımcı programı [Windows SysInternals](http://technet.microsoft.com/sysinternals/default) Tetikleyiciler veya isteğe bağlı göre işlem kilitlenme döküm dosyaları oluşturabilirsiniz. Bkz: [gereksinimleri ve sınırlamaları](../debugger/using-dump-files.md#BKMK_Requirements_and_limitations) döküm dosyalarını oluşturmak için diğer araçları kullanma hakkında ek bilgi için bu konuda.

##  <a name="BKMK_Open_a_dump_file"></a> Bir döküm dosyası Aç

1.  Visual Studio'da **dosya**, **açık**, **dosya**.

2.  İçinde **açık dosya** iletişim kutusunda, döküm dosyasını bulup seçin. Çoğunlukla .dmp uzantısına sahip olacaktır. Ardından **Tamam**.

3.  **Döküm dosyası özeti** penceresi görüntülenir. Bu pencerede, döküm dosyasının hata ayıklama özet bilgilerini görüntüleyebilir, sembol yolunu ayarlayabilir, hata ayıklamayı başlatabilir ve özet bilgilerini panoya kopyalayabilirsiniz.

     ![Mini döküm Özet sayfası](../debugger/media/dbg_dump_summarypage.png "DBG_DUMP_SummaryPage")

4.  Hata ayıklamayı başlatmak için Git **eylemleri** bölüm ve seçmeniz **ile yalnızca yönetilen hata ayıklama**, **sadece Yerelle Hata Ayıkla** veya **karışıkolanlaHataAyıkla**.

##  <a name="BKMK_Find_binaries__symbol___pdb__files__and_source_files"></a> İkili dosyalar, sembol (.pdb) dosyalarını ve kaynak dosyaları bulma
 Bir döküm dosyasında hata ayıklamak üzere Visual Studio'nun tam özelliklerini kullanmak aşağıdakilere erişim gerekir:

- Dökümün alındığı .Exe dosyası ve döküm işleminde kullanılan diğer ikili dosyalar (DLL'ler vb.).

   Yığın veriler ile bir dökümün hatalarını ayıklıyorsanız, Visual Studio bazı modüller için eksik ikili dosyalarla başa çıkabilir, ancak geçerli çağrı yığınları oluşturmak için yeterli modüller için ikili dosyalara sahip olmalıdır. Visual Studio, yığın ile döküm dosyasında yerel modüller içerir.

- .exe ve diğer ikili dosyalar için sembol (.pdb) dosyaları.

- İlgilendiğiniz modüller için kaynak dosyaları.

   Yürütülebilir ve .pdb dosyaları, döküm oluşturulduğunda kullanılan dosyaların sürüm ve yapısıyla tam olarak eşleşmelidir.

   Kaynak dosyaları bulamazsanız modüllerin ayrıştırılmasını kullanarak ayıklayabilirsiniz,

  **Yürütülebilir dosyalar için varsayılan arama yolları**

  Visual Studio, döküm dosyasında bulunmayan yürütülebilir dosyalar için bu konumları otomatik olarak arar:

1. Döküm dosyasını içeren dizin.

2. Döküm dosyasında belirtilen modül yolu. Bu, makinede dökümün toplandığı modül yoludur.

3. Belirtilen sembol yollarını **hata ayıklama**, **seçenekleri**, **sembolleri** sayfa Visual Studio'nun **Araçları**, **seçenekleri**  iletişim kutusu. Bu sayfada arama yapmak için daha fazla konum ekleyebilirsiniz.

   **İkili yok kullanarak > Sembol > kaynak sayfaları**

   Visual Studio dökümdeki bir modülün hatalarını ayıklamak için gerekli dosyaları bulamazsa, uygun bir sayfayı gösterir (**hiçbir ikili bulunamadı**, **hiçbir sembol bulunamadı**, veya **hiçbir kaynak bulunamadı**). Bu sayfalar, sorunun nedeni hakkında ayrıntılı bilgi sağlar ve dosyaların doğru konumunu belirlememenize yardımcı olabilecek eylem bağlantıları sağlar. Bkz: [sembol (.pdb) belirtin ve kaynak dosyaları](../debugger/specify-symbol-dot-pdb-and-source-files-in-the-visual-studio-debugger.md).

## <a name="see-also"></a>Ayrıca bkz.

- [Tam Zamanında Hata Ayıklama](../debugger/just-in-time-debugging-in-visual-studio.md)
- [Simge (.pdb) ve Kaynak Dosyaları Belirtme](../debugger/specify-symbol-dot-pdb-and-source-files-in-the-visual-studio-debugger.md)
- [IntelliTrace](../debugger/intellitrace.md)