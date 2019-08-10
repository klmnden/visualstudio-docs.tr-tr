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
ms.openlocfilehash: d466a508eade835563627a829f937416a24972a0
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68920644"
---
# <a name="ca2135-level-2-assemblies-should-not-contain-linkdemands"></a>CA2135: Düzey 2 derlemeler LinkDemands içermemelidir

|||
|-|-|
|TypeName|SecurityRuleSetLevel2MethodsShouldNotBeProtectedWithLinkDemands|
|CheckId|CA2135|
|Kategori|Microsoft.Security|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
Sınıf veya sınıf üyesi, düzey 2 güvenliği <xref:System.Security.Permissions.SecurityAction> kullanan bir uygulamada bir kullanıyor.

## <a name="rule-description"></a>Kural açıklaması
LinkDemands, düzey 2 güvenlik kural kümesinden kaldırılmıştır. Tam zamanında (JIT) derleme zamanında güvenliği zorlamak için linktaleplerini kullanmak yerine, yöntemleri, türleri ve alanları <xref:System.Security.SecurityCriticalAttribute> özniteliğiyle işaretleyin.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kural ihlalini onarmak için öğesini kaldırın <xref:System.Security.Permissions.SecurityAction> ve <xref:System.Security.SecurityCriticalAttribute> özniteliği ile türü veya üyeyi işaretleyin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek
Aşağıdaki örnekte <xref:System.Security.Permissions.SecurityAction> , öğesinin kaldırılması ve <xref:System.Security.SecurityCriticalAttribute> özniteliği ile işaretlenmiş yöntemi olması gerekir.

[!code-csharp[FxCop.Security.CA2135.SecurityRuleSetLevel2MethodsShouldNotBeProtectedWithLinkDemands#1](../code-quality/codesnippet/CSharp/ca2135-level-2-assemblies-should-not-contain-linkdemands_1.cs)]