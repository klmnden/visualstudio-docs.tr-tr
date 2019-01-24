---
title: 'CA2133: Temsilciler tutarlı saydamlığı olan yöntemlere bağlanmalıdır | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- CA2133
ms.assetid: a09672e2-63cb-4abd-9e8f-dff515e101ce
caps.latest.revision: 13
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: e9fb3a7aab243465ac4412e9d3adea9152d909ee
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54786494"
---
# <a name="ca2133-delegates-must-bind-to-methods-with-consistent-transparency"></a>CA2133: Temsilciler tutarlı saydamlığı olan metotlara bağlanmalıdır
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|DelegatesMustBindWithConsistentTransparency|
|CheckId|CA2133|
|Kategori|Microsoft.Security|
|Yeni Değişiklik|Yeni|

> [!NOTE]
>  Bu uyarı yalnızca CoreCLR (Silverlight Web uygulamalarına özel olan CLR sürümü) çalışan kodu uygulanır.

## <a name="cause"></a>Sebep
 Bu uyarı tetikler ile işaretlenmiş temsilciyi bağlayan bir yöntemi <xref:System.Security.SecurityCriticalAttribute> saydam veya ile işaretlenmiş bir yönteme <xref:System.Security.SecuritySafeCriticalAttribute>. Uyarı, saydam veya kritik bir yöntem için kritik güvenli temsilciyi bağlayan yöntemi de tetikler.

## <a name="rule-description"></a>Kural Tanımı
 Temsilci türleri ve bunların bağlamak yöntemleri tutarlı saydamlığı olmalıdır. Saydam ve güvenli kritik Temsilciler, yalnızca diğer saydam veya güvenli kritik yöntem bağlayabilirsiniz. Benzer şekilde, kritik temsilcileri yalnızca kritik yönteme bağlayabilirsiniz. Bu bağlama kurallarını bir yöntem bir temsilci aracılığıyla çağırabilirsiniz tek bir kod da aynı yöntemi doğrudan emin olun. Örneğin, bağlama kurallarını saydam kod saydam bir temsilci yoluyla doğrudan kritik kodu çağırmasını engellemek.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu uyarı ihlalini düzeltmek için temsilci veya iki saydamlık, böylece eşdeğer bağlar, yöntemin saydamlık değiştirin.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Bu kuraldan uyarıyı bastırmayın.

### <a name="code"></a>Kod
 [!code-csharp[FxCop.Security.CA2133.DelegatesMustBindWithConsistentTransparency#1](../snippets/csharp/VS_Snippets_CodeAnalysis/fxcop.security.ca2133.delegatesmustbindwithconsistenttransparency/cs/ca2133 - delegatesmustbindwithconsistenttransparency.cs#1)]
