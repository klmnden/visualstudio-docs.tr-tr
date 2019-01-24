---
title: '&lt;customErrorReporting&gt; öğesi (ClickOnce dağıtımı) | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-deployment
ms.topic: conceptual
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- <customErrorReporting> element [ClickOnce deployment manifest]
ms.assetid: 7d31816e-c692-46b5-9cc9-753284b3bcda
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: b7e8a0db3e10a277fe1c4a2f8fcd2bb85fa69e69
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54790796"
---
# <a name="ltcustomerrorreportinggt-element-clickonce-deployment"></a>&lt;customErrorReporting&gt; öğesi (ClickOnce dağıtımı)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bir hata oluştuğunda göstermek için bir URI belirtir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
<customErrorReporting  
   uri  
/>  
```  
  
## <a name="remarks"></a>Açıklamalar  
 Bu öğe isteğe bağlıdır. Bu olmadan, [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] özel yığının gösteren bir hata iletişim kutusu görüntüler. Varsa `customErrorReporting` öğesi mevcutsa, [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] tarafından gösterilen URI'yi bunun yerine görüntülenir `uri` parametresi. Dıştaki özel durum sınıfı, iç özel durum sınıfı ve iç özel durum iletisi ' % s'hedef URI parametreleri olarak dahil edilir.  
  
 Hata Raporlama işlevselliği uygulamanıza eklemek için bu öğeyi kullanırsınız. Oluşturulan URI hata türü hakkında bilgi içerdiğinden, Web sitenizi bilgileri ve görüntü, örneğin, uygun bir sorun giderme ekranı ayrıştırabilirsiniz.  
  
## <a name="example"></a>Örnek  
 Aşağıdaki kod parçacığında gösterildiği `customErrorReporting` bunu üretebilir oluşturulan URI ile birlikte bir öğe.  
  
```  
<customErrorReporting uri=http://www.contoso.com/applications/error.asp />  
  
Example Generated Error:  
http://www.contoso.com/applications/error.asp? outer=System.Deployment.Application.InvalidDeploymentException&&inner=System.Deployment.Application.InvalidDeploymentException&&msg=The%20application%20manifest%20is%20signed,%20but%20the%20deployment%20manifest%20is%20unsigned.%20Both%20manifests%20must%20be%20either%20signed%20or%20unsigned.  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [ClickOnce Dağıtım Bildirimi](../deployment/clickonce-deployment-manifest.md)
