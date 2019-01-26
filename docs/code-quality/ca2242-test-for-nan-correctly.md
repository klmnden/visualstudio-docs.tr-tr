---
title: 'CA2242: NaN için doğru test edin'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
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
ms.openlocfilehash: 671febac88142159b89f0888dead24605cbc0caa
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54991755"
---
# <a name="ca2242-test-for-nan-correctly"></a>CA2242: NaN için doğru test edin

|||
|-|-|
|TypeName|TestForNaNCorrectly|
|CheckId|CA2242|
|Kategori|Microsoft.Usage|
|Yeni Değişiklik|Bozucu olmayan|

## <a name="cause"></a>Sebep
 Bir ifade bir değer karşı sınar <xref:System.Single.NaN?displayProperty=fullName> veya <xref:System.Double.NaN?displayProperty=fullName>.

## <a name="rule-description"></a>Kural açıklaması
 <xref:System.Double.NaN?displayProperty=fullName>, temsil ettiği bir sayı değil, bir aritmetik işlemi tanımlanmamış olduğunda oluşur. Bir değer arasındaki eşitliği sınar herhangi bir ifade ve <xref:System.Double.NaN?displayProperty=fullName> her zaman döndürür `false`. Bir değer arasındaki eşitsizliği sınar herhangi bir ifade ve <xref:System.Double.NaN?displayProperty=fullName> her zaman döndürür `true`.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Bu kural ihlalini düzeltmek ve doğru bir şekilde bir değeri temsil edip etmediğini belirlemek için <xref:System.Double.NaN?displayProperty=fullName>, kullanın <xref:System.Single.IsNaN%2A?displayProperty=fullName> veya <xref:System.Double.IsNaN%2A?displayProperty=fullName> değerini test etmek için.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek
 Aşağıdaki örnek, yanlış bir değer karşı test iki ifadeleri gösterir <xref:System.Double.NaN?displayProperty=fullName> ve doğru şekilde kullanan bir ifade <xref:System.Double.IsNaN%2A?displayProperty=fullName> değerini test etmek için.

 [!code-vb[FxCop.Usage.TestForNaN#1](../code-quality/codesnippet/VisualBasic/ca2242-test-for-nan-correctly_1.vb)]
 [!code-csharp[FxCop.Usage.TestForNaN#1](../code-quality/codesnippet/CSharp/ca2242-test-for-nan-correctly_1.cs)]