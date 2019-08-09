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
ms.openlocfilehash: c144db920bfa04055c81227e4cc2c230ed2f097d
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68921336"
---
# <a name="ca1811-avoid-uncalled-private-code"></a>CA1811: Çağırılmayan özel kodlardan kaçının

|||
|-|-|
|TypeName|AvoidUncalledPrivateCode|
|CheckId|CA1811|
|Kategori|Microsoft. Performance|
|Yeni Değişiklik|Kırılmamış|

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