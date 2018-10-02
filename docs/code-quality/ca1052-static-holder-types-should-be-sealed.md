---
title: 'CA1052: Statik tutucu türleri mühürlenmelidir'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-ide-code-analysis
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
manager: douge
dev_langs:
- CPP
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: 2c5d22db6a973947faf228e2e3844d63a916e24e
ms.sourcegitcommit: ad5fb20f18b23eb8bd2568717f61edc6b7eee5e7
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/01/2018
ms.locfileid: "47859503"
---
# <a name="ca1052-static-holder-types-should-be-sealed"></a>CA1052: Statik tutucu türleri mühürlenmelidir

|||
|-|-|
|TypeName|StaticHolderTypesShouldBeSealed|
|CheckId|CA1052|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Ortak veya korumalı tür yalnızca statik üyeleri içerir ve ile bildirilmedi [korumalı](/dotnet/csharp/language-reference/keywords/sealed) ([NotInheritable](/dotnet/visual-basic/language-reference/modifiers/notinheritable)) değiştiricisi.

## <a name="rule-description"></a>Kural açıklaması
 Bu kural türü türetilmiş türde geçersiz kılınabilir herhangi bir işlevsellik sağlamaz çünkü yalnızca statik üyeleri içeren bir tür devralınacak şekilde tasarlanmamıştır olduğunu varsayar. Devralınan düşünülmemiştir bir tür ile işaretlenmelidir `sealed` değiştiricisi, bir taban türü olarak kullanılmasını önlemek için.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Bu kural ihlalini düzeltmek için türü olarak işaretlemek `sealed`. Hedeflediğiniz .NET Framework 2.0 veya sonraki sürümlerde, türü olarak işaretlemek için daha iyi bir yaklaşım ise `static`. Bu şekilde, sınıf oluşturulmasını önlemek için bir özel yapıcı bildirmek olmamasına özen gösterin.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Türü yalnızca devralınacak şekilde tasarlanmıştır, bu kuraldan bir uyarıyı gizler. Olmaması `sealed` değiştiricisi önerir türü temel tür olarak kullanışlıdır.

## <a name="example-of-a-violation"></a>Bir ihlali örneği

### <a name="description"></a>Açıklama
 Aşağıdaki örnek kuralını ihlal eden bir tür gösterir.

### <a name="code"></a>Kod
 [!code-csharp[FxCop.Design.StaticMembers#1](../code-quality/codesnippet/CSharp/ca1052-static-holder-types-should-be-sealed_1.cs)]
 [!code-vb[FxCop.Design.StaticMembers#1](../code-quality/codesnippet/VisualBasic/ca1052-static-holder-types-should-be-sealed_1.vb)]
 [!code-cpp[FxCop.Design.StaticMembers#1](../code-quality/codesnippet/CPP/ca1052-static-holder-types-should-be-sealed_1.cpp)]

## <a name="fix-with-the-static-modifier"></a>Statik değiştirici ile düzeltin

### <a name="description"></a>Açıklama
 Aşağıdaki örnek, türü ile işaretleyerek bu kural ihlalini düzeltmek gösterilmektedir `static` değiştiricisi.

### <a name="code"></a>Kod
 [!code-csharp[FxCop.Design.StaticMembersFixed#1](../code-quality/codesnippet/CSharp/ca1052-static-holder-types-should-be-sealed_2.cs)]

## <a name="related-rules"></a>İlgili kuralları
 [CA1053: Statik tutucu türlerinde oluşturucular bulunmamalıdır](../code-quality/ca1053-static-holder-types-should-not-have-constructors.md)
