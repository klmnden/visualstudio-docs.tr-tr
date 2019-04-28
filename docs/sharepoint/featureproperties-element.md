---
title: FeatureProperties öğesi | Microsoft Docs
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- FeatureProperties element
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 6860a91067daa6da1d4223ae5060385087ad3433
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62967337"
---
# <a name="featureproperties-element"></a>FeatureProperties öğesi
  SharePoint'te dağıtıldığında bir özellikle birlikte eklenen özellik değerleri koleksiyonu. Bir özellik dağıtıldıktan sonra kodunuzdaki özellik değerlerine erişebilirsiniz.

## <a name="syntax"></a>Sözdizimi

```xml
<FeatureProperties>
  <FeatureProperty.../>
</FeatureProperties>
```

## <a name="attributes-and-elements"></a>Öznitelikler ve öğeler
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.

### <a name="attributes"></a>Öznitelikler
 Yok.

### <a name="child-elements"></a>Alt öğeleri

|Öğe|Açıklama|
|-------------|-----------------|
|[FeatureProperty](../sharepoint/featureproperty-element.md)|İsteğe bağlı öğe.<br /><br /> Anahtar/değer biçimde özel bir özellik temsil eder.|

### <a name="parent-elements"></a>Üst öğeler

|Öğe|Açıklama|
|-------------|-----------------|
|[ProjectItem](../sharepoint/projectitem-element.md)|Bir SharePoint proje öğesi temsil eder. Bu öğe gerekli kök öğe, `.spdata` dosya.|

## <a name="remarks"></a>Açıklamalar
 Özellik özellikleri hakkında daha fazla bilgi için bkz: [proje öğelerinde paketleme ve dağıtım bilgileri sağlayan](../sharepoint/providing-packaging-and-deployment-information-in-project-items.md).

## <a name="element-information"></a>Öğe bilgileri

|Öğe|Açıklama|
|-------------|-----------------|
|**Namespace**|http:\/\/schemas.microsoft.com/VisualStudio/<br>2010/SharePointTools/SharePointProjectItemModel|
|**Şema adı**|SharePoint proje öğesi şema|
|**Doğrulama dosyası**|ProjectItemModelSchema.xsd|
|**Boş olabilir**|Hayır|

## <a name="see-also"></a>Ayrıca bkz.
- [SharePoint proje öğesi şema başvurusu](../sharepoint/sharepoint-project-item-schema-reference.md)
- [Proje öğelerinde paketleme ve dağıtım bilgileri sağlayın](../sharepoint/providing-packaging-and-deployment-information-in-project-items.md)
