---
title: 'CA1043: Dizin oluşturucular için tam sayı veya dize bağımsız değişken kullanın'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA1043
- UseIntegralOrStringArgumentForIndexers
helpviewer_keywords:
- CA1043
- UseIntegralOrStringArgumentForIndexers
ms.assetid: d7f14b9e-2220-4f80-b6b8-48c655a05701
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CPP
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: f3bd308e35e36c18cf9231f7fd2ed9d9f442a9ca
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55922478"
---
# <a name="ca1043-use-integral-or-string-argument-for-indexers"></a>CA1043: Dizin oluşturucular için tam sayı veya dize bağımsız değişken kullanın

|||
|-|-|
|TypeName|UseIntegralOrStringArgumentForIndexers|
|CheckId|CA1043|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Ortak veya korumalı tür dışındaki bir dizin türü kullanan bir ortak veya korumalı dizin oluşturucu içeren <xref:System.Int32?displayProperty=fullName>, <xref:System.Int64?displayProperty=fullName>, <xref:System.Object?displayProperty=fullName>, veya <xref:System.String?displayProperty=fullName>.

## <a name="rule-description"></a>Kural açıklaması
 Dizin Oluşturucular, diğer bir deyişle, Dizinlenmiş özelliklere dizin için tamsayı veya dize türleri kullanmalıdır. Bu türler, genellikle veri yapılarını dizinleme için kullanılır ve kitaplığın kullanılabilirliğini artırın. Kullanım <xref:System.Object> türü burada belirli bir tamsayı veya dize türü belirtilemez tasarım zamanında, bu gibi durumlarda sınırlı olmalıdır. Tasarım dizini diğer türleri gerektiriyorsa, bir mantıksal veri deposu türü temsil edip etmediğini yeniden belirleyin. Bir mantıksal veri deposunu temsil etmez, bir yöntem kullanın.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Bu kural ihlalini düzeltmek için dizini bir tamsayı veya dize türü değiştirmek veya bir yöntem yerine dizin oluşturucuyu kullanın.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Standart olmayan bir dizin oluşturucu için gereken dikkatle ele sonra yalnızca bu kuraldan bir uyarıyı gizler.

## <a name="example"></a>Örnek
 Aşağıdaki örnek, bir dizin oluşturucu kullanan gösterir. bir <xref:System.Int32> dizini.

 [!code-csharp[FxCop.Design.IntegralOrStringIndexers#1](../code-quality/codesnippet/CSharp/ca1043-use-integral-or-string-argument-for-indexers_1.cs)]
 [!code-cpp[FxCop.Design.IntegralOrStringIndexers#1](../code-quality/codesnippet/CPP/ca1043-use-integral-or-string-argument-for-indexers_1.cpp)]
 [!code-vb[FxCop.Design.IntegralOrStringIndexers#1](../code-quality/codesnippet/VisualBasic/ca1043-use-integral-or-string-argument-for-indexers_1.vb)]

## <a name="related-rules"></a>İlgili kuralları
 [CA1023: Dizin oluşturucular çok boyutlu olmamalıdır](../code-quality/ca1023-indexers-should-not-be-multidimensional.md)

 [CA1024: Uygun yerlerde özellikler kullan](../code-quality/ca1024-use-properties-where-appropriate.md)