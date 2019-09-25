---
title: 'CA1008: Sabit listelerinin sıfır değeri olmalıdır'
ms.date: 03/11/2019
ms.topic: reference
f1_keywords:
- CA1008
- EnumsShouldHaveZeroValue
helpviewer_keywords:
- CA1008
- EnumsShouldHaveZeroValue
ms.assetid: 3503a73c-360c-416d-8ee4-c2aa44365a05
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CPP
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: c9b6e48fb82be5a41c420827a32926630bb725ed
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71236496"
---
# <a name="ca1008-enums-should-have-zero-value"></a>CA1008: Sabit listelerinin sıfır değeri olmalıdır

|||
|-|-|
|TypeName|EnumsShouldHaveZeroValue|
|CheckId|CA1008|
|Kategori|Microsoft.Design|
|Son değişiklik|Bölünmez olmayan bir numaralandırmaya bir değer eklemeniz istendiğinde, uyarı **yok** . Parçalama-herhangi bir numaralandırma değerini yeniden adlandırmanız veya kaldırmanız istenir.|

## <a name="cause"></a>Sebep

Uygulanamayan <xref:System.FlagsAttribute?displayProperty=fullName> bir numaralandırma, sıfır değerine sahip bir üye tanımlamaz. Veya uygulanmış <xref:System.FlagsAttribute> bir numaralandırma, sıfır değerine sahip bir üyeyi tanımlar, ancak adı ' none ' değil. Ya da, sabit listesi birden çok, sıfır değerli üye tanımlıyor.

Bu kural varsayılan olarak yalnızca dışarıdan görünür numaralandırmalara bakar, ancak bu [yapılandırılabilir](#configurability).

## <a name="rule-description"></a>Kural açıklaması

Yalnızca diğer değer türleri gibi başlatılmamış bir numaralandırmanın varsayılan değeri sıfırdır. Bayraksız olmayan bir numaralandırma, varsayılan değer sabit listesinin geçerli bir değeri olacak şekilde sıfır değerine sahip bir üye tanımlamalıdır. Uygunsa, üyeyi ' none ' olarak adlandırın. Aksi takdirde, en sık kullanılan üyeye sıfır atayın. Varsayılan olarak, ilk numaralandırma üyesinin değeri bildirimde ayarlanmamışsa, değeri sıfırdır.

<xref:System.FlagsAttribute> Uygulanmış bir sabit listesi sıfır değerli bir üyeyi tanımlıyorsa, numaralandırmada hiçbir değer ayarlanamadığını göstermek için adı ' none ' olmalıdır. Başka herhangi bir amaçla sıfır değerli bir üyenin kullanılması, ve ' nin, <xref:System.FlagsAttribute> ve ve bit düzeyinde operatörlerin üye ile kullanılamaz durumda olduğu ' ın kullanımını tersine kullanır. Bu, yalnızca bir üyenin sıfır değerine atanması gerektiğini gösterir. Sıfır değerine sahip birden çok üye Flags ile Öznitelikli bir numaralandırmada gerçekleşirse, `Enum.ToString()` sıfır olmayan üyeler için hatalı sonuçlar döndürür.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Bayrak atanmış olmayan Numaralandırmalar için bu kural ihlalini onarmak için, sıfır değerine sahip bir üye tanımlayın; Bu bir kırılmamış değişiklik değildir. Sıfır değerli bir üyeyi tanımlayan bayraklarla öznitelikli Numaralandırmalar için, bu üyeyi ' none ' olarak adlandırın ve sıfır değerine sahip diğer tüm üyeleri silin; Bu, bir son değişiklik.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Daha önce sevk edilmiş bayraklarla ilişkilendirilen numaralandırmalar hariç bu kuraldan bir uyarıyı bastırmayın.

## <a name="configurability"></a>Yapılandırılabilirlik

Bu kuralı [FxCop çözümleyicilerinin](install-fxcop-analyzers.md) (eski analizler olmadan) çalıştırıyorsanız, kod tabanınızın hangi bölümlerinin bu kuralı çalıştırmak için erişilebilirliğini temel alarak yapılandırabilirsiniz. Örneğin, kuralın yalnızca genel olmayan API yüzeyine karşı çalışması gerektiğini belirtmek için, aşağıdaki anahtar-değer çiftini projenizdeki bir. editorconfig dosyasına ekleyin:

```ini
dotnet_code_quality.ca1008.api_surface = private, internal
```

Bu seçeneği yalnızca bu kural için, tüm kurallar için veya bu kategorideki tüm kurallar (tasarım) için yapılandırabilirsiniz. Daha fazla bilgi için bkz. [FxCop çözümleyicileri yapılandırma](configure-fxcop-analyzers.md).

## <a name="example"></a>Örnek

Aşağıdaki örnek, kuralı ve bir numaralandırmayı karşılayan, kuralı ihlal eden iki sabit `BadTraceOptions`listesini gösterir.

[!code-cpp[FxCop.Design.EnumsZeroValue#1](../code-quality/codesnippet/CPP/ca1008-enums-should-have-zero-value_1.cpp)]
[!code-csharp[FxCop.Design.EnumsZeroValue#1](../code-quality/codesnippet/CSharp/ca1008-enums-should-have-zero-value_1.cs)]
[!code-vb[FxCop.Design.EnumsZeroValue#1](../code-quality/codesnippet/VisualBasic/ca1008-enums-should-have-zero-value_1.vb)]

## <a name="related-rules"></a>İlgili kurallar

- [CA2217 Numaralandırmaları FlagsAttribute ile işaretlemeyin](../code-quality/ca2217-do-not-mark-enums-with-flagsattribute.md)
- [CA1700 ' Ayrılmış ' Enum değerlerini adlandırma](../code-quality/ca1700-do-not-name-enum-values-reserved.md)
- [CA1712 Tür adı ile Enum değerlerini önek olarak kullanmayın](../code-quality/ca1712-do-not-prefix-enum-values-with-type-name.md)
- [CA1028 Sabit Listesi depolaması Int32 olmalıdır](../code-quality/ca1028-enum-storage-should-be-int32.md)
- [CA1027 Numaralandırmaları FlagsAttribute ile işaretle](../code-quality/ca1027-mark-enums-with-flagsattribute.md)

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Enum?displayProperty=fullName>