---
title: Projectıtemfile öğesi | Microsoft Docs
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- ProjectItemFile element
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 73578d564714ff6e596dca62942f12e24589d235
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54867752"
---
# <a name="projectitemfile-element"></a>ProjectItemFile öğesi
  SharePoint'te dağıtıldığında proje öğesi ile eklenecek özellik öğesi dosyası gibi bir SharePoint dosyasını temsil eder.  
  
## <a name="syntax"></a>Sözdizimi  
  
```xml  
<ProjectItemFile Source = "Name of the file"  
    Target = "Deployment path of the file"  
    Type = "Type of deployment for the file" />  
```  
  
## <a name="type"></a>Tür  
 **ProjectItemFileType**  
  
## <a name="attributes-and-elements"></a>Öznitelikler ve öğeler
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.  
  
### <a name="attributes"></a>Öznitelikler  
  
|Öznitelik|Açıklama|  
|---------------|-----------------|  
|**Kaynak**|Gerekli **xs: String** özniteliği.<br /><br /> Proje öğesi ile dağıtmak için dosya adı.|  
|**Hedef**|İsteğe bağlı **xs: String** özniteliği.<br /><br /> Dosyanın SharePoint üzerinde dağıtım kök klasörünün göreli dağıtılacağı yolu. Dağıtım türü tarafından belirtilen dağıtım kök klasörü belirlenir **türü** özniteliği. Varsa **hedef** özniteliği belirtilmezse, belirtilen ada sahip dosyayı bir klasöre dağıtılacak **kaynak** özniteliği.<br /><br /> Daha fazla bilgi için açıklamalar için bkz. **dağıtım yolu** ve **dağıtım kökü** özelliklerini SharePoint Proje öğeleri [geliştirme SharePoint çözümleri](../sharepoint/developing-sharepoint-solutions.md).|  
|**Tür**|Gerekli **xs: String** özniteliği.<br /><br /> Dosya için dağıtım türü. Açıklama için olası değerler hakkında daha fazla bilgi için bkz **dağıtım türü** özelliğin SharePoint proje öğelerinin [geliştirme SharePoint çözümleri](../sharepoint/developing-sharepoint-solutions.md).|  
  
### <a name="child-elements"></a>Alt öğeleri
 Yok.  
  
### <a name="parent-elements"></a>Üst öğeler
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[Dosyalar](../sharepoint/files-element.md)|SharePoint'te dağıtıldığında SharePoint proje öğesi ile dahil edilecek dosyalar belirtir.|  
  
## <a name="remarks"></a>Açıklamalar  
 Tipik olarak anılan SharePoint dosyaları **Projectıtemfile** öğelerini özellik öğesi dosyaları içerir (*Elements.xml*), liste tanımları için şema dosyalarını (*Schema.xml*) ve Web bölümleri için Web Bölümü tanım dosyalarını (*.webpart*).  
  
## <a name="element-information"></a>Öğe bilgileri
  
|||  
|-|-|  
|**Namespace**|HTTP<nolink>: //schemas.microsoft.com/VisualStudio/<br>2010/SharePointTools/SharePointProjectItemModel|  
|**Şema adı**|SharePoint proje öğesi şema|  
|**Doğrulama dosyası**|ProjectItemModelSchema.xsd|  
|**Boş olabilir**|Hayır|  
  
## <a name="see-also"></a>Ayrıca bkz.
 [SharePoint proje öğesi şema başvurusu](../sharepoint/sharepoint-project-item-schema-reference.md)  
