---
title: GetWinFXPath görevi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- getting the directory of the current .NET Framework runtime [WPF MSBuild]
- GetWinFXPath task [WPF MSBuild], parameters
- GetWinFXPath task [WPF MSBuild]
- obtaining the path to the current .NET Framework runtime [WPF MSBuild]
ms.assetid: b1dfb467-f3d3-47f3-83ef-af7b0e33a772
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: c95e5ad882d7021b597d7ba0ad8c38177f4a5136
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56646935"
---
# <a name="getwinfxpath-task"></a>GetWinFXPath task
<xref:Microsoft.Build.Tasks.Windows.GetWinFXPath> Görev geçerli dizinin döndürür [!INCLUDE[TLA#tla_winfx](../msbuild/includes/tlasharptla_winfx_md.md)] çalışma zamanı.

## <a name="task-parameters"></a>Görev parametreleri

| Parametre | Açıklama |
|-------------------| - |
| `WinFXPath` | İsteğe bağlı **dize** çıkış parametresi.<br /><br /> Gerçek yolunu belirtir [!INCLUDE[TLA2#tla_winfx](../msbuild/includes/tla2sharptla_winfx_md.md)] çalışma zamanı. |
| `WinFXNativePath` | Gerekli **dize** parametresi.<br /><br /> Yerel yolu belirtir [!INCLUDE[TLA2#tla_titlewinfx](../msbuild/includes/tla2sharptla_titlewinfx_md.md)] çalışma zamanı. |
| `WinFXWowPath` | Gerekli **dize** parametresi.<br /><br /> Yolunu belirtir [!INCLUDE[TLA#tla_winfx](../msbuild/includes/tlasharptla_winfx_md.md)] 32-bit derlemelerde **Windows üzerinde Windows** 64-bit sistemlerde modülü. |

## <a name="remarks"></a>Açıklamalar
 Varsa <xref:Microsoft.Build.Tasks.Windows.GetWinFXPath> görev bir 64-bit işlemci üzerinde yürütme yaptığı **WinFXPath** parametrenin depolanan yoluna ayarlanmış **WinFXWowPath** parametre; Aksi takdirde **WinFXPath**  parametrenin depolanan yoluna ayarlanmış **WinFXNativePath** parametresi.

## <a name="example"></a>Örnek
 Aşağıdaki örnek nasıl kullanılacağını gösterir **GetWinFXPath** yerel yolu algılamak için görev [!INCLUDE[TLA2#tla_titlewinfx](../msbuild/includes/tla2sharptla_titlewinfx_md.md)] çalışma zamanı.

```xml
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">
  <UsingTask
    TaskName="Microsoft.Build.Tasks.Windows.GetWinFXPath"
    AssemblyFile="C:\Program Files\Reference Assemblies\Microsoft\Framework\v3.0\PresentationBuildTasks.dll" />
  <Target Name="GetWinFXPathTask">
    <GetWinFXPath
      WinFXNativePath="c:\WinFXNative"
      WinFXWowPath="c:\WinFXWowNative" />
  </Target>
  <Import Project="$(MSBuildBinPath)\Microsoft.WinFX.targets" />
</Project>
```

## <a name="see-also"></a>Ayrıca bkz.
- [WPF MSBuild başvurusu](../msbuild/wpf-msbuild-reference.md)
- [Görev başvurusu](../msbuild/wpf-msbuild-task-reference.md)
- [MSBuild başvurusu](../msbuild/msbuild-reference.md)
- [Görev başvurusu](../msbuild/msbuild-task-reference.md)
- [Bir WPF uygulaması (WPF) oluşturma](/dotnet/framework/wpf/app-development/building-a-wpf-application-wpf)
