---
title: 'DA0024: Aşırı GC CPU süresi | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
f1_keywords:
- vs.performance.DA0024
- vs.performance.24
- vs.performance.rules.DA0024
ms.assetid: 228872da-77d0-4da5-b455-ac57fb1867c9
caps.latest.revision: 15
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: d40377c28e0987ac902ab8aa5cf778715eb899cd
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63435846"
---
# <a name="da0024-excessive-gc-cpu-time"></a>DA0024: Aşırı GC CPU Süresi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Kural Kimliği | DA0024 |  
| Kategori |. NET Framework kullanım |  
| Profil oluşturma yöntemi | Tüm |  
| İleti | % gc'de zaman çok yüksek. Aşırı miktarda çöp toplama taşması yoktur. |  
| Kural türü | Uyarı |  
  
 Örnekleme, .NET bellek ve kaynak çekişmesi yöntemleri kullanılarak profili, bu kural tetiklemek için en az 10 örnekleri toplamanız gerekir.  
  
## <a name="cause"></a>Sebep  
 Profil oluşturma sırasında toplanan sistem performansı verilerini toplam uygulama işleme süresi ile karşılaştırıldığında, çöp toplamaya harcanan süreyi aşırı yüksek olduğunu gösterir.  
  
## <a name="rule-description"></a>Kural Tanımı  
 Microsoft .NET ortak dil çalışma zamanı (CLR) nesnelerden artık uygulamanın kullandığı belleği geri kazanmak için atık Toplayıcıya kullanan bir otomatik bellek yönetimi mekanizması sağlar. Atık toplayıcı nesil odaklı birçok ayırmaları ömürlüdür varsayımına dayanır. Örneğin, yerel değişkenler, kısa süreli olmalıdır. Yeni oluşturulan nesneleri nesil 0 (gen 0) başlatın ve bunların uygulama yine de bunları kullanıyorsa, ne zaman, bir çöp toplama çalıştırın ve son olarak 2. nesil geçiş varlığını sürdürmesini nesil 1 ilerleme durumu.  
  
 Nesil 0'daki nesneleri, sık ve genellikle çok verimli bir şekilde toplanır. 1. nesil nesneler, daha az sıklıkta ve daha az verimli bir şekilde toplanır. Son olarak, uzun süreli nesneler nesil 2 içinde bile daha az sık toplanması. Tam çöp toplama çalıştırmak olan 2. nesil koleksiyonu da en pahalı bir işlemdir.  
  
 Toplam uygulama işleme süresi ile karşılaştırıldığında çöp toplamaya harcanan süreyi aşırı yüksek olduğunda, bu kural tetiklenir.  
  
> [!NOTE]
> Ne zaman zaman oranını çöp toplamaya harcanan önemlidir, ancak değil aşırı toplam uygulama işleme süresi ile karşılaştırıldığında [DA0023: Yüksek GC CPU süresi](../profiling/da0023-high-gc-cpu-time.md) yerine bu kural uyarı ateşlenir.  
  
## <a name="how-to-investigate-a-warning"></a>Bir uyarı araştırma  
 Hata Listesi penceresindeki iletiyi gitmek için çift tıklatın [işaret görünümü](../profiling/marks-view.md) profil oluşturma verilerinin. Bulma **.NET CLR bellek\\% gc'de zaman** sütun. Varsa belirli program yürütme aşamaları çöp toplamanın yönetilen bellek yükü diğer aşamaları ağır olduğu belirleyin. Gc'de zaman % değerlerini değer çöp toplama oranını karşılaştırma bildirilen içinde **Gen 0 toplamaları sayısı**, **Gen 1 toplamaları sayısı**, **Gen 2 toplamaları sayısı** değerleri .  
  
 Bir uygulama işleme toplam tutarı orantılı gerçekleştirme çöp toplama için harcadığı süreyi bildirmek % GC değerindeki zamanı çalışır. Bazı durumlarda % GC değerindeki zamanı çok yüksek bir değere bildirebilirsiniz, ancak nedeniyle aşırı çöp toplama değil unutmayın. % GC değerindeki zamanı hesaplanır biçimi hakkında daha fazla bilgi için bkz. [fark arasındaki performans verileri tarafından bildirilen farklı araçları – 4](http://go.microsoft.com/fwlink/?LinkId=177863) girişi **Maoni'nın blog** MSDN'de. Sayfa hataları ortaya çıkan veya uygulama tarafından diğer daha yüksek öncelikli iş makinede çöp toplama sırasında geçersiz kılınırsa, GC sayacı zaman % bu ek gecikmelere ücreti yansıtılır.
