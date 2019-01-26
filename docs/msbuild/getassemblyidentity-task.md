---
title: Getassemblyıdentity görevi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/msbuild/2003#GetAssemblyIdentity
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- MSBuild, GetAssemblyIdentity task
- GetAssemblyIdentity task [MSBuild]
ms.assetid: a977e072-37ad-4941-84a6-32a4483be55d
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 9c5c716f34ed1603c4f0ed2965c1fd6184f44654
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54982110"
---
# <a name="getassemblyidentity-task"></a>GetAssemblyIdentity görevi
Belirtilen dosyalardan derleme kimlikleri alır ve kimlik bilgilerini çıkarır.  
  
## <a name="task-parameters"></a>Görev parametreleri  
 Parametreleri aşağıdaki tabloda açıklanmıştır `GetAssemblyIdentity` görev.  
  
|Parametre|Açıklama|  
|---------------|-----------------|  
|`Assemblies`|İsteğe bağlı <xref:Microsoft.Build.Framework.ITaskItem> `[]` çıkış parametresi.<br /><br /> Alınan derleme kimliklerini içerir.|  
|`AssemblyFiles`|Gerekli <xref:Microsoft.Build.Framework.ITaskItem>`[]` parametresi.<br /><br /> Kimliklerden alınacak dosyaları belirtir.|  
  
## <a name="remarks"></a>Açıklamalar  
 Öğeleri tarafından çıkarılan `Assemblies` parametre içeren adlı öğesi meta veri girdileri `Version`, `PublicKeyToken`, ve `Culture`.  
  
 Yukarıda listelenen parametrelerin yanı sıra, bu görev parametreleri devralan <xref:Microsoft.Build.Tasks.TaskExtension> kendisi sınıfının devraldığı <xref:Microsoft.Build.Utilities.Task> sınıfı. Bu ek parametrelerin ve Tanımlamaların bir listesi için bkz. [TaskExtension taban sınıfı](../msbuild/taskextension-base-class.md).  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnek belirtilen dosyaları kimliğini alır. `MyAssemblies` öğesi ekleyin ve bunları çıkarır `MyAssemblyIdentities` öğesi.  
  
```xml
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">
    <ItemGroup>
        <MyAssemblies Include="File1.dll;File2.dll" />
    </ItemGroup>
    <Target Name="RetrieveIdentities">
        <GetAssemblyIdentity AssemblyFiles="@(MyAssemblies)">
            <Output TaskParameter="Assemblies" ItemName="MyAssemblyIdentities" />
        </GetAssemblyIdentity>
    </Target>  
</Project>  
```

## <a name="see-also"></a>Ayrıca bkz.  
 [Görevleri](../msbuild/msbuild-tasks.md)   
 [Görev başvurusu](../msbuild/msbuild-task-reference.md)
