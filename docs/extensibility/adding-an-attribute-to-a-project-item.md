---
title: Bir proje öğesine öznitelik ekleme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- attributes [Visual Studio], adding to a project item
ms.assetid: 404a71d5-cce5-44e7-9eaf-d747c794fedb
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: f60a47180a95c7609f784a2d0a03b51d0d4a7a6b
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53874131"
---
# <a name="add-an-attribute-to-a-project-item"></a>Bir proje öğesine öznitelik ekleme
Yöntemleri <xref:Microsoft.VisualStudio.Shell.Interop.IVsBuildPropertyStorage.GetItemAttribute%2A> ve <xref:Microsoft.VisualStudio.Shell.Interop.IVsBuildPropertyStorage.SetItemAttribute%2A> alın ve bir proje öğesi özniteliklerini ayarlayın. Zaten yoksa SetItemAttribute proje öğesi meta verilere ekleme öznitelik oluşturur.  
  
## <a name="add-an-attribute-to-a-project-item"></a>Bir proje öğesine öznitelik ekleme  
  
-   Aşağıdaki kod <xref:EnvDTE.DTE> Otomasyon nesnesi ve <xref:Microsoft.VisualStudio.Shell.Interop.IVsBuildPropertyStorage.SetItemAttribute%2A> bir proje öğesine öznitelik eklemek için yöntemi. Proje öğesi Kimliğine proje öğesi adı "program.cs" alınır. ' % S'özniteliği "IMyData" Bu proje öğesine eklenir ve "MyValue" değeri verildiğinde.  
  
    ```csharp  
    EnvDTE.DTE dte = (EnvDTE.DTE)Package.GetGlobalService(typeof(EnvDTE.DTE));  
    EnvDTE.Project project = dte.Solution.Projects.Item(1);  
  
    string uniqueName = project.UniqueName;  
    IVsSolution solution =     (IVsSolution)Package.GetGlobalService(typeof(SVsSolution));  
    IVsHierarchy hierarchy;  
    solution.GetProjectOfUniqueName(uniqueName, out hierarchy);  
    IVsBuildPropertyStorage buildPropertyStorage = hierarchy as IVsBuildPropertyStorage;  
    if (buildPropertyStorage != null)  
    {  
        uint itemId;  
        string fullPath =         (string)project.ProjectItems.Item("Program.cs").Properties.Item("FullPath").Value;  
        hierarchy.ParseCanonicalName(fullPath, out itemId);  
        buildPropertyStorage.SetItemAttribute(  
            itemId, "MyAttribute", "MyValue");  
    }  
  
    ```  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [MSBuild proje dosyasında verileri kalıcı hale getirmenize](../extensibility/internals/persisting-data-in-the-msbuild-project-file.md)