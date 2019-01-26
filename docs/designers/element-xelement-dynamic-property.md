---
title: Öğe (XElement dinamik özelliği)
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
apiname:
- XElement.Element
apitype: Assembly
ms.assetid: c6c25b8d-a1da-41ff-aeff-867ff1dcf749
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 520df74dae14fe672eb7d3db1bdc23a0a6437b16
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54976764"
---
# <a name="element-xelement-dynamic-property"></a>Öğe (XElement dinamik özelliği)

Alt almak için kullanılan bir dizin oluşturucu, belirtilen Genişletilmiş adı için karşılık gelen öğe örneğini alır.

## <a name="syntax"></a>Sözdizimi

```xaml
elem.Element[{namespaceName}localName]
```

## <a name="property-valuereturn-value"></a>Özellik Değeri/Dönüş Değeri

Bir dizin oluşturucu türü `XElement Item(String expandedName)`. Bu dizin oluşturucu genişletilmiş adı bir parametre alır ve buna karşılık gelen döndürür <xref:System.Xml.Linq.XElement>, veya `null` varsa belirtilen ada sahip bir öğe yok.

## <a name="remarks"></a>Açıklamalar

Bu özellik değerine eşdeğer olan <xref:System.Xml.Linq.XContainer.Element%2A> yöntemi <xref:System.Xml.Linq.XContainer?displayProperty=fullName> sınıfı.

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Xml.Linq.XContainer.Element%2A?displayProperty=fullName>
- [XElement sınıfı dinamik özellikleri](../designers/xelement-class-dynamic-properties.md)
- [Elements](../designers/elements-xelement-dynamic-property.md)