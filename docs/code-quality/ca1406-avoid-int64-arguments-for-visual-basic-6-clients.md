---
title: 'CA1406: Visual Basic 6 istemcileri için Int64 bağımsız değişkenlerinden kaçının'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- AvoidInt64ArgumentsForVB6Clients
- CA1406
helpviewer_keywords:
- AvoidInt64ArgumentsForVB6Clients
- CA1406
ms.assetid: d5d0d3fc-f105-43da-be5b-923ab023309c
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: 4dfcc612e931756b0e3d817556c9b37844bc3cfd
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68922033"
---
# <a name="ca1406-avoid-int64-arguments-for-visual-basic-6-clients"></a>CA1406: Visual Basic 6 istemcileri için Int64 bağımsız değişkenlerinden kaçının

|||
|-|-|
|TypeName|AvoidInt64ArgumentsForVB6Clients|
|CheckId|CA1406|
|Kategori|Microsoft. çalışabilirliği|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
Özellikle bileşen nesne modeli (com) tarafından görünür olarak işaretlenen bir tür, <xref:System.Int64?displayProperty=fullName> bağımsız değişken alan bir üye bildirir.

## <a name="rule-description"></a>Kural açıklaması
Visual Basic 6 COM istemcileri, 64-bit tamsayıya erişemiyor.

Varsayılan olarak, aşağıdakiler COM 'a görünür: derlemeler, ortak türler, ortak türlerdeki ortak örnek üyeleri ve tüm ortak değer türleri üyeleri. Ancak, hatalı pozitif sonuçları azaltmak için bu kural, türün COM görünürlüğünü açık bir şekilde ifade etmek için gereklidir; kapsayan bütünleştirilmiş kod <xref:System.Runtime.InteropServices.ComVisibleAttribute?displayProperty=fullName> , olarak `false` ayarlanmış olarak işaretlenmelidir ve türü olarak <xref:System.Runtime.InteropServices.ComVisibleAttribute> `true`kümesiyle işaretlenmelidir.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Değeri her zaman 32 bitlik bir integral olarak ifade edilebilir bir parametre için bu kural ihlalini onarmak için, parametre türünü olarak <xref:System.Int32?displayProperty=fullName>değiştirin. Parametrenin değeri 32 bitlik bir integral olarak ifade edilebileceğinden daha büyük olabilir, parametre türünü olarak <xref:System.Decimal?displayProperty=fullName>değiştirin. Hem hem de <xref:System.Single?displayProperty=fullName> <xref:System.Double?displayProperty=fullName> <xref:System.Int64> veri türünün üst aralıklarında duyarlık kaybı olduğunu unutmayın. Üyenin com 'a görünür olması belirtilmemişse, <xref:System.Runtime.InteropServices.ComVisibleAttribute> kümesini olarak `false`işaretleyin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Visual Basic 6 COM istemcilerinin türe erişememesi durumunda, bu kuraldan bir uyarının görüntülenmesini güvenli hale gelir.

## <a name="example"></a>Örnek
Aşağıdaki örnek, kuralı ihlal eden bir türü gösterir.

[!code-csharp[FxCop.Interoperability.LongArgument#1](../code-quality/codesnippet/CSharp/ca1406-avoid-int64-arguments-for-visual-basic-6-clients_1.cs)]
[!code-vb[FxCop.Interoperability.LongArgument#1](../code-quality/codesnippet/VisualBasic/ca1406-avoid-int64-arguments-for-visual-basic-6-clients_1.vb)]

## <a name="related-rules"></a>İlgili kurallar
[CA1413 COM görünebilir değer türlerinde genel olmayan alanlardan kaçının](../code-quality/ca1413-avoid-non-public-fields-in-com-visible-value-types.md)

[CA1407 COM görünebilir türler içinde statik üyelerden kaçının](../code-quality/ca1407-avoid-static-members-in-com-visible-types.md)

[CA1017 Derlemeleri ComVisibleAttribute ile işaretleyin](../code-quality/ca1017-mark-assemblies-with-comvisibleattribute.md)

## <a name="see-also"></a>Ayrıca bkz.

- [Yönetilmeyen Kod ile Birlikte Çalışma](/dotnet/framework/interop/index)
- [Long Veri Türü](/dotnet/visual-basic/language-reference/data-types/long-data-type)