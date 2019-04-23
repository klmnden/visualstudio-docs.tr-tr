---
title: 'DA0003: Pek çok çekirdek örneği | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.performance.rules.DA0003
- vs.performance.DA0003
- vs.performance.3
- vs.performance.rules.DAManyKernelSamples
ms.assetid: c1f46f77-eb95-42e5-b340-d86bc9de41b4
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 1cd12b4944da36e480aa44f312b44133c657365f
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60039941"
---
# <a name="da0003-many-kernel-samples"></a>DA0003: Pek çok çekirdek örneği

|||
|-|-|
|Kural Kimliği|DA0003|
|Kategori|Profil oluşturma araçları kullanım|
|Profil oluşturma yöntemleri|Örnekleme|
|İleti|Çekirdek modunda bir yüksek oranda örnekleri var. Bu, yüksek hacimli g/ç etkinliğinin veya yüksek oranda bağlam belirtebilir. Uygulamanızı Instrumentation Mode kullanarak yeniden profil oluşturmayı göz önünde bulundurun.|
|Kural türü|Bilgiler|

## <a name="cause"></a>Sebep
 Uygulama için toplanan çağrı yığını örnekleri önemli bir kısmı çekirdek modunda yürütülüyor. Farklı bir profil oluşturma yöntemini kullanarak uygulamanızın profilini oluşturmanız göz önünde bulundurun.

## <a name="rule-description"></a>Kural açıklaması
 Windows çekirdek modu veya kullanıcı modu kod çalıştırılabilir. (Çekirdek modu da ayrıcalıklı modu olarak adlandırılır.) Bir aygıt sürücüsü gibi alt düzey sistem kodu yalnızca çekirdek modunda çalışır. Bir kullanıcı modu uygulaması için iş parçacığı veya işlem eşitleme temellerine bekleyin ya da sistem çağrıları yapmak için g/ç işlemleri gerçekleştirmek için çekirdek moduna geçiş yapabilirsiniz.

 Örnekleme, kullanıcı modunda çalışmayı yapan zamanlarının çoğunu harcama uygulamaları profil oluştururken en etkili olur. Uygulama çekirdek modunda yürütülürken toplanan örneklerin sayısı sık g/ç işlemleri belirtebilir veya anahtarlarının oluşan bu bağlamı gösterebilir. Bu işlemlerin hiçbiri örnekleme metodu kullanılarak araştırılabilir. Çok fazla sayıda çekirdek modu örneği alınır, örnekleme verileri istatistiksel açıdan anlamlı olması için yeterli kullanıcı modu örnekleri içerebilir.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Uygulamanız aşağıdaki seçeneklerden birini kullanarak yeniden profil oluşturmayı göz önünde bulundurun:

- İzleme metodunu kullanarak profili.

- Daha fazla örnek kullanıcı modunda toplanacak denemek için örnekleme hızını artırın.