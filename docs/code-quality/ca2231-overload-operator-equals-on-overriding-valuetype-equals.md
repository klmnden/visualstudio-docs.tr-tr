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
ms.openlocfilehash: 81c9a94e318638837fb4ab8fe1a822dc0cfec46a
ms.sourcegitcommit: f7c401a376ce410336846835332a693e6159c551
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/14/2019
ms.locfileid: "57872762"
---
# <a name="ca2231-overload-operator-equals-on-overriding-valuetypeequals"></a>CA2231: Eşittir işlecini ValueType.Equals'ı geçersiz kılarak aşırı yükleyin

|||
|-|-|
|TypeName|OverloadOperatorEqualsOnOverridingValueTypeEquals|
|CheckId|CA2231|
|Kategori|Microsoft.Usage|
|Yeni Değişiklik|Bozucu olmayan|

## <a name="cause"></a>Sebep

Bir değer türü geçersiz kılmalar <xref:System.Object.Equals%2A?displayProperty=fullName> ama eşitlik işlecini uygulamaz.

Varsayılan olarak, bu kural yalnızca dışarıdan görülebilen türler görünür, ancak bu [yapılandırılabilir](#configurability).

## <a name="rule-description"></a>Kural açıklaması

Çoğu programlama dilinde, hiçbir varsayılan değer türleri için eşitlik operatörünün (==) uygulaması yok. İşleç aşırı yüklemeleri programlama dilini destekler, eşitlik imlecini uygulamadan düşünmelisiniz. Davranışını olarak aynı <xref:System.Object.Equals%2A>.

Eşitlik işleci aşırı yüklenmiş bir uygulamada varsayılan eşitlik işlecini kullanamazsınız. Bunun yapılması, yığın taşmasına neden olur. Eşitlik işleci uygulamak için uygulamanızda Object.Equals yöntemi kullanın. Örneğin:

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

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Bu kural ihlalini düzeltmek için eşitlik işlecini uygular.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Bu kuraldan bir uyarıyı bastırmak güvenlidir; Ancak, mümkünse eşitlik işlecini sağlamanızı öneririz.

## <a name="configurability"></a>Etkiler ve yapılandırma

Bu kuraldan çalıştırıyorsanız [FxCop Çözümleyicileri](install-fxcop-analyzers.md) (ve statik kod analizi üzerinden değil), hangi parçalarının yapılandırabilirsiniz, bu kuralı çalıştırmak için kod tabanı, kendi erişilebilirliği temel. Örneğin, kural yalnızca genel olmayan API yüzeyi karşı çalışması gerektiğini belirtmek için projenizi bir .editorconfig dosyasında şu anahtar-değer çifti ekleyin:

```
dotnet_code_quality.ca2231.api_surface = private, internal
```

Bu kategoride (kullanım), bu seçenek yalnızca bu kural, tüm kuralları veya tüm kuralları yapılandırabilirsiniz. Daha fazla bilgi için [yapılandırma FxCop Çözümleyicileri](configure-fxcop-analyzers.md).

## <a name="example"></a>Örnek

Aşağıdaki örnek bu kuralı ihlal eden bir tür tanımlar:

[!code-csharp[FxCop.Usage.EqualsGetHashCode#1](../code-quality/codesnippet/CSharp/ca2231-overload-operator-equals-on-overriding-valuetype-equals_1.cs)]

## <a name="related-rules"></a>İlgili kuralları

- [CA1046: Başvuru türlerinde eşittir işleçlerini aşırı yüklemeyin](../code-quality/ca1046-do-not-overload-operator-equals-on-reference-types.md)
- [CA2225: İşleç aşırı yüklemeleri adlandırılmış Alternatiflere sahiptir](../code-quality/ca2225-operator-overloads-have-named-alternates.md)
- [CA2226: İşleçler simetrik aşırı yüklemelere sahip olmalıdır](../code-quality/ca2226-operators-should-have-symmetrical-overloads.md)
- [CA2224: Eşittir işlecini aşırı yüklemesi üzerinde geçersiz kılma değerine eşittir](../code-quality/ca2224-override-equals-on-overloading-operator-equals.md)
- [CA2218: Gethashcode'u eşittir geçersiz kılmada geçersiz kıl](../code-quality/ca2218-override-gethashcode-on-overriding-equals.md)

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Object.Equals%2A?displayProperty=fullName>