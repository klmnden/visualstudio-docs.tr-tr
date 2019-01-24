---
title: VSTU tarafından oluşturulan proje dosyalarını özelleştirme | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: tgt-pltfrm-cross-plat
ms.topic: conceptual
ms.assetid: 60b8cc1d-cacc-404d-b768-77e81bc354f8
caps.latest.revision: 4
author: conceptdev
ms.author: crdun
manager: jillfra
ms.openlocfilehash: 14b04de6ea4c945b67bada257d7822790b683b38
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54772954"
---
# <a name="customize-project-files-created-by-vstu"></a>VSTU Tarafından Oluşturulan Proje Dosyalarını Özelleştirme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
Unity için Visual Studio Araçları, proje dosyası oluşturma işlemi sırasında Unity stili geri çağırma olanağı sağlar. Kaydolmalı `VisualStudioIntegration.ProjectFileGeneration` yeniden oluşturuldu her proje dosyasını değiştirmek için olay.  
  
## <a name="demonstrates"></a>Gösteriler  
 Unity için Visual Studio Araçları tarafından oluşturulan Visual Studio proje dosyalarını özelleştirme yapma.  
  
## <a name="example"></a>Örnek  
  
```csharp  
using System;  
using System.IO;  
using System.Linq;  
using System.Text;  
using System.Xml.Linq;  
  
using UnityEngine;  
using UnityEditor;  
  
using SyntaxTree.VisualStudio.Unity.Bridge;  
  
[InitializeOnLoad]  
public class ProjectFileHook  
{  
    // necessary for XLinq to save the xml project file in utf8  
    class Utf8StringWriter : StringWriter  
    {  
        public override Encoding Encoding  
        {  
            get { return Encoding.UTF8; }  
        }  
    }  
  
    static ProjectFileHook()  
    {  
        ProjectFilesGenerator.ProjectFileGeneration += (string name, string content) =>  
        {  
            // parse the document and make some changes  
            var document = XDocument.Parse(content);  
            document.Root.Add(new XComment("FIX ME"));  
  
            // save the changes using the Utf8StringWriter  
            var str = new Utf8StringWriter();  
            document.Save(str);  
  
            return str.ToString();  
        };  
    }  
}  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Örnek: Günlük geri çağırma](../cross-platform/share-the-unity-log-callback-with-vstu.md)
