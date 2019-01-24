---
title: '&lt;derleme&gt; öğesi (ClickOnce uygulaması) | Microsoft Docs'
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
- <assembly> element [ClickOnce application manifest]
ms.assetid: 51410569-10f9-4c0a-96b5-d39185edbefc
caps.latest.revision: 17
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: d619b8b3cd81e5b00fc689077a95ade08f4d7eed
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54758899"
---
# <a name="ltassemblygt-element-clickonce-application"></a>&lt;derleme&gt; öğesi (ClickOnce uygulaması)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Uygulama bildirimi için üst düzey öğe.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
  
      <assembly  
   manifestVersion  
/>  
```  
  
## <a name="elements-and-attributes"></a>Öğeler ve öznitelikler  
 `assembly` Öğesi kök öğe ve gereklidir. Alt ilk bağımsız öğe olmalıdır bir `assemblyIdentity` öğesi. Bildirim öğeler şu ad alanlarından birinde olmalıdır:  
  
 `urn:schemas-microsoft-com:asm.v1`  
  
 `urn:schemas-microsoft-com:asm.v2`  
  
 `http://www.w3.org/2000/09/xmldsig#`  
  
 Derlemenin alt öğeleri, bu ad alanlarında, devralma veya etiketleme tarafından da olması gerekir.  
  
 `assembly` Öğesi aşağıdaki özniteliklere sahiptir.  
  
|Öznitelik|Açıklama|  
|---------------|-----------------|  
|`manifestVersion`|Gerekli. `manifestVersion` Özniteliği ayarlanmalıdır `1.0`.|  
  
## <a name="example"></a>Örnek  
 Aşağıdaki kod örneğinde gösterilmiştir bir `assembly` öğesi için bir uygulama bildiriminde bir [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] uygulama. Bu kod örneği, sağlanan daha büyük bir örneğin parçasıdır [ClickOnce Uygulama bildirimi](../deployment/clickonce-application-manifest.md).  
  
```  
<asmv1:assembly   
  xsi:schemaLocation="urn:schemas-microsoft-com:asm.v1 assembly.adaptive.xsd"   
  manifestVersion="1.0"   
  xmlns:asmv3="urn:schemas-microsoft-com:asm.v3"  
  xmlns:dsig=http://www.w3.org/2000/09/xmldsig#  
  xmlns:co.v2="urn:schemas-microsoft-com:clickonce.v2"  
  xmlns="urn:schemas-microsoft-com:asm.v2"  
  xmlns:asmv1="urn:schemas-microsoft-com:asm.v1"  
  xmlns:asmv2="urn:schemas-microsoft-com:asm.v2"  
  xmlns:xsi=http://www.w3.org/2001/XMLSchema-instance  
  xmlns:co.v1="urn:schemas-microsoft-com:clickonce.v1">  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [ClickOnce Uygulama bildirimi](../deployment/clickonce-application-manifest.md)   
 [\<derleme > öğesi](../deployment/assembly-element-clickonce-deployment.md)
