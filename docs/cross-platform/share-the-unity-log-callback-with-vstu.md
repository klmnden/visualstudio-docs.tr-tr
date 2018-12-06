---
title: VSTU ile Unity günlük geri çağırması paylaşma | Microsoft Docs
ms.custom: ''
ms.date: 07/26/2018
ms.technology: vs-unity-tools
ms.topic: conceptual
ms.assetid: 5d71f906-6e50-4399-b59b-d38c6dfef7ee
author: johmil
ms.author: therealjohn
manager: crdun
ms.workload:
- unity
ms.openlocfilehash: 7717dd1c95d77437f21d5d12e44d44c3dd3aa69e
ms.sourcegitcommit: 150fa6ec89ea2d086c0af9ababbaf6103a12eff1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/06/2018
ms.locfileid: "52953921"
---
# <a name="share-the-unity-log-callback-with-vstu"></a>VSTU ile Unity günlük geri çağrısı paylaşma
Unity için Visual Studio Araçları, Unity'nin konsolunu Visual Studio'ya aktarabilmek için Unity'ye bir günlük geri çağrısı kaydeder. Düzenleyici betiklerinizi Unity ile aynı zamanda günlük geri kaydolursanız, geri çağırma işleminizi VSTU geri çağırma etkileyebilir. Bu olasılığını önlemek için `VisualStudioIntegration.LogCallback` VSTU ile işbirliği yapmayı olay.

## <a name="demonstrates"></a>Gösteriler
 Unity için Visual Studio Araçları tarafından oluşturulan Unity günlük geri çağırması paylaşma yapma.

## <a name="example"></a>Örnek

```csharp
#if ENABLE_VSTU
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
#endif
```

## <a name="see-also"></a>Ayrıca bkz.
 [Örnek: Proje dosyası oluşturma](../cross-platform/customize-project-files-created-by-vstu.md)
