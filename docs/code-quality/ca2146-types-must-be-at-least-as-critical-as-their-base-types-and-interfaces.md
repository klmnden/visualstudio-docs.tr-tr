---
title: 'CA2146: Türler en az kendi taban türleri ve arabirimleri kadar kritik olmalıdır'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA2146
ms.assetid: 241fb784-1f6b-46e5-8ceb-c438e341d38e
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: a70e999505bd900a7b3d89693ef4f6a1cef9de7d
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68920420"
---
# <a name="ca2146-types-must-be-at-least-as-critical-as-their-base-types-and-interfaces"></a>CA2146: Türler en az kendi taban türleri ve arabirimleri kadar kritik olmalıdır

|||
|-|-|
|TypeName|Typesmusbeatliastakaralama Ticalasbasetypes|
|CheckId|CA2146|
|Kategori|Microsoft.Security|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
<xref:System.Security.SecuritySafeCriticalAttribute> Saydam bir tür, <xref:System.Security.SecurityCriticalAttribute>veya ile işaretlenmiş bir türden türetilir veya <xref:System.Security.SecuritySafeCriticalAttribute> özniteliğiyle işaretlenmiş bir tür özniteliğiyle işaretlenmiş bir <xref:System.Security.SecurityCriticalAttribute> türden türetilir.

## <a name="rule-description"></a>Kural açıklaması
Bu kural, kendi temel türü kadar kritik olmayan saydam güvenlik özniteliğine sahip bir tür türetildiğinde veya arabirim uygulandığında tetiklenir. Yalnızca kritik türler, kritik temel türlerden veya kritik arabirimleri uygulayanlardan türeyebilir ve sadece kritik ya da kritik güvenli türler, kritik güvenli temel türler veya kritik güvenli arabirim uygulamalarından türeyebilir. Düzey 2 saydamlığının içindeki bu kuralın ihlalleri türetilmiş tür için <xref:System.TypeLoadException> bir ile sonuçlanır.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu ihlalin giderilmesi için, türetilmiş veya uygulama türünü, en az temel tür veya arabirim olarak kritik olan bir saydamlık özniteliğiyle işaretleyin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek
[!code-csharp[FxCop.Security.CA2146.TypesMustBeAtLeastAsCriticalAsBaseTypes#1](../code-quality/codesnippet/CSharp/ca2146-types-must-be-at-least-as-critical-as-their-base-types-and-interfaces_1.cs)]