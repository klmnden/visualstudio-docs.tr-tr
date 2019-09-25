---
title: 'CA2219: Özel durum yan tümceleri içinde özel durum harekete geçirmeyin'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- DoNotRaiseExceptionsInExceptionClauses
- CA2219
helpviewer_keywords:
- DoNotRaiseExceptionsInExceptionClauses
- CA2219
ms.assetid: 7b9b0bee-4e8e-49a4-8c40-52142b49061f
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 3c06f8693034b9943de8072f110f4661b87098a5
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71231148"
---
# <a name="ca2219-do-not-raise-exceptions-in-exception-clauses"></a>CA2219: Özel durum yan tümceleri içinde özel durum harekete geçirmeyin

|||
|-|-|
|TypeName|DoNotRaiseExceptionsInExceptionClauses|
|CheckId|CA2219|
|Kategori|Microsoft. Usage|
|Son değişiklik|Bölünmez, kırılmamış|

## <a name="cause"></a>Sebep
Bir `finally`, Filter veya fault yan tümcesinden bir özel durum atılır.

## <a name="rule-description"></a>Kural açıklaması
Özel durum yan tümcesinde bir özel durum ortaya çıktığında hata ayıklama zorluğunu büyük ölçüde artırır.

Bir `finally` veya fault yan tümcesinde bir özel durum ortaya çıktığında, yeni özel durum varsa etkin özel durumu gizler. Bu, özgün hatayı algılamaya ve hata ayıklamasına keskin hale getirir.

Bir filtre yan tümcesinde bir özel durum harekete geçirilir, çalışma zamanı özel durumu sessizce yakalar ve filtrenin false olarak değerlendirilmesini sağlar. Filtre ve bir filtreden throw bir özel durum arasındaki farkı anlatmak için bir yol yoktur. Bu, filtrenin mantığındaki hataları algılamayı ve hata ayıklamayı zorlaştırır.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kuralın bu ihlalini onarmak için, bir özel durumu, bir `finally`filtre veya hata tümceciğinden açık bir şekilde yapılandırmayın.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bu kural için bir uyarı bastırmayın. Bir özel durum yan tümcesinde oluşturulan özel durumun, yürütülen koda bir avantaj sağladığı bir senaryo yoktur.

## <a name="related-rules"></a>İlgili kurallar
[CA1065 Beklenmeyen konumlarda özel durum yükseltmeyin](../code-quality/ca1065-do-not-raise-exceptions-in-unexpected-locations.md)

## <a name="see-also"></a>Ayrıca bkz.
[Tasarım Uyarıları](../code-quality/design-warnings.md)