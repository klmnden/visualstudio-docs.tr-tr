---
title: MergeLocalizationDirectives görevi | Microsoft Docs
ms.date: 11/04/2016
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
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 0cb537f045f3ed2409dfcf0def2826057fd55687
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55927754"
---
# <a name="mergelocalizationdirectives-task"></a>MergeLocalizationDirectives görevi
<xref:Microsoft.Build.Tasks.Windows.MergeLocalizationDirectives> Yerelleştirme öznitelikleri ve yorumlar veya birden fazla görev birleştirir [!INCLUDE[TLA2#tla_xaml](../msbuild/includes/tla2sharptla_xaml_md.md)] tüm derleme için tek bir dosya halinde ikili biçimi dosyaları.

## <a name="task-parameters"></a>Görev parametreleri

| Parametre | Açıklama |
|------------------------------| - |
| `GeneratedLocalizationFiles` | Gerekli **Itaskıtem []** parametresi.<br /><br /> Tek tek dosyalar için yerelleştirme yönergeleri dosyaların listesini belirtir [!INCLUDE[TLA2#tla_xaml](../msbuild/includes/tla2sharptla_xaml_md.md)] ikili biçimi. |
| `OutputFile` | Gerekli **dize** çıkış parametresi.<br /><br /> Yerelleştirme yönergeleri derlenmiş bütünleştirilmiş kodun çıkış yolunu belirtir. |

## <a name="remarks"></a>Açıklamalar
Yerelleştirme öznitelikleri ve yorumlar için ekleyebileceğiniz [!INCLUDE[TLA#tla_xaml](../msbuild/includes/tlasharptla_xaml_md.md)] içeriği. İle [!INCLUDE[TLA#tla_wpf](../msbuild/includes/tlasharptla_wpf_md.md)] yerelleştirme desteğini, Şerit Yerelleştirme öznitelikleri ve yorumlar ve bunları koymak bir *.loc* oluşturulan derlemeden farklıdır dosya. Kullanarak bunu yapabilirsiniz **LocalizationPropertyStorage** özniteliği. Yerelleştirme öznitelikleri ve Yorumlar hakkında daha fazla bilgi ve **LocalizationPropertyStorage**, bkz: [Yerelleştirme öznitelikleri ve Yorumlar](/dotnet/framework/wpf/advanced/localization-attributes-and-comments).

## <a name="example"></a>Örnek
Aşağıdaki örnek birkaç yerelleştirme açıklamalarını birleştirir [!INCLUDE[TLA2#tla_xaml](../msbuild/includes/tla2sharptla_xaml_md.md)] tek bir ikili biçimi dosyalarıyla *.loc* dosya.

```xml
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

## <a name="see-also"></a>Ayrıca bkz.
[WPF MSBuild başvurusu](../msbuild/wpf-msbuild-reference.md)  
[WPF MSBuild görev başvurusu](../msbuild/wpf-msbuild-task-reference.md)  
[MSBuild başvurusu](../msbuild/msbuild-reference.md)  
[MSBuild görev başvurusu](../msbuild/msbuild-task-reference.md)  
[Bir WPF uygulaması (WPF) oluşturma](/dotnet/framework/wpf/app-development/building-a-wpf-application-wpf)  
