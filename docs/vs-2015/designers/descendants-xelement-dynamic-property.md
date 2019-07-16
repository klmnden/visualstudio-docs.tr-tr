---
title: Alt öğeler (XElement dinamik özelliği) | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-designers
ms.topic: conceptual
ms.assetid: 9611d00f-23bf-444b-ab0c-f30701bfc13d
caps.latest.revision: 4
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 8c89e04346a4b08d6ee7bbc0012ef52f3b648512
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68178206"
---
# <a name="descendants-xelement-dynamic-property"></a>Alt öğeler (XElement dinamik özelliği)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Belirtilen genişletilmiş adı ile eşleşen tüm azalan öğeleri geçerli öğenin almak için kullanılan bir dizin oluşturucuyu alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
elem.Descendants[{namespaceName}localName]  
```  
  
## <a name="property-valuereturn-value"></a>Özellik Değeri/Dönüş Değeri  
 Bir dizin oluşturucu türü `IEnumerable<XElement> Item(String expandedName)`. Bu dizin oluşturucu, belirtilen alt öğeleri genişletilmiş adını alır ve eşleşen alt öğeleri döndürür bir <xref:System.Collections.IEnumerable> `<` <xref:System.Xml.Linq.XElement> `>` koleksiyonu.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu özellik değerine eşdeğer olan <xref:System.Xml.Linq.XContainer.Descendants%28System.Xml.Linq.XName%29?displayProperty=fullName> yöntemi <xref:System.Xml.Linq.XContainer> sınıfı.  
  
 İade edilen koleksiyon içinde XML kaynak belge düzeninde öğeleridir.  
  
 Bu özellik, ertelenmiş yürütme kullanır.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [XElement sınıfı dinamik özellikleri](../designers/xelement-class-dynamic-properties.md)   
 [Elements](../designers/elements-xelement-dynamic-property.md)
