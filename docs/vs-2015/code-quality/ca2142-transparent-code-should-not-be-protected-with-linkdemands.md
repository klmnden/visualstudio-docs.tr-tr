---
title: 'CA2142: Saydam kod korumalı LinkDemands ile | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- CA2142
ms.assetid: 6dc59053-5dd9-4583-bf10-5f339107e59f
caps.latest.revision: 12
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 11bd1668e4ab599461d3619c63cd3c9732a05b4f
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68142687"
---
# <a name="ca2142-transparent-code-should-not-be-protected-with-linkdemands"></a>CA2142: Saydam kod LinkDemands ile korunmamalıdır
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|TransparentMethodsShouldNotBeProtectedWithLinkDemands|
|CheckId|CA2142|
|Kategori|Microsoft.Security|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Saydam bir yöntem gerektirir bir <xref:System.Security.Permissions.SecurityAction> veya diğer güvenlik talebi.

## <a name="rule-description"></a>Kural Tanımı
 Bu kural, bunlara erişen LinkDemands gerektiren saydam yöntemleri tetikler. Saydam güvenlik kodu, bir işlemin güvenlik doğrulaması için sorumlu olmamalıdır ve bu nedenle izin talep edilmemelidir. Saydam yöntemler güvenlik bağımsız olması gereken olduğundan, bunlar tüm güvenlik kararları değil. Ayrıca, güvenlik kararını, güvenli kritik kod daha önce bu karar verdik saydam kod sağlayacağına değil.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için saydam yöntem bağlantı üzerine kaldırın veya yöntemi işaretlemek <xref:System.Security.SecuritySafeCriticalAttribute> güvenlik gerçekleştiriliyorsa özniteliği denetimleri, güvenlik taleplerini gibi.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek
 Aşağıdaki örnekte, kural tetikler metodunda yöntem saydam ve bir LinkDemand ile işaretlenmiş olduğundan <xref:System.Security.PermissionSet> içeren bir <xref:System.Security.Permissions.SecurityAction>.

 [!code-csharp[FxCop.Security.CA2142.TransparentMethodsShouldNotBeProtectedWithLinkDemands#1](../snippets/csharp/VS_Snippets_CodeAnalysis/fxcop.security.ca2142.transparentmethodsshouldnotbeprotectedwithlinkdemands/cs/ca2142 -transparentmethodsshouldnotbeprotectedwithlinkdemands.cs#1)]

 Bu kuraldan uyarıyı bastırmayın.
