---
title: "&lt;entryPoint&gt; öğesi (Visual Studio'da Office Geliştirme)"
titleSuffix: ''
ms.custom: seodec18
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- application manifests [Office development in Visual Studio], <entryPoint> element
- <entryPoint> element
- entryPoint element
author: John-Hart
ms.author: johnhart
manager: douge
ms.workload:
- office
ms.openlocfilehash: c99b6b052fcb411d3f5972d174f804f3000faabe
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53902135"
---
# <a name="ltentrypointgt-element-office-development-in-visual-studio"></a>&lt;entryPoint&gt; öğesi (Visual Studio'da Office Geliştirme)
  Her `entryPoint` öğesinin `vstav3` ad alanı, ne zaman çalıştırılması gerektiğini özelleştirme bütünleştirilmiş kodu tanımlayan bu [!INCLUDE[ndptecclick](../vsto/includes/ndptecclick-md.md)] uygulama yüklenir.

## <a name="syntax"></a>Sözdizimi

```xml
<entryPoint class>
    <assemblyIdentity />
</entryPoint>
```

## <a name="elements-and-attributes"></a>Öğeler ve öznitelikler
 `entryPoint` Öğesi gereklidir ve içinde `vstav3` ad alanı.

 Her `entryPoint` öğesi yalnızca bir özelleştirme bütünleştirilmiş kodu içerebilir. Birden çok da olabilir `entryPoint` uygulama bildiriminde tanımlanan öğeleri.

 `entryPoint` Öğesinde şu öznitelikler bulunur.

|Öznitelik|Açıklama|
|---------------|-----------------|
|`class`|Gerekli. Yürütülecek bir özelleştirme bütünleştirilmiş kodu tanımlar. Bu öznitelik sözdizimi *gt;NamespaceName.ClassName &*.|

 `entryPoint` şu öğe var.

### <a name="assemblyidentity"></a>assemblyIdentity
 Gerekli. `assemblyIdentity` Öğesinde `vstav3` ad alanı başvuruyor varolan `assemblyIdentity` öğesinde [!INCLUDE[ndptecclick](../vsto/includes/ndptecclick-md.md)] uygulama bildirimi.

 Rolü `assemblyIdentity` ve özniteliklerini tanımlanmış [ &#60;assemblyIdentity&#62; öğesi &#40;ClickOnce uygulaması&#41;](../deployment/assemblyidentity-element-clickonce-application.md).

## <a name="document-level-customization-example"></a>Belge düzeyi özelleştirmesi örneği

### <a name="description"></a>Açıklama
 Aşağıdaki kod örneğinde gösterilmiştir `entryPoint` bildiriminde bir uygulamada kullanılarak dağıtılan bir belge düzeyinde Office çözümü için [!INCLUDE[ndptecclick](../vsto/includes/ndptecclick-md.md)]. Bu kod örneği, sağlanan daha büyük bir örneğin parçasıdır [Office çözümleri için uygulama bildirimleri](../vsto/application-manifests-for-office-solutions.md).

### <a name="code"></a>Kod

```xml
<vstav3:entryPoint
  class="ContosoExcelWorkbook.ThisWorkbook">
  <assemblyIdentity
    name="ContosoExcelWorkbook"
    version="1.0.0.0"
    language="neutral"
    processorArchitecture="msil" />
</vstav3:entryPoint>
<vstav3:entryPoint
  class="ContosoExcelWorkbook.Sheet1">
  <assemblyIdentity
    name="ContosoExcelWorkbook"
    version="1.0.0.0"
    language="neutral"
    processorArchitecture="msil" />
</vstav3:entryPoint>
<vstav3:entryPoint
  class="ContosoExcelWorkbook.Sheet2">
  <assemblyIdentity
    name="ContosoExcelWorkbook"
    version="1.0.0.0"
    language="neutral"
    processorArchitecture="msil" />
</vstav3:entryPoint>
<vstav3:entryPoint
  class="ContosoExcelWorkbook.Sheet3">
  <assemblyIdentity
    name="ContosoExcelWorkbook"
    version="1.0.0.0"
    language="neutral"
    processorArchitecture="msil" />
</vstav3:entryPoint>
```

## <a name="vsto-add-in-example"></a>VSTO eklenti örneği

### <a name="description"></a>Açıklama
 Aşağıdaki kod örneğinde gösterilmiştir bir `entryPoint` öğesi kullanılarak dağıtılan bir uygulama düzeyinde Office çözümü için uygulama bildiriminde [!INCLUDE[ndptecclick](../vsto/includes/ndptecclick-md.md)]. Bu kod örneği, sağlanan daha büyük bir örneğin parçasıdır [Office çözümleri için uygulama bildirimleri](../vsto/application-manifests-for-office-solutions.md).

### <a name="code"></a>Kod

```xml
<vstav3:entryPoint
  class="ContosoOutlookAddIn.ThisAddIn">
  <assemblyIdentity
    name="ContosoOutlookAddIn"
    version="1.0.0.0"
    language="neutral"
    processorArchitecture="msil" />
</vstav3:entryPoint>
```

## <a name="see-also"></a>Ayrıca bkz.

- [Office çözümleri için uygulama bildirimleri](../vsto/application-manifests-for-office-solutions.md)
- [Office çözümleri için dağıtım bildirimleri](../vsto/deployment-manifests-for-office-solutions.md)
- [ClickOnce Uygulama bildirimi](../deployment/clickonce-application-manifest.md)