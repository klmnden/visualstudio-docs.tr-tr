---
title: 'CA1043: Dizin oluşturucular için tam sayı veya dize bağımsız değişken kullanın'
ms.date: 03/11/2019
ms.topic: reference
f1_keywords:
- CA1043
- UseIntegralOrStringArgumentForIndexers
helpviewer_keywords:
- CA1043
- UseIntegralOrStringArgumentForIndexers
ms.assetid: d7f14b9e-2220-4f80-b6b8-48c655a05701
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CPP
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: 298c92263903c3799f1e7e184a554f896366566c
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71235839"
---
# <a name="ca1043-use-integral-or-string-argument-for-indexers"></a>CA1043: Dizin oluşturucular için tam sayı veya dize bağımsız değişken kullanın

|||
|-|-|
|TypeName|UseIntegralOrStringArgumentForIndexers|
|CheckId|CA1043|
|Kategori|Microsoft.Design|
|Son değişiklik|Yeni|

## <a name="cause"></a>Sebep

<xref:System.Int32?displayProperty=fullName>Bir tür <xref:System.Int64?displayProperty=fullName> ,<xref:System.Object?displayProperty=fullName>,, veya<xref:System.String?displayProperty=fullName>dışında bir dizin türü kullanan bir Dizin Oluşturucu içerir.

Varsayılan olarak, bu kural yalnızca ortak ve korumalı türlere bakar, ancak bu [yapılandırılabilir](#configurability).

## <a name="rule-description"></a>Kural açıklaması

Dizin oluşturucular, diğer bir deyişle dizinli özellikler, dizin için tamsayı veya dize türleri kullanmalıdır. Bu türler genellikle veri yapılarını dizinleme için kullanılır ve kitaplığın kullanılabilirliğini artırır. <xref:System.Object> Bu tür kullanımı, belirli bir tamsayı veya dize türünün tasarım zamanında belirtilebileceği durumlar ile sınırlandırılmalıdır. Tasarım, dizin için başka türler gerektiriyorsa, türün bir mantıksal veri deposunu temsil edip etmediğini yeniden düşünün. Bir mantıksal veri deposunu temsil ediyorsa, bir yöntemi kullanın.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Bu kural ihlalini onarmak için, dizini bir tamsayı veya dize türü olarak değiştirin ya da Dizin Oluşturucu yerine bir yöntem kullanın.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Bu kuraldan bir uyarıyı yalnızca standart olmayan Dizin Oluşturucu gereksinimini dikkatle ele aldıktan sonra gizleyin.

## <a name="configurability"></a>Yapılandırılabilirlik

Bu kuralı [FxCop çözümleyicilerinin](install-fxcop-analyzers.md) (eski analizler olmadan) çalıştırıyorsanız, kod tabanınızın hangi bölümlerinin bu kuralı çalıştırmak için erişilebilirliğini temel alarak yapılandırabilirsiniz. Örneğin, kuralın yalnızca genel olmayan API yüzeyine karşı çalışması gerektiğini belirtmek için, aşağıdaki anahtar-değer çiftini projenizdeki bir. editorconfig dosyasına ekleyin:

```ini
dotnet_code_quality.ca1043.api_surface = private, internal
```

Bu seçeneği yalnızca bu kural için, tüm kurallar için veya bu kategorideki tüm kurallar (tasarım) için yapılandırabilirsiniz. Daha fazla bilgi için bkz. [FxCop çözümleyicileri yapılandırma](configure-fxcop-analyzers.md).

## <a name="example"></a>Örnek

Aşağıdaki örnek, <xref:System.Int32> Dizin kullanan bir dizin oluşturucuyu gösterir.

[!code-csharp[FxCop.Design.IntegralOrStringIndexers#1](../code-quality/codesnippet/CSharp/ca1043-use-integral-or-string-argument-for-indexers_1.cs)]
[!code-cpp[FxCop.Design.IntegralOrStringIndexers#1](../code-quality/codesnippet/CPP/ca1043-use-integral-or-string-argument-for-indexers_1.cpp)]
[!code-vb[FxCop.Design.IntegralOrStringIndexers#1](../code-quality/codesnippet/VisualBasic/ca1043-use-integral-or-string-argument-for-indexers_1.vb)]

## <a name="related-rules"></a>İlgili kurallar

- [CA1023 Dizin oluşturucular çok boyutlu olmamalıdır](../code-quality/ca1023-indexers-should-not-be-multidimensional.md)
- [CA1024 Uygun yerlerde özellikleri kullanın](../code-quality/ca1024-use-properties-where-appropriate.md)