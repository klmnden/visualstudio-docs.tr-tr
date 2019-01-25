---
title: SharePoint proje öğesi şema başvurusu | Microsoft Docs
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- FeatureProperty element
- SafeControls element
- SafeControl element
- .spdata files
- ExtensionData element
- FeatureProperties element
- ProjectOutputFile element
- Files element
- ProjectItemFolder element
- ProjectItemFile element
- ExtensionDataItem element
- ProjectItem element
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: c261115b21d1067b7494d09ad8031b3f4dc5a8c5
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54864923"
---
# <a name="sharepoint-project-item-schema-reference"></a>SharePoint proje öğesi şema başvurusu
  Visual Studio, içeriğini doğrulamak için SharePoint proje öğesi şema kullanır *.spdata* dosyaları. Bir *.spdata* dosya içeriğini ve bir SharePoint Proje öğesinin davranışını belirtir. SharePoint Proje öğeleri içeriği hakkında daha fazla bilgi için bkz. [öğe şablonları ve proje şablonları SharePoint Proje öğeleri için oluşturma](../sharepoint/creating-item-templates-and-project-templates-for-sharepoint-project-items.md).  
  
 SharePoint proje öğesi şema ProjectItemModelSchema.xsd olarak adlandırılır ve % Program Files (x86)%\Microsoft Visual Studio 11.0\Xml\Schemas. varsayılan olarak yüklenir  
  
 Kök öğe [ProjectItem](../sharepoint/projectitem-element.md) öğesi. Aşağıdaki tabloda şema tarafından tanımlanan tüm öğeleri açıklar.  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[ExtensionData](../sharepoint/extensiondata-element.md)|SharePoint proje öğesi ile ilişkilendirilmiş özel veri öğelerinin bir koleksiyonunu temsil eder.|  
|[Extensiondataıtem](../sharepoint/extensiondataitem-element.md)|Anahtar/değer biçiminde SharePoint proje öğesi ile ilişkili bir özel veri öğesini temsil eder. Dize, anahtar ve değer olmalıdır.|  
|[FeatureProperties](../sharepoint/featureproperties-element.md)|SharePoint'te dağıtıldığında bir özellikle birlikte eklenen özellik değerleri koleksiyonunu temsil eder. Bir özellik dağıtıldıktan sonra kodunuzdaki özellik değerlerine erişebilirsiniz.|  
|[FeatureProperty](../sharepoint/featureproperty-element.md)|SharePoint'te dağıtıldığında bir özellikle birlikte eklenen değer özel bir özelliği temsil eder. Bir özellik dağıtıldıktan sonra kodunuzdaki özellik erişebilirsiniz.|  
|[Dosyalar](../sharepoint/files-element.md)|Bir özellik öğe dosyası veya proje çıktısı gibi SharePoint proje öğesi ile dağıtmak için dosyaları belirtir.|  
|[ProjectItem](../sharepoint/projectitem-element.md)|Bir SharePoint proje öğesi temsil eder.|  
|[Projectıtemfile](../sharepoint/projectitemfile-element.md)|SharePoint'te dağıtıldığında proje öğesi ile eklenecek özellik öğesi dosyası gibi bir SharePoint dosyasını temsil eder.|  
|[Projectıtemfolder](../sharepoint/projectitemfolder-element.md)|Eşlenmiş bir klasörü temsil eder.|  
|[ProjectOutputFile](../sharepoint/projectoutputfile-element.md)|SharePoint'te dağıtıldığında ile proje öğesi eklemek için bir proje çıktısını temsil eder.|  
|[SafeControl](../sharepoint/safecontrol-element.md)|ASPX denetim ya da herhangi bir SharePoint sitesinde ASPX sayfasında erişmek herhangi bir kullanıcı için güvenli olarak tasarlanmış bir Web Bölümü temsil eder.|  
|[SafeControls](../sharepoint/safecontrols-element.md)|ASPX denetimleri ve Web bölümleri, herhangi bir SharePoint sitesinde ASPX sayfasında erişmek herhangi bir kullanıcı için güvenli olarak belirlenmiş bir koleksiyonunu temsil eder.|  
  
## <a name="see-also"></a>Ayrıca bkz.
 [Öğe şablonları ve SharePoint Proje öğeleri için proje şablonları oluşturma](../sharepoint/creating-item-templates-and-project-templates-for-sharepoint-project-items.md)  
