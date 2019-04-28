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
ms.openlocfilehash: 12b00c202373310b04021a46e74af2af7e10d535
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62779002"
---
# <a name="ca1036-override-methods-on-comparable-types"></a>CA1036: Karşılaştırılabilir türlerde metotları geçersiz kıl

|||
|-|-|
|TypeName|OverrideMethodsOnComparableTypes|
|CheckId|CA1036|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep

Bir türün uyguladığı <xref:System.IComparable?displayProperty=fullName> arabirim ve geçersiz <xref:System.Object.Equals%2A?displayProperty=fullName> veya dile özgü işleci eşitlik, eşitsizlik durumu olabilir, daha az aşırı değil-daha küçük veya büyük-daha. Türü arabiriminin bir uygulamasını devralırsa kuralı ihlal raporlamaz.

Varsayılan olarak, bu kural yalnızca genel ve korumalı türler görünür, ancak bu [yapılandırılabilir](#configurability).

## <a name="rule-description"></a>Kural açıklaması

Özel sıralama düzenini tanımlamak türleri uygulayan <xref:System.IComparable> arabirimi. <xref:System.IComparable.CompareTo%2A> Yöntem türü iki örneği için doğru sıralama düzenini belirten bir tamsayı değeri döndürür. Bu kural, bir sıralama düzeni kümesi türlerini tanımlar. Gelir bir sıralama düzeni ayarı olağan anlamını eşitlik, eşitsizlik durumu olabilir, daha az-daha küçük ve büyük-daha geçerli değildir. Bir uygulamasını sağlaması zaman <xref:System.IComparable>, genellikle gerekir ayrıca geçersiz <xref:System.Object.Equals%2A> ile tutarlı olan değerler döndürür, böylece <xref:System.IComparable.CompareTo%2A>. Kılarsanız <xref:System.Object.Equals%2A> ve Kodladığınız İşleç aşırı yüklemeleri destekler bir dilde tutarlı işleçleri de sağlamalıdır <xref:System.Object.Equals%2A>.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Bu kural ihlalini düzeltmek için geçersiz kılın <xref:System.Object.Equals%2A>. İşleç aşırı yüklemesi programlama dilini destekler, aşağıdaki işleçleri sağlayın:

- op_Equality
- op_Inequality
- op_LessThan
- op_GreaterThan

C# içinde bu işleçler temsil etmek için kullanılan belirteçleri aşağıda belirtilmiştir:

```csharp
==
!=
<
>
```

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Visual Basic ile olduğu gibi İşleç aşırı yüklemesi, işleçler ve programlama dilini eksik ihlali neden olduğu CA1036 desteklemiyor kuraldan bir uyarıyı bastırmak güvenlidir. İşleçler uygulama, uygulama bağlamında anlamsız olduğunu belirlerseniz, ayrıca op_Equality farklı eşitlik operatörleri başlatıldığında bu kuraldan bir uyarıyı bastırmak güvenlidir. Ancak, her zaman op_Equality geçersiz kılmalıdır ve kılarsanız == işleci <xref:System.Object.Equals%2A?displayProperty=nameWithType>.

## <a name="configurability"></a>Etkiler ve yapılandırma

Bu kuraldan çalıştırıyorsanız [FxCop Çözümleyicileri](install-fxcop-analyzers.md) (ve statik kod analizi üzerinden değil), hangi parçalarının yapılandırabilirsiniz, bu kuralı çalıştırmak için kod tabanı, kendi erişilebilirliği temel. Örneğin, kural yalnızca genel olmayan API yüzeyi karşı çalışması gerektiğini belirtmek için projenizi bir .editorconfig dosyasında şu anahtar-değer çifti ekleyin:

```
dotnet_code_quality.ca1036.api_surface = private, internal
```

Bu kategoride (tasarımı), bu seçenek yalnızca bu kural, tüm kuralları veya tüm kuralları yapılandırabilirsiniz. Daha fazla bilgi için [yapılandırma FxCop Çözümleyicileri](configure-fxcop-analyzers.md).

## <a name="examples"></a>Örnekler

Aşağıdaki kodu doğru uygulayan bir tür içeren <xref:System.IComparable>. Kod açıklamaları için ilgili çeşitli kuralları karşılayan yöntemleri tanımlamak <xref:System.Object.Equals%2A> ve <xref:System.IComparable> arabirimi.

[!code-csharp[FxCop.Design.IComparable#1](../code-quality/codesnippet/CSharp/ca1036-override-methods-on-comparable-types_1.cs)]

Aşağıdaki uygulama kodu davranışını testleri <xref:System.IComparable> daha önce gösterilen uygulama.

[!code-csharp[FxCop.Design.TestIComparable#1](../code-quality/codesnippet/CSharp/ca1036-override-methods-on-comparable-types_2.cs)]

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.IComparable?displayProperty=fullName>
- <xref:System.Object.Equals%2A?displayProperty=fullName>
- [Eşitlik işleçleri](/dotnet/standard/design-guidelines/equality-operators)