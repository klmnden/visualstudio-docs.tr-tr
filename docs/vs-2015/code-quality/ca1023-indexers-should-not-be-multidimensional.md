---
title: 'CA1023: Dizin oluşturucular çok boyutlu olmamalıdır | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- IndexersShouldNotBeMultidimensional
- CA1023
helpviewer_keywords:
- CA1023
- IndexersShouldNotBeMultidimensional
ms.assetid: ae499879-97f6-434e-a61d-1fedd231d2fb
caps.latest.revision: 16
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 2b9cf9cd97dd50577a466ed4d433e0e1dbd5da4d
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68158040"
---
# <a name="ca1023-indexers-should-not-be-multidimensional"></a>CA1023: Dizin oluşturucular çok boyutlu olmamalıdır
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|IndexersShouldNotBeMultidimensional|
|CheckId|CA1023|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Ortak veya korumalı tür, birden fazla dizin kullanan bir ortak veya korumalı dizin oluşturucu içerir.

## <a name="rule-description"></a>Kural Tanımı
 Dizin Oluşturucular, diğer bir deyişle, Dizinli Özellikler tek bir dizinde kullanmanız gerekir. Çok boyutlu dizin oluşturucular kitaplığın kullanılabilirliğini önemli ölçüde azaltabilir. Tasarım birden çok dizin gerektiriyorsa, bir mantıksal veri deposu türü temsil edip etmediğini yeniden belirleyin. Aksi durumda, bir yöntem kullanın.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için tasarım silmenizin tamsayı veya dize dizini değiştirmek veya bir yöntem yerine dizin oluşturucuyu kullanın.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Standart olmayan bir dizin oluşturucu için gereken dikkatle ele sonra yalnızca bu kuraldan bir uyarıyı gizler.

## <a name="example"></a>Örnek
 Aşağıdaki örnek, bir tür gösterir `DayOfWeek03`, kuralı ihlal çok boyutlu bir dizin oluşturucu ile. Dizin Oluşturucu, bir dönüştürme türü olarak görülebilir ve bu nedenle daha uygun bir yöntem olarak sunulur. Tür olarak yeniden tasarlandı `RedesignedDayOfWeek03` kural karşılamak için.

 [!code-cpp[FxCop.Design.OneDimensionForIndexer#1](../snippets/cpp/VS_Snippets_CodeAnalysis/FxCop.Design.OneDimensionForIndexer/cpp/FxCop.Design.OneDimensionForIndexer.cpp#1)]
 [!code-csharp[FxCop.Design.OneDimensionForIndexer#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Design.OneDimensionForIndexer/cs/FxCop.Design.OneDimensionForIndexer.cs#1)]
 [!code-vb[FxCop.Design.OneDimensionForIndexer#1](../snippets/visualbasic/VS_Snippets_CodeAnalysis/FxCop.Design.OneDimensionForIndexer/vb/FxCop.Design.OneDimensionForIndexer.vb#1)]

## <a name="related-rules"></a>İlgili kuralları
 [CA1043: Dizin oluşturucular için tamsayı veya dize bağımsız değişkeni kullanın](../code-quality/ca1043-use-integral-or-string-argument-for-indexers.md)

 [CA1024: Uygun yerlerde özellikler kullan](../code-quality/ca1024-use-properties-where-appropriate.md)
