---
title: 'CA2230: Değişken bağımsız değişkenler için params kullanın'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- UseParamsForVariableArguments
- CA2230
helpviewer_keywords:
- CA2230
- UseParamsForVariableArguments
ms.assetid: bf98b733-4855-4110-9f16-eba5a9e79421
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 0639d30771b3a6bb288ddbf9644dda2efcd5f90d
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71231355"
---
# <a name="ca2230-use-params-for-variable-arguments"></a>CA2230: Değişken bağımsız değişkenler için params kullanın

|||
|-|-|
|TypeName|UseParamsForVariableArguments|
|CheckId|CA2230|
|Kategori|Microsoft. Usage|
|Son değişiklik|Yeni|

## <a name="cause"></a>Sebep
Ortak veya korumalı bir tür, `VarArgs` çağırma kuralını kullanan ortak veya korumalı bir yöntem içerir.

## <a name="rule-description"></a>Kural açıklaması
`VarArgs` Çağırma kuralı, değişken sayıda parametre alan belirli yöntem tanımlarıyla birlikte kullanılır. `VarArgs` Çağırma kuralını kullanan bir yöntem ortak dil belirtimi (CLS) uyumlu değil ve programlama dilleri arasında erişilebilir olmayabilir.

' C#De, `VarArgs` bir yöntemin parametre `__arglist` listesi anahtar sözcüğüyle sona erdiğinde çağırma kuralı kullanılır. Visual Basic, `VarArgs` çağırma kuralını desteklemez ve görsel C++ yalnızca elips `...` gösterimini kullanan yönetilmeyen kodda kullanılmasına izin verir.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
İçindeki C#bu kuralın ihlalini onarmak için yerine [params](/dotnet/csharp/language-reference/keywords/params) `__arglist`anahtar sözcüğünü kullanın.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek
Aşağıdaki örnek, biri kuralı ve kuralı karşılayan birini ihlal eden iki yöntemi gösterir.

[!code-csharp[FxCop.Usage.UseParams#1](../code-quality/codesnippet/CSharp/ca2230-use-params-for-variable-arguments_1.cs)]

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Reflection.CallingConventions?displayProperty=fullName>
- [Dil Bağımsızlığı ve Dilden Bağımsız Bileşenler](/dotnet/standard/language-independence-and-language-independent-components)