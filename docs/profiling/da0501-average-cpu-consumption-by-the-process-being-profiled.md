---
title: 'DA0501: Profil oluşturulan işlem tarafından ortalama CPU kullanımı. | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.performance.rules.DA0501
- vs.performance.DA0501
- vs.performance.501
ms.assetid: b01946b4-75e3-47d5-a1a1-cebfae66a3af
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: f3b9ed2a0a27c3be992f6dadd2a6f18c1f8df9bd
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56598914"
---
# <a name="da0501-average-cpu-consumption-by-the-process-being-profiled"></a>DA0501: Profil oluşturulan işlem tarafından ortalama CPU kullanımı.

|||
|-|-|
|Kural Kimliği|DA501|
|Kategori|Kaynak İzleme|
|Profil oluşturma yöntemi|Tümü|
|İleti|Profil oluşturulan işlem tarafından ortalama CPU kullanımı.|
|Kural türü|Bilgiler|

 Örnekleme, .NET bellek ve kaynak çekişmesi yöntemleri kullanılarak profili, bu kural tetiklemek için en az 10 örnekleri toplamanız gerekir.

## <a name="rule-description"></a>Kural açıklaması
 Bu ileti bir işlemci yönergeleri uygulamadan çalıştırmakla meşgul olduğu sürenin yüzdesini bildirir. Bildirilen değer profil oluşturulan işlem etkin olduğu tüm ölçüm aralıklarında bir ortalamadır. Değeri, birden çok işlemcili bir makinede % 100'den daha büyük olabilir.

## <a name="how-to-use-rule-data"></a>Kural verileri kullanma
 Kural değeri, farklı sürümlerin performans veya programın yapıları karşılaştırmak veya farklı test senaryoları altında uygulama performansını anlamak için kullanın.