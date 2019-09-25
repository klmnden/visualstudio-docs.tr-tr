---
title: 'CA2145: Saydam metotlar SuppressUnmanagedCodeSecurityAttribute ile donatılmamalıdır'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA2145
ms.assetid: 81970700-b438-4b3b-9239-16887e16f7b7
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 3cca385c346a7daa8aaddb377f999506ffb1abaa
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71232046"
---
# <a name="ca2145-transparent-methods-should-not-be-decorated-with-the-suppressunmanagedcodesecurityattribute"></a>CA2145: Saydam metotlar SuppressUnmanagedCodeSecurityAttribute ile donatılmamalıdır

|||
|-|-|
|TypeName|TransparentMethodsShouldNotUseSuppressUnmanagedCodeSecurity|
|CheckId|CA2145|
|Kategori|Microsoft.Security|
|Son değişiklik|Yeni|

## <a name="cause"></a>Sebep

Saydam bir yöntem, <xref:System.Security.SecuritySafeCriticalAttribute> yöntemiyle işaretlenmiş bir yöntem veya bir yöntemi içeren bir tür, <xref:System.Security.SuppressUnmanagedCodeSecurityAttribute> özniteliğiyle işaretlenir.

## <a name="rule-description"></a>Kural açıklaması

Özniteliği ile donatılmış Yöntemler <xref:System.Security.SuppressUnmanagedCodeSecurityAttribute> , onu çağıran herhangi bir yönteme yerleştirilmiş bir örtülü LinkDemand 'a sahiptir. Bu LinkDemand, çağıran kodun kritik güvenlikli olmasını gerektirir. SuppressUnmanagedCodeSecurity <xref:System.Security.SecurityCriticalAttribute> kullanan yöntemi özniteliğiyle işaretlemek, bu gereksinimi metodun çağıranları için daha belirgin hale getirir.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Bu kural ihlalini onarmak için yöntemini veya türünü <xref:System.Security.SecurityCriticalAttribute> özniteliğiyle işaretleyin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Bu kuraldan uyarıyı bastırmayın.

### <a name="code"></a>Kod

[!code-csharp[FxCop.Security.CA2145.TransparentMethodsShouldNotUseSuppressUnmanagedCodeSecurity#1](../code-quality/codesnippet/CSharp/ca2145-transparent-methods-should-not-be-decorated-with-the-suppressunmanagedcodesecurityattribute_1.cs)]