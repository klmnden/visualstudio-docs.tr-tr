---
title: UidManager görevi | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: msbuild
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
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 5fd8175911def7fb1b63dc63d967c404d649e9e4
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65703689"
---
# <a name="uidmanager-task"></a>UidManager Görevi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

<xref:Microsoft.Build.Tasks.Windows.UidManager> Görev denetler, güncelleştirir veya tüm yerelleştirmek için benzersiz tanımlayıcıları (Uıd'leri) kaldırır [!INCLUDE[TLA#tla_xaml](../includes/tlasharptla-xaml-md.md)] kaynakta bulunan öğeleri [!INCLUDE[TLA2#tla_xaml](../includes/tla2sharptla-xaml-md.md)] dosyaları.  
  
## <a name="task-parameters"></a>Görev parametreleri  
  
|Parametre|Açıklama|  
|---------------|-----------------|  
|`IntermediateDirectory`|İsteğe bağlı **dize** parametresi.<br /><br /> Kaynağını yedeklemeye kullanılacak dizini belirtir [!INCLUDE[TLA2#tla_xaml](../includes/tla2sharptla-xaml-md.md)] tarafından belirtilen dosyalarını **MarkupFiles** parametresi.|  
|`MarkupFiles`|Gerekli **Itaskıtem []** parametresi.<br /><br /> Kaynak belirtir [!INCLUDE[TLA2#tla_xaml](../includes/tla2sharptla-xaml-md.md)] için denetleme, güncelleştirme veya kaldırma UID dahil edilecek dosyalar.|  
|`Task`|Gerekli **dize** parametresi.<br /><br /> Gerçekleştirmek istediğiniz UID yönetim görevini belirtir. Geçerli seçenekler **denetleyin**, **güncelleştirme**, veya **Kaldır**.|  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnekte <xref:Microsoft.Build.Tasks.Windows.UidManager> denetlemek için görev belirtilen kaynak [!INCLUDE[TLA2#tla_xaml](../includes/tla2sharptla-xaml-md.md)] dosyaları içeren [!INCLUDE[TLA2#tla_xaml](../includes/tla2sharptla-xaml-md.md)] uygun Uıd'leri olan öğeler.  
  
```  
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
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [WPF MSBuild başvurusu](../msbuild/wpf-msbuild-reference.md)   
 [Görev başvurusu](../msbuild/wpf-msbuild-task-reference.md)   
 [MSBuild başvurusu](../msbuild/msbuild-reference.md)   
 [Görev başvurusu](../msbuild/msbuild-task-reference.md)   
 [WPF uygulaması (WPF) oluşturma](https://msdn.microsoft.com/library/a58696fd-bdad-4b55-9759-136dfdf8b91c)   
 [Nasıl yapılır: Bir uygulamayı yerelleştirme](https://msdn.microsoft.com/library/5001227e-9326-48a4-9dcd-ba1b89ee6653)
