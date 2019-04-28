---
title: Alt öğeler (XElement dinamik özelliği)
ms.date: 11/04/2016
ms.topic: reference
ms.assetid: 9611d00f-23bf-444b-ab0c-f30701bfc13d
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: fa3bf24178f1096cd05e8471c18f466fdd8ee17f
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62897683"
---
# <a name="descendants-xelement-dynamic-property"></a>Alt öğeler (XElement dinamik özelliği)

Belirtilen genişletilmiş adı ile eşleşen tüm azalan öğeleri geçerli öğenin almak için kullanılan bir dizin oluşturucuyu alır.

## <a name="syntax"></a>Sözdizimi

```xaml
elem.Descendants[{namespaceName}localName]
```

## <a name="property-valuereturn-value"></a>Özellik Değeri/Dönüş Değeri

Bir dizin oluşturucu türü `IEnumerable<XElement> Item(String expandedName)`. Bu dizin oluşturucu, belirtilen alt öğeleri genişletilmiş adını alır ve eşleşen alt öğeleri döndürür bir <xref:System.Collections.IEnumerable> `<` <xref:System.Xml.Linq.XElement> `>` koleksiyonu.

## <a name="remarks"></a>Açıklamalar

Bu özellik değerine eşdeğer olan <xref:System.Xml.Linq.XContainer.Descendants(System.Xml.Linq.XName)?displayProperty=fullName> yöntemi <xref:System.Xml.Linq.XContainer> sınıfı.

İade edilen koleksiyon içinde XML kaynak belge düzeninde öğeleridir.

Bu özellik, ertelenmiş yürütme kullanır.

## <a name="see-also"></a>Ayrıca bkz.

- [XElement sınıfı dinamik özellikleri](../designers/xelement-class-dynamic-properties.md)
- [Elements](../designers/elements-xelement-dynamic-property.md)