---
title: 'CA2142: Saydam kod LinkDemands ile korunmamalıdır'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA2142
ms.assetid: 6dc59053-5dd9-4583-bf10-5f339107e59f
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: bf5bb8320a8876582cc325ecf973c83593777193
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68920505"
---
# <a name="ca2142-transparent-code-should-not-be-protected-with-linkdemands"></a>CA2142: Saydam kod LinkDemands ile korunmamalıdır

|||
|-|-|
|TypeName|TransparentMethodsShouldNotBeProtectedWithLinkDemands|
|CheckId|CA2142|
|Kategori|Microsoft.Security|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
Saydam bir yöntem, ya <xref:System.Security.Permissions.SecurityAction> da başka bir güvenlik talebi gerektirir.

## <a name="rule-description"></a>Kural açıklaması
Bu kural, bunlara erişmek için Linktaleplerini gerektiren saydam yöntemler üzerinde ateşlenir. Saydam güvenlik kodu, bir işlemin güvenlik doğrulaması için sorumlu olmamalıdır ve bu nedenle izin talep edilmemelidir. Saydam yöntemlerin güvenlik açısından nötr olması gerektiğinden, herhangi bir güvenlik kararı getirmemelidir. Ayrıca, güvenlik kararları veren güvenli kritik kod, daha önce böyle bir karar vermek için saydam koda bağlı olmamalıdır.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kural ihlalini onarmak için, saydam yöntemdeki bağlantı talebini kaldırın veya güvenlik istekleri gibi güvenlik denetimleri yapıyorsa yöntemi <xref:System.Security.SecuritySafeCriticalAttribute> özniteliğiyle işaretleyin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek
Aşağıdaki örnekte, yöntemi saydam olduğu ve <xref:System.Security.PermissionSet> <xref:System.Security.Permissions.SecurityAction>içeren bir LinkDemand ile işaretlenmiş olduğundan kural yöntemi üzerinde ateşlenir.

[!code-csharp[FxCop.Security.CA2142.TransparentMethodsShouldNotBeProtectedWithLinkDemands#1](../code-quality/codesnippet/CSharp/ca2142-transparent-code-should-not-be-protected-with-linkdemands_1.cs)]

Bu kuraldan uyarıyı bastırmayın.