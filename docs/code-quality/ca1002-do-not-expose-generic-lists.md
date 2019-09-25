---
title: 'CA1002: Genel listeleri gösterme'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- DoNotExposeGenericLists
- CA1002
helpviewer_keywords:
- CA1002
- DoNotExposeGenericLists
ms.assetid: 5caac810-1a79-47df-a27b-c46c5040bf34
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 0612886bf92a4ca6a30e5e15ae1c4a4950d9ddad
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71236665"
---
# <a name="ca1002-do-not-expose-generic-lists"></a>CA1002: Genel listeleri gösterme

|||
|-|-|
|TypeName|DoNotExposeGenericLists|
|CheckId|CA1002|
|Kategori|Microsoft.Design|
|Son değişiklik|Yeni|

## <a name="cause"></a>Sebep

Bir tür, bir türü olan <xref:System.Collections.Generic.List%601?displayProperty=fullName> , bir türü <xref:System.Collections.Generic.List%601> döndüren veya imzası bir <xref:System.Collections.Generic.List%601> parametre içeren dışarıdan görünür bir üye içeriyor.

## <a name="rule-description"></a>Kural açıklaması

<xref:System.Collections.Generic.List%601?displayProperty=fullName>, performans için tasarlanan ve devralmayla ilgili genel bir koleksiyondur. <xref:System.Collections.Generic.List%601>devralınan bir sınıfın davranışının değiştirilmesini kolaylaştıran sanal üyeler içermez. Aşağıdaki genel Koleksiyonlar devralma için tasarlanmıştır ve yerine <xref:System.Collections.Generic.List%601>sunulmalıdır.

- <xref:System.Collections.ObjectModel.Collection%601?displayProperty=fullName>

- <xref:System.Collections.ObjectModel.ReadOnlyCollection%601?displayProperty=fullName>

- <xref:System.Collections.ObjectModel.KeyedCollection%602?displayProperty=fullName>

- <xref:System.Collections.Generic.IList%601?displayProperty=fullName>

- <xref:System.Collections.Generic.ICollection%601?displayProperty=fullName>

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Bu kural ihlalini onarmak için, <xref:System.Collections.Generic.List%601?displayProperty=fullName> türü devralma için tasarlanan genel koleksiyonlardan biriyle değiştirin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Bu uyarıyı Başlatan derleme yeniden kullanılabilir bir kitaplık olmadığı için bu kuraldan bir uyarıyı bastırmayın. Örneğin, bir performans avantajı genel listeler kullanılarak kazanıldığı performansa göre ayarlanmış bir uygulamada bu uyarının görüntülenmesini güvenli hale gelir.

## <a name="related-rules"></a>İlgili kurallar

[CA1005 Genel türlerde aşırı parametrelerden kaçının](../code-quality/ca1005-avoid-excessive-parameters-on-generic-types.md)

[CA1010 Koleksiyonlar genel arabirimi uygulamalıdır](../code-quality/ca1010-collections-should-implement-generic-interface.md)

[CA1000 Genel türlerde statik üye bildirme](../code-quality/ca1000-do-not-declare-static-members-on-generic-types.md)

[CA1006 Üye imzalarında genel türleri iç içe kullanmayın](../code-quality/ca1006-do-not-nest-generic-types-in-member-signatures.md)

[CA1004 Genel metotlar tür parametresi sağlamalıdır](../code-quality/ca1004-generic-methods-should-provide-type-parameter.md)

[CA1003 Genel olay işleyici örnekleri kullan](../code-quality/ca1003-use-generic-event-handler-instances.md)

[CA1007 Uygun yerlerde genel türleri kullanın](../code-quality/ca1007-use-generics-where-appropriate.md)

## <a name="see-also"></a>Ayrıca bkz.

[Genel Türler](/dotnet/csharp/programming-guide/generics/index)
