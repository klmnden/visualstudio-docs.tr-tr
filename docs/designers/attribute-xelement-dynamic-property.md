---
title: Öznitelik (XElement dinamik özelliği)
ms.date: 11/04/2016
ms.topic: reference
ms.assetid: 8440fc7d-b3b4-4726-8ec8-492e6af79642
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 0ec27fe2d7824ca32cbf97dbabac8b7ea6c4aed6
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55948504"
---
# <a name="attribute-xelement-dynamic-property"></a>Öznitelik (XElement dinamik özelliği)

Belirtilen genişletilmiş adı için karşılık gelen öznitelik örneği almak için kullanılan bir dizin oluşturucuyu alır.

## <a name="syntax"></a>Sözdizimi

```xaml
elem.Attribute[{namespaceName}attribName]
```

## <a name="property-valuereturn-value"></a>Özellik Değeri/Dönüş Değeri

Bir dizin oluşturucu türü `XAttribute Item(String expandedName)`. Bu dizin oluşturucu, belirtilen öznitelik genişletilmiş adını alır ve buna karşılık gelen döndürür <xref:System.Xml.Linq.XAttribute>, veya `null` varsa belirtilen ada sahip bir öznitelik yok.

## <a name="remarks"></a>Açıklamalar

Bu özellik değerine eşdeğer olan <xref:System.Xml.Linq.XElement.Attribute%2A> yöntemi <xref:System.Xml.Linq.XElement?displayProperty=fullName> sınıfı.

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Xml.Linq.XElement.Attribute%2A?displayProperty=fullName>
- [XElement Sınıfı Dinamik Özellikleri](../designers/xelement-class-dynamic-properties.md)
- [Değer](../designers/value-xattribute-dynamic-property.md)