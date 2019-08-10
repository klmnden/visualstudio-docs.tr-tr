---
title: "CA2218: GetHashCode'u Eşittir'i geçersiz kılarak geçersiz kılın"
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA2218
- OverrideGetHashCodeOnOverridingEquals
helpviewer_keywords:
- OverrideGetHashCodeOnOverridingEquals
- CA2218
ms.assetid: 69b020cd-29e8-45a6-952e-32cf3ce2e21d
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 5dbd8580f5aaeb88c08d35b50258510cb1a85ba2
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68920298"
---
# <a name="ca2218-override-gethashcode-on-overriding-equals"></a>CA2218: GetHashCode'u Eşittir'i geçersiz kılarak geçersiz kılın

|||
|-|-|
|TypeName|OverrideGetHashCodeOnOverridingEquals|
|CheckId|CA2218|
|Kategori|Microsoft. Usage|
|Yeni Değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep
Ortak tür geçersiz kılınır <xref:System.Object.Equals%2A?displayProperty=fullName> ancak geçersiz kılınmaz <xref:System.Object.GetHashCode%2A?displayProperty=fullName>.

## <a name="rule-description"></a>Kural açıklaması
 <xref:System.Object.GetHashCode%2A>karma algoritmalar ve karma tablo gibi veri yapıları için uygun olan geçerli örneğe bağlı olarak bir değer döndürür. Aynı türde ve eşit olan iki nesne, aşağıdaki türlerin örneklerinin doğru şekilde çalışmasını sağlamak için aynı karma kodu döndürmelidir:

- <xref:System.Collections.Hashtable?displayProperty=fullName>

- <xref:System.Collections.SortedList?displayProperty=fullName>

- <xref:System.Collections.Generic.Dictionary%602?displayProperty=fullName>

- <xref:System.Collections.Generic.SortedDictionary%602?displayProperty=fullName>

- <xref:System.Collections.Generic.SortedList%602?displayProperty=fullName>

- <xref:System.Collections.Specialized.HybridDictionary?displayProperty=fullName>

- <xref:System.Collections.Specialized.ListDictionary?displayProperty=fullName>

- <xref:System.Collections.Specialized.OrderedDictionary?displayProperty=fullName>

- Uygulayan türler<xref:System.Collections.Generic.IEqualityComparer%601?displayProperty=fullName>

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kural ihlalini onarmak için uygulamasının bir uygulamasını <xref:System.Object.GetHashCode%2A>sağlayın. Aynı türde bir nesne çifti için, bir çiftin uygulamanız <xref:System.Object.Equals%2A> için dönerse `true` uygulamanın aynı değeri döndürdüğünden emin olmanız gerekir.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bu kuraldan uyarıyı bastırmayın.

## <a name="class-example"></a>Sınıf örneği

### <a name="description"></a>Açıklama
Aşağıdaki örnek, bu kuralı ihlal eden bir sınıfı (başvuru türü) gösterir.

### <a name="code"></a>Kod
[!code-csharp[FxCop.Usage.GetHashCodeErrorClass#1](../code-quality/codesnippet/CSharp/ca2218-override-gethashcode-on-overriding-equals_1.cs)]

### <a name="comments"></a>Açıklamalar
Aşağıdaki örnek, geçersiz kılarak <xref:System.Object.GetHashCode>ihlalin düzeltir.

### <a name="code"></a>Kod
[!code-csharp[FxCop.Usage.GetHashCodeFixedClass#1](../code-quality/codesnippet/CSharp/ca2218-override-gethashcode-on-overriding-equals_2.cs)]

## <a name="structure-example"></a>Yapı örneği

### <a name="description"></a>Açıklama
Aşağıdaki örnek, bu kuralı ihlal eden bir yapıyı (değer türü) gösterir.

### <a name="code"></a>Kod
[!code-csharp[FxCop.Usage.GetHashCodeErrorStruct#1](../code-quality/codesnippet/CSharp/ca2218-override-gethashcode-on-overriding-equals_3.cs)]

### <a name="comments"></a>Açıklamalar
Aşağıdaki örnek, geçersiz kılarak <xref:System.Object.GetHashCode>ihlalin düzeltir.

### <a name="code"></a>Kod
[!code-csharp[FxCop.Usage.GetHashCodeFixedStruct#1](../code-quality/codesnippet/CSharp/ca2218-override-gethashcode-on-overriding-equals_4.cs)]

## <a name="related-rules"></a>İlgili kurallar
[CA1046 Eşittir işlecini başvuru türlerinde aşırı yüklemeyin](../code-quality/ca1046-do-not-overload-operator-equals-on-reference-types.md)

[CA2225 İşleç aşırı yüklemelerinin adlandırılmış alternatifleri var](../code-quality/ca2225-operator-overloads-have-named-alternates.md)

[CA2226 İşleçler, simetrik aşırı yüklemeleri içermelidir](../code-quality/ca2226-operators-should-have-symmetrical-overloads.md)

[CA2224 Aşırı yükleme işlecinin eşittir ile eşittir geçersiz kıl](../code-quality/ca2224-override-equals-on-overloading-operator-equals.md)

[CA2231 ValueType. Equals geçersiz kılınırken aşırı yükleme işleci Equals](../code-quality/ca2231-overload-operator-equals-on-overriding-valuetype-equals.md)

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Object.Equals%2A?displayProperty=fullName>
- <xref:System.Object.GetHashCode%2A?displayProperty=fullName>
- <xref:System.Collections.Hashtable?displayProperty=fullName>
- [Eşitlik İşleçleri](/dotnet/standard/design-guidelines/equality-operators)