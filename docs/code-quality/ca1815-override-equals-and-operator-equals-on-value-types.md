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
ms.openlocfilehash: 1c4cf84a292e11b20eb37bee562cd039096e56af
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62545312"
---
# <a name="ca1815-override-equals-and-operator-equals-on-value-types"></a>CA1815: Değer türlerinde eşittir ve işleç eşittiri geçersiz kılın

|||
|-|-|
|TypeName|OverrideEqualsAndOperatorEqualsOnValueTypes|
|CheckId|CA1815|
|Kategori|Microsoft.Performance|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep

Bir değer türü geçersiz <xref:System.Object.Equals%2A?displayProperty=fullName> veya eşitlik operatörünün (==) uygulamıyor. Bu kural, sabit listeleri denetlemez.

Varsayılan olarak, bu kural yalnızca dışarıdan görülebilen türler görünür, ancak bu [yapılandırılabilir](#configurability).

## <a name="rule-description"></a>Kural açıklaması

Değer türleri için ' ın devralınmış uygulaması <xref:System.Object.Equals%2A> Reflection kitaplığını kullanır ve tüm alanların içeriğini karşılaştırır. Yansıma hesaplama açısından pahalıdır ve her alan için eşitlik karşılaştırma gereksiz olabilir. Karşılaştırma ya da sıralama örnekleri için kullanıcıların ya da tablo anahtarlarını karma olarak kullandığınız, değer türünüz uygulamalıdır <xref:System.Object.Equals%2A>. İşleç aşırı yüklemesi programlama dilini destekler, ayrıca eşitlik ve eşitsizlik işleci bir uygulama sağlamalıdır.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Bu kural ihlalini düzeltmek için bir uygulamasını sağlamak <xref:System.Object.Equals%2A>. Mümkünse, eşitlik işlecini uygular.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Değer türü örneklerini birbirine karşılaştırılmayacak varsa bu kuraldan bir uyarıyı bastırmak güvenlidir.

## <a name="configurability"></a>Etkiler ve yapılandırma

Bu kuraldan çalıştırıyorsanız [FxCop Çözümleyicileri](install-fxcop-analyzers.md) (ve statik kod analizi üzerinden değil), hangi parçalarının yapılandırabilirsiniz, bu kuralı çalıştırmak için kod tabanı, kendi erişilebilirliği temel. Örneğin, kural yalnızca genel olmayan API yüzeyi karşı çalışması gerektiğini belirtmek için projenizi bir .editorconfig dosyasında şu anahtar-değer çifti ekleyin:

```
dotnet_code_quality.ca1815.api_surface = private, internal
```

Bu kategoride (performans), bu seçenek yalnızca bu kural, tüm kuralları veya tüm kuralları yapılandırabilirsiniz. Daha fazla bilgi için [yapılandırma FxCop Çözümleyicileri](configure-fxcop-analyzers.md).

## <a name="example"></a>Örnek

Aşağıdaki kod bu kuralı ihlal eden bir yapı (değer türü) göstermektedir:

[!code-csharp[FxCop.Performance.OverrideEqualsViolation#1](../code-quality/codesnippet/CSharp/ca1815-override-equals-and-operator-equals-on-value-types_1.cs)]

Aşağıdaki kod önceki ihlali geçersiz kılarak düzeltmeleri <xref:System.ValueType.Equals%2A?displayProperty=fullName> ve eşitlik işleçleri (==,! =):

[!code-csharp[FxCop.Performance.OverrideEqualsFixed#1](../code-quality/codesnippet/CSharp/ca1815-override-equals-and-operator-equals-on-value-types_2.cs)]

## <a name="related-rules"></a>İlgili kuralları

- [CA2224: Eşittir işlecini aşırı yüklemesi üzerinde geçersiz kılma değerine eşittir](../code-quality/ca2224-override-equals-on-overloading-operator-equals.md)
- [CA2231: Eşittir işlecini ValueType.equals'ı geçersiz kılarak üzerinde](../code-quality/ca2231-overload-operator-equals-on-overriding-valuetype-equals.md)
- [CA2226: İşleçler simetrik aşırı yüklemelere sahip olmalıdır](../code-quality/ca2226-operators-should-have-symmetrical-overloads.md)

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Object.Equals%2A?displayProperty=fullName>