---
title: 'CA2140: Saydam kod güvenlik kritik nesnelerine başvurmamalıdır'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA2129
- SecurityTransparentCodeShouldNotReferenceNonpublicSecurityCriticalCode
- CA2140
helpviewer_keywords:
- CA2140
- SecurityTransparentCodeShouldNotReferenceNonpublicSecurityCriticalCode
- CA2129
ms.assetid: 251a12da-0557-47f5-a4f7-0229d590ae7b
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: d4f02938aed7456762f1ef51da716b6b96bdf437
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71232156"
---
# <a name="ca2140-transparent-code-must-not-reference-security-critical-items"></a>CA2140: Saydam kod güvenlik kritik nesnelerine başvurmamalıdır

|||
|-|-|
|TypeName|TransparentMethodsMustNotReferenceCriticalCode|
|CheckId|CA2140|
|Kategori|Microsoft.Security|
|Son değişiklik|Yeni|

## <a name="cause"></a>Sebep

Saydam bir yöntem:

- Güvenlik açısından kritik güvenlik özel durum türünü işler

- , güvenlik açısından kritik tür olarak işaretlenmiş bir parametreye sahiptir

- kritik güvenlik kısıtlamalarına sahip genel bir parametreye sahiptir

- , güvenlik açısından kritik bir tür yerel değişkenine sahiptir

- Güvenlik açısından kritik olarak işaretlenmiş bir türe başvurur

- Güvenlik açısından kritik olarak işaretlenen bir yöntemi çağırır

- Güvenlik açısından kritik olarak işaretlenmiş bir alana başvurur

- Güvenlik açısından kritik olarak işaretlenen bir tür döndürür

## <a name="rule-description"></a>Kural açıklaması

<xref:System.Security.SecurityCriticalAttribute> Özniteliğiyle işaretlenmiş bir kod öğesi güvenlik açısından kritik ' dir. Saydam bir yöntem, kritik güvenlik öğesini kullanamaz. Saydam bir tür, <xref:System.TypeAccessException> <xref:System.MethodAccessException> bir güvenlik kritik türünü kullanmayı denerse, veya <xref:System.FieldAccessException> oluşturulur.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Bu kuralın ihlalini onarmak için aşağıdakilerden birini yapın:

- Güvenlik açısından kritik kodu <xref:System.Security.SecurityCriticalAttribute> kullanan kod öğesini özniteliğiyle işaretle

     \- veya -

- Özniteliği güvenlik açısından kritik olarak işaretlenen kod öğelerinden kaldırın ve bunun yerine bunları <xref:System.Security.SecuritySafeCriticalAttribute> veya <xref:System.Security.SecurityTransparentAttribute> özniteliğiyle işaretleyin. <xref:System.Security.SecurityCriticalAttribute>

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek

Aşağıdaki örneklerde, saydam bir yöntem güvenlik açısından kritik Genel koleksiyona, güvenlik açısından kritik alana ve güvenlik açısından kritik bir yönteme başvurmasına çalışır.

[!code-csharp[FxCop.Security.CA2140.TransparentMethodsMustNotReferenceCriticalCode#1](../code-quality/codesnippet/CSharp/ca2140-transparent-code-must-not-reference-security-critical-items_1.cs)]

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Security.SecurityTransparentAttribute>
- <xref:System.Security.SecurityCriticalAttribute>
- <xref:System.Security.SecurityTransparentAttribute>
- <xref:System.Security.SecurityTreatAsSafeAttribute>
- <xref:System.Security?displayProperty=fullName>