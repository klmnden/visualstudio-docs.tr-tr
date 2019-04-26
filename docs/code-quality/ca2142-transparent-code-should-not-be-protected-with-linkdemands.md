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
ms.openlocfilehash: 9b05228ef22dee20506b728164d22976feb662ae
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62545022"
---
# <a name="ca2142-transparent-code-should-not-be-protected-with-linkdemands"></a>CA2142: Saydam kod LinkDemands ile korunmamalıdır

|||
|-|-|
|TypeName|TransparentMethodsShouldNotBeProtectedWithLinkDemands|
|CheckId|CA2142|
|Kategori|Microsoft.Security|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Saydam bir yöntem gerektirir bir <xref:System.Security.Permissions.SecurityAction> veya diğer güvenlik talebi.

## <a name="rule-description"></a>Kural açıklaması
 Bu kural, bunlara erişen LinkDemands gerektiren saydam yöntemleri tetikler. Saydam güvenlik kodu, bir işlemin güvenlik doğrulaması için sorumlu olmamalıdır ve bu nedenle izin talep edilmemelidir. Saydam yöntemler güvenlik bağımsız olması gereken olduğundan, bunlar tüm güvenlik kararları değil. Ayrıca, güvenlik kararını, güvenli kritik kod daha önce bu karar verdik saydam kod sağlayacağına değil.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Bu kural ihlalini düzeltmek için saydam yöntem bağlantı üzerine kaldırın veya yöntemi işaretlemek <xref:System.Security.SecuritySafeCriticalAttribute> güvenlik gerçekleştiriliyorsa özniteliği denetimleri, güvenlik taleplerini gibi.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek
 Aşağıdaki örnekte, kural tetikler metodunda yöntem saydam ve bir LinkDemand ile işaretlenmiş olduğundan <xref:System.Security.PermissionSet> içeren bir <xref:System.Security.Permissions.SecurityAction>.

 [!code-csharp[FxCop.Security.CA2142.TransparentMethodsShouldNotBeProtectedWithLinkDemands#1](../code-quality/codesnippet/CSharp/ca2142-transparent-code-should-not-be-protected-with-linkdemands_1.cs)]

 Bu kuraldan uyarıyı bastırmayın.