---
title: "&lt;formRegion&gt; öğesi (Visual Studio'da Office Geliştirme)"
titleSuffix: ''
ms.custom: seodec18
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- application manifests [Office development in Visual Studio], <formRegion> element
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 33bc2ce58f90f37a1219427558a01bd13e5654df
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54875345"
---
# <a name="ltformregiongt-element-office-development-in-visual-studio"></a>&lt;formRegion&gt; öğesi (Visual Studio'da Office Geliştirme)
  `formRegion` Öğesinin `vstov4` ad alanı, VSTO eklentisi ile ilişkilendirilen bir Microsoft Office Outlook form bölgesi tanımlar.

## <a name="syntax"></a>Sözdizimi

```xml
<formRegion
  name>
  <messageClass
    name/>
</formRegion>
```

## <a name="elements-and-attributes"></a>Öğeler ve öznitelikler
 `formRegion` Öğesinin `vstov4` form bölgesini Outlook VSTO eklenti ile ilişkili ad alanı tanımlar. Yalnızca Outlook VSTO form bölgeleri içeren eklentileri için gereklidir.

 Birden çok da olabilir `formRegion` içinde tanımlanan öğeler bir `formRegions` tek bir VSTO eklentisi için öğe.

 `formRegion` Öğesi aşağıdaki özniteliklere sahiptir.

|Öznitelik|Açıklama|
|---------------|-----------------|
|`name`|Gerekli. Form bölgesi adı tanımlar.|

 `formRegion` Öğesi şu alt öğelerden sahiptir.

### <a name="messageclass"></a>iletisınıfı
 `messageClass` Öğesi form bölgesi ile ilişkili Outlook biçimini tanımlar.

 `messageClass` Öğesi aşağıdaki özniteliklere sahiptir.

|Öznitelik|Açıklama|
|---------------|-----------------|
|`name`|Gerekli. Form bölgesi ile ilişkili formu tanımlar.|

## <a name="example"></a>Örnek
 Aşağıdaki kod örneğinde gösterilmiştir bir `formRegion` Outlook VSTO kullanılarak dağıtılan eklenti için bir uygulama bildirimi öğesinde [!INCLUDE[ndptecclick](../vsto/includes/ndptecclick-md.md)]. Bu bir form bölgesi ile ilişkili üç ileti sınıfı vardır. Bu kod örneği, sağlanan daha büyük bir örneğin parçasıdır [Office çözümleri için uygulama bildirimleri](../vsto/application-manifests-for-office-solutions.md).

```xml
<vstov4:formRegion
    name="OutlookAddIn1.FormRegion1">
  <vstov4:messageClass name="IPM.Note" />
  <vstov4:messageClass name="IPM.Contact" />
  <vstov4:messageClass name="IPM.Appointment" />
</vstov4:formRegion>
```

## <a name="see-also"></a>Ayrıca bkz.

- [Outlook form bölgeleri oluşturma](../vsto/creating-outlook-form-regions.md)
- [Office çözümleri için uygulama bildirimleri](../vsto/application-manifests-for-office-solutions.md)
- [Office çözümleri için dağıtım bildirimleri](../vsto/deployment-manifests-for-office-solutions.md)
- [ClickOnce Uygulama bildirimi](../deployment/clickonce-application-manifest.md)