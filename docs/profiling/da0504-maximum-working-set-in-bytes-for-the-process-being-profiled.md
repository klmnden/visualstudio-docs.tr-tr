---
title: 'DA0504: En yüksek çalışma kümesi profil oluşturulan işlem için bayt cinsinden | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.performance.DA0504
- vs.performance.504
- vs.performance.rules.DA0504
ms.assetid: 36e71603-ece7-4000-85fc-9da4eed61bf2
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 0f8956626d1ae03e52b9051730c3b7767532a5e7
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62935945"
---
# <a name="da0504-maximum-working-set-in-bytes-for-the-process-being-profiled"></a>DA0504: Profili oluşturulan İşlemin Bayt Cinsinden En Yüksek Sayıda Çalışma Kümesi

|||
|-|-|
|Kural Kimliği|DA0504|
|Kategori|Kaynak Yönetimi|
|Profil oluşturma yöntemi|Tümü|
|İleti|Bu bilgiler yalnızca bilgi toplanmıştır. İşlem çalışma kümesi sayacı profil bir işlem tarafından fiziksel bellek kullanımını ölçer. Bildirilen değer tüm ölçüm aralıklarında gözlemlenen en yüksek.|
|Kural türü|Bilgiler|

 Örnekleme, .NET bellek ve kaynak çekişmesi yöntemleri kullanılarak profili, bu kural tetiklemek için en az 10 örnekleri toplamanız gerekir.

## <a name="rule-description"></a>Kural açıklaması
 Bu ileti, en fazla işlem şu anda kullandığı bayt cinsinden fiziksel bellek miktarını bildirir. İşlem çalışma kümesi, işlemin adres alanından şu anda fiziksel bellekte bulunan sayfaları temsil eder. Bu kural, profil oluşturma etkinken işlem çalışma kümesi için maksimum değeri bildirir.

 Bildirilen değeri yerleşik sayfalarından işlem başvurmuş paylaşılan bellek segmentler içerir. Paylaşılan dll işlem başvuruları sayılan paylaşılan bellek segmentler dahildir. Değer işlemin çalışma kümesi paylaşılan bellek kesimler nedeniyle işlemin ayırdığı sanal bellek miktarından daha yüksek olabilir.

 İşlem çalışma kümesi boyutu işlemi etkin bir şekilde kullanarak ne kadar sanal bellek yansıtır. Fiziksel bellek (veya RAM) miktarı tarafından etkilenir uygulama ve fiziksel belleğin için Çekişme diğer çalışan işlemlerini çalıştırmak kullanılabilir. İşlem çalışma kümeleri hakkında daha fazla bilgi için bkz. [çalışma kümesi](http://go.microsoft.com/fwlink/?LinkId=177830) msdn'in Windows bellek yönetimi belgelerinde.

## <a name="how-to-use-rule-data"></a>Kural verileri kullanma
 Kural Windows performansı izleme olanağı Bu ölçüm verilerini toplar ve yalnızca bilgi bildirir. Bunu, farklı sürümlerin performans veya programın yapıları karşılaştırmak veya farklı test senaryoları altında uygulama performansını anlamak için kullanın.

 Hata Listesi penceresindeki iletiyi gitmek için çift tıklatın [işaret görünümü](../profiling/marks-view.md) profil oluşturma verilerinin. Bulma **Process\Working ayarlamak** ve **Bellek\Sayfa/sn** sayaç sütun. Ardından en büyük değerini bulmak **Process\Working ayarlamak** ve karşılaştırmak için **Bellek\Sayfa/sn** değeri. Genellikle, özellikle makine bellek kısıtlı olduğunda maksimum küme çalışma azalan sayfalama g/ç etkinliğini olduğu zaman aralığı ile ilişkilidir.