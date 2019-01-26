---
title: 'CA2140: Saydam kod güvenlik kritik nesnelerine başvurmamalıdır'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
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
ms.openlocfilehash: a67bd5649bd0f3f06d30f14f233cf3501871c25b
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55033023"
---
# <a name="ca2140-transparent-code-must-not-reference-security-critical-items"></a>CA2140: Saydam kod güvenlik kritik nesnelerine başvurmamalıdır

|||
|-|-|
|TypeName|TransparentMethodsMustNotReferenceCriticalCode|
|CheckId|CA2140|
|Kategori|Microsoft.Security|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep

Saydam bir yöntem:

- bir güvenlik kritik güvenlik özel durum türü işleme

- kritik güvenlik türünü işaretlenmiş bir parametre içeriyor

- Güvenlik kritik kısıtlamalar içeren genel bir parametre içeriyor

- kritik güvenlik türünü, yerel bir değişken yok

- Güvenlik kritik olarak işaretlenmiş bir türe başvuran

- Güvenlik kritik olarak işaretlenmiş bir yöntemi çağırır

- Güvenlik kritik olarak işaretlenmiş bir alana başvuruyor

- Güvenlik kritik olarak işaretlenmiş bir tür döndürür

## <a name="rule-description"></a>Kural açıklaması

İle işaretlenmiş bir kod öğesi <xref:System.Security.SecurityCriticalAttribute> güvenlik açısından kritik bir özniteliktir. Saydam bir yöntem, kritik güvenlik öğesini kullanamaz. Saydam bir tür kritik güvenlik türünü kullanmayı deneyip denemeyeceğini bir <xref:System.TypeAccessException>, <xref:System.MethodAccessException> , veya <xref:System.FieldAccessException> tetiklenir.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Bu kural ihlalini düzeltmek için aşağıdakilerden birini yapın:

- Güvenlik kritik kod ile kod öğesini Web sayfasında işaretlemek <xref:System.Security.SecurityCriticalAttribute> özniteliği

     \- veya -

- Kaldırma <xref:System.Security.SecurityCriticalAttribute> öznitelik güvenlik kritik olarak işaretlenmiş ve bunun yerine bunları ile işaretleyin kod öğelerinden <xref:System.Security.SecuritySafeCriticalAttribute> veya <xref:System.Security.SecurityTransparentAttribute> özniteliği.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek

Aşağıdaki örneklerde, bir güvenlik kritik genel koleksiyon, bir güvenlik kritik alan ve güvenlik kritik yöntem başvurmak saydam bir yöntem çalışır.

[!code-csharp[FxCop.Security.CA2140.TransparentMethodsMustNotReferenceCriticalCode#1](../code-quality/codesnippet/CSharp/ca2140-transparent-code-must-not-reference-security-critical-items_1.cs)]

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Security.SecurityTransparentAttribute>
- <xref:System.Security.SecurityCriticalAttribute>
- <xref:System.Security.SecurityTransparentAttribute>
- <xref:System.Security.SecurityTreatAsSafeAttribute>
- <xref:System.Security?displayProperty=fullName>