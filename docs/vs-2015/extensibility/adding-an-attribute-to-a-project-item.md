---
title: Bir proje öğesine öznitelik ekleme | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- attributes [Visual Studio], adding to a project item
ms.assetid: 404a71d5-cce5-44e7-9eaf-d747c794fedb
caps.latest.revision: 5
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 6854b4895ff03d575a3d26fad0e1117debf932f1
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49302698"
---
# <a name="adding-an-attribute-to-a-project-item"></a>Proje Öğesine Öznitelik Ekleme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Yöntemleri <xref:Microsoft.VisualStudio.Shell.Interop.IVsBuildPropertyStorage.GetItemAttribute%2A> ve <xref:Microsoft.VisualStudio.Shell.Interop.IVsBuildPropertyStorage.SetItemAttribute%2A> alın ve bir proje öğesi özniteliklerini ayarlayın. Zaten yoksa SetItemAttribute proje öğesi meta verilere ekleme öznitelik oluşturur.  
  
## <a name="adding-an-attribute-to-a-project-item"></a>Bir proje öğesine öznitelik ekleme  
  
#### <a name="to-add-an-attribute-to-a-project-item"></a>Öznitelik bir proje öğesine eklemek için  
  
-   Aşağıdaki kod <xref:EnvDTE.DTE> Otomasyon nesnesi ve <xref:Microsoft.VisualStudio.Shell.Interop.IVsBuildPropertyStorage.SetItemAttribute%2A> bir proje öğesine öznitelik eklemek için yöntemi. Proje öğesi Kimliğine proje öğesi adı "program.cs" alınır. ' % S'özniteliği "IMyData" Bu proje öğesine eklenir ve "MyValue" değeri verildiğinde.  
  
    ```  
    EnvDTE.DTE dte = (EnvDTE.DTE)Package.GetGlobalService(typeof(EnvDTE.DTE));  
    EnvDTE.Project project = dte.Solution.Projects.Item(1);  
  
    string uniqueName = project.UniqueName;  
    IVsSolution solution =     (IVsSolution)Package.GetGlobalService(typeof(SVsSolution));  
    IVsHierarchy hierarchy;  
    solution.GetProjectOfUniqueName(uniqueName, out hierarchy);  
    IVsBuildPropertyStorage buildPropertyStorage = hierarchy as IVsBuildPropertyStorage;  
    if (buildPropertyStorage != null)  
    {  
        uint itemId;  
        string fullPath =         (string)project.ProjectItems.Item("Program.cs").Properties.Item("FullPath").Value;  
        hierarchy.ParseCanonicalName(fullPath, out itemId);  
        buildPropertyStorage.SetItemAttribute(  
            itemId, "MyAttribute", "MyValue");  
    }  
  
    ```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [MSBuild Proje Dosyasında Verileri Kalıcı Hale Getirme](../extensibility/internals/persisting-data-in-the-msbuild-project-file.md)

