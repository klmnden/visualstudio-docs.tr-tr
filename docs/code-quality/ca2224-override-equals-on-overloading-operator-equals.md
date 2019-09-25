---
title: "CA2224: Eşittir işlecini aşırı yüklerken Equals'ı geçersiz kılın"
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA2224
- OverrideEqualsOnOverloadingOperatorEquals
- OverrideEqualsOnOverridingOperatorEquals
helpviewer_keywords:
- OverrideEqualsOnOverloadingOperatorEquals
- CA2224
ms.assetid: 7312afd9-84ba-417f-923e-7a159b53bf70
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 72bcf01b9c0613bb390ac9adbbba2fb176db13bd
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71231210"
---
# <a name="ca2224-override-equals-on-overloading-operator-equals"></a>CA2224: Eşittir işlecini aşırı yüklerken Equals'ı geçersiz kılın

|||
|-|-|
|TypeName|OverrideEqualsOnOverloadingOperatorEquals|
|CheckId|CA2224|
|Kategori|Microsoft. Usage|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep

Ortak tür eşitlik işlecini uygular, ancak geçersiz kılmaz <xref:System.Object.Equals%2A?displayProperty=fullName>.

## <a name="rule-description"></a>Kural açıklaması

Eşitlik işlecinin, <xref:System.Object.Equals%2A> yöntemin işlevselliğine erişmek için sözdizimsel olarak uygun bir yol olması amaçlanmıştır. Eşitlik işlecini uygularsanız, mantığı ile özdeş <xref:System.Object.Equals%2A>olmalıdır.

Kodunuz C# bu kuralı ihlal ederse derleyici bir uyarı verir.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Bu kural ihlalini onarmak için eşitlik işlecinin uygulamasını kaldırmanız veya geçersiz kılmalı <xref:System.Object.Equals%2A> ve iki yöntemin aynı değerleri döndürmesini sağlayabilirsiniz. Eşitlik işleci tutarsız bir davranış oluşturmasa, <xref:System.Object.Equals%2A> <xref:System.Object.Equals%2A> yöntemi temel sınıfta Çağıran bir uygulamasını sağlayarak ihlalin düzeltmesini çözebilirsiniz.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Eşitlik operatörü devralınan uygulamasıyla <xref:System.Object.Equals%2A>aynı değeri döndürürse, bu kuraldan bir uyarı bastırmayı güvenli hale getirmektir. Bu makaledeki örneklerde, bu kuraldan bir uyarıyı güvenle gizedebilen bir tür bulunur.

## <a name="examples-of-inconsistent-equality-definitions"></a>Tutarsız eşitlik tanımlarının örnekleri

Aşağıdaki örnekte, tutarsız bir eşitlik tanımları içeren bir tür gösterilmektedir. `BadPoint`eşitlik işlecinin özel bir uygulamasını sağlayarak eşitlik anlamını değiştirir, ancak aynı şekilde davranması için geçersiz kılmaz <xref:System.Object.Equals%2A> .

[!code-csharp[FxCop.Usage.OperatorEqualsRequiresEquals#1](../code-quality/codesnippet/CSharp/ca2224-override-equals-on-overloading-operator-equals_1.cs)]

Aşağıdaki kod davranışını `BadPoint`sınar.

[!code-csharp[FxCop.Usage.TestOperatorEqualsRequiresEquals#1](../code-quality/codesnippet/CSharp/ca2224-override-equals-on-overloading-operator-equals_2.cs)]

Bu örnek aşağıdaki çıktıyı üretir:

```txt
a =  ([0] 1,1) and b = ([1] 2,2) are equal? No
a == b ? No
a1 and a are equal? Yes
a1 == a ? Yes
b and bcopy are equal ? No
b == bcopy ? Yes
```

Aşağıdaki örnek, teknik olarak bu kuralı ihlal eden, ancak tutarsız bir şekilde davranmayan bir türü gösterir.

[!code-csharp[FxCop.Usage.ValueTypeEquals#1](../code-quality/codesnippet/CSharp/ca2224-override-equals-on-overloading-operator-equals_3.cs)]

Aşağıdaki kod davranışını `GoodPoint`sınar.

[!code-csharp[FxCop.Usage.TestValueTypeEquals#1](../code-quality/codesnippet/CSharp/ca2224-override-equals-on-overloading-operator-equals_4.cs)]

Bu örnek aşağıdaki çıktıyı üretir:

```txt
a =  (1,1) and b = (2,2) are equal? No
a == b ? No
a1 and a are equal? Yes
a1 == a ? Yes
b and bcopy are equal ? Yes
b == bcopy ? Yes
```

## <a name="class-example"></a>Sınıf örneği

Aşağıdaki örnek, bu kuralı ihlal eden bir sınıfı (başvuru türü) gösterir.

[!code-csharp[FxCop.Usage.OverrideEqualsClassViolation#1](../code-quality/codesnippet/CSharp/ca2224-override-equals-on-overloading-operator-equals_5.cs)]

Aşağıdaki örnek, geçersiz kılarak <xref:System.Object.Equals%2A?displayProperty=fullName>ihlalin düzeltir.

[!code-csharp[FxCop.Usage.OverrideEqualsClassFixed#1](../code-quality/codesnippet/CSharp/ca2224-override-equals-on-overloading-operator-equals_6.cs)]

## <a name="structure-example"></a>Yapı örneği

Aşağıdaki örnek, bu kuralı ihlal eden bir yapıyı (değer türü) gösterir:

[!code-csharp[FxCop.Usage.OverrideEqualsStructViolation#1](../code-quality/codesnippet/CSharp/ca2224-override-equals-on-overloading-operator-equals_7.cs)]

Aşağıdaki örnek, geçersiz kılarak <xref:System.ValueType.Equals%2A?displayProperty=fullName>ihlalin düzeltir.

[!code-csharp[FxCop.Usage.OverrideEqualsStructFixed#1](../code-quality/codesnippet/CSharp/ca2224-override-equals-on-overloading-operator-equals_8.cs)]

## <a name="related-rules"></a>İlgili kurallar

[CA1046 Eşittir işlecini başvuru türlerinde aşırı yüklemeyin](../code-quality/ca1046-do-not-overload-operator-equals-on-reference-types.md)

[CA2225 İşleç aşırı yüklemelerinin adlandırılmış alternatifleri var](../code-quality/ca2225-operator-overloads-have-named-alternates.md)

[CA2226 İşleçler, simetrik aşırı yüklemeleri içermelidir](../code-quality/ca2226-operators-should-have-symmetrical-overloads.md)

[CA2218 Geçersiz kılma için GetHashCode geçersiz kılma](../code-quality/ca2218-override-gethashcode-on-overriding-equals.md)

[CA2231 ValueType. Equals geçersiz kılınırken aşırı yükleme işleci Equals](../code-quality/ca2231-overload-operator-equals-on-overriding-valuetype-equals.md)