---
title: 'CA1023: Dizin oluşturucular çok boyutlu olmamalıdır'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IndexersShouldNotBeMultidimensional
- CA1023
helpviewer_keywords:
- CA1023
- IndexersShouldNotBeMultidimensional
ms.assetid: ae499879-97f6-434e-a61d-1fedd231d2fb
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CPP
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: 08a45219eb2fceeaa9c58a140990ea577c941ff7
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68923033"
---
# <a name="ca1023-indexers-should-not-be-multidimensional"></a>CA1023: Dizin oluşturucular çok boyutlu olmamalıdır

|||
|-|-|
|TypeName|IndexersShouldNotBeMultidimensional|
|CheckId|CA1023|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
Ortak veya korumalı bir tür, birden fazla dizin kullanan ortak veya korumalı bir Dizin Oluşturucu içerir.

## <a name="rule-description"></a>Kural açıklaması
Dizin oluşturucular, yani dizinli özellikler tek bir dizin kullanmalıdır. Çok boyutlu Dizin oluşturucular kitaplığın kullanılabilirliğini önemli ölçüde azaltabilir. Tasarımda birden çok dizin gerekiyorsa, türün bir mantıksal veri deposunu temsil edip etmediğini yeniden düşünün. Aksi takdirde, bir yöntemi kullanın.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kural ihlalini onarmak için, tasarımı bir tek tamsayı veya dize dizini kullanacak şekilde değiştirin ya da Dizin Oluşturucu yerine bir yöntem kullanın.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bu kuraldan bir uyarıyı yalnızca standart olmayan Dizin Oluşturucu gereksinimini dikkatle ele aldıktan sonra gizleyin.

## <a name="example"></a>Örnek
Aşağıdaki örnek, kuralını ihlal eden çok `DayOfWeek03`boyutlu bir Dizin Oluşturucu ile bir türü gösterir. Dizin Oluşturucu bir dönüştürme türü olarak görülebilir ve bu nedenle bir yöntem olarak daha uygun şekilde kullanıma sunulabilir. Türü, kuralı karşılamak için `RedesignedDayOfWeek03` ' de yeniden tasarlanmıştır.

[!code-vb[FxCop.Design.OneDimensionForIndexer#1](../code-quality/codesnippet/VisualBasic/ca1023-indexers-should-not-be-multidimensional_1.vb)]
[!code-cpp[FxCop.Design.OneDimensionForIndexer#1](../code-quality/codesnippet/CPP/ca1023-indexers-should-not-be-multidimensional_1.cpp)]
[!code-csharp[FxCop.Design.OneDimensionForIndexer#1](../code-quality/codesnippet/CSharp/ca1023-indexers-should-not-be-multidimensional_1.cs)]

## <a name="related-rules"></a>İlgili kurallar
[CA1043 Dizin oluşturucular için integral veya dize bağımsız değişkeni kullanın](../code-quality/ca1043-use-integral-or-string-argument-for-indexers.md)

[CA1024 Uygun yerlerde özellikleri kullanın](../code-quality/ca1024-use-properties-where-appropriate.md)