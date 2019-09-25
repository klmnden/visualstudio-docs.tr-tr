---
title: CA2141:Transparent yöntemleri LinkDemands'i karşılamamalıdır
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA2141
ms.assetid: 2957f5f7-c511-4180-ba80-752034f10a77
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 0365d82917b8cfbaf291d557a6ac2d95c220562a
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71232130"
---
# <a name="ca2141transparent-methods-must-not-satisfy-linkdemands"></a>CA2141:Transparent yöntemleri LinkDemands'i karşılamamalıdır

|||
|-|-|
|TypeName|TransparentMethodsMustNotSatisfyLinkDemands|
|CheckId|CA2141|
|Kategori|Microsoft.Security|
|Son değişiklik|Yeni|

## <a name="cause"></a>Sebep
Bir güvenlik saydam yöntemi, <xref:System.Security.AllowPartiallyTrustedCallersAttribute> (aptca) özniteliğiyle işaretlenmemiş bir derlemede bir yöntemi çağırır veya bir güvenlik saydam yöntemi bir tür ya da Yöntem `.LinkDemand` için öğesini <xref:System.Security.Permissions.SecurityAction> karşılar.

## <a name="rule-description"></a>Kural açıklaması
LinkDemand yerine, ayrıcalıkların yanlışlıkla yükseltilmesine neden olabilecek güvenliğe duyarlı bir işlemdir. Güvenliği saydam kod, güvenlik açısından kritik kod ile aynı güvenlik denetimi gereksinimlerine tabi olmadığından, bağlantı taleplerini karşılamamalıdır. Güvenlik kuralı kümesi düzey 1 derlemelerindeki saydam Yöntemler, tüm bağlantı taleplerinin çalışma zamanında tam taleplerine dönüştürülmesini sağlar ve bu da performans sorunlarına neden olabilir. Güvenlik kuralı set Level 2 derlemeleri içinde, bir LinkDemand ile yararlanmaya çalıştıklarında, saydam Yöntemler tam zamanında (JıT) derleyicide derlenmeyecektir.

2\. düzey güvenlik kullanan derlemelerde, bir bağlantı talebini karşılamak için bir güvenlik saydam yöntemi veya bir aptca derlemesinde bir yöntemi çağırmak çalışır a <xref:System.MethodAccessException>; düzey 1 derlemelerde, LinkDemand tam talep haline gelir.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kural ihlalini onarmak için, erişim yöntemini <xref:System.Security.SecurityCriticalAttribute> veya <xref:System.Security.SecuritySafeCriticalAttribute> özniteliğiyle işaretleyin ya da bağlantı talebini erişilen yöntemden kaldırın.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek
Bu örnekte, saydam bir yöntem LinkDemand içeren bir yöntemi çağırmaya çalışır. Bu kural, bu kodda harekete geçmeyecektir.

[!code-csharp[FxCop.Security.CA2141.TransparentMethodsMustNotSatisfyLinkDemands#1](../code-quality/codesnippet/CSharp/ca2141-transparent-methods-must-not-satisfy-linkdemands_1.cs)]