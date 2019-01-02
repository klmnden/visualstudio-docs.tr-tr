---
title: 'CA2133: Temsilciler tutarlı saydamlığı olan yöntemlere bağlanmalıdır'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- CA2133
ms.assetid: a09672e2-63cb-4abd-9e8f-dff515e101ce
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 8053090802c77b310bc04d6e95be8d3c538a4cb9
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53939790"
---
# <a name="ca2133-delegates-must-bind-to-methods-with-consistent-transparency"></a>CA2133: Temsilciler tutarlı saydamlığı olan yöntemlere bağlanmalıdır

|||
|-|-|
|TypeName|DelegatesMustBindWithConsistentTransparency|
|CheckId|CA2133|
|Kategori|Microsoft.Security|
|Yeni Değişiklik|Yeni|

> [!NOTE]
> Bu uyarı yalnızca CoreCLR (Silverlight web uygulamalarına özel olan CLR sürümü) çalışan kodu uygulanır.

## <a name="cause"></a>Sebep

Bu uyarı tetikler ile işaretlenmiş temsilciyi bağlayan bir yöntemi <xref:System.Security.SecurityCriticalAttribute> saydam veya ile işaretlenmiş bir yönteme <xref:System.Security.SecuritySafeCriticalAttribute>. Uyarı, saydam veya kritik bir yöntem için kritik güvenli temsilciyi bağlayan yöntemi de tetikler.

## <a name="rule-description"></a>Kural açıklaması

Temsilci türleri ve bunların bağlamak yöntemleri tutarlı saydamlığı olmalıdır. Saydam ve güvenli kritik Temsilciler, yalnızca diğer saydam veya güvenli kritik yöntem bağlayabilirsiniz. Benzer şekilde, kritik temsilcileri yalnızca kritik yönteme bağlayabilirsiniz. Bu bağlama kurallarını bir yöntem bir temsilci aracılığıyla çağırabilirsiniz tek bir kod da aynı yöntemi doğrudan emin olun. Örneğin, bağlama kurallarını saydam kod saydam bir temsilci yoluyla doğrudan kritik kodu çağırmasını engellemek.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Bu uyarı ihlalini düzeltmek için temsilci veya iki saydamlık, böylece eşdeğer bağlar, yöntemin saydamlık değiştirin.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Bu kuraldan uyarıyı bastırmayın.

### <a name="code"></a>Kod

[!code-csharp[FxCop.Security.CA2133.DelegatesMustBindWithConsistentTransparency#1](../code-quality/codesnippet/CSharp/ca2133-delegates-must-bind-to-methods-with-consistent-transparency_1.cs)]