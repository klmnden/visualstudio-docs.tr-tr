---
title: Öğeler (XElement dinamik özelliği) | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-designers
ms.topic: conceptual
api_name:
- XElement.Elements
api_type:
- Assembly
ms.assetid: 3d5737f2-d2ed-410a-821c-349dbb2b574f
caps.latest.revision: 4
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 158e200a33b4783df9f63f42a1eca7bb8957d449
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68145680"
---
# <a name="elements-xelement-dynamic-property"></a>Öğeler (XElement dinamik özelliği)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Geçerli öğenin belirtilen Genişletilmiş adı ile eşleşen alt öğeleri almak için kullanılan bir dizin oluşturucuyu alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
elem.Elements[{namespaceName}localName]   
```  
  
## <a name="property-valuereturn-value"></a>Özellik Değeri/Dönüş Değeri  
 Bir dizin oluşturucu türü `IEnumerable<XElement> Item(String expandedName)`. Bu dizin oluşturucu genişletilmiş adının istenen alt öğeleri alır ve eşleşen alt öğeleri döndürür bir <xref:System.Collections.IEnumerable> `<` <xref:System.Xml.Linq.XElement> `>` koleksiyonu.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu özellik değerine eşdeğer olan <xref:System.Xml.Linq.XContainer.Elements%28System.Xml.Linq.XName%29?displayProperty=fullName> yöntemi <xref:System.Xml.Linq.XContainer> sınıfı.  
  
 İade edilen koleksiyon içinde XML kaynak belge düzeninde öğeleridir.  
  
 Bu özellik, ertelenmiş yürütme kullanır.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [XElement sınıfı dinamik özellikleri](../designers/xelement-class-dynamic-properties.md)   
 [Öğesi](../designers/element-xelement-dynamic-property.md)   
 [Alt Öğeler](../designers/descendants-xelement-dynamic-property.md)
