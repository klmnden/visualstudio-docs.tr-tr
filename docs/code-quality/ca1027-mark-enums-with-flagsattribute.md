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
ms.openlocfilehash: acdb8406d43f90414cf255abae6f1ca5f549e92e
ms.sourcegitcommit: 2ee11676af4f3fc5729934d52541e9871fb43ee9
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/17/2019
ms.locfileid: "65842478"
---
# <a name="ca1027-mark-enums-with-flagsattribute"></a>CA1027: Sabit listelerini FlagsAttribute ile işaretleyin

|||
|-|-|
|TypeName|MarkEnumsWithFlags|
|CheckId|CA1027|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep

Bir numaralandırma değerlerini iki powers veya numaralandırmada tanımlanan diğer değerleri birleşimlerini ve <xref:System.FlagsAttribute?displayProperty=fullName> özniteliği mevcut değil. Hatalı pozitif sonuçları azaltmak için bu kuralı ihlal bitişik değerlere sahip sabit listeleri için raporlamaz.

Varsayılan olarak, bu kural ortak numaralandırmalar yalnızca görünür, ancak bu [yapılandırılabilir](#configurability).

## <a name="rule-description"></a>Kural açıklaması

Bir numaralandırma ilişkili adlandırılmış sabitler kümesini tanımlayan değer türüdür. Uygulama <xref:System.FlagsAttribute> anlamsız atayamayacağına birleştirilebilir, bir sabit listesi. Örneğin, bir uygulamada hangi günün kaynaklar kullanılabilir izler haftanın günlerini numaralandırması göz önünde bulundurun. Her kaynak kullanılabilirliğini sahip numaralandırma kullanılarak kodlanır <xref:System.FlagsAttribute> yoksa, herhangi bir birleşimini gün gösterilebileceği. Öznitelik olmadan, yalnızca haftanın bir gününü temsil edilebilir.

Combinable numaralandırmalar depolama alanları için tek tek numaralandırma değerlerinin bit alanına grupları olarak kabul edilir. Bu nedenle, bu tür alanlar olarak da adlandırılır *bit alanları*. Numaralandırma değerlerinin bit alanı depolama birleştirmek için koşullu Boole işleçlerini kullanın. Bir bit alanı, belirli bir sabit listesi değeri mevcut olup olmadığını belirlemek için test etmek için Boolean mantıksal işleçleri kullanın. Bir bit alanı birleşik numaralandırma değerlerinin doğru şekilde depolanıp numaralandırmada tanımlanan her bir değeri ikinin üssü olmalıdır. Bu olmadığı sürece, Boolean mantıksal işleçler alanında depolanan tek bir sabit listesi değerlerini ayıklamak mümkün olmayacaktır.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Bu kural ihlalini düzeltmek için ekleme <xref:System.FlagsAttribute> için sabit listesi.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Numaralandırma değerlerinin combinable olmasını istemiyorsanız bu kuraldan bir uyarıyı gizler.

## <a name="configurability"></a>Etkiler ve yapılandırma

Bu kuraldan çalıştırıyorsanız [FxCop Çözümleyicileri](install-fxcop-analyzers.md) (ve statik kod analizi üzerinden değil), hangi parçalarının yapılandırabilirsiniz, bu kuralı çalıştırmak için kod tabanı, kendi erişilebilirliği temel. Örneğin, kural yalnızca genel olmayan API yüzeyi karşı çalışması gerektiğini belirtmek için projenizi bir .editorconfig dosyasında şu anahtar-değer çifti ekleyin:

```ini
dotnet_code_quality.ca1027.api_surface = private, internal
```

Bu kategoride (tasarımı), bu seçenek yalnızca bu kural, tüm kuralları veya tüm kuralları yapılandırabilirsiniz. Daha fazla bilgi için [yapılandırma FxCop Çözümleyicileri](configure-fxcop-analyzers.md).

## <a name="example"></a>Örnek

Aşağıdaki örnekte, `DaysEnumNeedsFlags` kullanma gereksinimleri karşılayan bir sabit listesidir <xref:System.FlagsAttribute> yok ancak. `ColorEnumShouldNotHaveFlag` Numaralandırma powers iki olan değerleri yok, ancak yanlış belirtir <xref:System.FlagsAttribute>. Bu kuralı ihlal ediyor [CA2217: Sabit listelerini FlagsAttribute ile işaretlemeyin](../code-quality/ca2217-do-not-mark-enums-with-flagsattribute.md).

[!code-csharp[FxCop.Design.EnumFlags#1](../code-quality/codesnippet/CSharp/ca1027-mark-enums-with-flagsattribute_1.cs)]

## <a name="related-rules"></a>İlgili kuralları

- [CA2217: Sabit listelerini FlagsAttribute ile işaretlemeyin](../code-quality/ca2217-do-not-mark-enums-with-flagsattribute.md)

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.FlagsAttribute?displayProperty=fullName>