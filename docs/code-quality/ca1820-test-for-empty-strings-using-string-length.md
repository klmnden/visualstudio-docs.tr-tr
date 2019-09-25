---
title: 'CA1820: Dize uzunluğunu kullanarak boş dizeleri test edin'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- TestForEmptyStringsUsingStringLength
- CA1820
helpviewer_keywords:
- TestForEmptyStringsUsingStringLength
- CA1820
ms.assetid: da1e70c8-b1dc-46b9-8b8f-4e6e48339681
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: b197cacc764f1f5472d3eb074ac89199db508408
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71233423"
---
# <a name="ca1820-test-for-empty-strings-using-string-length"></a>CA1820: Dize uzunluğunu kullanarak boş dizeleri test edin

|||
|-|-|
|TypeName|TestForEmptyStringsUsingStringLength|
|CheckId|CA1820|
|Kategori|Microsoft. Performance|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep

Dize, kullanılarak <xref:System.Object.Equals%2A?displayProperty=nameWithType>boş dizeyle karşılaştırılır.

## <a name="rule-description"></a>Kural açıklaması

<xref:System.String.Length%2A?displayProperty=nameWithType> Özelliği <xref:System.Object.Equals%2A>veya yöntemikullanılarakdizelerikarşılaştırmak,kullanmaktandahahızlıdır.<xref:System.String.IsNullOrEmpty%2A?displayProperty=nameWithType> Bunun nedeni <xref:System.Object.Equals%2A> , <xref:System.String.Length%2A> özellik değerini almak ve değeri sıfıra karşılaştırmak <xref:System.String.IsNullOrEmpty%2A> için yürütülen yönergelerin sayısından ya da daha fazla MSIL yönergesi yürütür.

Null dizeler <xref:System.Object.Equals%2A> için ve `<string>.Length == 0` farklı davranır. <xref:System.String.Length%2A> Özelliğin değerini null bir dizeye almaya çalışırsanız, ortak dil çalışma zamanı bir <xref:System.NullReferenceException?displayProperty=fullName>oluşturur. Null dize ve boş dize arasında bir karşılaştırma gerçekleştirirseniz, ortak dil çalışma zamanı bir özel durum oluşturmaz ve döndürür `false`. Null testi, bu iki yaklaşımın göreli performansını önemli ölçüde etkilemez. .NET Framework 2,0 veya sonraki bir sürümü hedeflerken <xref:System.String.IsNullOrEmpty%2A> yöntemini kullanın. Aksi takdirde, mümkün <xref:System.String.Length%2A> olduğunda = = 0 karşılaştırmayı kullanın.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Bu kural ihlalini onarmak için, karşılaştırma <xref:System.String.IsNullOrEmpty%2A> yöntemini metodunu kullanacak şekilde değiştirin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Performans bir sorun değilse, bu kuraldan bir uyarıyı gizlemek güvenlidir.

## <a name="example"></a>Örnek

Aşağıdaki örnek, boş bir dizeyi aramak için kullanılan farklı teknikleri gösterir.

[!code-csharp[FxCop.Performance.StringTest#1](../code-quality/codesnippet/CSharp/ca1820-test-for-empty-strings-using-string-length_1.cs)]