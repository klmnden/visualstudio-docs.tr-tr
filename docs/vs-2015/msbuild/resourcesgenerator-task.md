---
title: ResourcesGenerator görevi | Microsoft Docs
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
- embedding resources into a .resources file [WPF MSBuild]
- ResourcesGenerator task [WPF MSBuild]
- ResourcesGenerator task [WPF MSBuild], parameters
ms.assetid: e782bbac-9ee6-472b-8171-3ee008c77b4e
caps.latest.revision: 9
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: f53f6f66b30509b56fbaf7cf54eecd0fe93b1434
ms.sourcegitcommit: a83c60bb00bf95e6bea037f0e1b9696c64deda3c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/19/2019
ms.locfileid: "54805403"
---
# <a name="resourcesgenerator-task"></a>ResourcesGenerator Görevi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
<xref:Microsoft.Build.Tasks.Windows.ResourcesGenerator> Görev bir veya daha fazla kaynak katıştırır (.jpg, .ico, .bmp, [!INCLUDE[TLA2#tla_xaml](../includes/tla2sharptla-xaml-md.md)] ikili biçimi ve diğer uzantı türleri) bir .resources dosyasına.  
  
## <a name="task-parameters"></a>Görev parametreleri  
  
|Parametre|Açıklama|  
|---------------|-----------------|  
|`OutputPath`|Gerekli **dize** parametresi.<br /><br /> Çıktı dizini yolunu belirtir. Yol mutlak bir yol değil ise kök proje dizinine göreli bir yol olarak kabul edilir.|  
|`OutputResourcesFile`|Gerekli **Itaskıtem []** çıkış parametresi.<br /><br /> Oluşturulan .resources dosyasının adını ve yolunu belirtir. Yol mutlak bir yol değil, .resources dosyasının kök proje dizinine göreli oluşturulur.|  
|`ResourcesFiles`|Gerekli **Itaskıtem []** parametresi.<br /><br /> Oluşturulan bir .resources dosyasına eklemek için bir veya daha fazla kaynak belirtir.|  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnek, tek .bmp kaynağı olan bir .resources dosyası oluşturur. Proje kök dizinine göreli bir dizine .bmp kaynak oluşturulur.  
  
```  
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">  
  <UsingTask   
    TaskName="Microsoft.Build.Tasks.Windows.ResourcesGenerator"   
    AssemblyFile="C:\Program Files\Reference Assemblies\Microsoft\Framework\v3.0\PresentationBuildTasks.dll" />  
  <Target Name="ResourcesGeneratorTask">  
    <ResourcesGenerator  
      ResourceFiles="Resource1.bmp"  
      OutputPath="myresources"  
      OutputResourcesFile="myresources\my.resources" />  
  </Target>  
</Project>  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [WPF MSBuild başvurusu](../msbuild/wpf-msbuild-reference.md)   
 [Görev başvurusu](../msbuild/wpf-msbuild-task-reference.md)   
 [MSBuild başvurusu](../msbuild/msbuild-reference.md)   
 [Görev başvurusu](../msbuild/msbuild-task-reference.md)   
 [WPF uygulaması (WPF) oluşturma](http://msdn.microsoft.com/library/a58696fd-bdad-4b55-9759-136dfdf8b91c)
