---
title: 'CA1813: Mühürsüz özniteliklerden kaçının'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA1813
- AvoidUnsealedAttributes
helpviewer_keywords:
- CA1813
- AvoidUnsealedAttributes
ms.assetid: f5e31b4c-9f8b-49e1-a2a8-bb5f1140729a
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: 12371c34c846991a0ec41f5e9d9588c5bde8e4d6
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71233590"
---
# <a name="ca1813-avoid-unsealed-attributes"></a>CA1813: Mühürsüz özniteliklerden kaçının

|||
|-|-|
|TypeName|AvoidUnsealedAttributes|
|CheckId|CA1813|
|Kategori|Microsoft. Performance|
|Son değişiklik|Yeni|

## <a name="cause"></a>Sebep

Ortak bir tür öğesinden <xref:System.Attribute?displayProperty=fullName>devralınır, soyut değildir ve korumalı değildir (`NotInheritable` Visual Basic).

## <a name="rule-description"></a>Kural açıklaması

.NET özel özniteliklerin alınması için yöntemler sağlar. Varsayılan olarak, bu yöntemleri öznitelik devralma hiyerarşisinde arar. Örneğin, <xref:System.Attribute.GetCustomAttribute%2A?displayProperty=fullName> belirtilen öznitelik türünü veya belirtilen öznitelik türünü genişleten herhangi bir öznitelik türünü arar. Özniteliği mühürde devralma hiyerarşisinde arama kaldırılır ve performans iyileştirebilirler.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Bu kural ihlalini onarmak için öznitelik türünü mühürleyin veya soyut hale getirin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Bu kuraldan bir uyarıyı gizlemek güvenlidir. Yalnızca bir öznitelik hiyerarşisi tanımlıyorsanız ve özniteliği mühürleyip soyut hale getirmemek istiyorsanız gizleyin.

## <a name="example"></a>Örnek

Aşağıdaki örnek, bu kuralı karşılayan özel bir özniteliği gösterir.

[!code-csharp[FxCop.Performance.AttributesSealed#1](../code-quality/codesnippet/CSharp/ca1813-avoid-unsealed-attributes_1.cs)]
[!code-vb[FxCop.Performance.AttributesSealed#1](../code-quality/codesnippet/VisualBasic/ca1813-avoid-unsealed-attributes_1.vb)]

## <a name="related-rules"></a>İlgili kurallar

- [CA1019 Öznitelik bağımsız değişkenleri için erişimcileri tanımlayın](../code-quality/ca1019-define-accessors-for-attribute-arguments.md)
- [CA1018 Öznitelikleri AttributeUsageAttribute ile işaretle](../code-quality/ca1018-mark-attributes-with-attributeusageattribute.md)

## <a name="see-also"></a>Ayrıca bkz.

- [Öznitelikler](/dotnet/standard/design-guidelines/attributes)