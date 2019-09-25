---
title: 'CA1811: Çağırılmayan özel kodlardan kaçının'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- AvoidUncalledPrivateCode
- CA1811
helpviewer_keywords:
- CA1811
- AvoidUncalledPrivateCode
ms.assetid: aadbba74-7821-475f-8980-34d17c0a0a8b
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 92a7542499eceeccbd62ce327b386dc099b726b2
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71233617"
---
# <a name="ca1811-avoid-uncalled-private-code"></a>CA1811: Çağırılmayan özel kodlardan kaçının

|||
|-|-|
|TypeName|AvoidUncalledPrivateCode|
|CheckId|CA1811|
|Kategori|Microsoft. Performance|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep
Özel veya iç (derleme düzeyi) bir üyenin derlemede çağıranları yok, ortak dil çalışma zamanı tarafından Çağrılmıyor ve bir temsilci tarafından çağrılmıyor. Aşağıdaki Üyeler bu kural tarafından denetlenmiyor:

- Açık arabirim üyeleri.

- Statik oluşturucular.

- Serileştirme oluşturucuları.

- <xref:System.Runtime.InteropServices.ComRegisterFunctionAttribute?displayProperty=fullName> Veya<xref:System.Runtime.InteropServices.ComUnregisterFunctionAttribute?displayProperty=fullName>ile işaretlenmiş yöntemler.

- Geçersiz kılan Üyeler.

## <a name="rule-description"></a>Kural açıklaması
Bu kural, kural mantığı tarafından şu anda tanımlı olmayan giriş noktaları oluşursa, yanlış pozitif durumları bildirebilir. Ayrıca, bir derleyici, çağrılabilir olmayan kodu bir derlemeye yayabilir.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kural ihlalini onarmak için, çağrılabilir olmayan kodu kaldırın veya onu çağıran kodu ekleyin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bu kuraldan bir uyarıyı gizlemek güvenlidir.

## <a name="related-rules"></a>İlgili kurallar
[CA1812 Örneklenmemiş iç sınıflardan kaçının](../code-quality/ca1812-avoid-uninstantiated-internal-classes.md)

[CA1801 Kullanılmayan parametreleri gözden geçir](../code-quality/ca1801-review-unused-parameters.md)

[CA1804 Kullanılmayan yerelleri kaldır](../code-quality/ca1804-remove-unused-locals.md)