---
title: VSTU ile Unity günlük geri çağırması paylaşma | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-unity-tools
ms.topic: conceptual
ms.assetid: 5d71f906-6e50-4399-b59b-d38c6dfef7ee
caps.latest.revision: 5
author: conceptdev
ms.author: crdun
manager: jillfra
ms.openlocfilehash: 5e4fcfdc35e9329429421fd03a941e611e6b5b8f
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54789175"
---
# <a name="share-the-unity-log-callback-with-vstu"></a>VSTU ile Unity Günlük Geri Çağırması paylaşma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
Unity için Visual Studio Araçları, Unity'nin konsolunu Visual Studio'ya aktarabilmek için Unity'ye bir günlük geri çağrısı kaydeder. Düzenleyici betiklerinizi Unity ile aynı zamanda günlük geri kaydolursanız, geri çağırma işleminizi VSTU geri çağırma etkileyebilir. Bu olasılığını önlemek için `VisualStudioIntegration.LogCallback` VSTU ile işbirliği yapmayı olay.  
  
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
 [Örnek: Proje dosyası oluşturma](../cross-platform/customize-project-files-created-by-vstu.md)
