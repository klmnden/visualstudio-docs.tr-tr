---
title: 'CA1027: Sabit listelerini FlagsAttribute ile işaretleyin'
ms.date: 03/11/2019
ms.topic: reference
f1_keywords:
- MarkEnumsWithFlags
- CA1027
helpviewer_keywords:
- CA1027
- MarkEnumsWithFlags
ms.assetid: 249e882c-8cd1-4c00-a2de-7b6bdc1849ff
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 8375d2096417948b19a228d8a4f02accac7c0b5f
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71236122"
---
# <a name="ca1027-mark-enums-with-flagsattribute"></a>CA1027: Sabit listelerini FlagsAttribute ile işaretleyin

|||
|-|-|
|TypeName|MarkEnumsWithFlags|
|CheckId|CA1027|
|Kategori|Microsoft.Design|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep

Bir numaralandırmanın değerleri ikinin üsleridir ve numaralandırmada tanımlanan diğer değerlerin birleşimleridir ve <xref:System.FlagsAttribute?displayProperty=fullName> öznitelik mevcut değildir. Hatalı pozitif sonuçları azaltmak için, bu kural bitişik değerleri olan Numaralandırmalar için bir ihlal raporlamaz.

Varsayılan olarak, bu kural yalnızca genel numaralandırmalara bakar, ancak bu [yapılandırılabilir](#configurability).

## <a name="rule-description"></a>Kural açıklaması

Bir numaralandırma ilişkili adlandırılmış sabitler kümesini tanımlayan değer türüdür. Adlandırılmış <xref:System.FlagsAttribute> sabitleri anlamlı bir şekilde birleştirilebilecek bir numaralandırmaya Uygula. Örneğin, bir uygulamadaki haftanın günleri, hangi gün kaynakların kullanılabilir olduğunu izleyen bir sabit listesini göz önünde bulundurun. Her bir kaynağın kullanılabilirliği, <xref:System.FlagsAttribute> mevcut olan numaralandırma kullanılarak kodlanmışsa, tüm gün bileşimleri temsil edilebilir. Özniteliği olmadan haftanın yalnızca bir günü temsil edilebilir.

Combinable numaralandırmaları depolayan alanlar için, tek tek numaralandırma değerleri alanındaki bit grupları olarak değerlendirilir. Bu nedenle, bu tür alanlar bazen *bit alanları*olarak adlandırılır. Bir bit alanındaki depolama için numaralandırma değerlerini birleştirmek için, Boole koşullu işleçlerini kullanın. Belirli bir numaralandırma değerinin var olup olmadığını anlamak üzere bir bit alanını test etmek için, Boole mantıksal işleçlerini kullanın. Bir bit alanının birleştirilmiş numaralandırma değerlerini doğru bir şekilde depolaması ve alması için, numaralandırmada tanımlanan her bir değer ikisinin bir üssü olmalıdır. Bu nedenle, Boolean mantıksal işleçler alanda depolanan bireysel numaralandırma değerlerini ayıklayamayacak.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Bu kuralın ihlalini onarmak için, numaralandırmaya ekleyin <xref:System.FlagsAttribute> .

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Numaralandırma değerlerinin combinable olmasını istemiyorsanız bu kuraldan bir uyarı gizleyin.

## <a name="configurability"></a>Yapılandırılabilirlik

Bu kuralı [FxCop çözümleyicilerinin](install-fxcop-analyzers.md) (eski analizler olmadan) çalıştırıyorsanız, kod tabanınızın hangi bölümlerinin bu kuralı çalıştırmak için erişilebilirliğini temel alarak yapılandırabilirsiniz. Örneğin, kuralın yalnızca genel olmayan API yüzeyine karşı çalışması gerektiğini belirtmek için, aşağıdaki anahtar-değer çiftini projenizdeki bir. editorconfig dosyasına ekleyin:

```ini
dotnet_code_quality.ca1027.api_surface = private, internal
```

Bu seçeneği yalnızca bu kural için, tüm kurallar için veya bu kategorideki tüm kurallar (tasarım) için yapılandırabilirsiniz. Daha fazla bilgi için bkz. [FxCop çözümleyicileri yapılandırma](configure-fxcop-analyzers.md).

## <a name="example"></a>Örnek

Aşağıdaki örnekte, `DaysEnumNeedsFlags` kullanma <xref:System.FlagsAttribute> gereksinimlerini karşılayan ancak içermeyen bir numaralandırmadır. Numaralandırmada iki üsleri olan ancak yanlış bir şekilde belirten <xref:System.FlagsAttribute>değer yok. `ColorEnumShouldNotHaveFlag` Bu, CA2217 [kuralını ihlal ediyor: Numaralandırmaları FlagsAttribute](../code-quality/ca2217-do-not-mark-enums-with-flagsattribute.md)ile işaretlemeyin.

[!code-csharp[FxCop.Design.EnumFlags#1](../code-quality/codesnippet/CSharp/ca1027-mark-enums-with-flagsattribute_1.cs)]

## <a name="related-rules"></a>İlgili kurallar

- [CA2217 Numaralandırmaları FlagsAttribute ile işaretlemeyin](../code-quality/ca2217-do-not-mark-enums-with-flagsattribute.md)

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.FlagsAttribute?displayProperty=fullName>