---
title: 'CA1039: Listeler kesin türdedir'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA1039
- ListsAreStronglyTyped
helpviewer_keywords:
- CA1039
- ListsAreStronglyTyped
ms.assetid: 5ac366c4-fd87-4d5c-95d5-f755510c8e5c
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: fcc399457f4dde1c65836d9c9498c782ba92ecc2
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71235984"
---
# <a name="ca1039-lists-are-strongly-typed"></a>CA1039: Listeler kesin türdedir

|||
|-|-|
|TypeName|ListsAreStronglyTyped|
|CheckId|CA1039|
|Kategori|Microsoft.Design|
|Son değişiklik|Yeni|

## <a name="cause"></a>Sebep

Ortak veya korumalı tür uygular <xref:System.Collections.IList?displayProperty=fullName> , ancak aşağıdakilerden biri veya birkaçı için kesin olarak belirlenmiş bir yöntem sağlamaz:

- IList. Item

- IList. Add

- IList. Contains

- IList. IndexOf

- IList. Insert

- IList. Remove

## <a name="rule-description"></a>Kural açıklaması

Bu kural, <xref:System.Collections.IList> kullanıcıların, arabirim tarafından sunulan işlevleri kullanırken bağımsız değişkenleri <xref:System.Object?displayProperty=fullName> türüne dönüştürmeleri gerekmeden, türü kesin belirlenmiş Üyeler sağlamak için uygulamalar gerektirir. Arabirim <xref:System.Collections.IList> , dizin tarafından erişilebilen nesne koleksiyonları tarafından uygulanır. Bu kural, uygulayan <xref:System.Collections.IList> türün, daha <xref:System.Object>güçlü olan bir türün örnek koleksiyonunu yönettiğini varsayar.

<xref:System.Collections.IList><xref:System.Collections.ICollection?displayProperty=fullName> ve<xref:System.Collections.IEnumerable?displayProperty=fullName> arabirimlerini uygular. Uygulamasını uygularsanız <xref:System.Collections.ICollection>, için gerekli kesin olarak belirlenmiş üyeleri sağlamanız gerekir. <xref:System.Collections.IList> Koleksiyondaki nesneler genişlemişlerse <xref:System.ValueType?displayProperty=fullName>, kutulamayı neden olan performansın azalmasını önlemek için, için <xref:System.Collections.IEnumerable.GetEnumerator%2A> kesin olarak belirlenmiş bir üye sağlamalısınız; koleksiyonun nesneleri bir başvuru türü olduğunda bu gerekli değildir.

Bu kuralla uyum sağlamak için, ve gibi InterfaceName. InterfaceMemberName <xref:System.Collections.IList.Add%2A>biçimindeki adları kullanarak arabirim üyelerini açıkça uygulayın. Açık arabirim üyeleri, arabirimi tarafından belirtilen veri türlerini kullanır. Arabirim üye adını `Add`(gibi) kullanarak türü kesin belirlenmiş üyeleri uygulayın. Kesin olarak belirlenmiş üyeleri ortak olarak bildirin ve koleksiyon tarafından yönetilen güçlü türde parametreleri ve dönüş değerlerini bildirin. Güçlü türler, <xref:System.Object> ve gibi daha <xref:System.Array> zayıf türler yerine arabirim tarafından bildirilmiştir.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kuralın ihlalini onarmak için, üyeleri açık olarak <xref:System.Collections.IList> uygulayın ve daha önce belirtilen Üyeler için kesin olarak belirlenmiş alternatifler sağlayın. <xref:System.Collections.IList> Arabirimi doğru şekilde uygulayan ve gerekli kesin türü belirtilmiş üyeleri sağlayan kod için aşağıdaki örneğe bakın.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bağlantılı liste gibi yeni bir nesne tabanlı koleksiyon uygularken bu kuraldan bir uyarı göstermez, bu, yeni koleksiyonu genişleten türlerin güçlü türü belirlemesine neden olacak. Bu türler bu kurala uymalıdır ve türü kesin belirlenmiş üyeleri kullanıma sunmalıdır.

## <a name="example"></a>Örnek
Aşağıdaki örnekte, türü kesin belirlenmiş tüm `YourType` koleksiyonlar <xref:System.Collections.CollectionBase?displayProperty=fullName>olması gerektiği için tür genişletilir. <xref:System.Collections.CollectionBase>, sizin için <xref:System.Collections.IList> arabirimin açık uygulanmasını sağlar. Bu nedenle, ve <xref:System.Collections.IList> <xref:System.Collections.ICollection>için kesin olarak belirlenmiş üyeleri sağlamanız gerekir.

[!code-csharp[FxCop.Design.IListStrongTypes#1](../code-quality/codesnippet/CSharp/ca1039-lists-are-strongly-typed_1.cs)]

## <a name="related-rules"></a>İlgili kurallar
[CA1035 ICollection uygulamalarında kesin olarak yazılmış Üyeler var](../code-quality/ca1035-icollection-implementations-have-strongly-typed-members.md)

[CA1038 Numaralandırıcılar kesin bir şekilde yazılmalıdır](../code-quality/ca1038-enumerators-should-be-strongly-typed.md)

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Collections.CollectionBase?displayProperty=fullName>
- <xref:System.Collections.ICollection?displayProperty=fullName>
- <xref:System.Collections.IEnumerable?displayProperty=fullName>
- <xref:System.Collections.IList?displayProperty=fullName>
- <xref:System.Object?displayProperty=fullName>