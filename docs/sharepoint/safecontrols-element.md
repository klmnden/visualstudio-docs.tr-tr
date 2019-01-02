---
title: SafeControls öğesi | Microsoft Docs
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- SafeControls element
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: e08b414858db389e507dc9395d218807c9530db6
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53875974"
---
# <a name="safecontrols-element"></a>SafeControls öğesi
  ASPX denetimleri ve herhangi bir SharePoint sitesinde ASPX sayfasında erişmek herhangi bir kullanıcı için güvenli olarak belirlenmiş Web Bölümleri koleksiyonu.  
  
## <a name="syntax"></a>Sözdizimi  
  
```xml  
<SafeControls>  
  <SafeControl.../>  
</SafeControls>  
```  
  
## <a name="attributes-and-elements"></a>Öznitelikler ve öğeler
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.  
  
### <a name="attributes"></a>Öznitelikler  
 Yok.  
  
### <a name="child-elements"></a>Alt öğeleri
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[SafeControl](../sharepoint/safecontrol-element.md)|İsteğe bağlı öğe.<br /><br /> ASPX denetim ya da herhangi bir SharePoint sitesinde ASPX sayfasında erişmek herhangi bir kullanıcı için güvenli olarak tasarlanmış bir Web Bölümü temsil eder.|  
  
### <a name="parent-elements"></a>Üst öğeler
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[ProjectItem](../sharepoint/projectitem-element.md)|Bir SharePoint proje öğesi temsil eder. Bu öğe gerekli kök öğe, *.spdata* dosya.|  
  
## <a name="remarks"></a>Açıklamalar  
 Güvenli denetimler hakkında daha fazla bilgi için bkz: [proje öğelerinde paketleme ve dağıtım bilgileri sağlayan](../sharepoint/providing-packaging-and-deployment-information-in-project-items.md).  
  
## <a name="element-information"></a>Öğe bilgileri
  
|||  
|-|-|  
|**Namespace**|HTTP<nolink>: //schemas.microsoft.com/VisualStudio/<br>SharePointTools/2010/SharePointProjectItemModel|  
|**Şema adı**|SharePoint proje öğesi şema|  
|**Doğrulama dosyası**|ProjectItemModelSchema.xsd|  
|**Boş olabilir**|Hayır|  
  
## <a name="see-also"></a>Ayrıca bkz.
 [SharePoint proje öğesi şema başvurusu](../sharepoint/sharepoint-project-item-schema-reference.md)   
 [Proje öğelerinde paketleme ve dağıtım bilgileri sağlayın](../sharepoint/providing-packaging-and-deployment-information-in-project-items.md)  
