---
title: 'CA2126: Tür bağlantı talepleri kalıtım taleplerini gerektirir'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA2126
- TypeLinkDemandsRequireInheritanceDemands
helpviewer_keywords:
- CA2126
- TypeLinkDemandsRequireInheritanceDemands
ms.assetid: 07b604e5-5579-4df9-a578-dadd0d8370a7
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CPP
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: 2be42519f87c3c040c1f80c80d53d490853d986e
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68920758"
---
# <a name="ca2126-type-link-demands-require-inheritance-demands"></a>CA2126: Tür bağlantı talepleri kalıtım taleplerini gerektirir

|||
|-|-|
|TypeName|TypeLinkDemandsRequireInheritanceDemands|
|CheckId|CA2126|
|Kategori|Microsoft.Security|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
Genel korumasız bir tür, bağlantı talebi ile korunur, geçersiz kılınabilir bir yönteme sahiptir ve tür ya da yöntem bir devralma talebi ile korunmaz.

## <a name="rule-description"></a>Kural açıklaması
Bir yöntemde veya bildirim türünde bir bağlantı talebi, yöntemin hemen çağırıcının belirtilen izne sahip olmasını gerektirir. Bir yöntemde devralma talebi, belirtilen izne sahip olması için geçersiz kılan bir yöntem gerektirir. Bir tür üzerindeki devralma talebi, belirtilen izne sahip olması için türetilen bir sınıf gerektirir.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kural ihlalini onarmak için, tür ya da yöntemi, bağlantı isteği ile aynı izin için bir devralma talebi ile güvenli hale getirin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek
Aşağıdaki örnek, kuralı ihlal eden bir türü gösterir.

[!code-cpp[FxCop.Security.TypesWithLinkDemands#1](../code-quality/codesnippet/CPP/ca2126-type-link-demands-require-inheritance-demands_1.cpp)]
[!code-vb[FxCop.Security.TypesWithLinkDemands#1](../code-quality/codesnippet/VisualBasic/ca2126-type-link-demands-require-inheritance-demands_1.vb)]
[!code-csharp[FxCop.Security.TypesWithLinkDemands#1](../code-quality/codesnippet/CSharp/ca2126-type-link-demands-require-inheritance-demands_1.cs)]

## <a name="related-rules"></a>İlgili kurallar
[CA2108 Değer türlerinde bildirime dayalı güvenliği gözden geçirin](../code-quality/ca2108-review-declarative-security-on-value-types.md)

[CA2112 Güvenli türler alanları kullanıma sunmamalıdır](../code-quality/ca2112-secured-types-should-not-expose-fields.md)

[CA2122 Bağlantı taleplerine dolaylı olarak yöntemleri gösterme](../code-quality/ca2122-do-not-indirectly-expose-methods-with-link-demands.md)

[CA2123 Geçersiz kılma bağlantısı talepleri taban ile özdeş olmalıdır](../code-quality/ca2123-override-link-demands-should-be-identical-to-base.md)

## <a name="see-also"></a>Ayrıca bkz.

- [Güvenli Kodlama Yönergeleri](/dotnet/standard/security/secure-coding-guidelines)
- [Bağlantı talepleri](/dotnet/framework/misc/link-demands)