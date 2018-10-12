---
title: Çalışma zamanında proje alt türlerini doğrulama | Microsoft Docs
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
- project subtypes
- check subtypes
ms.assetid: b87780ec-36a3-4e9a-9ee2-7abdc26db739
caps.latest.revision: 12
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: e8aa68670b82fdba0f189cfb8bf2a06db15f33b4
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49215065"
---
# <a name="verifying-subtypes-of-a-project-at-run-time"></a>Çalışma Zamanında Proje Alt Türlerini Doğrulama
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Özel proje alt türü üzerinde olduğu bir VSPackage'ı alt tür ve böylece alt mevcut değilse düzgün bir şekilde devredebilirsiniz aramak için mantık eklemeniz gerekir. Aşağıdaki yordam, belirtilen alt varlığını doğrulamak gösterilmektedir.  
  
### <a name="to-verify-the-presence-of-a-subtype"></a>Bir alt varlığını doğrulamak için  
  
1.  Proje ve çözüm nesneler olarak proje hiyerarşisi almak bir <xref:Microsoft.VisualStudio.Shell.Interop.IVsHierarchy> , VSPackage için aşağıdaki kodu ekleyerek nesne.  
  
    ```  
    EnvDTE.DTE dte;  
    dte = (EnvDTE.DTE)Package.GetGlobalService(typeof(EnvDTE.DTE));  
  
    EnvDTE.Project project;  
    project = dte.Solution.Projects.Item(1);  
  
    IVsSolution solution;  
    solution = (IVsSolution)Package.GetGlobalService(typeof(SVsSolution));  
  
    IVsHierarchy hierarchy;  
    hierarchy = solution.GetProjectOfUniqueName(project.UniqueName);  
  
    ```  
  
2.  Hiyerarşi için cast <xref:Microsoft.VisualStudio.Shell.Flavor.IVsAggregatableProjectCorrected> arabirimi.  
  
    ```  
    IVsAggregatableProjectCorrected AP;  
    AP = hierarchy as IVsAggregatableProjectCorrected;  
  
    ```  
  
3.  Çağırarak proje türü GUID'ın listesini alın <xref:Microsoft.VisualStudio.Shell.Flavor.IVsAggregatableProjectCorrected.GetAggregateProjectTypeGuids%2A>.  
  
    ```  
    string projTypeGuids = AP.GetAggregateProjectTypeGuids().ToUpper();  
  
    ```  
  
4.  Belirtilen alt türe GUİD'i kontrol edin.  
  
    ```  
    // Replace the string "MyGUID" with the GUID of the subtype.  
    string guidMySubtype = "MyGUID";  
    if (projTypeGuids.IndexOf(guidMySubtype) > 0)  
    {  
        // The specified subtype is present.  
    }  
    ```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Proje alt türleri](../extensibility/internals/project-subtypes.md)   
 [Proje alt türleri tasarımı](../extensibility/internals/project-subtypes-design.md)   
 [Proje Alt Türleri Tarafından Genişletilen Özellikler ve Metotlar](../extensibility/internals/properties-and-methods-extended-by-project-subtypes.md)

