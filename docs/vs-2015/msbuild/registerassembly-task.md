---
title: RegisterAssembly görevi | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: msbuild
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/msbuild/2003#RegisterAssembly
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- MSBuild, RegisterAssembly task
- RegisterAssembly task [MSBuild]
ms.assetid: ba5f19ac-6764-4d28-9b79-a86de58f8987
caps.latest.revision: 19
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 71ef27b61e162fedbf0b8fcaac38d93bedbc77c1
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65682399"
---
# <a name="registerassembly-task"></a>RegisterAssembly Görevi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Belirtilen derleme içindeki meta veriyi okur ve oluşturmak COM istemcilerinin veren kayıt defterine gerekli girişleri ekler [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)] şeffaf bir şekilde sınıfları. Bu görevin benzer, ancak aynı, davranıştır [Regasm.exe (derleme kayıt aracı)](https://msdn.microsoft.com/library/e190e342-36ef-4651-a0b4-0e8c2c0281cb).  
  
## <a name="parameters"></a>Parametreler  
 Parametreleri aşağıdaki tabloda açıklanmıştır `RegisterAssembly` görev.  
  
|Parametre|Açıklama|  
|---------------|-----------------|  
|`Assemblies`|Gerekli <xref:Microsoft.Build.Framework.ITaskItem>`[]` parametresi.<br /><br /> Derlemeleri com ile Kaydettirilecek belirtir|  
|`AssemblyListFile`|İsteğe bağlı <xref:Microsoft.Build.Framework.ITaskItem> parametresi.<br /><br /> Arasında durumu hakkındaki bilgileri içeren `RegisterAssembly` görev ve [UnregisterAssembly](../msbuild/unregisterassembly-task.md) görev. Bu engeller `UnregisterAssembly` kaydetmek için başarısız bir derleme kaydını çalışılıyor görevin `RegisterAssembly` görev.|  
|`CreateCodeBase`|İsteğe bağlı `Boolean` parametresi.<br /><br /> Varsa `true`, genel derleme önbelleğinde yüklü olmayan bir derleme için dosya yolunu belirtir. kayıt defterinde bir kod temeli girişi oluşturur. Sonrasında genel derleme önbelleğine kaydettiriyor olduğunuz derlemeyi yükleyecekseniz bu seçeneği belirtmemelisiniz.|  
|`TypeLibFiles`|İsteğe bağlı <xref:Microsoft.Build.Framework.ITaskItem> `[]` çıkış parametresi.<br /><br /> Belirtilen bütünleştirilmiş koddan oluşturmak için tür kitaplığını belirtir. Üretilmiş tür kitaplığını derleme içinde tanımlanmış erişilebilir türlerin tanımlarını içerir. Tür kitaplığı, aşağıdakilerden biri doğruysa yalnızca oluşturulur:<br /><br /> -Bir tür kitaplığı adının bu konumda mevcut değil.<br />-Bir tür kitaplığı var, ancak geçirilen derlemesinden daha eski.<br /><br /> Tür kitaplığını geçirilen derlemeden daha yeniyse, yeni bir tane oluşturulmaz, ancak derleme hala kayıtlı.<br /><br /> Bu parametre belirtilmezse, aynı sayıda öğe olmalıdır `Assemblies` parametresi veya görev başarısız olur. Giriş belirtilmezse, görev derleme adını varsayılan ve uzantıyı öğesinin .tlb için değiştirin.|  
  
## <a name="remarks"></a>Açıklamalar  
 Yukarıda listelenen parametrelerin yanı sıra, bu görev parametreleri devralan <xref:Microsoft.Build.Tasks.TaskExtension> kendisi sınıfının devraldığı <xref:Microsoft.Build.Utilities.Task> sınıfı. Bu ek parametrelerin ve Tanımlamaların bir listesi için bkz. [TaskExtension temel sınıfı](../msbuild/taskextension-base-class.md).  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnekte `RegisterAssembly` tarafından belirtilen derlemeyi kaydetmek üzere görev `MyAssemblies` öğe koleksiyonu.  
  
```  
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">  
  
    <ItemGroup>  
        <MyAssemblies Include="MyAssembly.dll" />  
    <ItemGroup>  
  
    <Target Name="RegisterAssemblies">  
        <RegisterAssembly  
            Assemblies="@(MyAssemblies)" >  
    </Target>  
  
</Project>  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Görevleri](../msbuild/msbuild-tasks.md)   
 [Görev Başvurusu](../msbuild/msbuild-task-reference.md)
