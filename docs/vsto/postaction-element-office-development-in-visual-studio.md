---
title: "&lt;postAction&gt; öğesi (Visual Studio'da Office Geliştirme)"
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- application manifests [Office development in Visual Studio], <postAction> element
- <postAction> element
- postAction element
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 53cf47ef9a78ebb54c377e19b4f7fbad444bbfcd
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62976527"
---
# <a name="ltpostactiongt-element-office-development-in-visual-studio"></a>&lt;postAction&gt; öğesi (Visual Studio'da Office Geliştirme)
  `postAction` Öğesinin `vstav3` ad alanı içerir `entrypoint` öğeleri ve tüm `postActionData` Office çözümleri yüklendikten sonra çalışan dağıtım sonrası eylemleri ile ilişkili olan öğeler.

## <a name="syntax"></a>Sözdizimi

```xml
<postAction>
  <entryPoint>
  </entryPoint>
  <postActionData>
  </postActionData>
</postAction>
```

## <a name="elements-and-attributes"></a>Öğeler ve öznitelikler
 `postAction` Öğe isteğe bağlıdır ve durumda `vstav3` ad alanı. Bir `postAction` her dağıtım sonrası eylemi için uygulama bildiriminde tanımlanan öğe.

 `postAction` Öğesi özniteliklere sahip değildir.

 `postAction` Aşağıdaki öğelere sahiptir.

### <a name="entrypoint"></a>Giriş noktası
 İsteğe bağlı. Rolü `entryPoint` öğesinde `vstav3` ad alanı içinde tanımlanan [ &#60;giriş noktaları&#62; öğesi &#40;Visual Studio'da Office geliştirme&#41;](../vsto/entrypoints-element-office-development-in-visual-studio.md).

### <a name="postactiondata"></a>postActionData
 İsteğe bağlı. Rolü `postActionData` öğesinde `vstav3` ad alanı içinde tanımlanan [ &#60;postActionData&#62; öğesi &#40;Visual Studio'da Office geliştirme&#41;](../vsto/postactiondata-element-office-development-in-visual-studio.md).

## <a name="post-deployment-action-example"></a>Dağıtım sonrası eylemi örneği

### <a name="description"></a>Açıklama
 Aşağıdaki kod örneğinde gösterilmiştir `postAction` öğesi kullanılarak dağıtılan bir Office çözümü için uygulama bildiriminde [!INCLUDE[ndptecclick](../vsto/includes/ndptecclick-md.md)]. Bu kod örneği, sağlanan daha büyük bir örneğin parçasıdır [Office çözümleri için uygulama bildirimleri](../vsto/application-manifests-for-office-solutions.md).

### <a name="code"></a>Kod

```xml
<vstav3:postAction>
  <vstav3:entryPoint
    class="PostDeploymentAction.PostDeploymentActionSample">
    <assemblyIdentity
      name="PostDeploymentAction"
      version="1.0.0.0"
      language="neutral"
      processorArchitecture="msil" />
  </vstav3:entryPoint>
  <vstav3:postActionData>
  </vstav3:postActionData>
</vstav3:postAction>
```

## <a name="see-also"></a>Ayrıca bkz.

- [Office çözümleri için uygulama bildirimleri](../vsto/application-manifests-for-office-solutions.md)
- [Office çözümleri için dağıtım bildirimleri](../vsto/deployment-manifests-for-office-solutions.md)
- [ClickOnce Uygulama bildirimi](../deployment/clickonce-application-manifest.md)
