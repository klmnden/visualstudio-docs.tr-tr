---
title: 'CA1714: Bayrak sabit listeleri çoğul adlara sahip olmalıdır'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- FlagsEnumsShouldHavePluralNames
- CA1714
helpviewer_keywords:
- CA1714
- FlagsEnumsShouldHavePluralNames
ms.assetid: 95ef5b43-7681-49e9-a5a3-ac0357cf1be7
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 512e66c65cb3abd0b5e56f268b9a89e4d51758bf
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55953918"
---
# <a name="ca1714-flags-enums-should-have-plural-names"></a>CA1714: Bayrak sabit listeleri çoğul adlara sahip olmalıdır

|||
|-|-|
|TypeName|FlagsEnumsShouldHavePluralNames|
|CheckId|CA1714|
|Kategori|Microsoft.Naming|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Ortak bir numaralandırma olan <xref:System.FlagsAttribute?displayProperty=fullName> ve adını bitmeyen içinde 's'.

## <a name="rule-description"></a>Kural açıklaması
 İle işaretlenmiş türler <xref:System.FlagsAttribute> öznitelik birden fazla değer belirtilebilir, çünkü çoğul adları vardır. Örneğin, Haftanın günlerinin ingilizceleridir tanımlayan bir numaralandırma kullanılmak üzere bir uygulama birden çok gün belirleyebileceğiniz ayarlanmış olabilir. Bu numaralandırma olmalıdır <xref:System.FlagsAttribute> ve 'Gün' çağrılabilir. Belirtilecek yalnızca tek bir günde izin veren benzer bir sabit listesi özniteliğine sahip değil ve olabilir 'Day' denir.

 Adlandırma kuralları, ortak dil çalışma zamanını hedefleyen kitaplıkları için genel bir bakış sağlar. Bu, yeni yazılım kitaplıkları için gereklidir ve kitaplık geliştirme yönetilen kodda uzmanlığına sahip olan kişi tarafından geliştirilmiştir müşterilerinizin size olan güvenini artırır öğrenme eğrisini azaltır.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Sabit listesi adı çoğul bir sözcük olun ya da kaldırma <xref:System.FlagsAttribute> özniteliği birden fazla numaralandırma değerlerinin aynı anda belirtilmemelidir.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Adın çoğul bir sözcük ancak bitmiyor ihlalinin bastırmak güvenlidir 's'. Örneğin, 'DaysOfTheWeek' daha önce açıklanan birden çok günü numaralandırma adlandırılmışsa, bu kural ancak konuşmanın niyetini mantığını ihlal ediyor. Bu tür ihlalleri atlanması.

## <a name="related-rules"></a>İlgili kuralları
 [CA1027: Sabit listelerini FlagsAttribute ile işaretleyin](../code-quality/ca1027-mark-enums-with-flagsattribute.md)

 [CA2217: Sabit listelerini FlagsAttribute ile işaretlemeyin](../code-quality/ca2217-do-not-mark-enums-with-flagsattribute.md)

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.FlagsAttribute?displayProperty=fullName>
- [Sabit Listesi Tasarımı](/dotnet/standard/design-guidelines/enum)