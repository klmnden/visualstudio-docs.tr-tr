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
ms.openlocfilehash: e6da5a791237aefa037b2cb16bffef34576ac6e7
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62545902"
---
# <a name="ca1717-only-flagsattribute-enums-should-have-plural-names"></a>CA1717: Yalnızca FlagsAttribute sabit listeleri çoğul adlara sahip olmalıdır

|||
|-|-|
|TypeName|OnlyFlagsEnumsShouldHavePluralNames|
|CheckId|CA1717|
|Kategori|Microsoft.Naming|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep

Bir sabit listesi adı çoğul Word'de sona erer ve numaralandırma ile işaretlenmemiş <xref:System.FlagsAttribute?displayProperty=fullName> özniteliği.

Varsayılan olarak, bu kural yalnızca dışarıdan görünen bir numaralandırma sırasında görünür, ancak bu [yapılandırılabilir](#configurability).

## <a name="rule-description"></a>Kural açıklaması

Adlandırma kuralları numaralandırma için adlandırma aynı anda birden fazla numaralandırma değeri belirtilebilir gösterir. <xref:System.FlagsAttribute> Derleyiciler sabit numaralandırma üzerinde bit düzeyinde işlemler sağlayan bir bit alanı olarak değerlendirilmesi gerektiğini söyler.

Bir kerede tek bir numaralandırma değeri belirtilebilir yalnızca, sabit listesi adı tekil bir sözcük olmalıdır. Örneğin, Haftanın günlerinin ingilizceleridir tanımlayan bir numaralandırma kullanılmak üzere bir uygulama birden çok gün belirleyebileceğiniz ayarlanmış olabilir. Bu numaralandırma olmalıdır <xref:System.FlagsAttribute> ve 'Gün' çağrılabilir. Belirtilecek yalnızca tek bir günde izin veren benzer bir sabit listesi özniteliğine sahip değil ve olabilir 'Day' denir.

Adlandırma kuralları, ortak dil çalışma zamanını hedefleyen kitaplıkları için genel bir bakış sağlar. Bu, yeni bir yazılım kitaplığı öğrenmek için gereklidir ve kitaplık geliştirme yönetilen kodda uzmanlığına sahip olan kişi tarafından geliştirilmiştir müşterilerinizin size olan güvenini artırır süreyi azaltır.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Sabit listesi adı tekil bir sözcük yapın veya ekleme <xref:System.FlagsAttribute>.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Tekil bir sözcük adı sona ererse kuraldan bir uyarıyı bastırmak güvenlidir.

## <a name="configurability"></a>Etkiler ve yapılandırma

Bu kuraldan çalıştırıyorsanız [FxCop Çözümleyicileri](install-fxcop-analyzers.md) (ve statik kod analizi üzerinden değil), hangi parçalarının yapılandırabilirsiniz, bu kuralı çalıştırmak için kod tabanı, kendi erişilebilirliği temel. Örneğin, kural yalnızca genel olmayan API yüzeyi karşı çalışması gerektiğini belirtmek için projenizi bir .editorconfig dosyasında şu anahtar-değer çifti ekleyin:

```
dotnet_code_quality.ca1717.api_surface = private, internal
```

Bu kategoride (adlandırma), bu seçenek yalnızca bu kural, tüm kuralları veya tüm kuralları yapılandırabilirsiniz. Daha fazla bilgi için [yapılandırma FxCop Çözümleyicileri](configure-fxcop-analyzers.md).

## <a name="related-rules"></a>İlgili kuralları

- [CA1714: Bayrak numaralandırmalarında çoğul adlar olmalıdır](../code-quality/ca1714-flags-enums-should-have-plural-names.md)
- [CA1027: Sabit listelerini FlagsAttribute ile işaretleyin](../code-quality/ca1027-mark-enums-with-flagsattribute.md)
- [CA2217: Sabit listelerini FlagsAttribute ile işaretlemeyin](../code-quality/ca2217-do-not-mark-enums-with-flagsattribute.md)

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.FlagsAttribute?displayProperty=fullName>
- [Sabit listesi tasarımı](/dotnet/standard/design-guidelines/enum)