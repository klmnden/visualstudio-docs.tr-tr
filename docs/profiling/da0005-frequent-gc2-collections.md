---
title: 'DA0005: Sık kullanılan GC2 koleksiyonları | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.performance.DA0005
- vs.performance.rules.DAManyGC2Collections
- vs.performance.5
- vs.performance.rules.DA0005
ms.assetid: 8d3f267c-8a74-4cf4-91a5-0b06a76dc2bd
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: e338bb4bc2040359c4b72ba258fcfceb689c6b30
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62936580"
---
# <a name="da0005-frequent-gc2-collections"></a>DA0005: Sık kullanılan GC2 koleksiyonları

|||
|-|-|
|RuleId|DA0005|
|Kategori|.NET framework kullanımı|
|Profil oluşturma yöntemi|.NET bellek|
|İleti|Nesnelerinizin bir çoğu, nesil 2 çöp toplamada toplanmıyor.|
|İleti türü|Uyarı|

## <a name="cause"></a>Sebep
 Çok sayıda .NET bellek nesneleri nesil 2 çöp toplamada kazanılır.

## <a name="rule-description"></a>Kural açıklaması
 Microsoft .NET ortak dil çalışma zamanı (CLR) nesnelerden artık uygulamanın kullandığı belleği geri kazanmak için atık Toplayıcıya kullanan bir otomatik bellek yönetimi mekanizması sağlar. Atık toplayıcı nesil odaklı birçok ayırmaları ömürlüdür varsayımına dayanır. Örneğin, yerel değişkenler, kısa süreli olmalıdır. Yeni oluşturulan nesneleri nesil 0 (gen 0) başlatın ve bunların uygulama yine de bunları kullanıyorsa, ne zaman, bir çöp toplama çalıştırın ve son olarak 2. nesil geçiş varlığını sürdürmesini nesil 1 ilerleme durumu.

 Nesil 0'daki nesneleri, sık ve genellikle çok verimli bir şekilde toplanır. 1. nesil nesneler, daha az sıklıkta ve daha az verimli bir şekilde toplanır. Son olarak, uzun süreli nesneler nesil 2 içinde bile daha az sık toplanması. Tam çöp toplama çalıştırmak olan 2. nesil koleksiyonu da en pahalı bir işlemdir.

 Bu kural ne zaman orantılı olarak çok fazla nesil 2 çöp koleksiyonları oluşmuş tetikler. Çok fazla görece kısa süreli nesneleri nesil 1 toplamadan ancak ardından 2. nesil tam koleksiyonunda toplanır olanağına sahip olursunuz, bellek yönetimi maliyetini kolayca aşırı hale gelebilir. Daha fazla bilgi için [Orta yaşam kriz](http://go.microsoft.com/fwlink/?LinkId=177835) Rico Mariani'nın performans ipuçları MSDN Web sitesinde gönderin.

## <a name="how-to-investigate-a-warning"></a>Bir uyarı araştırma
 Gözden geçirme [.NET bellek verisi görünümleri](../profiling/dotnet-memory-data-views.md) bellek ayırma uygulama desenini anlamak için raporlar. Kullanım [nesne ömrü görünümü](../profiling/object-lifetime-view.md) 2. nesil ve ardından buradan iadesi nesneleri geri kalan hangi programın veri belirleme. Kullanım [ayırma görünümü](../profiling/dotnet-memory-allocations-view.md) bu ayırma sonuçlanan yürütme yolunu belirlemek için.

 Çöp toplama performansını artırma hakkında daha fazla bilgi için bkz. [çöp toplayıcı temelleri ve performans ipuçları](http://go.microsoft.com/fwlink/?LinkId=148226) Microsoft Web sitesinde. Otomatik çöp toplama yükü hakkında daha fazla bilgi için bkz. [büyük nesne yığını Kapatılmamışa](http://go.microsoft.com/fwlink/?LinkId=177836).