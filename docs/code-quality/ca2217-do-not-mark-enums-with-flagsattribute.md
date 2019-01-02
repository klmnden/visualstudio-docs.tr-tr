---
title: 'CA2217: Sabit listelerini FlagsAttribute ile işaretlemeyin'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
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
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: d8afe63de8630b3fa7466e8c0784c26ba00bb1ba
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53852485"
---
# <a name="ca2217-do-not-mark-enums-with-flagsattribute"></a>CA2217: Sabit listelerini FlagsAttribute ile işaretlemeyin

|||
|-|-|
|TypeName|DoNotMarkEnumsWithFlags|
|CheckId|CA2217|
|Kategori|Microsoft.Usage|
|Yeni Değişiklik|Bozucu olmayan|

## <a name="cause"></a>Sebep

Dışarıdan görünen bir sabit listesi ile işaretlenmiş <xref:System.FlagsAttribute>, varsa ve iki ya da diğer bir birleşimini tabanların olmayan daha fazla değer tanımlı değerler sabit listesi üzerinde.

## <a name="rule-description"></a>Kural açıklaması

Bir numaralandırma olmalıdır <xref:System.FlagsAttribute> her değer numaralandırmada tanımlanan iki ya da bir birleşimini gücünden ise mevcut tanımlanan değerleri.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Bu kural ihlalini düzeltmek için kaldırmak <xref:System.FlagsAttribute> gelen sabit listesi.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Bu kuraldan uyarıyı bastırmayın.

## <a name="example-that-should-not-have-the-attribute"></a>Örnek özniteliğine sahip olmamalıdır

Aşağıdaki örnek, bir numaralandırma gösterir `Color`, 3 değeri içeren. 3 iki ya da tanımlanmış değerlerden herhangi bir kombinasyonunu güç değil. `Color` Numaralandırması ile işaretlenir olmamalıdır <xref:System.FlagsAttribute>.

[!code-cpp[FxCop.Usage.EnumNoFlags#1](../code-quality/codesnippet/CPP/ca2217-do-not-mark-enums-with-flagsattribute_1.cpp)]
[!code-csharp[FxCop.Usage.EnumNoFlags#1](../code-quality/codesnippet/CSharp/ca2217-do-not-mark-enums-with-flagsattribute_1.cs)]
[!code-vb[FxCop.Usage.EnumNoFlags#1](../code-quality/codesnippet/VisualBasic/ca2217-do-not-mark-enums-with-flagsattribute_1.vb)]

## <a name="example-that-should-have-the-attribute"></a>Örnek özniteliğine sahip olmamalıdır

Aşağıdaki örnek, bir numaralandırma gösterir `Days`, ile işaretlenen gereksinimleri karşılayan <xref:System.FlagsAttribute>.

[!code-cpp[FxCop.Usage.EnumNoFlags2#1](../code-quality/codesnippet/CPP/ca2217-do-not-mark-enums-with-flagsattribute_2.cpp)]
[!code-csharp[FxCop.Usage.EnumNoFlags2#1](../code-quality/codesnippet/CSharp/ca2217-do-not-mark-enums-with-flagsattribute_2.cs)]
[!code-vb[FxCop.Usage.EnumNoFlags2#1](../code-quality/codesnippet/VisualBasic/ca2217-do-not-mark-enums-with-flagsattribute_2.vb)]

## <a name="related-rules"></a>İlgili kuralları

[CA1027: Sabit listelerini FlagsAttribute ile işaretleyin](../code-quality/ca1027-mark-enums-with-flagsattribute.md)

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.FlagsAttribute?displayProperty=fullName>
