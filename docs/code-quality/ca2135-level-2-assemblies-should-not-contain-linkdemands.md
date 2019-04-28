---
title: 'CA2135: Düzey 2 derlemeler LinkDemands içermemelidir'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA2135
ms.assetid: 7a775285-42d2-4f13-8434-3fdb0deeebe6
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: fcd9032d550e79a47941540408dc6e98a15e33f7
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62796725"
---
# <a name="ca2135-level-2-assemblies-should-not-contain-linkdemands"></a>CA2135: Düzey 2 derlemeler LinkDemands içermemelidir

|||
|-|-|
|TypeName|SecurityRuleSetLevel2MethodsShouldNotBeProtectedWithLinkDemands|
|CheckId|CA2135|
|Kategori|Microsoft.Security|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Bir sınıf veya sınıf üyesi kullanarak bir <xref:System.Security.Permissions.SecurityAction> uygulamada Düzey 2 güvenlik kullanıyor.

## <a name="rule-description"></a>Kural açıklaması
 LinkDemands, düzey 2 güvenlik kural kümesinden kaldırılmıştır. Just-ın-time (JIT) derleme zamanında güvenliği zorlayan LinkDemands kullanmak yerine, yöntemleri, türleri ve alanlarını ile işaretle <xref:System.Security.SecurityCriticalAttribute> özniteliği.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Bu kural ihlalini düzeltmek için kaldırmak <xref:System.Security.Permissions.SecurityAction> ve türe veya üyeye ile işaretleyin <xref:System.Security.SecurityCriticalAttribute> özniteliği.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek
 Aşağıdaki örnekte, <xref:System.Security.Permissions.SecurityAction> kaldırılmalıdır ve yöntem ile işaretlenmiş <xref:System.Security.SecurityCriticalAttribute> özniteliği.

 [!code-csharp[FxCop.Security.CA2135.SecurityRuleSetLevel2MethodsShouldNotBeProtectedWithLinkDemands#1](../code-quality/codesnippet/CSharp/ca2135-level-2-assemblies-should-not-contain-linkdemands_1.cs)]