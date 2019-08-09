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
ms.openlocfilehash: 47a2ad3b64055584551a63a2333e29286783d8cf
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68921355"
---
# <a name="ca1823-avoid-unused-private-fields"></a>CA1823: Kullanılmayan özel alanlardan kaçının

|||
|-|-|
|TypeName|AvoidUnusedPrivateFields|
|CheckId|CA1823|
|Kategori|Microsoft. Performance|
|Yeni Değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep
Bu kural, kodunuzdaki bir özel alan olduğunda ve herhangi bir kod yolu tarafından kullanılmazsa raporlanır.

## <a name="rule-description"></a>Kural açıklaması
Derlemede erişimi görülmeyen özel alanlar algılandı.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kural ihlalini onarmak için alanı kaldırın veya onu kullanan kodu ekleyin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bu kuraldan bir uyarıyı gizlemek güvenlidir.

## <a name="related-rules"></a>İlgili kurallar
[CA1812 Örneklenmemiş iç sınıflardan kaçının](../code-quality/ca1812-avoid-uninstantiated-internal-classes.md)

[CA1801 Kullanılmayan parametreleri gözden geçir](../code-quality/ca1801-review-unused-parameters.md)

[CA1804 Kullanılmayan yerelleri kaldır](../code-quality/ca1804-remove-unused-locals.md)

[CA1811 Çağrılmadı özel koddan kaçının](../code-quality/ca1811-avoid-uncalled-private-code.md)