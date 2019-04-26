---
title: 'CA1823: Kullanılmayan özel alanlardan kaçının'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- AvoidUnusedPrivateFields
- CA1823
helpviewer_keywords:
- AvoidUnusedPrivateFields
- CA1823
ms.assetid: 614f94f6-0dc7-430f-8124-cb889a4a720f
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 68d7f521927497a50779d77c4d7bdd8520ac222f
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62545260"
---
# <a name="ca1823-avoid-unused-private-fields"></a>CA1823: Kullanılmayan özel alanlardan kaçının

|||
|-|-|
|TypeName|AvoidUnusedPrivateFields|
|CheckId|CA1823|
|Kategori|Microsoft.Performance|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep
 Bu kural, kodunuzda bir özel alan var ancak herhangi bir kod yolu tarafından kullanılmayan bildirilir.

## <a name="rule-description"></a>Kural açıklaması
 Derlemede erişimi görülmeyen özel alanlar algılandı.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Bu kural ihlalini düzeltmek için alanı kaldırın veya onu kullanan kodu ekleyin.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Bu kuraldan bir uyarıyı bastırmak güvenlidir.

## <a name="related-rules"></a>İlgili kuralları
 [CA1812: Örneklenmemiş iç sınıflardan kaçının](../code-quality/ca1812-avoid-uninstantiated-internal-classes.md)

 [CA1801: Kullanılmayan parametreleri gözden geçir](../code-quality/ca1801-review-unused-parameters.md)

 [CA1804: Kullanılmayan yerel öğeleri kaldırın](../code-quality/ca1804-remove-unused-locals.md)

 [CA1811: Çağrılmayan özel kodlardan kaçının](../code-quality/ca1811-avoid-uncalled-private-code.md)