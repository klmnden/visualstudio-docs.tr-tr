---
title: 'CA1815: Değer türlerinde eşittir ve işleç eşittiri geçersiz kılın'
ms.date: 03/11/2019
ms.topic: reference
f1_keywords:
- CA1815
- OverrideEqualsAndOperatorEqualsOnValueTypes
helpviewer_keywords:
- OverrideEqualsAndOperatorEqualsOnValueTypes
- CA1815
ms.assetid: 0a8ab3a3-ee8e-46f7-985d-dcf00c89363b
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 97f56e406d00de1891647c4211d21336f9d1a266
ms.sourcegitcommit: 209ed0fcbb8daa1685e8d6b9a97f3857a4ce1152
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/16/2019
ms.locfileid: "69547049"
---
# <a name="ca1815-override-equals-and-operator-equals-on-value-types"></a>CA1815: Değer türlerinde eşittir ve işleç eşittiri geçersiz kılın

|||
|-|-|
|TypeName|OverrideEqualsAndOperatorEqualsOnValueTypes|
|CheckId|CA1815|
|Kategori|Microsoft. Performance|
|Yeni Değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep

Değer türü, eşitlik işleci ( <xref:System.Object.Equals%2A?displayProperty=fullName> = =) öğesini geçersiz kılmaz veya uygulamıyor. Bu kural numaralandırmalar denetlemez.

Bu kural varsayılan olarak yalnızca dışarıdan görünür türlere bakar, ancak bu [yapılandırılabilir](#configurability).

## <a name="rule-description"></a>Kural açıklaması

Değer türlerinde, devralınan uygulama <xref:System.Object.Equals%2A> yansıma kitaplığını kullanır ve tüm alanların içeriğini karşılaştırır. Yansıma hesaplama açısından pahalıdır ve her alan için eşitlik karşılaştırma gereksiz olabilir. Kullanıcıların örnekleri karşılaştırmasını veya sıralamasını veya bunları karma tablo anahtarları olarak kullanmasını bekleliyorsanız, değer türü uygulanmalıdır <xref:System.Object.Equals%2A>. Programlama diliniz işleç aşırı yüklemesini destekliyorsa eşitlik ve eşitsizlik işleçleri de bir uygulama sağlamalısınız.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Bu kural ihlalini onarmak için uygulamasının bir uygulamasını <xref:System.Object.Equals%2A>sağlayın. Mümkünse eşitlik işlecini uygulayın.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Değer türünün örnekleri birbirleriyle karşılaştırılmayacak şekilde bu kuraldan bir uyarı bastırılmak güvenlidir.

## <a name="configurability"></a>Yapılandırılabilirlik

Bu kuralı [FxCop çözümleyicilerinin](install-fxcop-analyzers.md) (eski analizler olmadan) çalıştırıyorsanız, kod tabanınızın hangi bölümlerinin bu kuralı çalıştırmak için erişilebilirliğini temel alarak yapılandırabilirsiniz. Örneğin, kuralın yalnızca genel olmayan API yüzeyine karşı çalışması gerektiğini belirtmek için, aşağıdaki anahtar-değer çiftini projenizdeki bir. editorconfig dosyasına ekleyin:

```ini
dotnet_code_quality.ca1815.api_surface = private, internal
```

Bu seçeneği yalnızca bu kural için, tüm kurallar için veya bu kategorideki tüm kurallar (performans) için yapılandırabilirsiniz. Daha fazla bilgi için bkz. [FxCop çözümleyicileri yapılandırma](configure-fxcop-analyzers.md).

## <a name="example"></a>Örnek

Aşağıdaki kod, bu kuralı ihlal eden bir yapıyı (değer türü) gösterir:

[!code-csharp[FxCop.Performance.OverrideEqualsViolation#1](../code-quality/codesnippet/CSharp/ca1815-override-equals-and-operator-equals-on-value-types_1.cs)]

Aşağıdaki kod, eşitlik işleçlerini geçersiz kılarak <xref:System.ValueType.Equals%2A?displayProperty=fullName> ve uygulayarak önceki ihlayi düzeltir (= =,! =):

[!code-csharp[FxCop.Performance.OverrideEqualsFixed#1](../code-quality/codesnippet/CSharp/ca1815-override-equals-and-operator-equals-on-value-types_2.cs)]

## <a name="related-rules"></a>İlgili kurallar

- [CA2224 Aşırı yükleme işlecinin eşittir ile eşittir geçersiz kıl](../code-quality/ca2224-override-equals-on-overloading-operator-equals.md)
- [CA2231 ValueType. Equals geçersiz kılınırken aşırı yükleme işleci Equals](../code-quality/ca2231-overload-operator-equals-on-overriding-valuetype-equals.md)
- [CA2226 İşleçler, simetrik aşırı yüklemeleri içermelidir](../code-quality/ca2226-operators-should-have-symmetrical-overloads.md)

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Object.Equals%2A?displayProperty=fullName>