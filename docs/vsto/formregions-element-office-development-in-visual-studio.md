---
title: "&lt;formRegions&gt; öğesi (Visual Studio'da Office Geliştirme)"
titleSuffix: ''
ms.custom: seodec18
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- formRegions element
- <formRegions> element
- application manifests [Office development in Visual Studio], <formRegions> element
author: John-Hart
ms.author: johnhart
manager: douge
ms.workload:
- office
ms.openlocfilehash: 997bd24861f986736d7d691a8d2877f9b5a78566
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53909105"
---
# <a name="ltformregionsgt-element-office-development-in-visual-studio"></a>&lt;formRegions&gt; öğesi (Visual Studio'da Office Geliştirme)
  `formRegions` Öğesinin `vstov4` ad alanı, VSTO eklentisi ile ilişkili olan Microsoft Office Outlook form bölgeleri içerir.

## <a name="syntax"></a>Sözdizimi

```xml
<formRegions>
  <formRegion>
  </formRegion>
</formRegions>
```

## <a name="elements-and-attributes"></a>Öğeler ve öznitelikler
 `formRegions` Öğesinin `vstov4` ad alanı içeren tüm `formRegion` bir Outlook VSTO eklentisi için öğeleri. Yalnızca Outlook VSTO form bölgeleri içeren eklentileri için gereklidir.

 Yalnızca bir `formRegions` uygulama bildiriminde tanımlanan öğe.

 `formRegions` Öğesi özniteliklere sahip değildir.

 `formRegions` Öğesinin şu öğe.

### <a name="formregion"></a>formRegion
 VSTO Outlook form bölgeleri içeren eklentileri için gereklidir. `formRegion` Öğe içinde tanımlanan [ &#60;formRegion&#62; öğesi &#40;Visual Studio'da Office geliştirme&#41;](../vsto/formregion-element-office-development-in-visual-studio.md).

## <a name="vsto-add-in-example"></a>VSTO eklenti örneği

### <a name="description"></a>Açıklama
 Aşağıdaki kod örneğinde gösterilmiştir bir `formRegions` öğesi kullanılarak dağıtılan bir uygulama düzeyinde Office çözümü için uygulama bildiriminde [!INCLUDE[ndptecclick](../vsto/includes/ndptecclick-md.md)]. Bu kod örneği, sağlanan daha büyük bir örneğin parçasıdır [Office çözümleri için uygulama bildirimleri](../vsto/application-manifests-for-office-solutions.md).

### <a name="code"></a>Kod

```xml
<vstov4:formRegions>
  <vstov4:formRegion
      name="OutlookAddIn1.FormRegion1">
    <vstov4:messageClass name="IPM.Note" />
    <vstov4:messageClass name="IPM.Contact" />
    <vstov4:messageClass name="IPM.Appointment" />
  </vstov4:formRegion>
</vstov4:formRegions>
```

## <a name="see-also"></a>Ayrıca bkz.

- [Office çözümleri için uygulama bildirimleri](../vsto/application-manifests-for-office-solutions.md)
- [Office çözümleri için dağıtım bildirimleri](../vsto/deployment-manifests-for-office-solutions.md)
- [ClickOnce Uygulama bildirimi](../deployment/clickonce-application-manifest.md)