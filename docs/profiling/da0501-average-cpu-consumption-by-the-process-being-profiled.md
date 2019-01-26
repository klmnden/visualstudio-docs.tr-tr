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
ms.openlocfilehash: b7bd27ceb83105a9d790937b3a5fcb904adf3abd
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54983982"
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