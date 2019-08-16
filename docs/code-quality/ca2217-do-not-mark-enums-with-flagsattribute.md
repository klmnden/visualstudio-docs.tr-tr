---
title: 'CA2217: Sabit listelerini FlagsAttribute ile işaretlemeyin'
ms.date: 03/11/2019
ms.topic: reference
f1_keywords:
- DoNotMarkEnumsWithFlags
- CA2217
helpviewer_keywords:
- DoNotMarkEnumsWithFlags
- CA2217
dev_langs:
- VB
- CSharp
- CPP
ms.assetid: 1b6f626c-66bf-45b0-a3e2-7c41ee9ceda7
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 377188183acdaa9aa86ae3344c8f6d5727b82ccc
ms.sourcegitcommit: 209ed0fcbb8daa1685e8d6b9a97f3857a4ce1152
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/16/2019
ms.locfileid: "69546844"
---
# <a name="ca2217-do-not-mark-enums-with-flagsattribute"></a>CA2217: Sabit listelerini FlagsAttribute ile işaretlemeyin

|||
|-|-|
|TypeName|DoNotMarkEnumsWithFlags|
|CheckId|CA2217|
|Kategori|Microsoft. Usage|
|Yeni Değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep

Sabit listesi ile <xref:System.FlagsAttribute> işaretlenir ve Numaralandırmadaki iki ya da daha fazla değere sahip olan bir veya daha fazla değere sahip olur.

Bu kural varsayılan olarak yalnızca dışarıdan görünür numaralandırmalara bakar, ancak bu [yapılandırılabilir](#configurability).

## <a name="rule-description"></a>Kural açıklaması

Sabit listesi <xref:System.FlagsAttribute> yalnızca numaralandırmada tanımlanan her bir değer iki ya da tanımlı değerlerden oluşan bir kuvvetle birlikte bulunmalıdır.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Bu kuralın ihlalini onarmak için, Numaralandırmadaki <xref:System.FlagsAttribute> kaldırın.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Bu kuraldan uyarıyı bastırmayın.

## <a name="configurability"></a>Yapılandırılabilirlik

Bu kuralı [FxCop çözümleyicilerinin](install-fxcop-analyzers.md) (eski analizler olmadan) çalıştırıyorsanız, kod tabanınızın hangi bölümlerinin bu kuralı çalıştırmak için erişilebilirliğini temel alarak yapılandırabilirsiniz. Örneğin, kuralın yalnızca genel olmayan API yüzeyine karşı çalışması gerektiğini belirtmek için, aşağıdaki anahtar-değer çiftini projenizdeki bir. editorconfig dosyasına ekleyin:

```ini
dotnet_code_quality.ca2217.api_surface = private, internal
```

Bu seçeneği yalnızca bu kural için, tüm kurallar için veya bu kategorideki tüm kurallar (kullanım) için yapılandırabilirsiniz. Daha fazla bilgi için bkz. [FxCop çözümleyicileri yapılandırma](configure-fxcop-analyzers.md).

## <a name="examples"></a>Örnekler

Aşağıdaki kod, 3 değerini içeren bir `Color`numaralandırma gösterir. 3 iki üssü veya tanımlanmış değerlerden herhangi birinin bir bileşimini değil. Sabit listesi ile <xref:System.FlagsAttribute>işaretlenmemelidir. `Color`

[!code-cpp[FxCop.Usage.EnumNoFlags#1](../code-quality/codesnippet/CPP/ca2217-do-not-mark-enums-with-flagsattribute_1.cpp)]
[!code-csharp[FxCop.Usage.EnumNoFlags#1](../code-quality/codesnippet/CSharp/ca2217-do-not-mark-enums-with-flagsattribute_1.cs)]
[!code-vb[FxCop.Usage.EnumNoFlags#1](../code-quality/codesnippet/VisualBasic/ca2217-do-not-mark-enums-with-flagsattribute_1.vb)]

Aşağıdaki kod, ile `Days` <xref:System.FlagsAttribute>işaretlenmekte olan gereksinimleri karşılayan bir sabit listesini gösterir:

[!code-cpp[FxCop.Usage.EnumNoFlags2#1](../code-quality/codesnippet/CPP/ca2217-do-not-mark-enums-with-flagsattribute_2.cpp)]
[!code-csharp[FxCop.Usage.EnumNoFlags2#1](../code-quality/codesnippet/CSharp/ca2217-do-not-mark-enums-with-flagsattribute_2.cs)]
[!code-vb[FxCop.Usage.EnumNoFlags2#1](../code-quality/codesnippet/VisualBasic/ca2217-do-not-mark-enums-with-flagsattribute_2.vb)]

## <a name="related-rules"></a>İlgili kurallar

[CA1027 Numaralandırmaları FlagsAttribute ile işaretle](../code-quality/ca1027-mark-enums-with-flagsattribute.md)

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.FlagsAttribute?displayProperty=fullName>
