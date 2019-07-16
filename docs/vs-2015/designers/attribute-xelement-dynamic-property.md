---
title: Öznitelik (XElement dinamik özelliği) | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-designers
ms.topic: conceptual
ms.assetid: 8440fc7d-b3b4-4726-8ec8-492e6af79642
caps.latest.revision: 4
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: ced05b8da63f9a7a242b166fe64e9e44f78b8065
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68162684"
---
# <a name="attribute-xelement-dynamic-property"></a>Öznitelik (XElement dinamik özelliği)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Belirtilen genişletilmiş adı için karşılık gelen öznitelik örneği almak için kullanılan bir dizin oluşturucuyu alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
elem.Attribute[{namespaceName}attribName]  
```  
  
## <a name="property-valuereturn-value"></a>Özellik Değeri/Dönüş Değeri  
 Bir dizin oluşturucu türü `XAttribute Item(String expandedName)`. Bu dizin oluşturucu, belirtilen öznitelik genişletilmiş adını alır ve buna karşılık gelen döndürür <xref:System.Xml.Linq.XAttribute>, veya `null` varsa belirtilen ada sahip bir öznitelik yok.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu özellik değerine eşdeğer olan <xref:System.Xml.Linq.XElement.Attribute%2A> yöntemi <xref:System.Xml.Linq.XElement?displayProperty=fullName> sınıfı.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 <xref:System.Xml.Linq.XElement.Attribute%2A?displayProperty=fullName>   
 [XElement sınıfı dinamik özellikleri](../designers/xelement-class-dynamic-properties.md)   
 [Değer](../designers/value-xattribute-dynamic-property.md)
