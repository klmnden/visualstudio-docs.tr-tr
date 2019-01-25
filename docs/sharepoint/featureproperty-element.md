---
title: FeatureProperty öğesi | Microsoft Docs
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- FeatureProperty element
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 3c9407e78a32ad9f9d8ee4ecd1ae4462409decfc
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54867916"
---
# <a name="featureproperty-element"></a>FeatureProperty öğesi
  SharePoint'te dağıtıldığında bir özellikle birlikte eklenen değer özel bir özelliği temsil eder. Bir özellik dağıtıldıktan sonra kodunuzdaki özellik erişebilirsiniz.  
  
## <a name="syntax"></a>Sözdizimi  
  
```xml  
<FeatureProperty Key = "Key of the property value"  
    Value = "Property value" />  
```  
  
## <a name="attributes-and-elements"></a>Öznitelikler ve öğeler
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.  
  
### <a name="attributes"></a>Öznitelikler  
  
|Öznitelik|Açıklama|  
|---------------|-----------------|  
|**Key**|Gerekli **xs: String** özniteliği.<br /><br /> Depolamak ve özellik değerini almak için kullanılan anahtar. Her bir özellik, özelliğin benzersiz olan bir anahtar olması gerekir.|  
|**Değer**|Gerekli **xs: String** özniteliği.<br /><br /> Özellik değeri.|  
  
### <a name="child-elements"></a>Alt öğeleri
 Yok.  
  
### <a name="parent-elements"></a>Üst öğeler
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[FeatureProperties](../sharepoint/featureproperties-element.md)|SharePoint'te dağıtıldığında bir özellikle birlikte eklenen özellik değerleri koleksiyonunu temsil eder.|  
  
## <a name="remarks"></a>Açıklamalar  
 Özellik özellikleri hakkında daha fazla bilgi için bkz: [proje öğelerinde paketleme ve dağıtım bilgileri sağlama](../sharepoint/providing-packaging-and-deployment-information-in-project-items.md).  
  
## <a name="element-information"></a>Öğe bilgileri
  
|||  
|-|-|  
|**Namespace**|HTTP<nolink>: //schemas.microsoft.com/VisualStudio/<br>2010/SharePointTools/SharePointProjectItemModel|  
|**Şema adı**|SharePoint proje öğesi şema|  
|**Doğrulama dosyası**|ProjectItemModelSchema.xsd|  
|**Boş olabilir**|Hayır|  
  
## <a name="see-also"></a>Ayrıca bkz.
 [SharePoint proje öğesi şema başvurusu](../sharepoint/sharepoint-project-item-schema-reference.md)   
 [Proje öğelerinde paketleme ve dağıtım bilgileri sağlayın](../sharepoint/providing-packaging-and-deployment-information-in-project-items.md)  
