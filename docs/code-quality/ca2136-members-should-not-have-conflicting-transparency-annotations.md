---
title: 'CA2136: Üyeler çakışan saydamlık ek açıklamalarına sahip olmamalıdır'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA2127
- SecurityTransparentAssembliesShouldNotContainSecurityCriticalCode
- CA2136
helpviewer_keywords:
- SecurityTransparentAssembliesShouldNotContainSecurityCriticalCode
- CA2127
ms.assetid: ff5a1d18-7c52-4da5-8990-60be83a8ea81
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 1dcef8fbfd61b8cd8c946f76d6fcb93dc46f1654
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68920627"
---
# <a name="ca2136-members-should-not-have-conflicting-transparency-annotations"></a>CA2136: Üyeler çakışan saydamlık ek açıklamalarına sahip olmamalıdır

|||
|-|-|
|TypeName|TransparencyAnnotationsShouldNotConflict|
|CheckId|CA2136|
|Kategori|Microsoft.Security|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
Bu kural, bir tür üyesi üyenin kapsayıcısının güvenlik özniteliğiyle farklı <xref:System.Security> bir saydamlığa sahip bir güvenlik özniteliğiyle işaretlendiğinde ateşlenir.

## <a name="rule-description"></a>Kural açıklaması
Saydamlık nitelikleri, geniş kapsam kodlu öğelerden daha küçük kapsamlı öğelere uygulanır. Geniş kapsamı ile kod öğelerinin saydamlık öznitelikleri ilk öğeden kapsayan kod öğelerinin saydam öznitelikleri önceliklidir. Örneğin, <xref:System.Security.SecurityCriticalAttribute> özniteliğiyle işaretlenmiş bir sınıf, <xref:System.Security.SecuritySafeCriticalAttribute> özniteliğiyle işaretlenmiş bir yöntemi içeremez.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu ihlalin giderilmesi için, alt kapsamına sahip kod öğesinden güvenlik özniteliğini kaldırın veya özniteliğini kapsayan kod öğesiyle aynı olacak şekilde değiştirin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bu kuraldan gelen uyarıları göstermez.

## <a name="example"></a>Örnek
Aşağıdaki örnekte, bir yöntemi <xref:System.Security.SecuritySafeCriticalAttribute> özniteliğiyle işaretlenir ve <xref:System.Security.SecurityCriticalAttribute> özniteliği ile işaretlenmiş bir sınıfın üyesidir. Güvenlik güvenli özniteliği kaldırılmalıdır.

[!code-csharp[FxCop.Security.CA2136.TransparencyAnnotationsShouldNotConflict#1](../code-quality/codesnippet/CSharp/ca2136-members-should-not-have-conflicting-transparency-annotations_1.cs)]