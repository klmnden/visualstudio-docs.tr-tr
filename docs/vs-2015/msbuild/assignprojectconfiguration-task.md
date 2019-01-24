---
title: AssignProjectConfiguration görevi | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: msbuild
ms.topic: reference
dev_langs:
- VB
- CSharp
- C++
- jsharp
ms.assetid: 09633a0b-8f6f-4aba-8058-7cb4d13ce2c0
caps.latest.revision: 11
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: c09b4b917e54277ca7f9418a82bdfef9d1663be3
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54790171"
---
# <a name="assignprojectconfiguration-task"></a>AssignProjectConfiguration Görevi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
Bu görev, bir yapılandırma dizeleri listesini kabul eder ve bunları belirtilen projelere atar.  
  
## <a name="task-parameters"></a>Görev parametreleri  
 Parametreleri aşağıdaki tabloda açıklanmıştır `AssignProjectConfiguration` görev.  
  
|Parametre|Açıklama|  
|---------------|-----------------|  
|`SolutionConfigurationContents`|İsteğe bağlı `string` çıkış parametresi.<br /><br /> Her proje için proje yapılandırmasını içeren bir XML dizesi içerir. Yapılandırmalar adlandırılmış projelere atanır.|  
|`DefaultToVcxPlatformMapping`|İsteğe bağlı `string` çıkış parametresi.<br /><br /> Kullanılan platform adlarından eşlemelerin noktalı virgülle ayrılmış bir listesini içerir<br /><br /> .vcxproj dosyaları tarafından kullanılan çoğu türe göre.<br /><br /> Örneğin:<br /><br /> `"AnyCPU=Win32;X86=Win32;X64=X64"`|  
|`VcxToDefaultPlatformMapping`|İsteğe Bağlı<br /><br /> `string` Çıkış parametresi.<br /><br /> .Vcxproj platform adlarından eşlemelerin türlerin çoğu tarafından platform adlarını kullanmak için noktalı virgül ile ayrılmış bir listesini içerir.<br /><br /> Örneğin:<br /><br /> `"Win32=AnyCPU;X64=X64"`|  
|`CurrentProjectConfiguration`|İsteğe bağlı `string` çıkış parametresi.<br /><br /> Geçerli proje yapılandırmasını içerir.|  
|`CurrentProjectPlatform`|İsteğe bağlı `string` çıkış parametresi.<br /><br /> Geçerli proje için platform içerir.|  
|`OnlyReferenceAndBuildProjectsEnabledInSolutionConfiguration`|İsteğe bağlı `bool` çıkış parametresi.<br /><br /> Proje yapılandırmasında devre dışı olsa bile başvuruları oluşturulması gerektiğini belirten bir bayrak içerir.|  
|`ShouldUnsetParentConfigurationAndPlatform`|İsteğe bağlı `bool` çıkış parametresi.<br /><br /> Üst yapılandırma ve platform ayarının kaldırılması gerekip gerekmediğini belirten bir bayrak içerir.|  
|`OutputType`|İsteğe bağlı `string` çıkış parametresi.<br /><br /> Projeye ilişkin çıktı türünü içerir.|  
|`ResolveConfigurationPlatformUsingMappings`|İsteğe bağlı `bool` çıkış parametresi.<br /><br /> Yapı varsayılan eşlemeleri yapılandırma ve platform geçirilen çözümlenecek kullanması gerekip gerekmediğini belirten bir bayrak içerir proje başvurularına.|  
|`AssignedProjects`|İsteğe bağlı <xref:Microsoft.Build.Framework.ITaskItem> `[]` çıkış parametresi.<br /><br /> Çözümlenen başvuru yollarının listesini içerir.|  
|`UnassignedProjects`|İsteğe bağlı <xref:Microsoft.Build.Framework.ITaskItem> `[]` çıkış parametresi.<br /><br /> Çıktıların önceden çözümlenmiş listesini kullanarak çözümlenemedi proje başvuru öğelerinin listesini içerir.|  
  
## <a name="remarks"></a>Açıklamalar  
 Yukarıda listelenen parametrelerin yanı sıra, bu görev parametreleri devralan <xref:Microsoft.Build.Tasks.TaskExtension> kendisi sınıfının devraldığı <xref:Microsoft.Build.Utilities.Task> sınıfı. Bu ek parametrelerin ve Tanımlamaların bir listesi için bkz. [TaskExtension temel sınıfı](../msbuild/taskextension-base-class.md).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Görevleri](../msbuild/msbuild-tasks.md)   
 [Görev Başvurusu](../msbuild/msbuild-task-reference.md)
