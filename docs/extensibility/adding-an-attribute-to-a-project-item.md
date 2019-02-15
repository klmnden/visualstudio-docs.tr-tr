---
title: Bir proje öğesine öznitelik ekleme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- attributes [Visual Studio], adding to a project item
ms.assetid: 404a71d5-cce5-44e7-9eaf-d747c794fedb
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: c3cf11a6ca7972a98b840ac514a4dff01d994778
ms.sourcegitcommit: 752f03977f45169585e407ef719450dbe219b7fc
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2019
ms.locfileid: "56318270"
---
# <a name="add-an-attribute-to-a-project-item"></a>Bir proje öğesine öznitelik ekleme
Yöntemleri <xref:Microsoft.VisualStudio.Shell.Interop.IVsBuildPropertyStorage.GetItemAttribute%2A> ve <xref:Microsoft.VisualStudio.Shell.Interop.IVsBuildPropertyStorage.SetItemAttribute%2A> alın ve bir proje öğesi özniteliklerini ayarlayın. Zaten yoksa SetItemAttribute proje öğesi meta verilere ekleme öznitelik oluşturur.

## <a name="add-an-attribute-to-a-project-item"></a>Bir proje öğesine öznitelik ekleme

- Aşağıdaki kod <xref:EnvDTE.DTE> Otomasyon nesnesi ve <xref:Microsoft.VisualStudio.Shell.Interop.IVsBuildPropertyStorage.SetItemAttribute%2A> bir proje öğesine öznitelik eklemek için yöntemi. Proje öğesi Kimliğine proje öğesi adı "program.cs" alınır. ' % S'özniteliği "IMyData" Bu proje öğesine eklenir ve "MyValue" değeri verildiğinde.

    ```csharp
    EnvDTE.DTE dte = (EnvDTE.DTE)Package.GetGlobalService(typeof(EnvDTE.DTE));
    EnvDTE.Project project = dte.Solution.Projects.Item(1);

    string uniqueName = project.UniqueName;
    IVsSolution solution = (IVsSolution)Package.GetGlobalService(typeof(SVsSolution));
    IVsHierarchy hierarchy;
    solution.GetProjectOfUniqueName(uniqueName, out hierarchy);
    IVsBuildPropertyStorage buildPropertyStorage = hierarchy as IVsBuildPropertyStorage;
    if (buildPropertyStorage != null)
    {
        uint itemId;
        string fullPath = (string)project.ProjectItems.Item("Program.cs").Properties.Item("FullPath").Value;
        hierarchy.ParseCanonicalName(fullPath, out itemId);
        buildPropertyStorage.SetItemAttribute(itemId, "MyAttribute", "MyValue");
    }

    ```

## <a name="see-also"></a>Ayrıca bkz.
[MSBuild proje dosyasında verileri kalıcı hale getirmenize](../extensibility/internals/persisting-data-in-the-msbuild-project-file.md)
