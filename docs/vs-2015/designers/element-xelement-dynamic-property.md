---
title: Öğe (XElement dinamik özelliği) | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-designers
ms.topic: conceptual
api_name:
- XElement.Element
api_type:
- Assembly
ms.assetid: c6c25b8d-a1da-41ff-aeff-867ff1dcf749
caps.latest.revision: 4
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: e7789a94c38f7c6d7db22d9214b19857e4c62055
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54753893"
---
# <a name="element-xelement-dynamic-property"></a>Öğe (XElement dinamik özelliği)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Alt almak için kullanılan bir dizin oluşturucu, belirtilen Genişletilmiş adı için karşılık gelen öğe örneğini alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
elem.Element[{namespaceName}localName]  
```  
  
## <a name="property-valuereturn-value"></a>Özellik Değeri/Dönüş Değeri  
 Bir dizin oluşturucu türü `XElement Item(String expandedName)`. Bu dizin oluşturucu genişletilmiş adı bir parametre alır ve buna karşılık gelen döndürür <xref:System.Xml.Linq.XElement>, veya `null` varsa belirtilen ada sahip bir öğe yok.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu özellik değerine eşdeğer olan <xref:System.Xml.Linq.XContainer.Element%2A> yöntemi <xref:System.Xml.Linq.XContainer?displayProperty=fullName> sınıfı.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 <xref:System.Xml.Linq.XContainer.Element%2A?displayProperty=fullName>   
 [XElement sınıfı dinamik özellikleri](../designers/xelement-class-dynamic-properties.md)   
 [Elements](../designers/elements-xelement-dynamic-property.md)
