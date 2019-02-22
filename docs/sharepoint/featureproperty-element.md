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
ms.openlocfilehash: 4bf3cbb84c32fdb3f5eba7ba8706c1035b1d9019
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56633479"
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
- [SharePoint proje öğesi şema başvurusu](../sharepoint/sharepoint-project-item-schema-reference.md)
- [Proje öğelerinde paketleme ve dağıtım bilgileri sağlayın](../sharepoint/providing-packaging-and-deployment-information-in-project-items.md)
