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
ms.openlocfilehash: 6c79a8a0558594e8981959750ebd348b6f9f4d60
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54773455"
---
# <a name="vs-shell-deployment"></a>VS Shell dağıtımı
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bir yalıtılmış Kabuk hangi Visual Studio belirlemenize olanak tanır işlevselliğe gereksinim, etki alanına özgü dil ve bu çözümü nasıl görüneceğini ile etkileşim kurmak. Visual Studio yalıtılmış Kabuk hakkında daha fazla bilgi için bkz. [yalıtılmış Kabuğu özelleştirme](../extensibility/customizing-the-isolated-shell.md). Yalıtılmış Kabuğu özelleştirme hakkında daha fazla bilgi bulabilirsiniz [yalıtılmış Kabuğu özelleştirme](http://msdn.microsoft.com/d75463cd-1155-42e4-8b7a-046ed6becbbf).  
  
### <a name="to-set-a-visual-studio-shell-as-the-deployment-target"></a>Bir Visual Studio Shell dağıtım hedefi olarak ayarlamak için  
  
1.  İçinde **DslPackage** projesini açarsanız **source.extension.tt**.  
  
2.  Altında `<SupportedProducts>` ekleyin:  
  
    ```  
    <IsolatedShell Version="1.0">MyIsolatedShell</IsolatedShell>  
    ```  
  
     Değiştirin *MyIsolatedShell* yalıtılmış Kabuk paketinizin ada sahip.
