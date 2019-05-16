---
title: 'CA1033: Arabirim yöntemleri alt türler tarafından çağırılabilir | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- InterfaceMethodsShouldBeCallableByChildTypes
- CA1033
helpviewer_keywords:
- CA1033
- InterfaceMethodsShouldBeCallableByChildTypes
ms.assetid: 9f171497-a5e3-4769-a77b-7aed755b2662
caps.latest.revision: 19
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: bd801e7afc1fa0a4edf043aba560bc4afcdae9de
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65682840"
---
# <a name="ca1033-interface-methods-should-be-callable-by-child-types"></a>CA1033: Arabirim metotları alt türler tarafından çağrılabilmelidir
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|InterfaceMethodsShouldBeCallableByChildTypes|
|CheckId|CA1033|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep
 Ağzı açık dışarıdan görünen bir tür açık yöntem uygulaması ortak bir arabirim sağlar ve aynı ada sahip alternatif dışarıdan görünen bir yöntem sağlamaz.

## <a name="rule-description"></a>Kural Tanımı
 Açıkça bir ortak arabirim yöntemini uygulayan bir taban türü göz önünde bulundurun. Temel türünden türetilen bir tür devralınan arabirim yöntemi yalnızca geçerli örneğe bir başvuru erişebilirsiniz (`this` C#) arabirimine dönüştürün. Temel uygulama artık türetilmiş bir tür (açıkça) devralınan arabirim yöntemini yeniden uyguluyorsa, erişilebilir. Geçerli örnek başvuru çağrısıyla türetilen uygulamaya çağırır; Bu, özyineleme ve bir nihai yığın taşmasına neden olur.

 Bu kural açık bir uygulama için bir ihlali raporlamaz <xref:System.IDisposable.Dispose%2A?displayProperty=fullName> dışarıdan görünür olduğunda `Close()` veya `System.IDisposable.Dispose(Boolean)` yöntemi sağlanır.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için aynı işlevselliği kullanıma sunma ve türetilmiş türlere de görünür olan yeni bir yöntem uygulayın veya açıkça verilmemiş bir uygulama için değiştirin. Bir değişiklik kabul edilebilir ise, korumalı tür alternatiftir.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Dışarıdan görünen bir yöntem sağlanır, ancak açıkça uygulanan yöntem yerine farklı bir ad ile aynı işlevlere sahiptir, bu kuraldan bir uyarıyı bastırmak güvenlidir.

## <a name="example"></a>Örnek
 Aşağıdaki örnek, bir tür gösterir `ViolatingBase`, kural ve bir tür ihlal `FixedBase`, ihlalin düzeltme gösterir.

 [!code-csharp[FxCop.Design.ExplicitMethodImplementations#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Design.ExplicitMethodImplementations/cs/FxCop.Design.ExplicitMethodImplementations.cs#1)]

## <a name="see-also"></a>Ayrıca Bkz.
 [Arabirimler](https://msdn.microsoft.com/library/2feda177-ce11-432d-81b4-d50f5f35fd37)
