---
title: 'CA1033: Arabirim metotları alt türler tarafından çağrılabilmelidir'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- InterfaceMethodsShouldBeCallableByChildTypes
- CA1033
helpviewer_keywords:
- CA1033
- InterfaceMethodsShouldBeCallableByChildTypes
ms.assetid: 9f171497-a5e3-4769-a77b-7aed755b2662
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 10db644fe4cf65a7336ef8bd50dcf62e072e1c46
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68922960"
---
# <a name="ca1033-interface-methods-should-be-callable-by-child-types"></a>CA1033: Arabirim metotları alt türler tarafından çağrılabilmelidir

|||
|-|-|
|TypeName|InterfaceMethodsShouldBeCallableByChildTypes|
|CheckId|CA1033|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep
Ağzı açık dışarıdan görünen bir tür açık yöntem uygulaması ortak bir arabirim sağlar ve aynı ada sahip alternatif dışarıdan görünen bir yöntem sağlamaz.

## <a name="rule-description"></a>Kural açıklaması
Açıkça bir ortak arabirim yöntemi uygulayan bir temel tür düşünün. Temel türden türetilen bir tür, devralınan arabirim yöntemine yalnızca, arabirime atama yapan geçerli örneğe (`this` içindeki C#) başvuru aracılığıyla erişebilir. Türetilmiş tür, devralınan arabirim yöntemini yeniden uygularsa (açıkça), temel uygulamaya artık erişilemez. Geçerli örnek başvurusu aracılığıyla yapılan çağrı, türetilmiş uygulamayı çağıracaktır; Bu, özyineleme ve nihai yığın taşmasına neden olur.

Bu kural dışarıdan görünür <xref:System.IDisposable.Dispose%2A?displayProperty=fullName> `Close()` veya `System.IDisposable.Dispose(Boolean)` Yöntem sağlandığında açık bir uygulama için bir ihlal raporlamaz.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kural ihlalini onarmak için, aynı işlevselliği kullanıma sunan ve türetilmiş türler tarafından görülebilen ve açık olmayan bir uygulamaya yapılan değişiklikler için yeni bir yöntem uygulayın. Son değişiklik kabul edilebilir ise, bir alternatif, türü korumalı hale getirmek için bir alternatiftir.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Aynı işlevselliğe sahip, ancak açıkça uygulanan yöntemden farklı bir ada sahip dışarıdan görünür bir yöntem sağlanmışsa, bu kuraldan bir uyarının görüntülenmesini güvenli hale gelir.

## <a name="example"></a>Örnek
Aşağıdaki örnek, ihlalin bir düzeltmesini `ViolatingBase`gösteren bir türü ve `FixedBase`kuralı ihlal eden bir türü gösterir.

[!code-csharp[FxCop.Design.ExplicitMethodImplementations#1](../code-quality/codesnippet/CSharp/ca1033-interface-methods-should-be-callable-by-child-types_1.cs)]

## <a name="see-also"></a>Ayrıca bkz.
[Arabirimler](/dotnet/csharp/programming-guide/interfaces/index)