---
title: 'CA1026: Varsayılan parametreler kullanılmamalıdır'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA1026
- DefaultParametersShouldNotBeUsed
helpviewer_keywords:
- CA1026
- DefaultParametersShouldNotBeUsed
ms.assetid: 09643415-36ef-4d0f-9411-5721e14e2512
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 62de7654083f3fd64f95401f95e5ee593effb27d
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71236127"
---
# <a name="ca1026-default-parameters-should-not-be-used"></a>CA1026: Varsayılan parametreler kullanılmamalıdır

|||
|-|-|
|TypeName|DefaultParametersShouldNotBeUsed|
|CheckId|CA1026|
|Kategori|Microsoft.Design|
|Son değişiklik|Yeni|

## <a name="cause"></a>Sebep
Dışarıdan görünen bir tür, varsayılan bir parametre kullanan dışarıdan görünür bir yöntem içerir.

## <a name="rule-description"></a>Kural açıklaması
Varsayılan parametreleri kullanan yöntemlere ortak dil belirtimi (CLS) altında izin verilir; Ancak, CLS, derleyicilerin bu parametrelere atanan değerleri yoksaymasına olanak tanır. Varsayılan parametre değerlerini yoksayması gereken derleyiciler için yazılan kod, her varsayılan parametre için açıkça bağımsız değişken sağlamalıdır. Programlama dilleri arasında istediğiniz davranışı sürdürmek için, varsayılan parametreleri kullanan yöntemlerin varsayılan parametreleri sağlayan yöntem aşırı yüklemeleri ile değiştirilmelidir.

Derleyici, yönetilen koda eriştiğinde yönetilen uzantının C++ varsayılan parametrelerinin değerlerini yoksayar. Visual Basic Derleyicisi, [Isteğe bağlı](/dotnet/visual-basic/language-reference/modifiers/optional) anahtar sözcüğünü kullanan Varsayılan parametrelere sahip yöntemleri destekler.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kural ihlalini onarmak için varsayılan parametreleri kullanan yöntemi varsayılan parametreleri sağlayan yöntem aşırı yüklemeleri ile değiştirin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek
Aşağıdaki örnek, varsayılan parametreleri kullanan bir yöntemi ve eşdeğer işlevselliği sağlayan aşırı yüklenmiş yöntemleri gösterir.

[!code-vb[FxCop.Design.DefaultParameters#1](../code-quality/codesnippet/VisualBasic/ca1026-default-parameters-should-not-be-used_1.vb)]

## <a name="related-rules"></a>İlgili kurallar
[CA1025 Yinelenen bağımsız değişkenleri params dizisi ile değiştirin](../code-quality/ca1025-replace-repetitive-arguments-with-params-array.md)

## <a name="see-also"></a>Ayrıca bkz.
[Dil Bağımsızlığı ve Dilden Bağımsız Bileşenler](/dotnet/standard/language-independence-and-language-independent-components)