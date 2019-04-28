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
ms.openlocfilehash: 01a8a5609394f0dd428066e32fb425a2abb486c4
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62542059"
---
# <a name="ca2146-types-must-be-at-least-as-critical-as-their-base-types-and-interfaces"></a>CA2146: Türler en az kendi taban türleri ve arabirimleri kadar kritik olmalıdır

|||
|-|-|
|TypeName|TypesMustBeAtLeastAsCriticalAsBaseTypes|
|CheckId|CA2146|
|Kategori|Microsoft.Security|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Saydam bir tür ile işaretlenmiş bir tür türetilir <xref:System.Security.SecuritySafeCriticalAttribute> veya <xref:System.Security.SecurityCriticalAttribute>, veya ile işaretlenmiş bir tür <xref:System.Security.SecuritySafeCriticalAttribute> özniteliği ile işaretlenmiş bir tür türetilir <xref:System.Security.SecurityCriticalAttribute> özniteliği.

## <a name="rule-description"></a>Kural açıklaması
 Bu kural, kendi temel türü kadar kritik olmayan saydam güvenlik özniteliğine sahip bir tür türetildiğinde veya arabirim uygulandığında tetiklenir. Yalnızca kritik türler, kritik temel türlerden veya kritik arabirimleri uygulayanlardan türeyebilir ve sadece kritik ya da kritik güvenli türler, kritik güvenli temel türler veya kritik güvenli arabirim uygulamalarından türeyebilir. Bu kural, Düzey 2 saydamlık ihlalleri sonuçlanan bir <xref:System.TypeLoadException> türetilmiş bir tür için.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Bu ihlali gidermek için türetilmiş veya uygulama türü temel türü veya arabirim en az kadar kritik bir saydamlık özniteliği ile işaretleyin.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek
 [!code-csharp[FxCop.Security.CA2146.TypesMustBeAtLeastAsCriticalAsBaseTypes#1](../code-quality/codesnippet/CSharp/ca2146-types-must-be-at-least-as-critical-as-their-base-types-and-interfaces_1.cs)]