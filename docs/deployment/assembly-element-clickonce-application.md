---
title: '&lt;derleme&gt; öğesi (ClickOnce uygulaması) | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- urn:schemas-microsoft-com:asm.v2#assembly
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- <assembly> element [ClickOnce application manifest]
ms.assetid: 51410569-10f9-4c0a-96b5-d39185edbefc
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 6b629243920021adc3833f43f268f05638029dc7
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62900766"
---
# <a name="ltassemblygt-element-clickonce-application"></a>&lt;derleme&gt; öğesi (ClickOnce uygulaması)
Uygulama bildirimi için üst düzey öğe.

## <a name="syntax"></a>Sözdizimi

```xml

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
 Aşağıdaki kod örneğinde gösterilmiştir bir `assembly` öğesi için bir uygulama bildiriminde bir [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] uygulama. Bu kod örneği, sağlanan daha büyük bir örneğin parçasıdır [ClickOnce Uygulama bildirimi](../deployment/clickonce-application-manifest.md).

```xml
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

## <a name="see-also"></a>Ayrıca bkz.
- [ClickOnce Uygulama bildirimi](../deployment/clickonce-application-manifest.md)
- [\<derleme > öğesi](../deployment/assembly-element-clickonce-deployment.md)
