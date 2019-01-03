---
title: 'DA0008: Az sayıda örnek toplandı | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.performance.rules.DATooFewSamples
- vs.performance.8
- vs.performance.DA0008
- vs.performance.rules.DA0008
ms.assetid: 8a5b78aa-7b3d-476c-a47d-abfaff3fae7c
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 2c38aaed1c706cc8c5ddd9447fd30fadd5698133
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53987148"
---
# <a name="da0008-few-samples-collected"></a>DA0008: Toplanan örnek az

|||  
|-|-|  
|Kural Kimliği|DA0008|  
|Kategori|Profil oluşturma araçları kullanım|  
|Profil oluşturma yöntemi|Örnekleme|  
|İleti|Yalnızca birkaç örnek toplanmadı. Uzun bir veya daha hızlı çalışmasını örnekleme hızı daha geçerli sonuçlar için göz önünde bulundurun.|  
|Kural türü|Bilgiler|  

## <a name="cause"></a>Sebep  
 Yalnızca birkaç örnek profil oluşturma çalışmasında toplanmadı.  

## <a name="rule-description"></a>Kural açıklaması  
 Örnekleme yöntemi kullanıldığında, bir istatistiksel veriler gerçek program davranışını temsil emin olmak için örnek sayısı toplamanız gerekir. Örnekleme hataları en aza indirmek için en az 1000 program yönerge yürütme davranışını örnekleri toplamak çalışmanız gerekir. Yeterli örnekleri tahsil etmeme, profil oluşturma verilerinin analiz ederken, misled.  

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?  
 Bir uygulama bir artık çalıştırma profili oluşturma veya istatistiksel sonuçları elde etmek için daha hızlı bir örnekleme hızı kullanmayı düşünün. Visual Studio IDE'de örnekleme oranını değiştirme hakkında daha fazla bilgi için bkz: [nasıl yapılır: Örnekleme olayları seçme](../profiling/how-to-choose-sampling-events.md). Profil Araçları komut satırı özelliğini kullandığınızda, örnekleme hızını değiştirme hakkında daha fazla bilgi için bkz. [Zamanlayıcı](../profiling/timer.md) içinde [VSPerfCmd](../profiling/vsperfcmd.md) başvuru.