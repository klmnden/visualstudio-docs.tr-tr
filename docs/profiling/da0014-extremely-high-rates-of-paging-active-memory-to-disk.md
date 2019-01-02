---
title: 'DA0014: Diske etkin bellek Sayfalaması son derece yüksek oranlı | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.performance.rules.DAMemoryBound
- vs.performance.DA0014
- vs.performance.14
- vs.performance.rules.DA0014
ms.assetid: a7fa3749-9191-437a-9331-9d917181e62f
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 67882c56492f8b98daf6f2f1cca1972be8e4f667
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53932713"
---
# <a name="da0014-extremely-high-rates-of-paging-active-memory-to-disk"></a>DA0014: Diske etkin bellek Sayfalaması son derece yüksek oranları

|||  
|-|-|  
|Kural Kimliği|DA0014|  
|Kategori|Bellek ve disk belleği|  
|Profil oluşturma yöntemi|Tümü|  
|İleti|Yüksek oranda diske etkin bellek Sayfalaması gerçekleşiyor. Uygulamanız bellek-sınırlı olabilir.|  
|Kural türü|Uyarı|  

 Örnekleme, .NET bellek ve kaynak çekişmesi yöntemleri kullanılarak profili, bu kural tetiklemek için en az 25 örnekleri toplamanız gerekir.  

## <a name="cause"></a>Sebep  
 Profil oluşturma çalıştırmasını içinde toplanan sistem performans verileri, yüksek oranda diske gelen ve giden etkin bellek Sayfalaması profil oluşturma çalışması süresince oluştuğunu gösterir. Bu düzeyde ücretleri genellikle disk belleği, uygulama performansını ve yanıt hızını etkiler. Algoritmalar düzeltilmesi tarafından bellek ayırmaları azaltmayı göz önünde bulundurun. Uygulamanızın bellek gereksinimlerini göz önünde bulundurun gerekebilir. Daha fazla belleğe sahip bir bilgisayarda yeniden profil oluşturma çalışıyor.  

## <a name="rule-description"></a>Kural açıklaması  
 Diske aşırı disk belleği yetersiz fiziksel bellek tarafından neden olabilir. Disk belleği dosyasının bulunduğu fiziksel disk kullanımını sayfalandırma işlemleri baskındır varsa, bunlar aynı disk için diğer uygulama odaklı disk işlemleri yavaşlatabilir.  

 Genellikle, sayfalar diskten okunan veya toplu işlemleri içinde yazılan. Sayfa çıkış/sn örneğin sık çok sayfa Yazma/sn, sayıdan büyüktür. Sayfa çıktısı/sn sistem dosya önbelleği değiştirilen verileri sayfalarından da içerdiği için. Ancak, her zaman işlemi için disk belleği doğrudan sorumlu olduğunu belirlemek kolay değildir veya neden.  

> [!NOTE]
>  Bu kural active bellek düzeyi yüksek bir hızda ulaştığında tetikler. Disk belleği düzeyini önemli, ancak değil aşırı olduğunda, bilgilendirici kural [DA0017: Yüksek oranda diske etkin bellek Sayfalaması Sayfalaması](../profiling/da0017-high-rates-of-paging-active-memory-to-disk.md) yerine tetikler.  

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?  
 Hata Listesi penceresindeki iletiyi gitmek için çift tıklatın [işaretleri](../profiling/marks-view.md) görünümü. Bulma **Bellek\Sayfa/sn** sütun. Varsa belirli program yürütme aşamaları sayfalama g/ç etkinliği diğerlerinden daha ağır olduğu belirleyin.  

 Bir yük testi senaryosunda bir ASP.NET uygulaması için profil verileri toplamayı ek fiziksel bellek (veya RAM) ile yapılandırılmış bir makine üzerinde yük testi tekrar çalıştırmayı deneyin.  

 Bellek ayırmaları algoritmaları düzeltme ve bellek kullanımı yoğun API'leri String.Concat ve String.Substring gibi önleme azaltmayı deneyin.