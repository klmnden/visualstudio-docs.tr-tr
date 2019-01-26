---
title: UidManager görevi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- UidManager task [WPF MSBuild]
- UidManager task [WPF MSBuild], parameters
- managing UIDs when localizing XAML elements [WPF MSBuild]
- localizing XAML elements [WPF MSBuild], managing UIDs
- checking UIDs when localizing XAML elements [WPF MSBuild]
ms.assetid: 4fc7b5a5-11b0-46ca-9656-8c2a0b08d1fe
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: b2e6f653ca7fc6bc335ab58530242f94b1f95d39
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54963817"
---
# <a name="uidmanager-task"></a>UidManager görevi
<xref:Microsoft.Build.Tasks.Windows.UidManager> Görev denetler, güncelleştirir veya tüm yerelleştirmek için benzersiz tanımlayıcıları (Uıd'leri) kaldırır [!INCLUDE[TLA#tla_xaml](../msbuild/includes/tlasharptla_xaml_md.md)] kaynakta bulunan öğeleri [!INCLUDE[TLA2#tla_xaml](../msbuild/includes/tla2sharptla_xaml_md.md)] dosyaları.  
  
## <a name="task-parameters"></a>Görev parametreleri  
  
| Parametre | Açıklama |
|-------------------------| - |
| `IntermediateDirectory` | İsteğe bağlı **dize** parametresi.<br /><br /> Kaynağını yedeklemeye kullanılacak dizini belirtir [!INCLUDE[TLA2#tla_xaml](../msbuild/includes/tla2sharptla_xaml_md.md)] tarafından belirtilen dosyalarını **MarkupFiles** parametresi. |
| `MarkupFiles` | Gerekli **Itaskıtem []** parametresi.<br /><br /> Kaynak belirtir [!INCLUDE[TLA2#tla_xaml](../msbuild/includes/tla2sharptla_xaml_md.md)] için denetleme, güncelleştirme veya kaldırma UID dahil edilecek dosyalar. |
| `Task` | Gerekli **dize** parametresi.<br /><br /> Gerçekleştirmek istediğiniz UID yönetim görevini belirtir. Geçerli seçenekler **denetleyin**, **güncelleştirme**, veya **Kaldır**. |
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnekte <xref:Microsoft.Build.Tasks.Windows.UidManager> denetlemek için görev belirtilen kaynak [!INCLUDE[TLA2#tla_xaml](../msbuild/includes/tla2sharptla_xaml_md.md)] dosyaları içeren [!INCLUDE[TLA2#tla_xaml](../msbuild/includes/tla2sharptla_xaml_md.md)] uygun Uıd'leri olan öğeler.  
  
```xml  
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">  
  <UsingTask   
    TaskName="Microsoft.Build.Tasks.Windows.UidManager"   
    AssemblyFile="C:\Program Files\Reference Assemblies\Microsoft\Framework\v3.0\PresentationBuildTasks.dll" />  
  <Target Name="UidManagerTask">  
    <UidManager  
      Task="Check"  
      MarkupFiles="Page1.xaml;Page2.xaml"  
      IntermediateDirectory="c:\UidManagerIntermediateDirectory" />  
  </Target>  
</Project>  
```  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [WPF MSBuild başvurusu](../msbuild/wpf-msbuild-reference.md)   
 [Görev başvurusu](../msbuild/wpf-msbuild-task-reference.md)   
 [MSBuild başvurusu](../msbuild/msbuild-reference.md)   
 [Görev başvurusu](../msbuild/msbuild-task-reference.md)   
 [Bir WPF uygulaması (WPF) oluşturma](/dotnet/framework/wpf/app-development/building-a-wpf-application-wpf)   
 [Nasıl yapılır: Bir uygulamayı yerelleştirme](/dotnet/framework/wpf/advanced/how-to-localize-an-application)