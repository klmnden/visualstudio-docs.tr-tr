---
title: 'CA1059: Üyeler belirli somut türleri kullanıma sunmamalıdır'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA1059
- MembersShouldNotExposeCertainConcreteTypes
helpviewer_keywords:
- MembersShouldNotExposeCertainConcreteTypes
- CA1059
ms.assetid: 59f61f52-8d6c-49cb-aefb-191910523a3c
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 97ee4e11ceb3380c204d00203b9e81397a39e362
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71235472"
---
# <a name="ca1059-members-should-not-expose-certain-concrete-types"></a>CA1059: Üyeler belirli somut türleri kullanıma sunmamalıdır

|||
|-|-|
|TypeName|MembersShouldNotExposeCertainConcreteTypes|
|CheckId|CA1059|
|Kategori|Microsoft.Design|
|Son değişiklik|Yeni|

## <a name="cause"></a>Sebep
Dışarıdan görünür bir üye belirli bir somut türdür veya parametrelerinden biri veya dönüş değeri aracılığıyla belirli somut türleri gösterir. Şu anda, bu kural aşağıdaki somut türlerin görünürlüğünü raporlar:

- Öğesinden <xref:System.Xml.XmlNode?displayProperty=fullName>türetilmiş bir tür.

## <a name="rule-description"></a>Kural açıklaması
Somut tür tam bir uygulamaya sahiptir ve bu nedenle oluşturulabilecek bir türdür. Üyenin yaygın olarak kullanımına izin vermek için somut türü önerilen arabirimle değiştirin. Bu, üyenin arabirimini uygulayan veya arabirimi uygulayan bir türün beklendiği her türlü türü kabul etmesine izin verir.

Aşağıdaki tabloda hedeflenen somut türler ve bunların önerilen değiştirmeleri listelenmektedir.

|Somut tür|Başka|
|-------------------|-----------------|
|<xref:System.Xml.XPath.XPathDocument>|<xref:System.Xml.XPath.IXPathNavigable?displayProperty=fullName>.<br /><br /> Arabirimini kullanmak, üyeyi bir XML veri kaynağının belirli bir uygulamasından ayırır.|

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kural ihlalini onarmak için somut türü önerilen arabirimle değiştirin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Somut tür tarafından sunulan belirli işlevler gerekliyse, bu kuraldan gelen bir iletiyi gizlemek güvenlidir.

## <a name="related-rules"></a>İlgili kurallar
[CA1011 Temel türleri parametre olarak geçirmeyi düşünün](../code-quality/ca1011-consider-passing-base-types-as-parameters.md)