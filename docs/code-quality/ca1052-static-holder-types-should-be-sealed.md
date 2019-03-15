---
title: 'CA1052: Static tutucu türler sealed olmalıdır'
ms.date: 03/11/2019
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
ms.openlocfilehash: 46a8c9a4e22c7a54a4b2b68f95bb2b81f3a0888e
ms.sourcegitcommit: f7c401a376ce410336846835332a693e6159c551
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/14/2019
ms.locfileid: "57870392"
---
# <a name="ca1052-static-holder-types-should-be-sealed"></a>CA1052: Static tutucu türler sealed olmalıdır

|||
|-|-|
|TypeName|StaticHolderTypesShouldBeSealed|
|CheckId|CA1052|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep

Bir soyut olmayan tür yalnızca statik üyeleri içerir ve ile bildirilmedi [korumalı](/dotnet/csharp/language-reference/keywords/sealed) ([NotInheritable](/dotnet/visual-basic/language-reference/modifiers/notinheritable)) değiştiricisi.

Varsayılan olarak, bu kural yalnızca dışarıdan görülebilen türler görünür, ancak bu [yapılandırılabilir](#configurability).

## <a name="rule-description"></a>Kural açıklaması

Kural CA1052 türü türetilmiş türde geçersiz kılınabilir herhangi bir işlevsellik sağlamaz çünkü yalnızca statik üyeleri içeren bir tür devralınacak şekilde tasarlanmamıştır olduğunu varsayar. Devralınan düşünülmemiştir bir tür ile işaretlenmelidir `sealed` veya `NotInheritable` değiştiricisi, bir taban türü olarak kullanılmasını önlemek için. Bu kural, soyut sınıflar için başlatılmıyor.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Bu kural ihlalini düzeltmek için türü olarak işaretlemek `sealed` veya `NotInheritable`. .NET Framework 2.0, hedeflediğiniz veya daha sonra türü olarak işaretlemek için daha iyi bir yaklaşım ise `static` veya `Shared`. Bu şekilde sınıfı oluşturulmasını önlemek için bir özel yapıcı bildirmeniz gerekmez.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Türü yalnızca devralınacak şekilde tasarlanmıştır, bu kuraldan bir uyarıyı gizler. Olmaması `sealed` veya `NotInheritable` değiştiricisi önerir türü temel tür olarak kullanışlıdır.

## <a name="configurability"></a>Etkiler ve yapılandırma

Bu kuraldan çalıştırıyorsanız [FxCop Çözümleyicileri](install-fxcop-analyzers.md) (ve statik kod analizi üzerinden değil), hangi parçalarının yapılandırabilirsiniz, bu kuralı çalıştırmak için kod tabanı, kendi erişilebilirliği temel. Örneğin, kural yalnızca genel olmayan API yüzeyi karşı çalışması gerektiğini belirtmek için projenizi bir .editorconfig dosyasında şu anahtar-değer çifti ekleyin:

```
dotnet_code_quality.ca1052.api_surface = private, internal
```

Bu kategoride (tasarımı), bu seçenek yalnızca bu kural, tüm kuralları veya tüm kuralları yapılandırabilirsiniz. Daha fazla bilgi için [yapılandırma FxCop Çözümleyicileri](configure-fxcop-analyzers.md).

## <a name="example-of-a-violation"></a>Bir ihlali örneği

Aşağıdaki örnek, kuralını ihlal eden bir tür gösterir:

[!code-csharp[FxCop.Design.StaticMembers#1](../code-quality/codesnippet/CSharp/ca1052-static-holder-types-should-be-sealed_1.cs)]
[!code-vb[FxCop.Design.StaticMembers#1](../code-quality/codesnippet/VisualBasic/ca1052-static-holder-types-should-be-sealed_1.vb)]
[!code-cpp[FxCop.Design.StaticMembers#1](../code-quality/codesnippet/CPP/ca1052-static-holder-types-should-be-sealed_1.cpp)]

## <a name="fix-with-the-static-modifier"></a>Statik değiştirici ile düzeltin

Aşağıdaki örnek, türü ile işaretleyerek bu kural ihlalini düzeltmek gösterilmektedir `static` değiştiricisi C#:

[!code-csharp[FxCop.Design.StaticMembersFixed#1](../code-quality/codesnippet/CSharp/ca1052-static-holder-types-should-be-sealed_2.cs)]

## <a name="related-rules"></a>İlgili kuralları

- [CA1053: Statik tutucu türlerinde oluşturucular bulunmamalıdır](../code-quality/ca1053-static-holder-types-should-not-have-constructors.md)