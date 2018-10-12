---
title: VSTU ile Unity günlük geri çağırması paylaşma | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- tgt-pltfrm-cross-plat
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 5d71f906-6e50-4399-b59b-d38c6dfef7ee
caps.latest.revision: 5
author: TerryGLee
ms.author: tglee
manager: ghogen
ms.openlocfilehash: 9e309f7d7340eb73de587c7a5f569377354dbab9
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49186868"
---
# <a name="share-the-unity-log-callback-with-vstu"></a>VSTU ile Unity Günlük Geri Çağırması paylaşma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
Unity için Visual Studio Araçları ile Visual Studio, konsola akışını yapabilmek için Unity günlük geri çağırma kaydeder. Düzenleyici betiklerinizi Unity ile aynı zamanda günlük geri kaydolursanız, geri çağırma işleminizi VSTU geri çağırma etkileyebilir. Bu olasılığını önlemek için `VisualStudioIntegration.LogCallback` VSTU ile işbirliği yapmayı olay.  
  
## <a name="demonstrates"></a>Gösteriler  
 Unity için Visual Studio Araçları tarafından oluşturulan Unity günlük geri çağırması paylaşma yapma.  
  
## <a name="example"></a>Örnek  
  
```csharp  
using System;  
  
using UnityEngine;  
using UnityEditor;  
  
using SyntaxTree.VisualStudio.Unity.Bridge;  
  
[InitializeOnLoad]  
public class LogCallbackHook  
{  
    static LogCallbackHook()  
    {  
        VisualStudioIntegration.LogCallback += (string condition, string trace, LogType type) =>  
        {  
            // place code that implements your log callback here  
        };  
    }  
}  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Örnek: Proje Dosyası Oluşturma](../cross-platform/customize-project-files-created-by-vstu.md)

