---
title: 'CA1023: Dizin oluşturucular çok boyutlu olmamalıdır'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
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
ms.openlocfilehash: a9b708b1be65b8aefa34e9f0366a87d6f94b5b5c
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55043706"
---
# <a name="ca1023-indexers-should-not-be-multidimensional"></a>CA1023: Dizin oluşturucular çok boyutlu olmamalıdır

|||
|-|-|
|TypeName|IndexersShouldNotBeMultidimensional|
|CheckId|CA1023|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Ortak veya korumalı tür, birden fazla dizin kullanan bir ortak veya korumalı dizin oluşturucu içerir.

## <a name="rule-description"></a>Kural açıklaması
 Dizin Oluşturucular, diğer bir deyişle, Dizinli Özellikler tek bir dizinde kullanmanız gerekir. Çok boyutlu dizin oluşturucular kitaplığın kullanılabilirliğini önemli ölçüde azaltabilir. Tasarım birden çok dizin gerektiriyorsa, bir mantıksal veri deposu türü temsil edip etmediğini yeniden belirleyin. Aksi durumda, bir yöntem kullanın.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Bu kural ihlalini düzeltmek için tasarım silmenizin tamsayı veya dize dizini değiştirmek veya bir yöntem yerine dizin oluşturucuyu kullanın.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Standart olmayan bir dizin oluşturucu için gereken dikkatle ele sonra yalnızca bu kuraldan bir uyarıyı gizler.

## <a name="example"></a>Örnek
 Aşağıdaki örnek, bir tür gösterir `DayOfWeek03`, kuralı ihlal çok boyutlu bir dizin oluşturucu ile. Dizin Oluşturucu, bir dönüştürme türü olarak görülebilir ve bu nedenle daha uygun bir yöntem olarak sunulur. Tür olarak yeniden tasarlandı `RedesignedDayOfWeek03` kural karşılamak için.

 [!code-vb[FxCop.Design.OneDimensionForIndexer#1](../code-quality/codesnippet/VisualBasic/ca1023-indexers-should-not-be-multidimensional_1.vb)]
 [!code-cpp[FxCop.Design.OneDimensionForIndexer#1](../code-quality/codesnippet/CPP/ca1023-indexers-should-not-be-multidimensional_1.cpp)]
 [!code-csharp[FxCop.Design.OneDimensionForIndexer#1](../code-quality/codesnippet/CSharp/ca1023-indexers-should-not-be-multidimensional_1.cs)]

## <a name="related-rules"></a>İlgili kuralları
 [CA1043: Dizin oluşturucular için tamsayı veya dize bağımsız değişkeni kullanın](../code-quality/ca1043-use-integral-or-string-argument-for-indexers.md)

 [CA1024: Uygun yerlerde özellikler kullan](../code-quality/ca1024-use-properties-where-appropriate.md)