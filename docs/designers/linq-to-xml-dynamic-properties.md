---
title: LINQ to XML dinamik özellikleri
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 0455f47c-4a68-4f2e-a3f8-dd1d85b99012
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 181e9e4fb86a0348c0b5adb1d26a0a4e4e1721bb
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55970718"
---
# <a name="linq-to-xml-dynamic-properties"></a>LINQ to XML dinamik özellikleri

Bu bölümde, XML dinamik özellikleri LINQ hakkında başvuru bilgileri sağlar. Özellikle, bu özellikleri tarafından kullanıma sunulan <xref:System.Xml.Linq.XAttribute> ve <xref:System.Xml.Linq.XElement> bulunan sınıfları, <xref:System.Xml.Linq> ad alanı.

Konu başlığı altında açıklandığı gibi [LINQ to XML ile genel bakış, WPF verilerini bağlama](../designers/wpf-data-binding-with-linq-to-xml-overview.md), dinamik özelliklerin her birini bir standart genel özelliğin veya aynı sınıftaki yöntemi eşdeğerdir. Bu standart üyeleri birçok amaç için kullanılması gereken; Dinamik özellikler, LINQ to XML veri bağlama senaryoları için özel olarak sağlanır. Bu sınıfların standart üyeleri hakkında daha fazla bilgi için bkz. <xref:System.Xml.Linq.XAttribute> ve <xref:System.Xml.Linq.XElement> başvuru konuları.

Çözümlenen değerlerine göre dinamik özellikler bu bölümün iki kategoriye ayrılır:

- Basit olanlar gibi `Value` özelliklerinde <xref:System.Xml.Linq.XAttribute> ve <xref:System.Xml.Linq.XElement> çözümlenmesi için tek bir değer sınıfları.

- Değerleri gibi dizine [öğeleri](../designers/elements-xelement-dynamic-property.md) ve [alt öğeleri](../designers/descendants-xelement-dynamic-property.md) özelliklerini <xref:System.Xml.Linq.XElement>, bir dizin oluşturucu türüne çözün. Dizin oluşturucu türleri istediğiniz değeri veya koleksiyona çözülmesi için bir genişletilmiş adı parametresi geçirilmelidir.

Dizinli bir değer türü döndüren Dinamik Özellikler <xref:System.Collections.Generic.IEnumerable%601> ertelenmiş yürütme kullanın. Ertelenmiş yürütme hakkında daha fazla bilgi için bkz: [(C#) LINQ sorgularına giriş](/dotnet/csharp/programming-guide/concepts/linq/introduction-to-linq-queries).

## <a name="reference"></a>Başvuru

- <xref:System.Xml.Linq>
- <xref:System.Xml.Linq.XElement?displayProperty=fullName>
- <xref:System.Xml.Linq.XAttribute?displayProperty=fullName>

## <a name="see-also"></a>Ayrıca bkz.

- [LINQ to XML ile WPF verilerini bağlama](../designers/wpf-data-binding-with-linq-to-xml-overview.md)
- [LINQ ile WPF verilerini bağlama XML genel bakış](../designers/wpf-data-binding-with-linq-to-xml-overview.md)
- [LINQ sorguları (C#) giriş](/dotnet/csharp/programming-guide/concepts/linq/introduction-to-linq-queries)
