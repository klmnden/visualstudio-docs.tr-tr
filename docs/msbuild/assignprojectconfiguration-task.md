---
title: AssignProjectConfiguration görevi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
dev_langs:
- VB
- CSharp
- C++
- jsharp
ms.assetid: 09633a0b-8f6f-4aba-8058-7cb4d13ce2c0
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: d7ea5621c2285484c513a7602d934bbd14591262
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54970623"
---
# <a name="assignprojectconfiguration-task"></a>AssignProjectConfiguration görevi
Bu görev, bir yapılandırma dizeleri listesini kabul eder ve bunları belirtilen projelere atar.  
  
## <a name="task-parameters"></a>Görev parametreleri  
 Parametreleri aşağıdaki tabloda açıklanmıştır `AssignProjectConfiguration` görev.  
  
|Parametre|Açıklama|  
|---------------|-----------------|  
|`SolutionConfigurationContents`|İsteğe bağlı `string` çıkış parametresi.<br /><br /> Her proje için proje yapılandırmasını içeren bir XML dizesi içerir. Yapılandırmalar adlandırılmış projelere atanır.|  
|`DefaultToVcxPlatformMapping`|İsteğe bağlı `string` çıkış parametresi.<br /><br /> Tarafından kullanılan türlerin çoğu tarafından kullanılan platform adlarından eşlemelerin noktalı virgülle ayrılmış bir listesini içeren *.vcxproj* dosyaları.<br /><br /> Örneğin:<br /><br /> `"AnyCPU=Win32;X86=Win32;X64=X64"`|  
|`VcxToDefaultPlatformMapping`|İsteğe Bağlı<br /><br /> `string` Çıkış parametresi.<br /><br /> Eşlemelerin noktalı virgülle ayrılmış bir listesini içerir *.vcxproj* çoğu türe göre platform adlarına platform adlarını kullanın.<br /><br /> Örneğin:<br /><br /> `"Win32=AnyCPU;X64=X64"`|  
|`CurrentProjectConfiguration`|İsteğe bağlı `string` çıkış parametresi.<br /><br /> Geçerli proje yapılandırmasını içerir.|  
|`CurrentProjectPlatform`|İsteğe bağlı `string` çıkış parametresi.<br /><br /> Geçerli proje için platform içerir.|  
|`OnlyReferenceAndBuildProjectsEnabledInSolutionConfiguration`|İsteğe bağlı `bool` çıkış parametresi.<br /><br /> Proje yapılandırmasında devre dışı olsa bile başvuruları oluşturulması gerektiğini belirten bir bayrak içerir.|  
|`ShouldUnsetParentConfigurationAndPlatform`|İsteğe bağlı `bool` çıkış parametresi.<br /><br /> Üst yapılandırma ve platform ayarının kaldırılması gerekip gerekmediğini belirten bir bayrak içerir.|  
|`OutputType`|İsteğe bağlı `string` çıkış parametresi.<br /><br /> Projeye ilişkin çıktı türünü içerir.|  
|`ResolveConfigurationPlatformUsingMappings`|İsteğe bağlı `bool` çıkış parametresi.<br /><br /> Yapı varsayılan eşlemeleri yapılandırma ve platform geçirilen çözümlenecek kullanması gerekip gerekmediğini belirten bir bayrak içerir proje başvurularına.|  
|`AssignedProjects`|İsteğe bağlı <xref:Microsoft.Build.Framework.ITaskItem> `[]` çıkış parametresi.<br /><br /> Çözümlenen başvuru yollarının listesini içerir.|  
|`UnassignedProjects`|İsteğe bağlı <xref:Microsoft.Build.Framework.ITaskItem> `[]` çıkış parametresi.<br /><br /> Çıktıların önceden çözümlenmiş listesini kullanarak çözümlenemedi proje başvuru öğelerinin listesini içerir.|  
  
## <a name="remarks"></a>Açıklamalar  
 Yukarıda listelenen parametrelerin yanı sıra, bu görev parametreleri devralan <xref:Microsoft.Build.Tasks.TaskExtension> kendisi sınıfının devraldığı <xref:Microsoft.Build.Utilities.Task> sınıfı. Bu ek parametrelerin ve Tanımlamaların bir listesi için bkz. [TaskExtension taban sınıfı](../msbuild/taskextension-base-class.md).  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Görevleri](../msbuild/msbuild-tasks.md)   
 [Görev başvurusu](../msbuild/msbuild-task-reference.md)