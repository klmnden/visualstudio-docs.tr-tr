---
title: 'CA1823: Kullanılmayan özel alanlardan kaçının'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
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
ms.openlocfilehash: ad70fbcb8052e45f4819db2f8d423ce4f70ce697
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54971539"
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