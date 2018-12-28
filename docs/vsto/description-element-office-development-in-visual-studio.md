---
title: "&lt;Açıklama&gt; öğesi (Visual Studio'da Office Geliştirme)"
titleSuffix: ''
ms.custom: secdec18
ms.date: 02/02/2017
ms.technology:
- office-development
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- description element
- <description> element
- application manifests [Office development in Visual Studio], <description> element
author: John-Hart
ms.author: johnhart
manager: douge
ms.workload:
- office
ms.openlocfilehash: da75844d8c0aa1f39a639de77f916c948e64ea35
ms.sourcegitcommit: f6dd17b0864419083d0a1bf54910023045526437
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/27/2018
ms.locfileid: "53803941"
---
# <a name="ltdescriptiongt-element-office-development-in-visual-studio"></a>&lt;Açıklama&gt; öğesi (Visual Studio'da Office Geliştirme)
  `description` Öğesinin `vstov4` ad alanı, Microsoft Office uygulamasının COM eklentileri iletişim kutusunda görünen Office çözümünün açıklaması depolar.

## <a name="syntax"></a>Sözdizimi

```xml
<description>
</description>
```

## <a name="elements-and-attributes"></a>Öğeler ve öznitelikler
 İsteğe bağlı. `description` Öğe konusu `vstov4` ad alanı. Bu, Microsoft Office uygulamasının COM eklentileri iletişim kutusu görünür eklenti açıklamasını içerir.

 `description` Öğesinin öznitelikleri veya öğelerin yok.

## <a name="vsto-add-in-example"></a>VSTO eklenti örneği

### <a name="description"></a>Açıklama
 Aşağıdaki kod örneğinde gösterilmiştir `description` öğesi kullanılarak dağıtılan bir uygulama düzeyi çözümü [!INCLUDE[ndptecclick](../vsto/includes/ndptecclick-md.md)]. Bu kod örneği, sağlanan daha büyük bir örneğin parçasıdır [Office çözümleri için uygulama bildirimleri](../vsto/application-manifests-for-office-solutions.md).

### <a name="code"></a>Kod

```xml
<vstov4:description>
  ContosoOutlookAddIn - Outlook add-in
  created with Visual Studio Tools for Office
</vstov4:description>
```

## <a name="see-also"></a>Ayrıca bkz.

- [Office çözümleri için uygulama bildirimleri](../vsto/application-manifests-for-office-solutions.md)
- [Office çözümleri için dağıtım bildirimleri](../vsto/deployment-manifests-for-office-solutions.md)
- [ClickOnce Uygulama bildirimi](../deployment/clickonce-application-manifest.md)