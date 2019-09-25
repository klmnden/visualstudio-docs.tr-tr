---
title: 'CA2138: Saydam metotlar SuppressUnmanagedCodeSecurity özniteliğine sahip metotları çağırmamalıdır'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA2138
ms.assetid: a14c4d32-f079-4f3a-956c-a1657cde0f66
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- cplusplus
ms.openlocfilehash: d88b2f5c15d51ff840cc6ff116396ffd6b5efd60
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71232203"
---
# <a name="ca2138-transparent-methods-must-not-call-methods-with-the-suppressunmanagedcodesecurity-attribute"></a>CA2138: Saydam metotlar SuppressUnmanagedCodeSecurity özniteliğine sahip metotları çağırmamalıdır

|||
|-|-|
|TypeName|TransparentMethodsMustNotCallSuppressUnmanagedCodeSecurityMethods|
|CheckId|CA2138|
|Kategori|Microsoft.Security|
|Son değişiklik|Yeni|

## <a name="cause"></a>Sebep
Bir güvenlik saydam yöntemi, <xref:System.Security.SuppressUnmanagedCodeSecurityAttribute> özniteliğiyle işaretlenmiş bir yöntemi çağırır.

## <a name="rule-description"></a>Kural açıklaması
Bu kural, örneğin, bir P/Invoke (Platform Invoke) çağrısını kullanarak doğrudan yerel koda çağıran herhangi bir saydam yöntemi tetikler. <xref:System.Security.SuppressUnmanagedCodeSecurityAttribute> Özniteliği ile işaretlenen P/Invoke ve com birlikte çalışma yöntemleri, çağırma yöntemine karşı gerçekleştirilen bir LinkDemand ile sonuçlanır. Güvenlik saydam kodu Linktaleplerini karşılayamadığından, kod aynı zamanda SuppressUnmanagedCodeSecurity özniteliğiyle işaretlenmiş yöntemleri veya SuppressUnmanagedCodeSecurity özniteliğiyle işaretlenmiş sınıf yöntemlerini çağıramaz. Yöntem başarısız olur veya talep tam talebe dönüştürülür.

Bu kuralın ihlalleri, düzey 2 Güvenlik <xref:System.MethodAccessException> saydamlığı modelinde bir öğesine ve düzey 1 saydamlık modelinde için <xref:System.Security.Permissions.SecurityPermissionAttribute.UnmanagedCode%2A> tam talebe yol açabilir.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kural ihlalini onarmak için, <xref:System.Security.SuppressUnmanagedCodeSecurityAttribute> özniteliğini kaldırın ve yöntemi <xref:System.Security.SecurityCriticalAttribute> veya <xref:System.Security.SecuritySafeCriticalAttribute> özniteliğiyle işaretleyin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek
[!code-csharp[FxCop.Security.CA2138.TransparentMethodsMustNotCallSuppressUnmanagedCodeSecurityMethods#1](../code-quality/codesnippet/CSharp/ca2138-transparent-methods-must-not-call-methods-with-the-suppressunmanagedcodesecurity-attribute_1.cs)]