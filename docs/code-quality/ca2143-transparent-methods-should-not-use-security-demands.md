---
title: 'CA2143: Saydam metotlar güvenlik taleplerini kullanmamalıdır'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA2143
ms.assetid: 5d3923d7-cf40-4512-bc5c-0db0e0d6e25a
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: a182beba738e583fad83c3f51d7efa312761906d
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71231976"
---
# <a name="ca2143-transparent-methods-should-not-use-security-demands"></a>CA2143: Saydam metotlar güvenlik taleplerini kullanmamalıdır

|||
|-|-|
|TypeName|TransparentMethodsShouldNotDemand|
|CheckId|CA2143|
|Kategori|Microsoft.Security|
|Son değişiklik|Yeni|

## <a name="cause"></a>Sebep
Bir Tranparent türü ya da yöntemi bildirimli olarak bir <xref:System.Security.Permissions.SecurityAction?displayProperty=fullName> `.Demand` talep ile işaretlenir <xref:System.Security.CodeAccessPermission.Demand%2A?displayProperty=fullName> ya da Yöntemi yöntemini çağırır.

## <a name="rule-description"></a>Kural açıklaması
Saydam güvenlik kodu, bir işlemin güvenlik doğrulaması için sorumlu olmamalıdır ve bu nedenle izin talep edilmemelidir. Saydam güvenlik kodu, güvenlik kararını vermek için tüm talepleri kullanmalıdır ve güvenli kritik kod, saydam koda tüm talepleri vermek için güvenmemelidir. Güvenlik istekleri gerçekleştiren tüm kodlar, bunun yerine güvenli kritik öneme sahip olmalıdır.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Genel olarak, bu kural ihlalini onarmak için yöntemi <xref:System.Security.SecuritySafeCriticalAttribute> özniteliğiyle işaretleyin. Ayrıca talebi de kaldırabilirsiniz.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek
Bir saydam Yöntem bildirime dayalı bir güvenlik talebi yaptığından, aşağıdaki kodda kural dosyaları.

[!code-csharp[FxCop.Security.CA2143.TransparentMethodsShouldNotDemand#1](../code-quality/codesnippet/CSharp/ca2143-transparent-methods-should-not-use-security-demands_1.cs)]

## <a name="see-also"></a>Ayrıca bkz.
[CA2142 Saydam kod Linktaleplerini korumamalıdır](../code-quality/ca2142-transparent-code-should-not-be-protected-with-linkdemands.md)