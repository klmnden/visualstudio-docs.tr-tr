---
title: Komut satırından Profiler raporları oluşturma | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: c886f8af-2014-4fec-9b24-d98b68ecafb7
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: e6a6d31d15f7f7ed533d73683a3c12d152bd7046
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62552908"
---
# <a name="create-profiler-reports-from-the-command-line"></a>Komut satırından profil oluşturucu raporlar oluşturma
**VSPerfReport** komut satırı aracı oluşturmanıza olanak sağlar. *XML* veya virgülle ayrılmış değer (. *CSV*) profil oluşturma verilerini gelen raporlar (. *Vsp*) dosyaları. VSPerfReport rapor türleri arabirimi tablo tabanlı görünümlerini karşılayabilmesi [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)]. Rapor yalnızca sizin kodunuzu gösterir ve profil oluşturma veri dosyasını yalnızca bir segmentini gösterecek şekilde filtreleyebilirsiniz. Daha fazla bilgi için [VSPerfReport](../profiling/vsperfreport.md).

 Ayrıca, profil oluşturma veri dosyaları sembolleri ekleyerek paylaşmak kolay yapabilirsiniz. *vsp* dosyaları ve kriterlere göre önceden analiz edilmiş raporu (. *vsps*) dosyaları daha küçük ve daha hızlı açın.

## <a name="common-tasks"></a>Ortak görevler

|Görev|İlgili içerik|
|----------|---------------------|
|**Temel bir rapor oluşturun.** Tüm oluşturur veya bir alt kümesini VSPerfReport rapor türleri.|-   [Temel raporlar oluşturma](../profiling/creating-basic-profiling-reports-from-the-command-line.md)|
|**İki profil oluşturma veri dosyaları karşılaştırın.** İki profil oluşturma veri dosyaları performans verilerini karşılaştıran bir "fark" raporu oluşturun.|-   [Nasıl Yapılır: Bir komut isteminden profil oluşturucu Karşılaştırma raporu oluşturma](../profiling/how-to-create-a-profiler-comparison-report-from-a-command-prompt.md)|
|**Görünüm çağrı izleme ve olay izleme için Windows (ETW) verileri.** Uygulamanızın işlevlerine her giriş ve çıkış noktası ve işlevinizden diğer işlevlere her çağrı için zamanlama bilgileri listeleyen bir çağrı izleme raporu oluşturun. Veya profil oluşturma yürütmesine toplanmış olan tüm ETW olayları ayrıntılı bir listesi oluşturun.|-   [Nasıl Yapılır: Çağrı izleme raporu oluşturma](../profiling/how-to-create-a-profiling-tools-call-trace-report.md)|
|**Bir raporu filtreleyebilirsiniz.** Bir raporu yalnızca kodunuzu işlevler veya belirli bir zaman profil oluşturma veri dosyasını içinde sınırlar.|-   [Nasıl Yapılır: Komut satırından raporları filtreleme](../profiling/how-to-filter-reports-from-the-command-line.md)|
|**Taşınabilir profil oluşturma veri dosyaları oluşturun.** Profil oluşturma verilerini daha kolay paylaşım yapmak için bir oturum profil oluşturma için semboller gömebilirsiniz. *vsp* dosya. Önceden çözümlenmiş bir profil oluşturma verilerini de oluşturabilirsiniz (. *vsps*) daha küçük ve daha hızlı açmak dosya.|-   [Taşınabilir profil oluşturma veri dosyaları oluşturma](../profiling/creating-portable-profiling-data-files-from-the-command-line.md)|