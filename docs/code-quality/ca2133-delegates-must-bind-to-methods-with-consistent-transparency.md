---
title: 'CA2133: Temsilciler tutarlı saydamlığı olan metotlara bağlanmalıdır'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA2133
ms.assetid: a09672e2-63cb-4abd-9e8f-dff515e101ce
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 14061c0f54593a2cb9b591d39cb46a433b0e34be
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71232302"
---
# <a name="ca2133-delegates-must-bind-to-methods-with-consistent-transparency"></a>CA2133: Temsilciler tutarlı saydamlığı olan metotlara bağlanmalıdır

|||
|-|-|
|TypeName|DelegatesMustBindWithConsistentTransparency|
|CheckId|CA2133|
|Kategori|Microsoft.Security|
|Son değişiklik|Yeni|

> [!NOTE]
> Bu uyarı yalnızca CoreCLR (CLR 'nin Silverlight Web uygulamalarına özgü sürümü) çalıştıran koda uygulanır.

## <a name="cause"></a>Sebep

Bu uyarı, ile işaretlenmiş bir temsilciyi, <xref:System.Security.SecurityCriticalAttribute> saydam olan veya <xref:System.Security.SecuritySafeCriticalAttribute>ile işaretlenmiş bir yönteme bağlayan bir yöntem üzerinde ateşlenir. Uyarı, saydam veya kritik bir yöntem için kritik güvenli temsilciyi bağlayan yöntemi de tetikler.

## <a name="rule-description"></a>Kural açıklaması

Temsilci türleri ve bağlandıkları Yöntemler tutarlı saydamlığa sahip olmalıdır. Saydam ve güvenli kritik temsilciler yalnızca diğer saydam veya kritik öneme sahip yöntemlere bağlanamaz. Benzer şekilde, kritik temsilciler yalnızca kritik yöntemlere bağlanamaz. Bu bağlama kuralları yalnızca bir temsilci aracılığıyla bir yöntemi çağırabilen kodun aynı yöntemi doğrudan de çağrılabilir olmasını güvence altına alabilir. Örneğin, bağlama kuralları saydam kodun saydam bir temsilci aracılığıyla doğrudan kritik kodu aramasını engeller.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Bu uyarının ihlal edildiğini onarmak için temsilcinin veya bağlandığı yöntemin saydamlığını, ikisinin saydamlığının eşit olması için değiştirin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Bu kuraldan uyarıyı bastırmayın.

### <a name="code"></a>Kod

[!code-csharp[FxCop.Security.CA2133.DelegatesMustBindWithConsistentTransparency#1](../code-quality/codesnippet/CSharp/ca2133-delegates-must-bind-to-methods-with-consistent-transparency_1.cs)]