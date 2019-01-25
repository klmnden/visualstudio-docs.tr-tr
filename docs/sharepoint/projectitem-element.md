---
title: ProjectItem öğesi | Microsoft Docs
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- ProjectItem element
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 2d2736dbcde8708589b4918979acacfdafa34cc4
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54864287"
---
# <a name="projectitem-element"></a>ProjectItem öğesi
  Bir SharePoint proje öğesi temsil eder. Bu öğe gerekli kök öğe, *.spdata* dosya.  
  
## <a name="syntax"></a>Sözdizimi  
  
```xml  
<ProjectItem DefaultFile = "File that opens in the editor when you open the project item"  
    FeatureReceiverClass = "Class that implements a feature receiver for the project item"  
    FeatureReceiverAssembly = "Assembly that defines a feature receiver for the project item"  
    SupportedTrustLevels = "Trust levels that the project item supports"  
    SupportedDeploymentScopes = "Deployment scopes that the project item supports"  
    Type="Identifier for the project item">  
  <Files>...</Files>  
  <ProjectItemFolder>...</ProjectItemFolder>  
  <SafeControls>...</SafeControls>  
  <FeatureProperties>...</FeatureProperties>  
  <ExtensionData>...</ExtensionData>  
</ProjectItem>  
```  
  
## <a name="attributes-and-elements"></a>Öznitelikler ve öğeler
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.  
  
### <a name="attributes"></a>Öznitelikler  
  
|Öznitelik|Açıklama|  
|---------------|-----------------|  
|**DefaultFile**|İsteğe bağlı **xs: dize** özniteliği.<br /><br /> SharePoint proje öğesi içinde açtığınızda Visual Studio Düzenleyicisi'nde açılır dosyanın dosya adı dahil olmak üzere yolun göreli **Çözüm Gezgini**. İçeren klasöründen göreli yoludur *.spdata* dosya.|  
|**FeatureReceiverClass**|İsteğe bağlı **xs: String** özniteliği.<br /><br /> Bu SharePoint Proje öğesinin özellik alıcısı sınıfı tam adı. Özellik alıcıları hakkında daha fazla bilgi için bkz: [proje öğelerinde paketleme ve dağıtım bilgileri sağlayan](../sharepoint/providing-packaging-and-deployment-information-in-project-items.md).|  
|**FeatureReceiverAssembly**|İsteğe bağlı **xs: String** özniteliği.<br /><br /> Bu SharePoint Proje öğesinin özellik alıcısı tanımlayan bir derlemeye tam adını belirtir. Özellik alıcıları hakkında daha fazla bilgi için bkz: [proje öğelerinde paketleme ve dağıtım bilgileri sağlayan](../sharepoint/providing-packaging-and-deployment-information-in-project-items.md). Tam olarak nitelenmiş derleme adları hakkında daha fazla bilgi için bkz: [derleme adları](/dotnet/framework/app-domains/assembly-names).|  
|**SupportedTrustLevels**|İsteğe bağlı **xs: String** özniteliği.<br /><br /> Bu SharePoint proje öğesi destekleyen güven düzeyleri belirtir. Bu değer aşağıdaki dizelerini biri olabilir: Korumalı, FullTrust veya tüm. Değer Sandboxed hem FullTrust belirtir.<br /><br /> Atadığınız değerine karşılık gelen bir özel SharePoint proje öğesi türü içinde bu özniteliğin değeri <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemTypeDefinition.SupportedTrustLevels%2A> özelliği uygulamanızda <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemTypeProvider.InitializeType%2A> yöntemi. Bu öznitelik için farklı bir değer belirtirseniz, belirttiğiniz aynı güven düzeyine belirtir, böylece Visual Studio değerin üzerine yazar <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemTypeDefinition.SupportedTrustLevels%2A> özelliği.|  
|**SupportedDeploymentScopes**|İsteğe bağlı **xs: String** özniteliği.<br /><br /> Bu SharePoint proje öğesi destekleyen dağıtım kapsamları belirtir. Bu değer, bir veya daha fazla aşağıdaki dizelerden oluşan bir virgülle ayrılmış bir dizedir: Grup, Site, Web, WebApplication veya paket. Örneğin: `Web, Site`.<br /><br /> Atadığınız değerine karşılık gelen bir özel SharePoint proje öğesi türü içinde bu özniteliğin değeri <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemTypeDefinition.SupportedDeploymentScopes%2A> özelliği uygulamanızda <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemTypeProvider.InitializeType%2A> yöntemi. Bu öznitelik için farklı bir değer belirtirseniz, belirttiğiniz aynı güven düzeyine belirtir, böylece Visual Studio değerin üzerine yazar <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemTypeDefinition.SupportedDeploymentScopes%2A> özelliği.|  
|**Tür**|Gerekli **xs: String** özniteliği.<br /><br /> SharePoint proje öğesi için tanımlayıcı. Özel bir SharePoint proje öğesi türü içinde tanımlayıcı geçirdiğiniz dizedir <xref:Microsoft.VisualStudio.SharePoint.SharePointProjectItemTypeAttribute>. Daha fazla bilgi için [nasıl yapılır: Bir SharePoint proje öğesi türü tanımlayacağınızı](../sharepoint/how-to-define-a-sharepoint-project-item-type.md).<br /><br /> Visual Studio ile birlikte gelen yerleşik SharePoint Proje öğeleri için tanımlayıcılar listesi için bkz. [genişletmek SharePoint Proje öğeleri](../sharepoint/extending-sharepoint-project-items.md).|  
  
### <a name="child-elements"></a>Alt öğeleri
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[ExtensionData](../sharepoint/extensiondata-element.md)|İsteğe bağlı öğe.<br /><br /> SharePoint proje öğesi ile ilişkilendirilmiş özel veri öğelerinin bir koleksiyonunu temsil eder.<br /><br /> Yalnızca bir içerebilir **ExtensionData** öğesi.|  
|[FeatureProperties](../sharepoint/featureproperties-element.md)|İsteğe bağlı öğe.<br /><br /> SharePoint'te dağıtıldığında bir özellikle birlikte eklenen özellik değerleri koleksiyonunu temsil eder.<br /><br /> Yalnızca bir içerebilir **FeatureProperties** öğesi.|  
|[Dosyalar](../sharepoint/files-element.md)|İsteğe bağlı **FileCollectionType** öğesi.<br /><br /> SharePoint olmayan bağımlı proje çıktısı gibi özellik öğesi dosyaları SharePoint proje öğesi ile dağıtmak için dosyaları belirtir.<br /><br /> Ya da içeren bir **dosyaları** veya **Projectıtemfolder** öğesi, ancak ikisine birden değil.|  
|[Projectıtemfolder](../sharepoint/projectitemfolder-element.md)|İsteğe bağlı **ProjectItemFolderType** öğesi.<br /><br /> Eşlenmiş bir klasörü temsil eder.<br /><br /> Ya da içeren bir **dosyaları** veya **Projectıtemfolder** öğesi, ancak ikisine birden değil.|  
|[SafeControls](../sharepoint/safecontrols-element.md)|İsteğe bağlı öğe.<br /><br /> ASPX denetimleri ve Web bölümleri, herhangi bir SharePoint sitesinde ASPX sayfasında erişmek herhangi bir kullanıcı için güvenli olarak belirlenmiş bir koleksiyonunu temsil eder.<br /><br /> Yalnızca bir içerebilir **SafeControls** öğesi.|  
  
### <a name="parent-elements"></a>Üst öğeler
 Yok.  
  
## <a name="element-information"></a>Öğe bilgileri
  
|||  
|-|-|  
|**Namespace**|HTTP<nolink>: //schemas.microsoft.com/VisualStudio/<br>2010/SharePointTools/SharePointProjectItemModel|  
|**Şema adı**|SharePoint proje öğesi şema|  
|**Doğrulama dosyası**|ProjectItemModelSchema.xsd|  
|**Boş olabilir**|Hayır|  
  
## <a name="see-also"></a>Ayrıca bkz.
[SharePoint proje öğesi şema rseference](../sharepoint/sharepoint-project-item-schema-reference.md)  
