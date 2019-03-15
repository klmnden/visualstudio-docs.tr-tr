---
title: 'CA1010: Koleksiyonlar genel arabirimi uygulamalıdır'
ms.date: 03/11/2019
ms.topic: reference
f1_keywords:
- CA1010
- CollectionsShouldImplementGenericInterface
helpviewer_keywords:
- CA1010
- CollectionsShouldImplementGenericInterface
ms.assetid: c7d7126f-fa70-40be-8f93-3243e1760dc5
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: c71912fdd70226e1b4be3c14be7c4e0bac26259d
ms.sourcegitcommit: f7c401a376ce410336846835332a693e6159c551
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/14/2019
ms.locfileid: "57871908"
---
# <a name="ca1010-collections-should-implement-generic-interface"></a>CA1010: Koleksiyonlar genel arabirimi uygulamalıdır

|||
|-|-|
|TypeName|CollectionsShouldImplementGenericInterface|
|CheckId|CA1010|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep

Bir türün uyguladığı <xref:System.Collections.IEnumerable?displayProperty=fullName> arabirim ancak uygulamıyor <xref:System.Collections.Generic.IEnumerable%601?displayProperty=fullName> arabirimi ve içeren derleme hedefleri .NET. Bu kural uygulayan türler yoksayar <xref:System.Collections.IDictionary?displayProperty=fullName>.

Varsayılan olarak, bu kural yalnızca dışarıdan görülebilen türler görünür, ancak bu [yapılandırılabilir](#configurability).

## <a name="rule-description"></a>Kural açıklaması

Bir koleksiyon kullanılabilirliğini genişletmek için genel koleksiyon arabirimlerinden birini uygulayın. Ardından koleksiyonu, aşağıdaki gibi genel koleksiyon türlerini doldurmak için kullanılabilir:

- <xref:System.Collections.Generic.List%601?displayProperty=fullName>
- <xref:System.Collections.Generic.Queue%601?displayProperty=fullName>
- <xref:System.Collections.Generic.Stack%601?displayProperty=fullName>

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Bu kural ihlalini düzeltmek için aşağıdaki genel koleksiyon arabirimlerinden birini uygulayın:

- <xref:System.Collections.Generic.IEnumerable%601?displayProperty=fullName>
- <xref:System.Collections.Generic.ICollection%601?displayProperty=fullName>
- <xref:System.Collections.Generic.IList%601?displayProperty=fullName>

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Bu kuraldan bir uyarıyı bastırmak güvenlidir; Ancak, koleksiyon kullanımını daha sınırlı olacaktır.

## <a name="configurability"></a>Etkiler ve yapılandırma

Bu kuraldan çalıştırıyorsanız [FxCop Çözümleyicileri](install-fxcop-analyzers.md) (ve statik kod analizi üzerinden değil), hangi parçalarının yapılandırabilirsiniz, bu kuralı çalıştırmak için kod tabanı, kendi erişilebilirliği temel. Örneğin, kural yalnızca genel olmayan API yüzeyi karşı çalışması gerektiğini belirtmek için projenizi bir .editorconfig dosyasında şu anahtar-değer çifti ekleyin:

```
dotnet_code_quality.ca1010.api_surface = private, internal
```

Bu kategoride (tasarımı), bu seçenek yalnızca bu kural, tüm kuralları veya tüm kuralları yapılandırabilirsiniz. Daha fazla bilgi için [yapılandırma FxCop Çözümleyicileri](configure-fxcop-analyzers.md).

## <a name="example-violation"></a>Örnek ihlali

Aşağıdaki örnek, genel olmayan türeyen bir sınıf (başvuru türü) gösterir. `CollectionBase` sınıfını, bu kuralı ihlal ediyor.

[!code-csharp[FxCop.Design.CollectionsGenericViolation#1](../code-quality/codesnippet/CSharp/ca1010-collections-should-implement-generic-interface_1.cs)]

Bu kural ihlalini düzeltmek için aşağıdakilerden birini yapın:

- Genel arabirimler uygulayın.
- Temel sınıfı zaten gibi hem genel hem de genel olmayan arabirimleri uygulayan bir türe çeviremezsiniz `Collection<T>` sınıfı.

## <a name="fix-by-base-class-change"></a>Temel sınıf değişiklikten Düzelt

Aşağıdaki örnek genel olmayan koleksiyonu temel sınıfını değiştirerek ihlali giderir `CollectionBase` genel sınıfa `Collection<T>` (`Collection(Of T)` Visual Basic'te) sınıfı.

[!code-csharp[FxCop.Design.CollectionsGenericBase#1](../code-quality/codesnippet/CSharp/ca1010-collections-should-implement-generic-interface_2.cs)]

Zaten yayımlanmış bir sınıfın temel sınıf değiştirme, varolan tüketicilerde bozucu değişiklik olarak kabul edilir.

## <a name="fix-by-interface-implementation"></a>Arabirimi uygulama tarafından Düzelt

Aşağıdaki örnek bu genel arabirimler uygulayarak ihlali giderir: `IEnumerable<T>`, `ICollection<T>`, ve `IList<T>` (`IEnumerable(Of T)`, `ICollection(Of T)`, ve `IList(Of T)` Visual Basic'te).

[!code-csharp[FxCop.Design.CollectionsGenericInterface#1](../code-quality/codesnippet/CSharp/ca1010-collections-should-implement-generic-interface_3.cs)]

## <a name="related-rules"></a>İlgili kuralları

- [CA1005: Genel türlerde aşırı parametrelerden kaçının](../code-quality/ca1005-avoid-excessive-parameters-on-generic-types.md)
- [CA1000: Genel türlerde statik üyeleri bildirmeyin](../code-quality/ca1000-do-not-declare-static-members-on-generic-types.md)
- [CA1002: Genel listeleri gösterme](../code-quality/ca1002-do-not-expose-generic-lists.md)
- [CA1006: Üye imzalarında genel türleri iç içe kullanmayın](../code-quality/ca1006-do-not-nest-generic-types-in-member-signatures.md)
- [CA1004: Genel metotlar tür parametresi sağlamalıdır](../code-quality/ca1004-generic-methods-should-provide-type-parameter.md)
- [CA1003: Genel olay işleyici örnekleri kullan](../code-quality/ca1003-use-generic-event-handler-instances.md)
- [CA1007: Uygun yerlerde genel türleri kullanın](../code-quality/ca1007-use-generics-where-appropriate.md)

## <a name="see-also"></a>Ayrıca bkz.

- [Genel Türler](/dotnet/csharp/programming-guide/generics/index)