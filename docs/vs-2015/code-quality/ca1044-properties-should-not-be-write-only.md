---
title: 'CA1044: Özellikler yalnızca yazma olmamalıdır | Microsoft Docs'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology: vs-devops-test
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- PropertiesShouldNotBeWriteOnly
- CA1044
helpviewer_keywords:
- CA1044
- PropertiesShouldNotBeWriteOnly
ms.assetid: 8386bf3a-b161-4841-bf8b-92591595aea9
caps.latest.revision: 17
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 2cba8eb5507ce4ba08c46e7b324cce508e051f5b
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53822313"
---
# <a name="ca1044-properties-should-not-be-write-only"></a>CA1044: Özellikler yalnızca yazma olmamalıdır
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|PropertiesShouldNotBeWriteOnly|
|CheckId|CA1044|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Ortak veya korumalı özellik ayarlama erişimcisine sahip ancak get erişimcisine sahip değildir.

## <a name="rule-description"></a>Kural Tanımı
 Alma erişimcisi bir özelliği okuma erişimi ve set erişimcileri yazma erişimi sağlar. Salt okunur özelliğe sahip olmasına karşın kabul edilebilir ve genellikle gereklidir, tasarıma ilişkin yönergeler salt yazılır özellik kullanılmasını engeller. Bunun nedeni, bir kullanıcı bir değere ayarlayın, ve ardından kullanıcı değeri görüntülemeyi engellerse herhangi bir güvenlik sağlamaz. Ayrıca, okuma erişimi olmadan, yararsız olduklarını sınırlayan paylaşılan nesnelerin durumu görüntülenemez.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için özelliği bir alma erişimcisi ekleyin. Salt yazılır özelliği davranışını gerekliyse, alternatif olarak, bu özelliği yönteme dönüştürmek göz önünde bulundurun.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Bu kuraldan bir uyarıyı bastırmayın önemle tavsiye edilir.

## <a name="example"></a>Örnek
 Aşağıdaki örnekte, `BadClassWithWriteOnlyProperty` salt yazma özelliğine sahip bir tür. `GoodClassWithReadWriteProperty` Düzeltilen kod içerir.

 [!code-csharp[FxCop.Design.PropertiesNotWriteOnly#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Design.PropertiesNotWriteOnly/cs/FxCop.Design.PropertiesNotWriteOnly.cs#1)]
 [!code-vb[FxCop.Design.PropertiesNotWriteOnly#1](../snippets/visualbasic/VS_Snippets_CodeAnalysis/FxCop.Design.PropertiesNotWriteOnly/vb/PropertiesNotWriteOnly.vb#1)]
