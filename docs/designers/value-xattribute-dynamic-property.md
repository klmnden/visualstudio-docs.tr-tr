---
title: Değer (XAttribute dinamik özelliği)
ms.date: 11/04/2016
ms.topic: reference
apiname:
- XAttribute.Value
apitype: Assembly
ms.assetid: 019733d2-e050-4120-b537-831cd3fc008e
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: fe9127d4a7c691c34f15d399bd32f5e48cc6f0ed
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62892826"
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