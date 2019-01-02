---
title: Değer (XAttribute dinamik özelliği)
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
apiname:
- XAttribute.Value
apitype: Assembly
ms.assetid: 019733d2-e050-4120-b537-831cd3fc008e
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 2b97e33bdcb28a3c8790af752d5ab9786dc5ef3d
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53882899"
---
# <a name="value-xattribute-dynamic-property"></a>Değer (XAttribute dinamik özelliği)

Alır veya XML öznitelik değerini ayarlar.

## <a name="syntax"></a>Sözdizimi

```xaml
attrib.Value
```

## <a name="property-valuereturn-value"></a>Özellik değeri/dönüş değeri

A <xref:System.String> içeren bu özniteliğin değeri.

## <a name="exceptions"></a>Özel Durumlar

|Özel durum türü|Koşul|
| - |---------------|
|<xref:System.ArgumentNullException>|Ayarlarken `value` olduğu `null`.|

## <a name="remarks"></a>Açıklamalar

Bu özellik değerine eşdeğer olan <xref:System.Xml.Linq.XAttribute.Value%2A> özelliği <xref:System.Xml.Linq.XAttribute?displayProperty=fullName> sınıfı, ancak bu dinamik özellik de değişiklik bildirimleri destekler.

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Xml.Linq.XAttribute.Value%2A?displayProperty=fullName>
- [XAttribute sınıfı dinamik özellikleri](../designers/xattribute-class-dynamic-properties.md)
- [Öznitelik](../designers/attribute-xelement-dynamic-property.md)