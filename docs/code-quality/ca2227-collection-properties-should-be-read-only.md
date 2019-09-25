---
title: 'CA2227: Koleksiyon özellikleri salt okunur olmalıdır'
ms.date: 09/28/2018
ms.topic: reference
f1_keywords:
- CA2227
- CollectionPropertiesShouldBeReadOnly
helpviewer_keywords:
- CA2227
- CollectionPropertiesShouldBeReadOnly
ms.assetid: 26967aaf-6fbe-438a-b4d3-ac579b5dc0f9
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
- CPP
ms.workload:
- multiple
ms.openlocfilehash: 3d097a67c9a62a6847ff6ab0bb882257c082ca6f
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71231309"
---
# <a name="ca2227-collection-properties-should-be-read-only"></a>CA2227: Koleksiyon özellikleri salt okunur olmalıdır

|||
|-|-|
|TypeName|CollectionPropertiesShouldBeReadOnly|
|CheckId|CA2227|
|Kategori|Microsoft. Usage|
|Son değişiklik|Yeni|

## <a name="cause"></a>Sebep

Dışarıdan görülebilen yazılabilir bir özellik, uygulayan <xref:System.Collections.ICollection?displayProperty=fullName>bir türdür. Bu kural dizileri, Dizin oluşturucular (adı ' Item ' olan Özellikler) ve izin kümelerini yoksayar.

## <a name="rule-description"></a>Kural açıklaması

Yazılabilir bir koleksiyon özelliği, kullanıcının koleksiyonu tamamen farklı bir koleksiyonla değiştirmesine izin verir. Salt okunurdur özelliği, koleksiyonun değiştirilmesini engeller, ancak yine de tekil üyelerin ayarlamaya izin verir. Koleksiyonu değiştirmek bir hedeftir, tercih edilen tasarım alanı, koleksiyondaki tüm öğeleri kaldırmak için bir yöntem ve koleksiyonu yeniden doldurmak için bir yöntem dahil olmaktır. Bu düzenin bir <xref:System.Collections.ArrayList.AddRange%2A> örneği için <xref:System.Collections.ArrayList?displayProperty=fullName> sınıfının veyöntemlerinebakın.<xref:System.Collections.ArrayList.Clear%2A>

Hem ikili hem de XML serileştirme koleksiyonları olan salt yazılır özellikleri destekler. Sınıfı <xref:System.Xml.Serialization.XmlSerializer?displayProperty=fullName> , <xref:System.Collections.ICollection> ve<xref:System.Collections.IEnumerable?displayProperty=fullName> seri hale getirilebilir olması için uygulayan türler için özel gereksinimlere sahiptir.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Bu kuralın ihlalini onarmak için, özelliği salt okunurdur yapın. Tasarım için gerekiyorsa, koleksiyonu temizlemek ve yeniden doldurmak için yöntemler ekleyin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Özellik [veri aktarımı nesne (DTO)](/previous-versions/msp-n-p/ff649585(v=pandp.10)) sınıfının bir parçasıysa, bu uyarıyı gizleyebilirsiniz.

Aksi takdirde, bu kuraldan gelen uyarıları engellemez.

## <a name="example"></a>Örnek

Aşağıdaki örnek, yazılabilir bir koleksiyon özelliğine sahip bir tür gösterir ve koleksiyonun nasıl doğrudan değiştirileceğini gösterir. Ayrıca, ve `Clear` `AddRange` yöntemlerini kullanarak salt okunurdur bir koleksiyon özelliğinin değiştirilmesi için tercih edilen yöntemi gösterir.

[!code-csharp[FxCop.Usage.PropertiesReturningCollections#1](../code-quality/codesnippet/CSharp/ca2227-collection-properties-should-be-read-only_1.cs)]
[!code-vb[FxCop.Usage.PropertiesReturningCollections#1](../code-quality/codesnippet/VisualBasic/ca2227-collection-properties-should-be-read-only_1.vb)]
[!code-cpp[FxCop.Usage.PropertiesReturningCollections#1](../code-quality/codesnippet/CPP/ca2227-collection-properties-should-be-read-only_1.cpp)]

## <a name="related-rules"></a>İlgili kurallar

- [CA1819 Özellikler diziler döndürmemelidir](../code-quality/ca1819-properties-should-not-return-arrays.md)