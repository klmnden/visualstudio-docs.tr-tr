---
title: MergeLocalizationDirectives görevi | Microsoft Docs
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
- localizing XAML [WPF MSBuild], moving comments and attributes to a separate file
- MergeLocalizationDirectives task [WPF MSBuild], parameters
- MergeLocalizationDirectives task [WPF MSBuild]
- moving localization comments and attributes to a separate file [WPF MSBuild]
ms.assetid: 9095b4f1-88da-4194-914b-ee1456826830
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 2001a3278037eb1c2dc1866c9508bb8623af3370
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/17/2019
ms.locfileid: "59652493"
---
# <a name="mergelocalizationdirectives-task"></a>MergeLocalizationDirectives Görevi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

<xref:Microsoft.Build.Tasks.Windows.MergeLocalizationDirectives> Yerelleştirme öznitelikleri ve yorumlar veya birden fazla görev birleştirir [!INCLUDE[TLA2#tla_xaml](../includes/tla2sharptla-xaml-md.md)] tüm derleme için tek bir dosya halinde ikili biçimi dosyaları.  
  
## <a name="task-parameters"></a>Görev parametreleri  
  
|Parametre|Açıklama|  
|---------------|-----------------|  
|`GeneratedLocalizationFiles`|Gerekli **Itaskıtem []** parametresi.<br /><br /> Tek tek dosyalar için yerelleştirme yönergeleri dosyaların listesini belirtir [!INCLUDE[TLA2#tla_xaml](../includes/tla2sharptla-xaml-md.md)] ikili biçimi.|  
|`OutputFile`|Gerekli **dize** çıkış parametresi.<br /><br /> Yerelleştirme yönergeleri derlenmiş bütünleştirilmiş kodun çıkış yolunu belirtir.|  
  
## <a name="remarks"></a>Açıklamalar  
 Yerelleştirme öznitelikleri ve yorumlar için ekleyebileceğiniz [!INCLUDE[TLA#tla_xaml](../includes/tlasharptla-xaml-md.md)] içeriği. İle [!INCLUDE[TLA#tla_wpf](../includes/tlasharptla-wpf-md.md)] yerelleştirme desteğini, Şerit Yerelleştirme öznitelikleri ve yorumlar ve oluşturulan derlemeden ayrı bir .loc dosyası yerleştirin. Kullanarak bunu yapabilirsiniz **LocalizationPropertyStorage** özniteliği. Yerelleştirme öznitelikleri ve Yorumlar hakkında daha fazla bilgi ve **LocalizationPropertyStorage**, bkz: [Yerelleştirme öznitelikleri ve Yorumlar](http://msdn.microsoft.com/library/ead2d9ac-b709-4ec1-a924-39927a29d02f).  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnek birkaç yerelleştirme açıklamalarını birleştirir [!INCLUDE[TLA2#tla_xaml](../includes/tla2sharptla-xaml-md.md)] tek .loc dosyasına dosyaları ikili biçimi.  
  
```  
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">  
  <UsingTask   
    TaskName="Microsoft.Build.Tasks.Windows.MergeLocalizationDirectives"   
    AssemblyFile="C:\Program Files\Reference Assemblies\Microsoft\Framework\v3.0\PresentationBuildTasks.dll" />  
  <Target Name="MergeLocalizationDirectivesTask">  
    <MergeLocalizationDirectives   
      GeneratedLocalizationFiles="obj\debug\page1.loc;obj\debug\page2.loc;obj\debug\page3.loc"  
      OutputFile="obj\debug\WPFMSBuildSample.loc" />  
  </Target>  
</Project>  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [WPF MSBuild başvurusu](../msbuild/wpf-msbuild-reference.md)   
 [Görev başvurusu](../msbuild/wpf-msbuild-task-reference.md)   
 [MSBuild başvurusu](../msbuild/msbuild-reference.md)   
 [Görev başvurusu](../msbuild/msbuild-task-reference.md)   
 [WPF uygulaması (WPF) oluşturma](http://msdn.microsoft.com/library/a58696fd-bdad-4b55-9759-136dfdf8b91c)
