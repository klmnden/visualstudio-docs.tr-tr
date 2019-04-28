---
title: "&lt;customHostSpecified&gt; öğesi (Visual Studio'da Office Geliştirme)"
titleSuffix: ''
ms.custom: seodec18
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- application manifests [Office development in Visual Studio], <customHostSpecified> element
- <customHostSpecified> element
- customHostSpecified element
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 26597796c99d3ab8740812819cf3aa5568e2985b
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62956185"
---
# <a name="ltcustomhostspecifiedgt-element-office-development-in-visual-studio"></a>&lt;customHostSpecified&gt; öğesi (Visual Studio'da Office Geliştirme)
  `customHostSpecified` Öğesi olmadığını Bu çözüm bağımsız bir uygulama olduğunu belirtir. Office çözümleri, Microsoft Office uygulamalarında barındırılan bileşenler içeriyor.

## <a name="syntax"></a>Sözdizimi

```xml
<customHostSpecified />
```

## <a name="elements-and-attributes"></a>Öğeler ve öznitelikler
 `customHostSpecified` Öğesi Office çözümleri için gereklidir. Bu öğe `co.v1` ad alanı ve bu dağıtım için özel bir ana bilgisayar içinde dağıtılan bir bileşen içerdiğini belirtir ve tek başına bir uygulama değildir.

 Bu öğenin ilk alt öğesidir `<entrypoint>` uygulama bildiriminde öğesi. Uygulamasındaki diğer alt öğe yok olabilir `<entrypoint>` öğesi veya [!INCLUDE[ndptecclick](../vsto/includes/ndptecclick-md.md)] yükleme sırasında bir doğrulama hatası verir.

 Bu öğenin öznitelikleri ve alt öğeleri var.

## <a name="example"></a>Örnek
 Aşağıdaki kod örneğinde gösterilmiştir `customHostSpecified` bir Office çözümü için uygulama bildiriminde öğesi. Bu kod örneği, sağlanan daha büyük bir örneğin parçasıdır [Office çözümleri için uygulama bildirimleri](../vsto/application-manifests-for-office-solutions.md).

```xml
<entryPoint>
    <co.v1:customHostSpecified />
</entryPoint>
```

## <a name="see-also"></a>Ayrıca bkz.

- [Office çözümleri için uygulama bildirimleri](../vsto/application-manifests-for-office-solutions.md)
- [Office çözümleri için dağıtım bildirimleri](../vsto/deployment-manifests-for-office-solutions.md)
- [ClickOnce Uygulama bildirimi](../deployment/clickonce-application-manifest.md)