---
title: 'CA2242: NaN için doğru sınayın | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- TestForNaNCorrectly
- CA2242
helpviewer_keywords:
- CA2242
ms.assetid: e12dcffc-e255-4e1e-8fdf-3c6054d44abe
caps.latest.revision: 13
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 17a98ce3d213c5d9ae85bb5132a0a44e50112037
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68142352"
---
# <a name="ca2242-test-for-nan-correctly"></a>CA2242: NaN için doğru test edin
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|TestForNaNCorrectly|
|CheckId|CA2242|
|Kategori|Microsoft.Usage|
|Yeni Değişiklik|Bozucu olmayan|

## <a name="cause"></a>Sebep
 Bir ifade bir değer karşı sınar <xref:System.Single.NaN?displayProperty=fullName> veya <xref:System.Double.NaN?displayProperty=fullName>.

## <a name="rule-description"></a>Kural Tanımı
 <xref:System.Double.NaN?displayProperty=fullName>, temsil ettiği bir sayı değil, bir aritmetik işlemi tanımlanmamış olduğunda oluşur. Bir değer arasındaki eşitliği sınar herhangi bir ifade ve <xref:System.Double.NaN?displayProperty=fullName> her zaman döndürür `false`. Bir değer arasındaki eşitsizliği sınar herhangi bir ifade ve <xref:System.Double.NaN?displayProperty=fullName> her zaman döndürür `true`.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek ve doğru bir şekilde bir değeri temsil edip etmediğini belirlemek için <xref:System.Double.NaN?displayProperty=fullName>, kullanın <xref:System.Single.IsNaN%2A?displayProperty=fullName> veya <xref:System.Double.IsNaN%2A?displayProperty=fullName> değerini test etmek için.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek
 Aşağıdaki örnek, yanlış bir değer karşı test iki ifadeleri gösterir <xref:System.Double.NaN?displayProperty=fullName> ve doğru şekilde kullanan bir ifade <xref:System.Double.IsNaN%2A?displayProperty=fullName> değerini test etmek için.

 [!code-csharp[FxCop.Usage.TestForNaN#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Usage.TestForNaN/cs/FxCop.Usage.TestForNaN.cs#1)]
 [!code-vb[FxCop.Usage.TestForNaN#1](../snippets/visualbasic/VS_Snippets_CodeAnalysis/FxCop.Usage.TestForNaN/vb/FxCop.Usage.TestForNaN.vb#1)]
