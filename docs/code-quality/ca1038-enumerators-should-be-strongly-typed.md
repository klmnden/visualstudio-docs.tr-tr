---
title: 'CA1038: Numaralandırıcıların kesin türü belirtilmiş olmalıdır'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- EnumeratorsShouldBeStronglyTyped
- CA1038
helpviewer_keywords:
- EnumeratorsShouldBeStronglyTyped
- CA1038
ms.assetid: 8919f526-d487-42a4-87dc-2b2ee25260c4
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 2dae77bf7783edc165305f9b3ba60969d4f126a8
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68922888"
---
# <a name="ca1038-enumerators-should-be-strongly-typed"></a>CA1038: Numaralandırıcıların kesin türü belirtilmiş olmalıdır

|||
|-|-|
|TypeName|EnumeratorsShouldBeStronglyTyped|
|CheckId|CA1038|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
Ortak veya korumalı bir tür, <xref:System.Collections.IEnumerator?displayProperty=fullName> <xref:System.Collections.IEnumerator.Current%2A?displayProperty=fullName> özelliğinin kesin türü belirtilmiş bir sürümünü uygular ancak sağlamaz. Aşağıdaki türlerden türetilmiş türler bu kuraldan muaf tutulur:

- <xref:System.Collections.CollectionBase?displayProperty=fullName>

- <xref:System.Collections.DictionaryBase?displayProperty=fullName>

- <xref:System.Collections.ReadOnlyCollectionBase?displayProperty=fullName>

## <a name="rule-description"></a>Kural açıklaması
Bu kural, <xref:System.Collections.IEnumerator> kullanıcıların, arabirim tarafından sunulan işlevleri kullandıklarında döndürülen değeri güçlü <xref:System.Collections.IEnumerator.Current%2A> türe dönüştürmek için gerekli olmaması için, uygulamaların kesin türü belirtilmiş bir sürümünü de sağlaması gerekir. Bu kural, uygulayan <xref:System.Collections.IEnumerator> türün, daha <xref:System.Object>güçlü olan bir türün örnek koleksiyonunu içerdiğini varsayar.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kural ihlalini onarmak için Interface özelliğini açıkça uygulayın (olarak `IEnumerator.Current`bildirin). Özelliğin kesin türü belirtilmiş bir sürümünü ekleyin, olarak `Current`ve türü kesin belirlenmiş bir nesne döndürmesini sağlayabilirsiniz.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bir ikili ağaç gibi nesne tabanlı bir koleksiyonla birlikte kullanmak üzere nesne tabanlı bir Numaralandırıcı uyguladığınızda bu kuraldan bir uyarı gizleyin. Yeni koleksiyonu genişleten türler kesin türü belirtilmiş Numaralandırıcı tanımlar ve kesin türü belirtilmiş özelliği sunar.

## <a name="example"></a>Örnek
Aşağıdaki örnek, türü kesin belirlenmiş <xref:System.Collections.IEnumerator> bir tür uygulamak için doğru yolu gösterir.

[!code-csharp[FxCop.Design.IEnumeratorStrongTypes#1](../code-quality/codesnippet/CSharp/ca1038-enumerators-should-be-strongly-typed_1.cs)]

## <a name="related-rules"></a>İlgili kurallar
[CA1035 ICollection uygulamalarında kesin olarak yazılmış Üyeler var](../code-quality/ca1035-icollection-implementations-have-strongly-typed-members.md)

[CA1039 Listelerin türü kesin olarak belirlenmiş](../code-quality/ca1039-lists-are-strongly-typed.md)

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Collections.IEnumerator?displayProperty=fullName>
- <xref:System.Collections.CollectionBase?displayProperty=fullName>
- <xref:System.Collections.DictionaryBase?displayProperty=fullName>
- <xref:System.Collections.ReadOnlyCollectionBase?displayProperty=fullName>