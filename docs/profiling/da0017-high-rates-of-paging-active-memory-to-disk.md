---
title: 'DA0017: Yüksek oranda diske etkin bellek Sayfalaması Sayfalaması | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.performance.17
- vs.performance.rules.DA0017
- vs.performance.DA0017
ms.assetid: 01011eec-5930-43b3-980d-2cb01e2ca7f6
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 5499ff9451d3068cdef0e32dee45a6f6c7f63c71
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63425490"
---
# <a name="da0017-high-rates-of-paging-active-memory-to-disk"></a>DA0017: Yüksek oranda diske etkin bellek sayfalaması

|||
|-|-|
|Kural Kimliği|DA0017|
|Kategori|Bellek ve disk belleği|
|Profil oluşturma yöntemi|Tümü|
|İleti|Bir yüksek oranda diske etkin bellek Sayfalaması gerçekleşiyor. Uygulamanız bellek-sınırlı olabilir.|
|Kural türü|Bilgiler|

 Örnekleme, .NET bellek ve kaynak çekişmesi yöntemleri kullanılarak profili, bu kural tetiklemek için en az 10 örnekleri toplamanız gerekir.

## <a name="cause"></a>Sebep
 Profil oluşturma çalıştırmasını içinde toplanan sistem performans verileri, yüksek oranda bir disk gelen ve giden etkin bellek Sayfalaması profil oluşturma çalışması süresince oluştuğunu gösterir. Bu düzeyde sayfalama oranları, normalde uygulama performansını ve yanıt hızını etkiler. Algoritmalar düzeltilmesi tarafından bellek ayırmaları azaltmayı göz önünde bulundurun. Uygulamanızın bellek gereksinimlerini göz önünde bulundurun gerekebilir.

## <a name="rule-description"></a>Kural açıklaması

> [!NOTE]
> Bilgilendirme bu kural active bellek disk belleği düzeyde önemli ölçüde ulaştığında tetiklenir. Disk belleği çok yüksek bir düzeyde oluştuğunda, uyarı kuralı [DA0014: Diske etkin bellek Sayfalaması son derece yüksek oranlı](../profiling/da0014-extremely-high-rates-of-paging-active-memory-to-disk.md) yerine tetikler.

 Diske aşırı disk belleği yetersiz fiziksel bellek tarafından neden olabilir. Disk belleği dosyasının bulunduğu fiziksel disk kullanımını sayfalandırma işlemleri baskındır varsa, bunlar aynı disk için diğer uygulama odaklı disk işlemleri yavaşlatabilir.

 Sayfaları genellikle diskten okunan veya toplu işlemleri içinde yazılan. Sayfa çıkış/sn sayısı genellikle büyük olan sayfa Yazma/sn, örneğin sayısından büyük. Sayfa çıktısı/sn sistem dosya önbelleği değiştirilen verileri sayfalarından da içerdiği için. Ancak, her zaman işlemi için disk belleği doğrudan sorumlu olduğunu belirlemek kolay değildir veya neden.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Hata Listesi penceresindeki iletiyi gitmek için çift tıklatın [işaretleri](../profiling/marks-view.md) görünümü. Bulma **Bellek\Sayfa/sn** sütun. Varsa belirli program yürütme aşamaları sayfalama g/ç etkinliği diğerlerinden daha ağır olduğu belirleyin.

 Bir yük testi senaryosunda bir ASP.NET uygulaması için profil verileri toplamayı ek fiziksel bellek (veya RAM) ile yapılandırılmış bir makine üzerinde yük testi tekrar çalıştırmayı deneyin.

 Bellek ayırmaları algoritmaları düzeltme ve bellek kullanımı yoğun API'leri String.Concat ve String.Substring gibi önleme azaltmayı deneyin.