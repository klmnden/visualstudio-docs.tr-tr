---
title: 'CA1033: Arabirim yöntemleri alt türler tarafından çağırılabilir olmalıdır'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
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
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 2dcfc7bc557c16ec07beb46cce08c6a934033b45
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53829822"
---
# <a name="ca1033-interface-methods-should-be-callable-by-child-types"></a>CA1033: Arabirim yöntemleri alt türler tarafından çağırılabilir olmalıdır

|||
|-|-|
|TypeName|InterfaceMethodsShouldBeCallableByChildTypes|
|CheckId|CA1033|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep
 Ağzı açık dışarıdan görünen bir tür açık yöntem uygulaması ortak bir arabirim sağlar ve aynı ada sahip alternatif dışarıdan görünen bir yöntem sağlamaz.

## <a name="rule-description"></a>Kural açıklaması
 Açıkça bir ortak arabirim yöntemini uygulayan bir taban türü göz önünde bulundurun. Temel türünden türetilen bir tür devralınan arabirim yöntemi yalnızca geçerli örneğe bir başvuru erişebilirsiniz (`this` C#) arabirimine dönüştürün. Temel uygulama artık türetilmiş bir tür devralınan arabirim yöntemini (açıkça) in, erişilebilir. Geçerli örnek başvuru çağrısıyla türetilen uygulamaya çağırır; Bu, özyineleme ve bir nihai yığın taşmasına neden olur.

 Bu kural açık bir uygulama için bir ihlali raporlamaz <xref:System.IDisposable.Dispose%2A?displayProperty=fullName> dışarıdan görünür olduğunda `Close()` veya `System.IDisposable.Dispose(Boolean)` yöntemi sağlanır.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Bu kural ihlalini düzeltmek için aynı işlevselliği kullanıma sunma ve türetilmiş türlere de görünür olan yeni bir yöntem uygulayın veya açıkça verilmemiş bir uygulama için değiştirin. Bir değişiklik kabul edilebilir ise, korumalı tür alternatiftir.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Dışarıdan görünen bir yöntem sağlanır, ancak açıkça uygulanan yöntem yerine farklı bir ad ile aynı işlevlere sahiptir, bu kuraldan bir uyarıyı bastırmak güvenlidir.

## <a name="example"></a>Örnek
 Aşağıdaki örnek, bir tür gösterir `ViolatingBase`, kural ve bir tür ihlal `FixedBase`, ihlalin düzeltme gösterir.

 [!code-csharp[FxCop.Design.ExplicitMethodImplementations#1](../code-quality/codesnippet/CSharp/ca1033-interface-methods-should-be-callable-by-child-types_1.cs)]

## <a name="see-also"></a>Ayrıca bkz.
 [Arabirimler](/dotnet/csharp/programming-guide/interfaces/index)