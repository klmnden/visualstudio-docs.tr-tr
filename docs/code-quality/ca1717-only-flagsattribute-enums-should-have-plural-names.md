---
title: 'CA1717: Yalnızca FlagsAttribute sabit listeleri çoğul adlara sahip olmalıdır'
ms.date: 03/11/2019
ms.topic: reference
f1_keywords:
- CA1717
- OnlyFlagsEnumsShouldHavePluralNames
helpviewer_keywords:
- OnlyFlagsEnumsShouldHavePluralNames
- CA1717
ms.assetid: a6855d8b-d78a-42c1-834e-61c31f5572ed
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 2d760802422773b3713fa7ea08ce0ce7a191f418
ms.sourcegitcommit: 209ed0fcbb8daa1685e8d6b9a97f3857a4ce1152
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/16/2019
ms.locfileid: "69547124"
---
# <a name="ca1717-only-flagsattribute-enums-should-have-plural-names"></a>CA1717: Yalnızca FlagsAttribute sabit listeleri çoğul adlara sahip olmalıdır

|||
|-|-|
|TypeName|OnlyFlagsEnumsShouldHavePluralNames|
|CheckId|CA1717|
|Kategori|Microsoft. Naming|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep

Bir numaralandırmanın adı bir plural kelimesiyle <xref:System.FlagsAttribute?displayProperty=fullName> biter ve numaralandırma özniteliğiyle işaretlenmez.

Bu kural varsayılan olarak yalnızca dışarıdan görünür numaralandırmalara bakar, ancak bu [yapılandırılabilir](#configurability).

## <a name="rule-description"></a>Kural açıklaması

Adlandırma kuralları, bir numaralandırma için çoğul adının aynı anda birden fazla sabit değer olarak belirtilebileceğini gösterir. , <xref:System.FlagsAttribute> Derleyicilerin numaralandırma üzerinde bit düzeyinde işlemler sağlayan bir bit alanı olarak değerlendirildiğini söyler.

Tek seferde bir sabit listesinin yalnızca bir değeri belirtilenebilir, numaralandırmanın adı tekil bir sözcük olmalıdır. Örneğin, haftanın günlerini tanımlayan bir numaralandırma, birden çok gün belirtebileceğiniz bir uygulamada kullanılmak üzere tasarlanmış olabilir. Bu numaralandırma, <xref:System.FlagsAttribute> ve ' Days ' olarak çağrılabilir. Yalnızca tek bir günün belirtilmesini sağlayan benzer bir numaralandırma özniteliğe sahip değildir ve ' Day ' olarak çağrılabilir.

Adlandırma kuralları, ortak dil çalışma zamanını hedefleyen kitaplıklar için ortak bir görünüm sağlar. Bu, yeni bir yazılım kitaplığı öğrenmek için gereken süreyi azaltır ve müşterinin, kitaplığın yönetilen kod geliştirme konusunda uzmanlığa sahip olan birisi tarafından geliştirildiğini arttırır.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Sabit listesinin adını tekil bir sözcük yapın veya ekleyin <xref:System.FlagsAttribute>.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Ad tekil bir sözcüğe sonlanıyorsa kuraldan bir uyarının görüntülenmesini güvenli hale gelir.

## <a name="configurability"></a>Yapılandırılabilirlik

Bu kuralı [FxCop çözümleyicilerinin](install-fxcop-analyzers.md) (eski analizler olmadan) çalıştırıyorsanız, kod tabanınızın hangi bölümlerinin bu kuralı çalıştırmak için erişilebilirliğini temel alarak yapılandırabilirsiniz. Örneğin, kuralın yalnızca genel olmayan API yüzeyine karşı çalışması gerektiğini belirtmek için, aşağıdaki anahtar-değer çiftini projenizdeki bir. editorconfig dosyasına ekleyin:

```ini
dotnet_code_quality.ca1717.api_surface = private, internal
```

Bu seçeneği yalnızca bu kural için, tüm kurallar için veya bu kategorideki tüm kurallar (adlandırma) için yapılandırabilirsiniz. Daha fazla bilgi için bkz. [FxCop çözümleyicileri yapılandırma](configure-fxcop-analyzers.md).

## <a name="related-rules"></a>İlgili kurallar

- [CA1714 Bayrak numaralandırmalarında çoğul adlar olmalıdır](../code-quality/ca1714-flags-enums-should-have-plural-names.md)
- [CA1027 Numaralandırmaları FlagsAttribute ile işaretle](../code-quality/ca1027-mark-enums-with-flagsattribute.md)
- [CA2217 Numaralandırmaları FlagsAttribute ile işaretlemeyin](../code-quality/ca2217-do-not-mark-enums-with-flagsattribute.md)

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.FlagsAttribute?displayProperty=fullName>
- [Numaralandırma tasarımı](/dotnet/standard/design-guidelines/enum)