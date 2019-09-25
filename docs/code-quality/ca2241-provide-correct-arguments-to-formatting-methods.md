---
title: 'CA2241: Biçimlendirme metotlarına doğru bağımsız değişkenleri sağlayın'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA2241
- Provide correct arguments to formatting methods
- ProvideCorrectArgumentsToFormattingMethods
helpviewer_keywords:
- ProvideCorrectArgumentsToFormattingMethods
- CA2241
ms.assetid: 83639bc4-4c91-4a07-a40e-dc5e49a84494
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: 3767d361375ce1b3d54281a6850d9ac3b960ece6
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71237862"
---
# <a name="ca2241-provide-correct-arguments-to-formatting-methods"></a>CA2241: Biçimlendirme metotlarına doğru bağımsız değişkenleri sağlayın

|||
|-|-|
|TypeName|ProvideCorrectArgumentsToFormattingMethods|
|CheckId|CA2241|
|Kategori|Microsoft. Usage|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep
, `format` <xref:System.Console.WriteLine%2A> ,Veya<xref:System.String.Format%2A?displayProperty=fullName> gibi bir yönteme geçirilen dize bağımsız değişkeni, her bir nesne bağımsız değişkenine karşılık gelen bir biçim öğesi içermez veya tam tersi de geçerlidir. <xref:System.Console.Write%2A>

## <a name="rule-description"></a>Kural açıklaması
, <xref:System.Console.WriteLine%2A> <xref:System.Object?displayProperty=fullName> Ve gibi<xref:System.String.Format%2A> yöntemlere yönelik bağımsız değişkenler, ardından birkaç örnek tarafından bir biçim dizesi oluşur. <xref:System.Console.Write%2A> Biçim dizesi, {index [, hizalama] [: formatString]} biçiminde metin ve katıştırılmış biçim öğelerinden oluşur. ' index ', hangi nesnelerden biçimlendirileceğini gösteren sıfır tabanlı bir tamsayıdır. Bir nesne, biçim dizesinde karşılık gelen bir dizin içermiyorsa, nesne yok sayılır. ' İndex ' tarafından belirtilen nesne yoksa, çalışma zamanında bir <xref:System.FormatException?displayProperty=fullName> oluşturulur.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kural ihlalini onarmak için her bir nesne bağımsız değişkeni için bir biçim öğesi sağlayın ve her biçim öğesi için bir nesne bağımsız değişkeni sağlayın.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek
Aşağıdaki örnek, kuralın iki ihlalini gösterir.

[!code-vb[FxCop.Usage.FormattingArguments#1](../code-quality/codesnippet/VisualBasic/ca2241-provide-correct-arguments-to-formatting-methods_1.vb)]
[!code-csharp[FxCop.Usage.FormattingArguments#1](../code-quality/codesnippet/CSharp/ca2241-provide-correct-arguments-to-formatting-methods_1.cs)]