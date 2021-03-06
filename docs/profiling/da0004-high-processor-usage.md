---
title: 'DA0004: Yüksek işlemci kullanımı | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.performance.rules.DAHighProcessorUsage
- vs.performance.rules.DA0004
- vs.performance.DA0004
- vs.performance.4
ms.assetid: 2c4fb569-929e-4f1d-8c50-b590ee371351
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 7fcc468d3820e34db24edbbf311cbae17bda0732
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62936713"
---
# <a name="da0004-high-processor-usage"></a>DA0004: Yüksek işlemci kullanımı

|||
|-|-|
|Kural Kimliği|DA0004|
|Kategori|Profil oluşturma araçları kullanım|
|Profil oluşturma yöntemleri|İzleme<br /><br /> Örnekleme|
|İleti|Tutarlı bir şekilde işlemci kullanım %75 ' dir. CPU bağımlı uygulamalar için örnekleme modu kullanmayı düşünün.|
|Kural türü|Bilgiler|

 Örnekleme, .NET bellek ve kaynak çekişmesi yöntemleri kullanılarak profili, bu kural tetiklemek için en az 10 örnekleri toplamanız gerekir.

## <a name="cause"></a>Sebep
 İşlemci (CPU) kullanımı, profil oluşturma Araçlar yöntemini kullanarak toplanan veriyi yüksek. Örnekleme profili oluşturma yöntemi bir CPU profili oluşturma uygulama bağlı kullanmayı düşünün.

## <a name="rule-description"></a>Kural açıklaması
 Bu profil oluşturma çalışması süresince işlemci (veya işlemciler) tutarlı bir şekilde meşguldü. Yüksek CPU kullanımı, CPU bağımlı uygulama belirtebilirsiniz. İzleme eklenmiş profil CPU kullanım senaryoları araştırmak için en etkili yolu değildir. Örnekleme yönergeleri işlemci üzerinde yürütme zamanlarının çoğunu harcama uygulamaları profil oluştururken daha etkilidir.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Yeniden örnekleme yöntemini işlevi zamanlamaları gerektiren veya işlemci performans sorunlarını anlama, giriş/çıkış daha ilgi sürece yerine izleme metodunu kullanarak uygulamanızın profilini oluşturmanız göz önünde bulundurun.