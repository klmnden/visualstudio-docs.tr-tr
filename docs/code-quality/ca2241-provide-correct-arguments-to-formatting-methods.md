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
ms.openlocfilehash: f9f48f9cba146251aee1a58ffc7a3403ed899c4a
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55921503"
---
# <a name="ca2241-provide-correct-arguments-to-formatting-methods"></a>CA2241: Biçimlendirme metotlarına doğru bağımsız değişkenleri sağlayın

|||
|-|-|
|TypeName|ProvideCorrectArgumentsToFormattingMethods|
|CheckId|CA2241|
|Kategori|Microsoft.Usage|
|Yeni Değişiklik|Bozucu olmayan|

## <a name="cause"></a>Sebep
 `format` Dize gibi bir yönteme geçirilen bağımsız değişkenin <xref:System.Console.WriteLine%2A>, <xref:System.Console.Write%2A>, veya <xref:System.String.Format%2A?displayProperty=fullName> her nesne değişkeni veya tam tersi karşılık gelen bir biçim öğesi içermiyor.

## <a name="rule-description"></a>Kural açıklaması
 Gibi yöntemlerinin bağımsız değişkenleri <xref:System.Console.WriteLine%2A>, <xref:System.Console.Write%2A>, ve <xref:System.String.Format%2A> birkaç tarafından izlenen bir biçim dizesi oluşur <xref:System.Object?displayProperty=fullName> örnekleri. Biçim dizesi metin ve ekli biçim öğesi formunun oluşur {dizini [, hizalama] [: formatString]}. 'dizin' Biçimlendirilecek nesneler gösteren sıfır tabanlı bir tamsayıdır. Bir nesne Biçim dizesinde karşılık gelen bir dizin yoksa, nesne göz ardı edilir. 'Dizin' tarafından belirtilen nesnede mevcut değilse bir <xref:System.FormatException?displayProperty=fullName> çalışma zamanında oluşturulur.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Bu kural ihlalini düzeltmek için bir biçim öğesi sağlamak için her bir nesne bağımsız ve her biçim öğesi için bir nesne bağımsız değişken sağlayın.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek
 Aşağıdaki örnek, iki kural ihlalleri gösterir.

 [!code-vb[FxCop.Usage.FormattingArguments#1](../code-quality/codesnippet/VisualBasic/ca2241-provide-correct-arguments-to-formatting-methods_1.vb)]
 [!code-csharp[FxCop.Usage.FormattingArguments#1](../code-quality/codesnippet/CSharp/ca2241-provide-correct-arguments-to-formatting-methods_1.cs)]