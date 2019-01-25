---
title: ProjectOutputFile öğesi | Microsoft Docs
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- ProjectOutputFile element
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 69af1992ba07fb75859a8f71bd0ee3eecadeaa0d
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54865339"
---
# <a name="projectoutputfile-element"></a>ProjectOutputFile öğesi
  SharePoint'te dağıtıldığında ile proje öğesi eklemek için ayrı bir proje çıktısını temsil eder.  
  
## <a name="syntax"></a>Sözdizimi  
  
```xml  
<ProjectOutputFile ProjectId = "GUID of the project"  
    ProjectPath = "Relative path of the project"  
    Target = "Deployment path of the project output"  
    Type = "Type of deployment for the project output" />  
```  
  
## <a name="type"></a>Tür  
 **ProjectOutputFileType**  
  
## <a name="attributes-and-elements"></a>Öznitelikler ve öğeler
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.  
  
### <a name="attributes"></a>Öznitelikler  
  
|Öznitelik|Açıklama|  
|---------------|-----------------|  
|**Projectıd**|Gerekli **xs: String** özniteliği.<br /><br /> Eklemek istediğiniz bağımlı projenin çıktı olan GUID. Bu karşılık gelir **ProjectGuid** bağımlı proje dosyasında öğe.|  
|**ProjectPath**|Gerekli **xs: String** özniteliği.<br /><br /> Dahil etmek istediğiniz çıkış olan bağımlı projenin proje dosya adı dahil olmak üzere göreli yol. SharePoint proje öğesi içeren SharePoint projesinin kök klasörüne göreli yoludur.|  
|**Hedef**|İsteğe bağlı **xs: String** özniteliği.<br /><br /> Bağımlı proje çıktısı dağıtım kök klasörünün göreli SharePoint sunucusunda dağıtılıp bulunduğu yol. Dağıtım türü tarafından belirtilen dağıtım kök klasörü belirlenir **türü** özniteliği.<br /><br /> Daha fazla bilgi için açıklamalar için bkz. **dağıtım yolu** ve **dağıtım kökü** özelliklerini SharePoint Proje öğeleri [geliştirme SharePoint çözümleri](../sharepoint/developing-sharepoint-solutions.md).|  
|**Tür**|Gerekli **xs: String** özniteliği.<br /><br /> Bağımlı proje çıktısı için kullanılacak dağıtım türü. Açıklama için olası değerler hakkında daha fazla bilgi için bkz **dağıtım türü** özelliğin SharePoint proje öğelerinin [geliştirme SharePoint çözümleri](../sharepoint/developing-sharepoint-solutions.md).|  
  
### <a name="child-elements"></a>Alt öğeleri
 Yok.  
  
### <a name="parent-elements"></a>Üst öğeler
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[Dosyalar](../sharepoint/files-element.md)|SharePoint'te dağıtıldığında SharePoint proje öğesi ile dahil edilecek dosyalar belirtir.|  
  
## <a name="remarks"></a>Açıklamalar  
 Kullanım **ProjectOutputFile** bir projenin çıkışı SharePoint Proje öğesinin dağıtımına dahil edilecek öğe. Farklı bir proje veya proje öğesi içeren projenin belirtebilirsiniz. Daha fazla bilgi için [proje öğelerinde paketleme ve dağıtım bilgileri sağlayan](../sharepoint/providing-packaging-and-deployment-information-in-project-items.md).  
  
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
 [SharePoint çözümleri geliştirme](../sharepoint/developing-sharepoint-solutions.md)  
