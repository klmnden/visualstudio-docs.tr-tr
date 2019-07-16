---
title: '&lt;derleme&gt; öğesi (ClickOnce dağıtımı) | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-deployment
ms.topic: conceptual
f1_keywords:
- urn:schemas-microsoft-com:asm.v2#assembly
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- <assembly> element [ClickOnce deployment manifest]
ms.assetid: b8e3362a-f821-4696-b98d-571d4bbfe431
caps.latest.revision: 13
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 3b77cfacf3dca2c2cc20d674f79929e9958a16d4
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68155730"
---
# <a name="ltassemblygt-element-clickonce-deployment"></a>&lt;derleme&gt; öğesi (ClickOnce dağıtımı)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Dağıtım bildirimi için üst düzey öğe.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
  
      <assembly    
   manifestVersion  
/>  
```  
  
## <a name="elements-and-attributes"></a>Öğeler ve öznitelikler  
 `assembly` Öğesi kök öğe ve gereklidir. Alt ilk bağımsız öğe olmalıdır bir `assemblyIdentity` öğesi. Bildirim öğeler aşağıdaki alanlarında olmalıdır: `urn:schemas-microsoft-com:asm.v1`, `urn:schemas-microsoft-com:asm.v2`, ve `http://www.w3.org/2000/09/xmldsig#`. Derlemenin alt öğeleri, bu ad alanlarında, devralma veya etiketleme tarafından da olması gerekir.  
  
 `assembly` Öğesi aşağıdaki özniteliklere sahiptir.  
  
|Öznitelik|Açıklama|  
|---------------|-----------------|  
|`manifestVersion`|Gerekli. Bu öznitelik ayarlanmalıdır `1.0`.|  
  
## <a name="example"></a>Örnek  
 Aşağıdaki kod örneğinde gösterilmiştir bir `assembly` kullanılarak dağıtılan bir uygulama için bir dağıtım bildirimi öğesinde [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)]. Bu kod örneği için sağlanan daha büyük bir örneğin parçasıdır [ClickOnce dağıtım bildirimi](../deployment/clickonce-deployment-manifest.md) konu.  
  
```  
<asmv1:assembly   
  xsi:schemaLocation="urn:schemas-microsoft-com:asm.v1 assembly.adaptive.xsd"  
  manifestVersion="1.0"  
  xmlns:asmv3="urn:schemas-microsoft-com:asm.v3"  
  xmlns:dsig=http://www.w3.org/2000/09/xmldsig#  
  xmlns:co.v1="urn:schemas-microsoft-com:clickonce.v1"  
  xmlns:co.v2="urn:schemas-microsoft-com:clickonce.v2"  
  xmlns="urn:schemas-microsoft-com:asm.v2"  
  xmlns:asmv1="urn:schemas-microsoft-com:asm.v1"  
  xmlns:asmv2="urn:schemas-microsoft-com:asm.v2"  
  xmlns:xrml="urn:mpeg:mpeg21:2003:01-REL-R-NS"  
  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [ClickOnce dağıtım bildirimi](../deployment/clickonce-deployment-manifest.md)   
 [\<assembly> Öğesi](../deployment/assembly-element-clickonce-application.md)
