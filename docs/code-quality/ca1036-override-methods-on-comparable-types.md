---
title: 'CA1036: Karşılaştırılabilir türlerde metotları geçersiz kıl'
ms.date: 03/11/2019
ms.topic: reference
f1_keywords:
- CA1036
- OverrideMethodsOnComparableTypes
helpviewer_keywords:
- OverrideMethodsOnComparableTypes
- CA1036
ms.assetid: 2329f844-4cb8-426d-bee2-cd065d1346d0
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: be340314afe36f3a930474f345715965f566b2d4
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71235998"
---
# <a name="ca1036-override-methods-on-comparable-types"></a>CA1036: Karşılaştırılabilir türlerde metotları geçersiz kıl

|||
|-|-|
|TypeName|OverrideMethodsOnComparableTypes|
|CheckId|CA1036|
|Kategori|Microsoft.Design|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep

Bir tür, <xref:System.IComparable?displayProperty=fullName> arabirimini uygular ve <xref:System.Object.Equals%2A?displayProperty=fullName> eşitlik, eşitsizlik, küçüktür veya büyüktür için dile özgü işleci aşırı yüklemez veya aşırı yüklemez. Tür, arabirimin yalnızca bir uygulamasını devralırsa kural bir ihlal raporlamaz.

Varsayılan olarak, bu kural yalnızca ortak ve korumalı türlere bakar, ancak bu [yapılandırılabilir](#configurability).

## <a name="rule-description"></a>Kural açıklaması

Özel bir sıralama düzeni tanımlayan türler <xref:System.IComparable> arabirimini uygular. <xref:System.IComparable.CompareTo%2A> Yöntemi, türün iki örneği için doğru sıralama düzenini gösteren bir tamsayı değeri döndürür. Bu kural bir sıralama düzeni belirleyen türleri tanımlar. Bir sıralama düzeni ayarlamak, eşitlik, eşitsizlik, daha az ve daha büyük bir deyişle bunun uygulanmayacağı anlamına gelir. Uygulamasının bir uygulamasını <xref:System.IComparable>sağladığınızda, ile <xref:System.IComparable.CompareTo%2A>tutarlı değerler döndürmesi için genellikle geçersiz <xref:System.Object.Equals%2A> kılmanız gerekir. ' İ geçersiz <xref:System.Object.Equals%2A> kılar ve işleç aşırı yüklerini destekleyen bir dilde kodlama yapıyorsanız, ile <xref:System.Object.Equals%2A>tutarlı işleçler sağlamanız gerekir.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Bu kural ihlalini onarmak için geçersiz kılın <xref:System.Object.Equals%2A>. Programlama diliniz işleç aşırı yüklemesini destekliyorsa, aşağıdaki işleçleri sağlayın:

- op_Equality
- op_Inequality
- op_LessThan
- op_GreaterThan

' C#De, bu işleçleri temsil etmek için kullanılan belirteçler aşağıdaki gibidir:

```csharp
==
!=
<
>
```

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

İhlalin eksik işleçlerden kaynaklanmış olması ve programlama diliniz, Visual Basic olduğu gibi, işleç aşırı yüklemesini desteklemediğine ilişkin bir uyarı CA1036. İşleçleri uygulamanın uygulama içeriğiniz üzerinde anlamlı olmadığını belirlerseniz, op_Equality dışındaki eşitlik işleçlerinde tetiklendiğinde bu kuraldan bir uyarının görüntülenmesini de güvenlidir. Ancak, geçersiz kıldıysanız <xref:System.Object.Equals%2A?displayProperty=nameWithType>op_Equality ve = = işlecini her zaman geçersiz kılmanız gerekir.

## <a name="configurability"></a>Yapılandırılabilirlik

Bu kuralı [FxCop çözümleyicilerinin](install-fxcop-analyzers.md) (eski analizler olmadan) çalıştırıyorsanız, kod tabanınızın hangi bölümlerinin bu kuralı çalıştırmak için erişilebilirliğini temel alarak yapılandırabilirsiniz. Örneğin, kuralın yalnızca genel olmayan API yüzeyine karşı çalışması gerektiğini belirtmek için, aşağıdaki anahtar-değer çiftini projenizdeki bir. editorconfig dosyasına ekleyin:

```ini
dotnet_code_quality.ca1036.api_surface = private, internal
```

Bu seçeneği yalnızca bu kural için, tüm kurallar için veya bu kategorideki tüm kurallar (tasarım) için yapılandırabilirsiniz. Daha fazla bilgi için bkz. [FxCop çözümleyicileri yapılandırma](configure-fxcop-analyzers.md).

## <a name="examples"></a>Örnekler

Aşağıdaki kod doğru şekilde uygulayan <xref:System.IComparable>bir tür içerir. Kod açıklamaları, <xref:System.Object.Equals%2A> <xref:System.IComparable> ve arabirimiyle ilgili çeşitli kuralları karşılayan yöntemleri belirler.

[!code-csharp[FxCop.Design.IComparable#1](../code-quality/codesnippet/CSharp/ca1036-override-methods-on-comparable-types_1.cs)]

Aşağıdaki uygulama kodu, daha önce gösterilen uygulamanın davranışını <xref:System.IComparable> sınar.

[!code-csharp[FxCop.Design.TestIComparable#1](../code-quality/codesnippet/CSharp/ca1036-override-methods-on-comparable-types_2.cs)]

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.IComparable?displayProperty=fullName>
- <xref:System.Object.Equals%2A?displayProperty=fullName>
- [Eşitlik işleçleri](/dotnet/standard/design-guidelines/equality-operators)