---
title: 'DA0503: İşlem için profili oluşturulan ortalama çalışma kümesinin bayt cinsinden | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.performance.503
- vs.performance.DA0503
- vs.performance.rules.DA0503
ms.assetid: 9047a494-eaaf-4679-b422-c64e8bde77a4
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 5e2453b73d7dae0a6a53130156cdb1ce35d38d43
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62935994"
---
# <a name="da0503-average-working-set-in-bytes-for-the-process-being-profiled"></a>DA0503: Profil oluşturulan işlem için bayt cinsinden ortalama çalışma kümesi

|||
|-|-|
|Kural Kimliği|DA0503|
|Kategori|Kaynak İzleme|
|Profil oluşturma yöntemi|Tümü|
|İleti|Bu bilgiler yalnızca bilgi toplanmıştır. İşlem çalışma kümesi sayacı profil bir işlem tarafından fiziksel bellek kullanımını ölçer. Bildirilen değer tüm ölçüm aralıklarında ortalaması hesaplanır.|
|Kural türü|Bilgiler|

 Örnekleme, .NET bellek ve kaynak çekişmesi yöntemleri kullanılarak profili, bu kural tetiklemek için en az 10 örnekleri toplamanız gerekir.

## <a name="rule-description"></a>Kural açıklaması
 Bu ileti, ortalama bayt (çalışma kümesi) işlemi şu anda kullandığı fiziksel bellek miktarını bildirir. İşlem çalışma kümesi, işlemin adres alanından şu anda fiziksel bellekte bulunan sayfaları temsil eder.

 Bildirilen değeri yerleşik sayfalarından işlem başvurmuş paylaşılan bellek segmentler içerir. Paylaşılan dll işlem başvuruları sayılan paylaşılan bellek segmentler dahildir. İşlem çalışma kümesi değerine paylaşılan bellek kesimler nedeniyle işlemin ayırdığı sanal bellek miktarından daha yüksek olabilir.

 Bildirilen değer profil oluşturulan işlem etkin olduğu tüm ölçüm aralıklarında bir ortalamadır.

 İşlem çalışma kümesi boyutu işlemi etkin bir şekilde kullanarak ne kadar sanal bellek yansıtır. Fiziksel bellek (veya RAM) miktarı tarafından etkilenir uygulama ve fiziksel belleğin için Çekişme diğer çalışan işlemlerini çalıştırmak kullanılabilir. Fiziksel bellek kısıtlı ise işlem çalışma kümesini çalıştığında düzenli aralıklarla oldukça etkin olmayan işlem çalışma kümesi sayfalarından kırpma tarafından bellek kullanımı arasında etkin işlemleri dengelemek için işletim sistemleri olarak önemli ölçüde farklılık apt değeridir.

 İşlem çalışma kümeleri hakkında daha fazla bilgi için bkz. [çalışma kümesi](http://go.microsoft.com/fwlink/?LinkId=177830) msdn'in Windows bellek yönetimi belgelerinde.

## <a name="how-to-use-rule-data"></a>Kural verileri kullanma
 Kural değeri, farklı sürümlerin performans veya programın yapıları karşılaştırmak veya farklı bir profil oluşturma senaryoları altında uygulama performansını anlamanın kullanın.

 Hata Listesi penceresindeki iletiyi gitmek için çift tıklatın [işaret görünümü](../profiling/marks-view.md) profil oluşturma verilerinin görünümü. Bulma **Process\Working ayarlamak** ve **Bellek\Sayfa/sn** sütunları. İki sütun karşılaştırın ve artan sayfalama g/ç etkinliği ile ilişkili olabilir görünmesine belirli program yürütme aşamaları olup olmadığını belirleyin.