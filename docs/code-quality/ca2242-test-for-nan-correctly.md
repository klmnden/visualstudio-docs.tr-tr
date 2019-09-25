---
title: 'CA2242: NaN için doğru test edin'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- TestForNaNCorrectly
- CA2242
helpviewer_keywords:
- CA2242
ms.assetid: e12dcffc-e255-4e1e-8fdf-3c6054d44abe
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: 0e74ec49667a4fe66c399bd15e8b24aa6589ce88
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71237837"
---
# <a name="ca2242-test-for-nan-correctly"></a>CA2242: NaN için doğru test edin

|||
|-|-|
|TypeName|TestForNaNCorrectly|
|CheckId|CA2242|
|Kategori|Microsoft. Usage|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep
Bir ifade, veya <xref:System.Single.NaN?displayProperty=fullName> <xref:System.Double.NaN?displayProperty=fullName>ile karşılaştırarak bir değeri sınar.

## <a name="rule-description"></a>Kural açıklaması
 <xref:System.Double.NaN?displayProperty=fullName>, bir sayı değil, bir aritmetik işlem tanımsız olduğunda sonuçları gösterir. Bir değer ile <xref:System.Double.NaN?displayProperty=fullName> her zaman geri dönüş `false`arasındaki eşitliği test eden herhangi bir ifade. Bir değer ile <xref:System.Double.NaN?displayProperty=fullName> `true`her zaman arasında eşitsizlik test eden herhangi bir ifade.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kuralın ihlalini onarmak ve değerin temsil <xref:System.Double.NaN?displayProperty=fullName>edilip edilmeyeceğini doğru bir şekilde tespit etmek için, değerini kullanın <xref:System.Single.IsNaN%2A?displayProperty=fullName> veya <xref:System.Double.IsNaN%2A?displayProperty=fullName> test edin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek
Aşağıdaki örnek, bir değeri <xref:System.Double.NaN?displayProperty=fullName> yanlış test eden iki ifadeyi ve değeri sınamak için doğru şekilde kullanılan <xref:System.Double.IsNaN%2A?displayProperty=fullName> bir ifadeyi gösterir.

[!code-vb[FxCop.Usage.TestForNaN#1](../code-quality/codesnippet/VisualBasic/ca2242-test-for-nan-correctly_1.vb)]
[!code-csharp[FxCop.Usage.TestForNaN#1](../code-quality/codesnippet/CSharp/ca2242-test-for-nan-correctly_1.cs)]