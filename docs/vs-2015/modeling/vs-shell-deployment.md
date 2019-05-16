---
title: VS Shell dağıtımı | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-modeling
ms.topic: conceptual
ms.assetid: be8f2ffe-a322-4ac0-9c9e-873bd28e5d5e
caps.latest.revision: 4
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 5bfe88d7e7d742eb67273d307c3a8e72e9a85833
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65704041"
---
# <a name="vs-shell-deployment"></a>VS Shell dağıtımı
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bir yalıtılmış Kabuk hangi Visual Studio belirlemenize olanak tanır işlevselliğe gereksinim, etki alanına özgü dil ve bu çözümü nasıl görüneceğini ile etkileşim kurmak. Visual Studio yalıtılmış Kabuk hakkında daha fazla bilgi için bkz. [yalıtılmış Kabuğu özelleştirme](../extensibility/customizing-the-isolated-shell.md). Yalıtılmış Kabuğu özelleştirme hakkında daha fazla bilgi bulabilirsiniz [yalıtılmış Kabuğu özelleştirme](https://msdn.microsoft.com/d75463cd-1155-42e4-8b7a-046ed6becbbf).  
  
### <a name="to-set-a-visual-studio-shell-as-the-deployment-target"></a>Bir Visual Studio Shell dağıtım hedefi olarak ayarlamak için  
  
1. İçinde **DslPackage** projesini açarsanız **source.extension.tt**.  
  
2. Altında `<SupportedProducts>` ekleyin:  
  
    ```  
    <IsolatedShell Version="1.0">MyIsolatedShell</IsolatedShell>  
    ```  
  
     Değiştirin *MyIsolatedShell* yalıtılmış Kabuk paketinizin ada sahip.
