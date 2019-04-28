---
title: "&lt;vstoRuntime&gt; öğesi (Visual Studio'da Office Geliştirme)"
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- application manifests [Office development in Visual Studio], <vstoRuntime> element
- <vstoRuntime> element
- vstoRuntime element
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 98f483748cce9c3a053c800f9bdd6e0f3d651da2
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62982132"
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
