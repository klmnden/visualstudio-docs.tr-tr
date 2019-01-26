---
title: 'CA1717: Yalnızca FlagsAttribute sabit listeleri çoğul adlara sahip olmalıdır'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
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
ms.openlocfilehash: f8fa009c93f049938a198eabd1a5dcc86a45caa7
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54957253"
---
# <a name="ca1717-only-flagsattribute-enums-should-have-plural-names"></a>CA1717: Yalnızca FlagsAttribute sabit listeleri çoğul adlara sahip olmalıdır

|||
|-|-|
|TypeName|OnlyFlagsEnumsShouldHavePluralNames|
|CheckId|CA1717|
|Kategori|Microsoft.Naming|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Dışarıdan görünen bir sabit listesi adı çoğul Word'de sona erer ve numaralandırma ile işaretlenmemiş <xref:System.FlagsAttribute?displayProperty=fullName> özniteliği.

## <a name="rule-description"></a>Kural açıklaması
 Adlandırma kuralları numaralandırma için adlandırma aynı anda birden fazla numaralandırma değeri belirtilebilir gösterir. <xref:System.FlagsAttribute> Derleyiciler sabit numaralandırma üzerinde bit düzeyinde işlemler sağlayan bir bit alanı olarak değerlendirilmesi gerektiğini söyler.

 Bir kerede tek bir numaralandırma değeri belirtilebilir yalnızca, sabit listesi adı tekil bir sözcük olmalıdır. Örneğin, Haftanın günlerinin ingilizceleridir tanımlayan bir numaralandırma kullanılmak üzere bir uygulama birden çok gün belirleyebileceğiniz ayarlanmış olabilir. Bu numaralandırma olmalıdır <xref:System.FlagsAttribute> ve 'Gün' çağrılabilir. Belirtilecek yalnızca tek bir günde izin veren benzer bir sabit listesi özniteliğine sahip değil ve olabilir 'Day' denir.

 Adlandırma kuralları, ortak dil çalışma zamanını hedefleyen kitaplıkları için genel bir bakış sağlar. Bu, yeni bir yazılım kitaplığı öğrenmek için gereklidir ve kitaplık geliştirme yönetilen kodda uzmanlığına sahip olan kişi tarafından geliştirilmiştir müşterilerinizin size olan güvenini artırır süreyi azaltır.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Sabit listesi adı tekil bir sözcük yapın veya ekleme <xref:System.FlagsAttribute>.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Tekil bir sözcük adı sona ererse kuraldan bir uyarıyı bastırmak güvenlidir.

## <a name="related-rules"></a>İlgili kuralları
 [CA1714: Bayrak numaralandırmalarında çoğul adlar olmalıdır](../code-quality/ca1714-flags-enums-should-have-plural-names.md)

 [CA1027: Sabit listelerini FlagsAttribute ile işaretleyin](../code-quality/ca1027-mark-enums-with-flagsattribute.md)

 [CA2217: Sabit listelerini FlagsAttribute ile işaretlemeyin](../code-quality/ca2217-do-not-mark-enums-with-flagsattribute.md)

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.FlagsAttribute?displayProperty=fullName>
- [Sabit Listesi Tasarımı](/dotnet/standard/design-guidelines/enum)