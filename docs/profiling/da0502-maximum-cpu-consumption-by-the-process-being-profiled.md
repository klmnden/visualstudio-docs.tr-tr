---
title: 'DA0502: Profili oluşturulan işlemin maksimum CPU kullanımının | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.performance.rules.DA0502
- vs.performance.DA0502
- vs.performance.502
ms.assetid: 1ee53df5-b0dc-4265-9d4f-527830d08725
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: e7092e6424a5f00ed4461a91ed10bbf530597082
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56612263"
---
# <a name="da0502-maximum-cpu-consumption-by-the-process-being-profiled"></a>DA0502: Profil oluşturulan işlem tarafından en fazla CPU kullanımı

|||
|-|-|
|Kural Kimliği|DA0502|
|Kategori|Kaynak İzleme|
|Profil oluşturma yöntemi|Tümü|
|İleti|Bu kural yalnızca bilgi içindir. İşlem()\\% İşlemci Zamanı sayacı, profil oluşturma işleminin CPU kullanımını ölçer. Bildirilen değer tüm ölçüm aralıklarında gözlemlenen en yüksek.|
|Kural türü|Bilgi|

 Örnekleme, .NET bellek ve kaynak çekişmesi yöntemleri kullanılarak profili, bu kural tetiklemek için en az 10 örnekleri toplamanız gerekir.

## <a name="rule-description"></a>Kural açıklaması
 Bu ileti, en yüksek işlemci yönergeleri uygulamadan çalıştırmakla meşgul olduğu süre yüzdesi bildirir. Profil oluşturulan işlem etkin olduğu tüm ölçüm aralıklarında arasında bildirilen en yüksek değeri bildirilen değerdir. Yüzde, birden çok işlemcili bir makinede % 100'den daha büyük olabilir.

## <a name="how-to-use-the-rule-data"></a>Kural verileri kullanma
 Kural değeri, farklı sürümlerin performans veya programın yapıları karşılaştırmak veya farklı bir profil oluşturma senaryoları altında uygulama performansını anlamanın kullanın.