---
title: '&lt;assemblyIdentity&gt; öğesi (ClickOnce dağıtımı) | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-deployment
ms.topic: conceptual
f1_keywords:
- urn:schemas-microsoft-com:asm.v2#assemblyIdentity
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- <assemblyIdentity> element [ClickOnce deployment manifest]
ms.assetid: f4a3bb83-c800-47d0-9905-9a5ae2486838
caps.latest.revision: 25
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: bfc2ff97a2eb465fe7306ebe368a20e2a7fd8638
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68155722"
---
# <a name="ltassemblyidentitygt-element-clickonce-deployment"></a>&lt;assemblyIdentity&gt; öğesi (ClickOnce dağıtımı)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Birincil derlemenin tanımlayan [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] uygulama.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
  
      <assemblyIdentity    
   name   
   version  
   publicKeyToken  
   processorArchitecture  
    type  
/>  
```  
  
## <a name="elements-and-attributes"></a>Öğeler ve öznitelikler  
 `assemblyIdentity` Öğesi gereklidir. Alt öğe içerir ve aşağıdaki özniteliklere sahiptir.  
  
|Öznitelik|Açıklama|  
|---------------|-----------------|  
|`name`|Gerekli. Bilgilendirme amacıyla dağıtım okunabilir adını tanımlar.<br /><br /> Varsa `name` özel karakterler içeriyor ve tek veya çift tırnak gibi uygulama etkinleştirmesi başarısız olabilir.|  
|`version`|Gerekli. Derleme sürüm numarası şu biçimde belirtir: `major.minor.build.revision`.<br /><br /> Bu değer, bir uygulama güncelleştirmesi tetiklemek için güncelleştirilmiş bir bildirimde artırılması gereken.|  
|`publicKeyToken`|Gerekli. Son 8 bayt altında dağıtım bildirimini imzalanan ortak anahtarı SHA-1 karma değerini temsil eden 16 karakterlik bir onaltılık dize belirtir. İmzalamak için kullanılan ortak anahtar, 2048 bit olmalıdır veya büyük.<br /><br /> Bu öznitelik, bir derlemeyi imzalamayı önerilir ancak isteğe bağlı olsa da gereklidir. Bir derlemeyi imzalı değilse, değeri otomatik olarak imzalanan bir derlemeden kopyalama ya da sıfır "kukla" değerini kullanın.|  
|`processorArchitecture`|Gerekli. İşlemciyi belirtir. Geçerli değerler `msil` tüm işlemciler için `x86` 32-bit Windows için `IA64` 64 bit Windows için ve `Itanium` Intel 64-bit Itanium işlemcilere için.|  
|`type`|Gerekli. Windows yan yana yükleme teknolojisi ile uyumluluk için. Yalnızca izin verilen değer `win32`.|  
  
## <a name="remarks"></a>Açıklamalar  
  
## <a name="example"></a>Örnek  
 Aşağıdaki kod örneğinde gösterilmiştir bir `assemblyIdentity` öğesinde bir [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] dağıtım bildirimi. Bu kod örneği için sağlanan daha büyük bir örneğin parçasıdır [ClickOnce dağıtım bildirimi](../deployment/clickonce-deployment-manifest.md) konu.  
  
```  
<!-- Identify the deployment. -->  
<assemblyIdentity   
  name="My Application Deployment.app"  
  version="1.0.0.0"  
  publicKeyToken="43cb1e8e7a352766"  
  language="neutral"  
  processorArchitecture="x86"  
  xmlns="urn:schemas-microsoft-com:asm.v1" />  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [ClickOnce dağıtım bildirimi](../deployment/clickonce-deployment-manifest.md)   
 [\<assemblyIdentity> Öğesi](../deployment/assemblyidentity-element-clickonce-application.md)
