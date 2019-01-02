---
title: Extensiondataıtem öğesi | Microsoft Docs
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- ExtensionDataItem element
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: d95459be48b6d5e87b1a312e68e6ebea2645cb29
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53916945"
---
# <a name="extensiondataitem-element"></a>ExtensionDataItem öğesi
  Anahtar/değer biçiminde SharePoint proje öğesi ile ilişkili bir özel veri öğesi. Dize, anahtar ve değer olmalıdır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```xml  
<ExtensionDataItem Key = "Key of the data item"  
    Value = "Value of the data item" />  
```  
  
## <a name="attributes-and-elements"></a>Öznitelikler ve öğeler
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.  
  
### <a name="attributes"></a>Öznitelikler  
  
|Öznitelik|Açıklama|  
|---------------|-----------------|  
|**Key**|Gerekli **xs: dize** özniteliği.<br /><br /> Depolamak ve almak veri öğesi için kullanılan anahtar.|  
|**Değer**|Gerekli **xs: String** özniteliği.<br /><br /> Veriler öğesinin değeri.|  
  
### <a name="child-elements"></a>Alt öğeleri
 Yok.  
  
### <a name="parent-elements"></a>Üst öğeler
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[ExtensionData](../sharepoint/extensiondata-element.md)|SharePoint proje öğesi ile ilişkilendirilmiş özel veri öğelerinin bir koleksiyonunu temsil eder.|  
  
## <a name="remarks"></a>Açıklamalar  
 İlişkilendirdiğinizde özel veri sahip bir SharePoint proje öğesi kullanarak <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItem.ExtensionData%2A> özelliği bir <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItem> nesnesi, Visual Studio verileri yeni bir kaydeder **Extensiondataıtem** öğesinde `.spdata` dosya Proje öğesi. Daha fazla bilgi için [SharePoint Proje sisteminin uzantılarında veri kaydetme](../sharepoint/saving-data-in-extensions-of-the-sharepoint-project-system.md).  
  
## <a name="element-information"></a>Öğe bilgileri
  
|||  
|-|-|  
|**Namespace**|HTTP<nolink>: //schemas.microsoft.com/VisualStudio/<br>SharePointTools/2010/SharePointProjectItemModel| 
|**Şema adı**|SharePoint proje öğesi şema|  
|**Doğrulama dosyası**|ProjectItemModelSchema.xsd|  
|**Boş olabilir**|Hayır|  
  
## <a name="see-also"></a>Ayrıca bkz.
 [SharePoint proje öğesi şema başvurusu](../sharepoint/sharepoint-project-item-schema-reference.md)  
