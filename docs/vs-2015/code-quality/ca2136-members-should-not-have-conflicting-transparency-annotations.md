---
title: 'CA2136: Üyeler çakışan saydamlık ek açıklamalarına sahip olmamalıdır | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- CA2127
- SecurityTransparentAssembliesShouldNotContainSecurityCriticalCode
- CA2136
helpviewer_keywords:
- SecurityTransparentAssembliesShouldNotContainSecurityCriticalCode
- CA2127
ms.assetid: ff5a1d18-7c52-4da5-8990-60be83a8ea81
caps.latest.revision: 17
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: b18ee5c048b0214779cdbe2635f5b7a14db8c28e
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68154301"
---
# <a name="ca2136-members-should-not-have-conflicting-transparency-annotations"></a>CA2136: Üyeler çakışan saydamlık ek açıklamalarına sahip olmamalıdır
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|TransparencyAnnotationsShouldNotConflict|
|CheckId|CA2136|
|Kategori|Microsoft.Security|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Bu kural, bir tür üyesi ile işaretlendiğinde tetikler bir <xref:System.Security> farklı bir güvenlik özniteliğini bir kapsayıcının üyenin saydam olan güvenlik özniteliği.

## <a name="rule-description"></a>Kural Tanımı
 Saydamlık nitelikleri, geniş kapsam kodlu öğelerden daha küçük kapsamlı öğelere uygulanır. Geniş kapsamı ile kod öğelerinin saydamlık öznitelikleri ilk öğeden kapsayan kod öğelerinin saydam öznitelikleri önceliklidir. Örneğin, ile işaretlenmiş bir sınıf <xref:System.Security.SecurityCriticalAttribute> özniteliği ile işaretlenmiş bir yöntemi içeremez <xref:System.Security.SecuritySafeCriticalAttribute> özniteliği.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu ihlali gidermek için daha düşük kapsamı kod öğesini kaynaktan güvenlik özniteliğini kaldırın veya kendi özniteliği içeren kod öğesi ile aynı olacak şekilde değiştirin.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Bu kuraldan uyarıları bastırmayın.

## <a name="example"></a>Örnek
 Aşağıdaki örnekte, bir yöntem ile işaretlenmiş <xref:System.Security.SecuritySafeCriticalAttribute> ve özniteliği ile işaretlenmiş bir sınıf üyesi olan <xref:System.Security.SecurityCriticalAttribute> özniteliği. Güvenlik güvenli özniteliğini kaldırılması gerekir.

 [!code-csharp[FxCop.Security.CA2136.TransparencyAnnotationsShouldNotConflict#1](../snippets/csharp/VS_Snippets_CodeAnalysis/fxcop.security.ca2136.transparencyannotationsshouldnotconflict/cs/ca2136 - transparencyannotationsshouldnotconflict.cs#1)]
