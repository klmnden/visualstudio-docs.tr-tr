---
title: 'CA1035: ICollection uygulamalarının kesin türde üyeleri vardır'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- ICollectionImplementationsHaveStronglyTypedMembers
- CA1035
helpviewer_keywords:
- CA1035
- ICollectionImplementationsHaveStronglyTypedMembers
ms.assetid: ad404eb5-cf6a-44b7-b78a-8ebfb654bc7f
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: a20feb514b87f2906fd4db32dfb38d3d9b661999
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68922824"
---
# <a name="ca1035-icollection-implementations-have-strongly-typed-members"></a>CA1035: ICollection uygulamalarının kesin türde üyeleri vardır

|||
|-|-|
|TypeName|ICollectionImplementationsHaveStronglyTypedMembers|
|CheckId|CA1035|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
Ortak veya korumalı bir tür uygular <xref:System.Collections.ICollection?displayProperty=fullName> , ancak için <xref:System.Collections.ICollection.CopyTo%2A?displayProperty=fullName>kesin olarak belirlenmiş bir yöntem sağlamaz. Türü kesin belirlenmiş olan <xref:System.Collections.ICollection.CopyTo%2A> sürümü iki parametreyi kabul etmelidir ve ilk parametresi <xref:System.Object?displayProperty=fullName> olarak <xref:System.Array?displayProperty=fullName> bir veya dizisine sahip olamaz.

## <a name="rule-description"></a>Kural açıklaması
Bu kural, <xref:System.Collections.ICollection> kullanıcıların, arabirim tarafından sunulan işlevleri kullanırken bağımsız değişkenleri <xref:System.Object> türüne dönüştürmeleri gerekmeden, kesin olarak belirlenmiş Üyeler sağlaması için uygulamalar gerektirir. Bu kural, uygulayan türün, daha <xref:System.Collections.ICollection> <xref:System.Object>güçlü bir tür örnek koleksiyonunu yönetmek için bunu uyguladığı varsayılır.

 <xref:System.Collections.ICollection><xref:System.Collections.IEnumerable?displayProperty=fullName> arabirimini uygular. Koleksiyondaki nesneler genişlemişlerse <xref:System.ValueType?displayProperty=fullName>, kutulamaktan kaynaklanan performansı azaltmaktan kaçınmak için, için <xref:System.Collections.IEnumerable.GetEnumerator%2A> kesin olarak belirlenmiş bir üye sağlamalısınız. Koleksiyonun nesneleri bir başvuru türü olduğunda bu gerekli değildir.

Bir arabirim üyesinin kesin türü belirtilmiş bir sürümünü uygulamak için, formdaki `InterfaceName.InterfaceMemberName` <xref:System.Collections.ICollection.CopyTo%2A>adları kullanarak arabirim üyelerini açıkça uygulayın. Açık arabirim üyeleri, arabirimi tarafından belirtilen veri türlerini kullanır. Arabirim üye adını <xref:System.Collections.ICollection.CopyTo%2A>(gibi) kullanarak türü kesin belirlenmiş üyeleri uygulayın. Kesin olarak belirlenmiş üyeleri ortak olarak bildirin ve koleksiyon tarafından yönetilen güçlü türde parametreleri ve dönüş değerlerini bildirin. Güçlü türler, <xref:System.Object> ve gibi daha <xref:System.Array> zayıf türler yerine arabirim tarafından bildirilmiştir.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kural ihlalini onarmak için arabirim üyesini açıkça uygulayın (olarak <xref:System.Collections.ICollection.CopyTo%2A>bildirin). Olarak `CopyTo`belirtilen public türü kesin belirlenmiş üyeyi ekleyin ve ilk parametresi olarak türü kesin belirlenmiş bir diziyi alır.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Yeni koleksiyonu genişleten türlerin güçlü türü belirlemesi için bir ikili ağaç gibi yeni bir nesne tabanlı koleksiyon uygularsanız, bu kuraldan bir uyarı gizleyin. Bu türler bu kurala uymalıdır ve türü kesin belirlenmiş üyeleri kullanıma sunmalıdır.

## <a name="example"></a>Örnek
Aşağıdaki örnek, uygulamak <xref:System.Collections.ICollection>için doğru yolu gösterir.

[!code-csharp[FxCop.Design.ICollectionStrongTypes#1](../code-quality/codesnippet/CSharp/ca1035-icollection-implementations-have-strongly-typed-members_1.cs)]

## <a name="related-rules"></a>İlgili kurallar
[CA1038 Numaralandırıcılar kesin bir şekilde yazılmalıdır](../code-quality/ca1038-enumerators-should-be-strongly-typed.md)

[CA1039 Listelerin türü kesin olarak belirlenmiş](../code-quality/ca1039-lists-are-strongly-typed.md)

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Array?displayProperty=fullName>
- <xref:System.Collections.IEnumerable?displayProperty=fullName>
- <xref:System.Collections.ICollection?displayProperty=fullName>
- <xref:System.Object?displayProperty=fullName>