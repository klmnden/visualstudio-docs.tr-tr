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
ms.openlocfilehash: 3d47b39208fce297fd058d6976b9fa7d7593cb9a
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62778814"
---
# <a name="ca1043-use-integral-or-string-argument-for-indexers"></a>CA1043: Dizin oluşturucular için tam sayı veya dize bağımsız değişken kullanın

|||
|-|-|
|TypeName|UseIntegralOrStringArgumentForIndexers|
|CheckId|CA1043|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep

Bir türü dışında bir dizin türü kullanan bir dizin oluşturucu içeren <xref:System.Int32?displayProperty=fullName>, <xref:System.Int64?displayProperty=fullName>, <xref:System.Object?displayProperty=fullName>, veya <xref:System.String?displayProperty=fullName>.

Varsayılan olarak, bu kural yalnızca genel ve korumalı türler görünür, ancak bu [yapılandırılabilir](#configurability).

## <a name="rule-description"></a>Kural açıklaması

Dizin Oluşturucular, diğer bir deyişle, Dizinlenmiş özelliklere dizin için tamsayı veya dize türleri kullanmalıdır. Bu türler, genellikle veri yapılarını dizinleme için kullanılır ve kitaplığın kullanılabilirliğini artırın. Kullanım <xref:System.Object> türü burada belirli bir tamsayı veya dize türü belirtilemez tasarım zamanında, bu gibi durumlarda sınırlı olmalıdır. Tasarım dizini diğer türleri gerektiriyorsa, bir mantıksal veri deposu türü temsil edip etmediğini yeniden belirleyin. Bir mantıksal veri deposunu temsil etmez, bir yöntem kullanın.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Bu kural ihlalini düzeltmek için dizini bir tamsayı veya dize türü değiştirin veya bir yöntem yerine bir dizin oluşturucu kullanın.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Standart olmayan bir dizin oluşturucu için gereken dikkatle ele sonra yalnızca bu kuraldan bir uyarıyı gizler.

## <a name="configurability"></a>Etkiler ve yapılandırma

Bu kuraldan çalıştırıyorsanız [FxCop Çözümleyicileri](install-fxcop-analyzers.md) (ve statik kod analizi üzerinden değil), hangi parçalarının yapılandırabilirsiniz, bu kuralı çalıştırmak için kod tabanı, kendi erişilebilirliği temel. Örneğin, kural yalnızca genel olmayan API yüzeyi karşı çalışması gerektiğini belirtmek için projenizi bir .editorconfig dosyasında şu anahtar-değer çifti ekleyin:

```
dotnet_code_quality.ca1043.api_surface = private, internal
```

Bu kategoride (tasarımı), bu seçenek yalnızca bu kural, tüm kuralları veya tüm kuralları yapılandırabilirsiniz. Daha fazla bilgi için [yapılandırma FxCop Çözümleyicileri](configure-fxcop-analyzers.md).

## <a name="example"></a>Örnek

Aşağıdaki örnek, bir dizin oluşturucu kullanan gösterir. bir <xref:System.Int32> dizini.

[!code-csharp[FxCop.Design.IntegralOrStringIndexers#1](../code-quality/codesnippet/CSharp/ca1043-use-integral-or-string-argument-for-indexers_1.cs)]
[!code-cpp[FxCop.Design.IntegralOrStringIndexers#1](../code-quality/codesnippet/CPP/ca1043-use-integral-or-string-argument-for-indexers_1.cpp)]
[!code-vb[FxCop.Design.IntegralOrStringIndexers#1](../code-quality/codesnippet/VisualBasic/ca1043-use-integral-or-string-argument-for-indexers_1.vb)]

## <a name="related-rules"></a>İlgili kuralları

- [CA1023: Dizin oluşturucular çok boyutlu olmamalıdır](../code-quality/ca1023-indexers-should-not-be-multidimensional.md)
- [CA1024: Uygun yerlerde özellikler kullan](../code-quality/ca1024-use-properties-where-appropriate.md)