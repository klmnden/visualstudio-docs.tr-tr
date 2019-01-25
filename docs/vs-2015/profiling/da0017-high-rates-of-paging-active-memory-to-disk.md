---
title: 'DA0017: Yüksek oranda diske etkin bellek Sayfalaması Sayfalaması | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
f1_keywords:
- vs.performance.17
- vs.performance.rules.DA0017
- vs.performance.DA0017
ms.assetid: 01011eec-5930-43b3-980d-2cb01e2ca7f6
caps.latest.revision: 12
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 136a8489ed3eac621543cb40b004052c2c9d3324
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54803494"
---
# <a name="da0017-high-rates-of-paging-active-memory-to-disk"></a>DA0017: Yüksek oranda diske etkin bellek Sayfalaması Sayfalaması
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Kural Kimliği | DA0017 |  
| Kategori | Bellek ve disk belleği |  
| Profil oluşturma yöntemi | Tüm |  
| İleti | Bir yüksek oranda diske etkin bellek Sayfalaması gerçekleşiyor. Uygulamanız bellek-sınırlı olabilir. |  
| Kural türü | Bilgi |  
  
 Örnekleme, .NET bellek ve kaynak çekişmesi yöntemleri kullanılarak profili, bu kural tetiklemek için en az 10 örnekleri toplamanız gerekir.  
  
## <a name="cause"></a>Sebep  
 Profil oluşturma çalıştırmasını içinde toplanan sistem performans verileri, yüksek oranda bir disk gelen ve giden etkin bellek Sayfalaması profil oluşturma çalışması süresince oluştuğunu gösterir. Bu düzeyde sayfalama oranları, normalde uygulama performansını ve yanıt hızını etkiler. Algoritmalar düzeltilmesi tarafından bellek ayırmaları azaltmayı göz önünde bulundurun. Uygulamanızın bellek gereksinimlerini göz önünde bulundurun gerekebilir.  
  
## <a name="rule-description"></a>Kural Tanımı  
  
> [!NOTE]
>  Bilgilendirme bu kural active bellek disk belleği düzeyde önemli ölçüde ulaştığında tetiklenir. Disk belleği çok yüksek bir düzeyde oluştuğunda, uyarı kuralı [DA0014: Diske etkin bellek Sayfalaması son derece yüksek oranlı](../profiling/da0014-extremely-high-rates-of-paging-active-memory-to-disk.md) yerine tetikler.  
  
 Diske aşırı disk belleği yetersiz fiziksel bellek tarafından neden olabilir. Disk belleği dosyasının bulunduğu fiziksel disk kullanımını sayfalandırma işlemleri baskındır varsa, bunlar aynı disk için diğer uygulama odaklı disk işlemleri yavaşlatabilir.  
  
 Sayfaları genellikle diskten okunan veya toplu işlemleri içinde yazılan. Sayfa çıkış/sn sayısı genellikle büyük olan sayfa Yazma/sn, örneğin sayısından büyük. Sayfa çıktısı/sn sistem dosya önbelleği değiştirilen verileri sayfalarından da içerdiği için. Ancak, her zaman işlemi için disk belleği doğrudan sorumlu olduğunu belirlemek kolay değildir veya neden.  
  
## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?  
 Hata Listesi penceresindeki iletiyi gitmek için çift tıklatın [işaretleri](../profiling/marks-view.md) görünümü. Bulma **Bellek\Sayfa/sn** sütun. Varsa belirli program yürütme aşamaları sayfalama g/ç etkinliği diğerlerinden daha ağır olduğu belirleyin.  
  
 Bir yük testi senaryosunda bir ASP.NET uygulaması için profil verileri toplamayı ek fiziksel bellek (veya RAM) ile yapılandırılmış bir makine üzerinde yük testi tekrar çalıştırmayı deneyin.  
  
 Bellek ayırmaları algoritmaları düzeltme ve bellek kullanımı yoğun API'leri String.Concat ve String.Substring gibi önleme azaltmayı deneyin.
