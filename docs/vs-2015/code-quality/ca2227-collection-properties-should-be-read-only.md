---
title: 'CA2227: Koleksiyon Özellikleri kimler yalnızca | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- CA2227
- CollectionPropertiesShouldBeReadOnly
helpviewer_keywords:
- CA2227
- CollectionPropertiesShouldBeReadOnly
ms.assetid: 26967aaf-6fbe-438a-b4d3-ac579b5dc0f9
caps.latest.revision: 19
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 3182a254ed5e22c560523911f87dc852708a9eb1
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54784177"
---
# <a name="ca2227-collection-properties-should-be-read-only"></a>CA2227: Koleksiyon özellikleri salt okunur olmalıdır
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|CollectionPropertiesShouldBeReadOnly|
|CheckId|CA2227|
|Kategori|Microsoft.Usage|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Dışarıdan görünen bir yazılabilir özelliği uygulayan bir tür olan <xref:System.Collections.ICollection?displayProperty=fullName>. Diziler, dizin oluşturucular (Özellikler) 'Öğesini' adı ile ve izin kümeleri, kural tarafından göz ardı edilir.

## <a name="rule-description"></a>Kural Tanımı
 Yazılabilir koleksiyon özelliği kullanıcının koleksiyonun tamamen farklı bir koleksiyon ile değiştirin izin verir. Salt okunur özelliği değiştirilmesini durdurur ancak yine de tekil üyelerin ayarlamasına izin verir. Bir hedef koleksiyonunu değiştirme varsa, tercih edilen tasarım deseni koleksiyondaki tüm öğeleri kaldırmak için bir yöntem ve koleksiyonu yeniden doldurmak için bir yöntem eklemektir. Bkz: <xref:System.Collections.ArrayList.Clear%2A> ve <xref:System.Collections.ArrayList.AddRange%2A> yöntemlerinin <xref:System.Collections.ArrayList?displayProperty=fullName> sınıfı bu düzeni gösteren bir örnek.

 İkili hem XML serileştirme koleksiyonlar salt okunur özelliklerini destekler. <xref:System.Xml.Serialization.XmlSerializer?displayProperty=fullName> Sınıfında uygulayan türler için belirli gereksinimler <xref:System.Collections.ICollection> ve <xref:System.Collections.IEnumerable?displayProperty=fullName> seri hale getirilebilir olması.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için özelliği salt okunur yapma ve tasarım gerektiriyorsa, Temizle ve koleksiyonu yeniden doldurmak için yöntemleri ekleyin.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek
 Aşağıdaki örnek, bir yazılabilir koleksiyon özelliğini türüyle gösterir ve koleksiyonunu nasıl doğrudan değiştirilebilir gösterir. Ayrıca, tercih edilen şekilde salt okunur koleksiyon özelliğini kullanarak değiştirme `Clear` ve `AddRange` yöntemleri gösterilmektedir.

 [!code-cpp[FxCop.Usage.PropertiesReturningCollections#1](../snippets/cpp/VS_Snippets_CodeAnalysis/FxCop.Usage.PropertiesReturningCollections/cpp/FxCop.Usage.PropertiesReturningCollections.cpp#1)]
 [!code-csharp[FxCop.Usage.PropertiesReturningCollections#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Usage.PropertiesReturningCollections/cs/FxCop.Usage.PropertiesReturningCollections.cs#1)]
 [!code-vb[FxCop.Usage.PropertiesReturningCollections#1](../snippets/visualbasic/VS_Snippets_CodeAnalysis/FxCop.Usage.PropertiesReturningCollections/vb/FxCop.Usage.PropertiesReturningCollections.vb#1)]

## <a name="related-rules"></a>İlgili kuralları
 [CA1819: Özellikler diziler döndürmemelidir](../code-quality/ca1819-properties-should-not-return-arrays.md)
