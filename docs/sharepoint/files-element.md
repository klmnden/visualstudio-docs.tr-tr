---
title: Öğe dosyaları | Microsoft Docs
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Files element
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 1cf64fc8f70c0a3cf3ed5df1237603f490a703db
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56639576"
---
# <a name="files-element"></a>Dosyalar öğesi
  SharePoint olmayan bağımlı proje çıktısı gibi özellik öğesi dosyaları SharePoint proje öğesi ile dağıtmak için dosyaları belirtir.

## <a name="syntax"></a>Sözdizimi

```xml
<Files>
  <ProjectItemFile.../>
  <ProjectOutputFile.../>
</Files>
```

## <a name="type"></a>Tür
 **FileCollectionType**

## <a name="attributes-and-elements"></a>Öznitelikler ve öğeler
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.

### <a name="attributes"></a>Öznitelikler
 Yok.

### <a name="child-elements"></a>Alt öğeleri

|Öğe|Açıklama|
|-------------|-----------------|
|[Projectıtemfile](../sharepoint/projectitemfile-element.md)|İsteğe bağlı **ProjectItemFileType** öğesi.<br /><br /> SharePoint'te dağıtıldığında proje öğesi ile eklenecek özellik öğesi dosyası gibi bir SharePoint dosyasını temsil eder.|
|[ProjectOutputFile](../sharepoint/projectoutputfile-element.md)|İsteğe bağlı **ProjectOutputFileType** öğesi.<br /><br /> SharePoint'te dağıtıldığında ile proje öğesi eklemek için bir proje çıktısını temsil eder.|

### <a name="parent-elements"></a>Üst öğeler

|Öğe|Açıklama|
|-------------|-----------------|
|[ProjectItem](../sharepoint/projectitem-element.md)|Bir SharePoint proje öğesi temsil eder. Bu öğe gerekli kök öğe, `.spdata` dosya.|

## <a name="element-information"></a>Öğe bilgileri

|||
|-|-|
|**Namespace**|HTTP<nolink>: //schemas.microsoft.com/VisualStudio/<br>2010/SharePointTools/SharePointProjectItemModel|
|**Şema adı**|SharePoint proje öğesi şema|
|**Doğrulama dosyası**|ProjectItemModelSchema.xsd|
|**Boş olabilir**|Hayır|

## <a name="see-also"></a>Ayrıca bkz.
- [SharePoint proje öğesi şema başvurusu](../sharepoint/sharepoint-project-item-schema-reference.md)
