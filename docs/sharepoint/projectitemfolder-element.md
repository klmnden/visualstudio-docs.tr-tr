---
title: Projectıtemfolder öğesi | Microsoft Docs
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- ProjectItemFolder element
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 2e179cd742d2fbf2f1fbff59610c4dda50f3f996
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56598972"
---
# <a name="projectitemfolder-element"></a>ProjectItemFolder öğesi
  Eşlenmiş bir klasörü temsil eder.

## <a name="syntax"></a>Sözdizimi

```xml
<ProjectItemFolder Target = "Path of SharePoint folder the mapped folder corresponds to"
    Type = "Type of deployment for the mapped folder" />
```

## <a name="type"></a>Tür
 **ProjectItemFolderType**

## <a name="attributes-and-elements"></a>Öznitelikler ve öğeler
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.

### <a name="attributes"></a>Öznitelikler

|Öznitelik|Açıklama|
|---------------|-----------------|
|**Hedef**|Gerekli **xs: dize** özniteliği.<br /><br /> Eşlenmiş klasör, dağıtım kök klasörünün göreli karşılık gelen SharePoint yükleme klasörünün yolu. Dağıtım türü tarafından belirtilen dağıtım kök klasörü belirlenir **türü** özniteliği.<br /><br /> Daha fazla bilgi için açıklamalar için bkz. **dağıtım yolu** ve **dağıtım kökü** özelliklerini SharePoint Proje öğeleri [geliştirme SharePoint çözümleri](../sharepoint/developing-sharepoint-solutions.md).|
|**Tür**|Gerekli **xs: String** özniteliği.<br /><br /> Eşlenmiş klasör için dağıtım türü. Açıklama için olası değerler hakkında daha fazla bilgi için bkz **dağıtım türü** özelliğin SharePoint proje öğelerinin [geliştirme SharePoint çözümleri](../sharepoint/developing-sharepoint-solutions.md).|

### <a name="child-elements"></a>Alt öğeleri
 Yok.

### <a name="parent-elements"></a>Üst öğeler

|Öğe|Açıklama|
|-------------|-----------------|
|[ProjectItem](../sharepoint/projectitem-element.md)|Bir SharePoint proje öğesi temsil eder. Gerekli kök öğesidir bu öğe *.spdata* dosya.|

## <a name="remarks"></a>Açıklamalar
 Eşlenen klasörler hakkında daha fazla bilgi için bkz: [nasıl yapılır: eşlenmiş klasörler ekleme ve kaldırma](../sharepoint/how-to-add-and-remove-mapped-folders.md).

## <a name="element-information"></a>Öğe bilgileri

|||
|-|-|
|**Namespace**|HTTP<nolink>: //schemas.microsoft.com/VisualStudio/2010/<br>SharePointTools/SharePointProjectItemModel|
|**Şema adı**|SharePoint proje öğesi şema|
|**Doğrulama dosyası**|ProjectItemModelSchema.xsd|
|**Boş olabilir**|Hayır|

## <a name="see-also"></a>Ayrıca bkz.
- [SharePoint proje öğesi şema başvurusu](../sharepoint/sharepoint-project-item-schema-reference.md)
- [Nasıl yapılır: eşlenmiş klasörler ekleme ve kaldırma](../sharepoint/how-to-add-and-remove-mapped-folders.md)
