---
title: "CA2231: Eşittir işlecini ValueType.Equals'ı geçersiz kılarak aşırı yükleyin"
ms.date: 03/11/2019
ms.topic: reference
f1_keywords:
- OverloadOperatorEqualsOnOverridingValueTypeEquals
- CA2231
- OverrideOperatorEqualsOnOverridingValueTypeEquals
helpviewer_keywords:
- OverloadOperatorEqualsOnOverridingValueTypeEquals
- CA2231
ms.assetid: 114c0161-261a-40ad-8b2c-0932d6909d2a
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: b5826633737c3bb7d8f358ff090f0b1a55ac8eef
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71231050"
---
# <a name="ca2231-overload-operator-equals-on-overriding-valuetypeequals"></a>CA2231: Eşittir işlecini ValueType.Equals'ı geçersiz kılarak aşırı yükleyin

|||
|-|-|
|TypeName|OverloadOperatorEqualsOnOverridingValueTypeEquals|
|CheckId|CA2231|
|Kategori|Microsoft. Usage|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep

Değer türü geçersiz kılınır <xref:System.Object.Equals%2A?displayProperty=fullName> ancak eşitlik işlecini uygulamaz.

Bu kural varsayılan olarak yalnızca dışarıdan görünür türlere bakar, ancak bu [yapılandırılabilir](#configurability).

## <a name="rule-description"></a>Kural açıklaması

Çoğu programlama dilinde, değer türleri için eşitlik işlecinin (= =) varsayılan bir uygulamasý yoktur. Programlama diliniz operatör aşırı yüklerini destekliyorsa, eşitlik işlecini uygulamayı düşünmelisiniz. Davranışı ile özdeş <xref:System.Object.Equals%2A>olmalıdır.

Eşitlik işlecinin aşırı yüklenmiş bir uygulamasında varsayılan eşitlik işlecini kullanamazsınız. Bunun yapılması, yığın taşmasına neden olur. Eşitlik işlecini uygulamak için uygulamanızdaki Object. Equals yöntemini kullanın. Örneğin:

```vb
If (Object.ReferenceEquals(left, Nothing)) Then
    Return Object.ReferenceEquals(right, Nothing)
Else
    Return left.Equals(right)
End If
```

```csharp
if (Object.ReferenceEquals(left, null))
    return Object.ReferenceEquals(right, null);
return left.Equals(right);
```

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Bu kuralın ihlalini onarmak için eşitlik işlecini uygulayın.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Bu kuraldan bir uyarıyı gizlemek güvenlidir; Ancak, mümkünse eşitlik operatörünü sağlamanızı öneririz.

## <a name="configurability"></a>Yapılandırılabilirlik

Bu kuralı [FxCop çözümleyicilerinin](install-fxcop-analyzers.md) (eski analizler olmadan) çalıştırıyorsanız, kod tabanınızın hangi bölümlerinin bu kuralı çalıştırmak için erişilebilirliğini temel alarak yapılandırabilirsiniz. Örneğin, kuralın yalnızca genel olmayan API yüzeyine karşı çalışması gerektiğini belirtmek için, aşağıdaki anahtar-değer çiftini projenizdeki bir. editorconfig dosyasına ekleyin:

```ini
dotnet_code_quality.ca2231.api_surface = private, internal
```

Bu seçeneği yalnızca bu kural için, tüm kurallar için veya bu kategorideki tüm kurallar (kullanım) için yapılandırabilirsiniz. Daha fazla bilgi için bkz. [FxCop çözümleyicileri yapılandırma](configure-fxcop-analyzers.md).

## <a name="example"></a>Örnek

Aşağıdaki örnek, bu kuralı ihlal eden bir türü tanımlar:

[!code-csharp[FxCop.Usage.EqualsGetHashCode#1](../code-quality/codesnippet/CSharp/ca2231-overload-operator-equals-on-overriding-valuetype-equals_1.cs)]

## <a name="related-rules"></a>İlgili kurallar

- [CA1046 Eşittir işlecini başvuru türlerinde aşırı yüklemeyin](../code-quality/ca1046-do-not-overload-operator-equals-on-reference-types.md)
- [CA2225 İşleç aşırı yüklemelerinin adlandırılmış alternatifleri var](../code-quality/ca2225-operator-overloads-have-named-alternates.md)
- [CA2226 İşleçler, simetrik aşırı yüklemeleri içermelidir](../code-quality/ca2226-operators-should-have-symmetrical-overloads.md)
- [CA2224 Aşırı yükleme işlecinin eşittir ile eşittir geçersiz kıl](../code-quality/ca2224-override-equals-on-overloading-operator-equals.md)
- [CA2218 Geçersiz kılma için GetHashCode geçersiz kılma](../code-quality/ca2218-override-gethashcode-on-overriding-equals.md)

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Object.Equals%2A?displayProperty=fullName>