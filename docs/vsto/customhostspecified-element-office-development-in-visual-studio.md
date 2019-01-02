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
manager: douge
ms.workload:
- office
ms.openlocfilehash: 0880e0ddf4763cf2c67c10871992a24b76f59ef2
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53896649"
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