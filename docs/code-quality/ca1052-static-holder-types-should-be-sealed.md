---
title: 'CA1052: Static tutucu türler sealed olmalıdır'
ms.date: 11/09/2018
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- StaticHolderTypesShouldBeSealed
- CA1052
helpviewer_keywords:
- CA1052
- StaticHolderTypesShouldBeSealed
ms.assetid: 51a3165d-781e-4a55-aa0d-ea25fee7d4f2
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CPP
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: a8743dc617a7749a81528c8ef5c570f7d52b4a06
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54937093"
---
# <a name="ca1052-static-holder-types-should-be-sealed"></a>CA1052: Static tutucu türler sealed olmalıdır

|||
|-|-|
|TypeName|StaticHolderTypesShouldBeSealed|
|CheckId|CA1052|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep

Bir ortak veya korumalı, soyut olmayan tür yalnızca statik üyeleri içerir ve ile bildirilmedi [korumalı](/dotnet/csharp/language-reference/keywords/sealed) ([NotInheritable](/dotnet/visual-basic/language-reference/modifiers/notinheritable)) değiştiricisi.

## <a name="rule-description"></a>Kural açıklaması

Kural CA1052 türü türetilmiş türde geçersiz kılınabilir herhangi bir işlevsellik sağlamaz çünkü yalnızca statik üyeleri içeren bir tür devralınacak şekilde tasarlanmamıştır olduğunu varsayar. Devralınan düşünülmemiştir bir tür ile işaretlenmelidir `sealed` veya `NotInheritable` değiştiricisi, bir taban türü olarak kullanılmasını önlemek için. Bu kural, soyut sınıflar için başlatılmıyor.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Bu kural ihlalini düzeltmek için türü olarak işaretlemek `sealed` veya `NotInheritable`. .NET Framework 2.0, hedeflediğiniz veya daha sonra türü olarak işaretlemek için daha iyi bir yaklaşım ise `static` veya `Shared`. Bu şekilde sınıfı oluşturulmasını önlemek için bir özel yapıcı bildirmeniz gerekmez.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Türü yalnızca devralınacak şekilde tasarlanmıştır, bu kuraldan bir uyarıyı gizler. Olmaması `sealed` veya `NotInheritable` değiştiricisi önerir türü temel tür olarak kullanışlıdır.

## <a name="example-of-a-violation"></a>Bir ihlali örneği

Aşağıdaki örnek kuralını ihlal eden bir tür gösterir.

[!code-csharp[FxCop.Design.StaticMembers#1](../code-quality/codesnippet/CSharp/ca1052-static-holder-types-should-be-sealed_1.cs)]
[!code-vb[FxCop.Design.StaticMembers#1](../code-quality/codesnippet/VisualBasic/ca1052-static-holder-types-should-be-sealed_1.vb)]
[!code-cpp[FxCop.Design.StaticMembers#1](../code-quality/codesnippet/CPP/ca1052-static-holder-types-should-be-sealed_1.cpp)]

## <a name="fix-with-the-static-modifier"></a>Statik değiştirici ile düzeltin

Aşağıdaki örnek, türü ile işaretleyerek bu kural ihlalini düzeltmek gösterilmektedir `static` değiştiricisi C#.

[!code-csharp[FxCop.Design.StaticMembersFixed#1](../code-quality/codesnippet/CSharp/ca1052-static-holder-types-should-be-sealed_2.cs)]

## <a name="related-rules"></a>İlgili kuralları

[CA1053: Statik tutucu türlerinde oluşturucular bulunmamalıdır](../code-quality/ca1053-static-holder-types-should-not-have-constructors.md)