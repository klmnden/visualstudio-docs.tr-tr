---
title: 'CA1052: Statik tutucu türleri statik veya NotInheritable olmalıdır'
ms.date: 07/25/2019
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
ms.openlocfilehash: 757b6b46e0c0892f5eb4c868b15654b29cd51c0e
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71235627"
---
# <a name="ca1052-static-holder-types-should-be-static-or-notinheritable"></a>CA1052: Statik tutucu türleri statik veya NotInheritable olmalıdır

|||
|-|-|
|TypeName|StaticHolderTypesAnalyzer|
|CheckId|CA1052|
|Kategori|Microsoft.Design|
|Son değişiklik|Yeni|

## <a name="cause"></a>Sebep

Soyut olmayan bir tür yalnızca statik üyeler içerir (mümkün olan varsayılan oluşturucu dışında) ve [statik](/dotnet/csharp/language-reference/keywords/static) veya [paylaşılan](/dotnet/visual-basic/language-reference/modifiers/shared) değiştiriciyle bildirilmez.

Bu kural varsayılan olarak yalnızca dışarıdan görünür türlere bakar, ancak bu [yapılandırılabilir](#configurability).

## <a name="rule-description"></a>Kural açıklaması

Kural CA1052, türü türetilmiş bir türde geçersiz kılınabilen herhangi bir işlev sağlamadığından, yalnızca statik üyeler içeren bir türün devralınabilmesi için tasarlanmadığını varsayar. Devralınmayan bir tür, bir temel tür olarak kullanımını önlemek için içindeki `static` C# değiştiriciyle işaretlenmelidir. Ayrıca, varsayılan oluşturucusunun kaldırılması gerekir. Visual Basic, sınıfın bir [modüle](/dotnet/visual-basic/language-reference/statements/module-statement)dönüştürülmesi gerekir.

Bu kural, temel sınıfı olan soyut sınıflar veya sınıflar için başlatılmıyor. Ancak, kural boş bir arabirimi destekleyen sınıflar için ateşlenir.

> [!NOTE]
> Bu kuralın FxCop Çözümleyicisi uygulamasında [kural CA1053](../code-quality/ca1053-static-holder-types-should-not-have-constructors.md)işlevlerini de kapsar.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Bu kural ihlalini onarmak için, türü olarak `static` işaretleyin ve varsayılan oluşturucuyu (C#) kaldırın veya bir modüle dönüştürün (Visual Basic).

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Yalnızca tür devralınacak şekilde tasarlandıysa, bu kuraldan bir uyarı gizleyin. `static` Değiştiricinin yokluğu, türün temel tür olarak yararlı olmasını önerir.

## <a name="configurability"></a>Yapılandırılabilirlik

Bu kuralı [FxCop çözümleyicilerinin](install-fxcop-analyzers.md) (eski analizler olmadan) çalıştırıyorsanız, kod tabanınızın hangi bölümlerinin bu kuralı çalıştırmak için erişilebilirliğini temel alarak yapılandırabilirsiniz. Örneğin, kuralın yalnızca genel olmayan API yüzeyine karşı çalışması gerektiğini belirtmek için, aşağıdaki anahtar-değer çiftini projenizdeki bir EditorConfig dosyasına ekleyin:

```ini
dotnet_code_quality.ca1052.api_surface = private, internal
```

Bu seçeneği yalnızca bu kural için, tüm kurallar için veya bu kategorideki tüm kurallar (tasarım) için yapılandırabilirsiniz. Daha fazla bilgi için bkz. [FxCop çözümleyicileri yapılandırma](configure-fxcop-analyzers.md).

## <a name="example-of-a-violation"></a>İhlalin örneği

Aşağıdaki örnek, kuralı ihlal eden bir türü gösterir:

[!code-csharp[FxCop.Design.StaticMembers#1](../code-quality/codesnippet/CSharp/ca1052-static-holder-types-should-be-sealed_1.cs)]
[!code-vb[FxCop.Design.StaticMembers#1](../code-quality/codesnippet/VisualBasic/ca1052-static-holder-types-should-be-sealed_1.vb)]
[!code-cpp[FxCop.Design.StaticMembers#1](../code-quality/codesnippet/CPP/ca1052-static-holder-types-should-be-sealed_1.cpp)]

## <a name="fix-with-the-static-modifier"></a>Statik değiştiriciyle onarma

Aşağıdaki örnek, türü `static` değiştiriciyle birlikte işaretleyerek bu kural ihlalinin nasıl düzeltileceğini gösterir: C#

```csharp
public static class StaticMembers
{
    public static int SomeProperty { get; set; }
    public static void SomeMethod() { }
}
```