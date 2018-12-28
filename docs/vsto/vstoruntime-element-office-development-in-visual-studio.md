---
title: "&lt;vstoRuntime&gt; öğesi (Visual Studio'da Office Geliştirme)"
ms.custom: ''
ms.date: 02/02/2017
ms.technology:
- office-development
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- application manifests [Office development in Visual Studio], <vstoRuntime> element
- <vstoRuntime> element
- vstoRuntime element
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: 80ef1c8e347aa2447ff48838015bb6499236e123
ms.sourcegitcommit: f6dd17b0864419083d0a1bf54910023045526437
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/27/2018
ms.locfileid: "53802676"
---
# <a name="ltvstoruntimegt-element-office-development-in-visual-studio"></a>&lt;vstoRuntime&gt; öğesi (Visual Studio'da Office Geliştirme)
  `vstoRuntime` Öğesinin `vstav3` ad alanı, belirli bir Office çözümü için Office çalışma zamanı için Visual Studio Araçları'nın desteklenen bir sürümünü içerir.

## <a name="syntax"></a>Sözdizimi

```xml
<vstoRuntime
    release
    version
    supportUrl />
```

## <a name="elements-and-attributes"></a>Öğeler ve öznitelikler
 `vstoRuntime` Öğesi gereklidir ve içinde `vstav3` ad alanı. Office çözümünü Office çalışma zamanı için Visual Studio Araçları'nın iki sürümü destekliyorsa, var olan iki `vstoRuntime` uygulama bildiriminde öğeler.

 `vstoRuntime` Öğesinde şu öznitelikler bulunur.

|Öznitelik|Açıklama|
|---------------|-----------------|
|`release`|Gerekli. Office çalışma zamanı için Visual Studio Araçları'nın sürümü.|
|`version`|Gerekli. Office çalışma zamanı için Visual Studio Araçları sürüm numarası.|
|`supportUrl`|İsteğe bağlı. Office çalışma zamanı için Visual Studio Araçları yükleme konumunu bağlayın.|

 `vstoRuntime` öğe yok.

## <a name="example"></a>Örnek
 Aşağıdaki kod örneğinde gösterilmiştir `vstoRuntime` öğesi kullanılarak dağıtılan bir Office çözümü için uygulama bildiriminde [!INCLUDE[ndptecclick](../vsto/includes/ndptecclick-md.md)]. Bu kod örneği, sağlanan daha büyük bir örneğin parçasıdır [Office çözümleri için uygulama bildirimleri](../vsto/application-manifests-for-office-solutions.md).

```xml
<vstav3:vstoRuntime
    release="VSTOR40Beta1"
    version="10.0.20303"
    supportUrl="http://www.microsoft.com" />
```

## <a name="see-also"></a>Ayrıca bkz.

- [Office çözümleri için uygulama bildirimleri](../vsto/application-manifests-for-office-solutions.md)
- [Office çözümleri için dağıtım bildirimleri](../vsto/deployment-manifests-for-office-solutions.md)
- [ClickOnce Uygulama bildirimi](../deployment/clickonce-application-manifest.md)
