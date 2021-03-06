---
title: 'CA2140: Saydam kod güvenlik kritik öğeleri başvuramaz | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
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
caps.latest.revision: 19
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 1990e781b5793b05166c6ff5b6e9c14141ffdd69
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68154246"
---
# <a name="ca2140-transparent-code-must-not-reference-security-critical-items"></a>CA2140: Saydam kod güvenlik kritik nesnelerine başvurmamalıdır
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

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

## <a name="rule-description"></a>Kural Tanımı
 İle işaretlenmiş bir kod öğesi <xref:System.Security.SecurityCriticalAttribute> güvenlik açısından kritik bir özniteliktir. Saydam bir yöntem, kritik güvenlik öğesini kullanamaz. Saydam bir tür kritik güvenlik türünü kullanmayı deneyip denemeyeceğini bir <xref:System.TypeAccessException>, <xref:System.MethodAccessException> , veya <xref:System.FieldAccessException> tetiklenir.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için aşağıdakilerden birini yapın:

- Güvenlik kritik kod ile kod öğesini Web sayfasında işaretlemek <xref:System.Security.SecurityCriticalAttribute> özniteliği

     \- veya -

- Kaldırma <xref:System.Security.SecurityCriticalAttribute> öznitelik güvenlik kritik olarak işaretlenmiş ve bunun yerine bunları ile işaretleyin kod öğelerinden <xref:System.Security.SecuritySafeCriticalAttribute> veya <xref:System.Security.SecurityTransparentAttribute> özniteliği.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek
 Aşağıdaki örneklerde, bir güvenlik kritik genel koleksiyon, bir güvenlik kritik alan ve güvenlik kritik yöntem başvurmak saydam bir yöntem çalışır.

 [!code-csharp[FxCop.Security.CA2140.TransparentMethodsMustNotReferenceCriticalCode#1](../snippets/csharp/VS_Snippets_CodeAnalysis/fxcop.security.ca2140.transparentmethodsmustnotreferencecriticalcode/cs/ca2140 - transparentmethodsmustnotreferencecriticalcode.cs#1)]

## <a name="see-also"></a>Ayrıca Bkz.
 <xref:System.Security.SecurityTransparentAttribute><xref:System.Security.SecurityCriticalAttribute>
 <xref:System.Security.SecurityTransparentAttribute>
 <xref:System.Security.SecurityTreatAsSafeAttribute>
 <xref:System.Security?displayProperty=fullName>
