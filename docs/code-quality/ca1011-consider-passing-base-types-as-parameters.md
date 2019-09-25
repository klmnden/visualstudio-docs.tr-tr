---
title: 'CA1011: Parametre olarak temel türleri geçmeyi düşünün'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- ConsiderPassingBaseTypesAsParameters
- CA1011
helpviewer_keywords:
- CA1011
- ConsiderPassingBaseTypesAsParameters
ms.assetid: ce1e1241-dcf4-419b-9363-1d5bc4989279
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CPP
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: dcb5937f58088684e7bfc204ab4143434b0684ae
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71236403"
---
# <a name="ca1011-consider-passing-base-types-as-parameters"></a>CA1011: Parametre olarak temel türleri geçmeyi düşünün

|||
|-|-|
|TypeName|ConsiderPassingBaseTypesAsParameters|
|CheckId|CA1011|
|Kategori|Microsoft.Design|
|Son değişiklik|Yeni|

## <a name="cause"></a>Sebep

Yöntem bildirimi türetilmiş bir tür olan biçimsel bir parametre içerir ve yöntem yalnızca parametrenin temel türünün üyelerini çağırır.

## <a name="rule-description"></a>Kural açıklaması

Temel tür yöntem bildiriminde parametre olarak belirtildiğinde temel türünden türetilen herhangi bir tür yöntemine karşılık gelen bağımsız değişken olarak geçirilebilir. Metot gövdesi içinde bağımsız değişken kullanıldığında, yürütülen özel yöntem bağımsız değişkenin türüne bağlıdır. Türetilmiş tür tarafından belirtilen ek işlevler gerekmiyorsa, temel tür kullanımı yöntemin daha geniş kullanımına izin verir.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Bu kuralın ihlalini onarmak için parametrenin türünü temel türüne değiştirin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Bu kuraldan bir uyarıyı gizlemek güvenlidir

- yöntemi, türetilmiş tür tarafından belirtilen belirli işlevselliği gerektiriyorsa

     \- veya -

- yalnızca türetilmiş tür veya daha türetilmiş bir tür metoduna zorlamak için yöntemine geçirilir.

Bu durumlarda, derleyici ve çalışma zamanı tarafından belirtilen güçlü tür denetimi nedeniyle kod daha sağlam olacaktır.

## <a name="example"></a>Örnek

Aşağıdaki örnek, yalnızca bir `ManipulateFileStream` <xref:System.IO.FileStream> nesnesi ile kullanılabilen ve bu kuralı ihlal eden bir yöntemi gösterir. İkinci bir yöntem `ManipulateAnyStream`, <xref:System.IO.FileStream> parametresini bir <xref:System.IO.Stream>kullanarak değiştirerek kuralını karşılar.

[!code-csharp[FxCop.Design.ConsiderPassingBaseTypes#1](../code-quality/codesnippet/CSharp/ca1011-consider-passing-base-types-as-parameters_1.cs)]
[!code-cpp[FxCop.Design.ConsiderPassingBaseTypes#1](../code-quality/codesnippet/CPP/ca1011-consider-passing-base-types-as-parameters_1.cpp)]
[!code-vb[FxCop.Design.ConsiderPassingBaseTypes#1](../code-quality/codesnippet/VisualBasic/ca1011-consider-passing-base-types-as-parameters_1.vb)]

## <a name="related-rules"></a>İlgili kurallar

[CA1059 Üyeler belirli somut türleri kullanıma sunmamalıdır](../code-quality/ca1059-members-should-not-expose-certain-concrete-types.md)