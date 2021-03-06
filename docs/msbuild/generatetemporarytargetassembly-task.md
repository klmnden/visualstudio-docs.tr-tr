---
title: GenerateTemporaryTargetAssembly görevi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- build process [WPF MSBuild], XAML page refers to a locally declared type
- GenerateTemporaryTargetAssembly task [WPF MSBuild]
- GenerateTemporaryTargetAssembly task [WPF MSBuild], parameters
- creating an assembly [WPF MSBuild], XAML page refers to a locally declared type
ms.assetid: 92b6539c-6897-45e0-8989-0c234bbfe782
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 864c15203b0b9601f2c9f5bd1421acf48120bb41
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62977839"
---
# <a name="generatetemporarytargetassembly-task"></a>GenerateTemporaryTargetAssembly görevi
<xref:Microsoft.Build.Tasks.Windows.GenerateTemporaryTargetAssembly> En az bir görev oluşturur bir derleme [!INCLUDE[TLA#tla_xaml](../msbuild/includes/tlasharptla_xaml_md.md)] projesinde sayfasına başvuruda o projede yerel olarak bildirilmiş bir tür. Oluşturulan derleme, derleme işlemi tamamlandıktan sonra veya derleme işlemi başarısız olursa kaldırılır.

## <a name="task-parameters"></a>Görev parametreleri

| Parametre | Açıklama |
|--------------------------| - |
| `AssemblyName` | Gerekli **dize** parametresi.<br /><br /> Projesi oluşturulur ve ayrıca geçici olarak oluşturulan hedef derleme adını derlemenin kısa ad belirtir. Örneğin, bir projenin oluşturduğu bir [!INCLUDE[TLA#tla_mswin](../code-quality/includes/tlasharptla_mswin_md.md)] yürütülebilir dosya adı olan *WinExeAssembly.exe*, **AssemblyName** parametresinin değerini **WinExeAssembly**. |
| `CompileTargetName` | Gerekli **dize** parametresi.<br /><br /> Adını belirtir [!INCLUDE[TLA#tla_msbuild](../msbuild/includes/tlasharptla_msbuild_md.md)] kaynak kod dosyalarını derlemeleri oluşturmak için kullanılan hedef. İçin tipik bir değer **CompileTargetName** olduğu **CoreCompile**. |
| `CompileTypeName` | Gerekli **dize** parametresi.<br /><br /> Tarafından belirtilen hedef tarafından gerçekleştirilen derleme türünü belirtir **CompileTargetName** parametresi. İçin **CoreCompile** hedef, bu değer, **derleme**. |
| `CurrentProject` | Gerekli **dize** parametresi.<br /><br /> Tam yolunu belirtir [!INCLUDE[TLA2#tla_msbuild](../msbuild/includes/tla2sharptla_msbuild_md.md)] bir geçici hedef derlemeyi projesinin proje dosyası. |
| `GeneratedCodeFiles` | İsteğe bağlı **Itaskıtem []** parametresi.<br /><br /> Tarafından üretilen dile özgü yönetilen kod dosyalarının listesini belirtir [MarkupCompilePass1](../msbuild/markupcompilepass1-task.md) görev. |
| `IntermediateOutputPath` | Gerekli **dize** parametresi.<br /><br /> Geçici hedef derleme için oluşturulan dizini belirtir. |
| `MSBuildBinPath` | Gerekli **dize** parametresi.<br /><br /> Konumunu belirtir *MSBuild.exe*, geçici hedef derlemeyi derlemek için gereklidir. |
| `ReferencePath` | İsteğe bağlı **Itaskıtem []** parametresi.<br /><br /> Geçici hedef bütünleştirilmiş kod içine derlenmiş türleri tarafından başvurulan yolu ve dosya adı ile derlemelerin bir listesini belirtir. |
| `ReferencePathTypeName` | Gerekli **dize** parametresi.<br /><br /> Derleme hedefi tarafından kullanılan bir parametre belirtir (**CompileTargetName**) parametresi derleme başvurularını listesini belirtir (**ReferencePath**). Uygun değeri **ReferencePath**. |

## <a name="remarks"></a>Açıklamalar
Tarafından çalıştırılır ve ilk biçimlendirmesi derleme geçişi [MarkupCompilePass1](../msbuild/markupcompilepass1-task.md), derler [!INCLUDE[TLA2#tla_xaml](../msbuild/includes/tla2sharptla_xaml_md.md)] dosyaları ikili biçimi. Sonuç olarak, derleyici tarafından kullanılan türleri içeren başvurulan derlemelerin listesini gereken [!INCLUDE[TLA2#tla_xaml](../msbuild/includes/tla2sharptla_xaml_md.md)] dosyaları. Ancak, bir [!INCLUDE[TLA2#tla_xaml](../msbuild/includes/tla2sharptla_xaml_md.md)] dosyasını kullanır aynı projede tanımlanan bir tür, karşılık gelen bir derleme, bu proje için proje oluşturulana kadar oluşturulmaz. Bu nedenle, bir bütünleştirilmiş kod başvurusu ilk biçimlendirme derleme geçişi sırasında sağlanamaz.

Bunun yerine, **MarkupCompilePass1** dönüştürülmesi erteler [!INCLUDE[TLA2#tla_xaml](../msbuild/includes/tla2sharptla_xaml_md.md)] ikinci bir biçimlendirme derleme aynı proje türlerinde başvuruları içeren dosyaları geçirmek, tarafından yürütülen [MarkupCompilePass2](../msbuild/markupcompilepass2-task.md). Önce **MarkupCompilePass2** olan yürütüldü, geçici bir derleme oluşturulur. Bu derleme tarafından kullanılan türler içerir [!INCLUDE[TLA2#tla_xaml](../msbuild/includes/tla2sharptla_xaml_md.md)] , biçimlendirme derleme geçişi ertelenmiş dosyaları. Oluşturulan derleme başvurusu için sağlanan **MarkupCompilePass2** ne zaman çalışacağını ertelenmiş derleme izin vermek için [!INCLUDE[TLA2#tla_xaml](../msbuild/includes/tla2sharptla_xaml_md.md)] ikili biçimine dönüştürülecek dosyaları.

## <a name="example"></a>Örnek
Aşağıdaki örnek geçici bir derleme oluşturur çünkü *Page1.xaml* aynı proje içinde bir türe başvuru içeriyor.

```xml
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">
  <UsingTask
    TaskName="Microsoft.Build.Tasks.Windows.GenerateTemporaryTargetAssembly"
    AssemblyFile="C:\Program Files\Reference Assemblies\Microsoft\Framework\v3.0\PresentationBuildTasks.dll" />
  <Target Name="GenerateTemporaryTargetAssemblyTask">
    <GenerateTemporaryTargetAssembly
      AssemblyName="WPFMSBuildSample"
      CompileTargetName="CoreCompile"
      CompileTypeName="Compile"
      CurrentProject="FullBuild.proj"
      GeneratedCodeFiles="obj\debug\app.g.cs;obj\debug\Page1.g.cs;obj\debug\Page2.g.cs"
      ReferencePath="c:\windows\Microsoft.net\Framework\v2.0.50727\System.dll;C:\Program Files\Reference Assemblies\Microsoft\WinFx\v3.0\PresentationCore.dll;C:\Program Files\Reference Assemblies\Microsoft\WinFx\v3.0\PresentationFramework.dll;C:\Program Files\Reference Assemblies\Microsoft\WinFx\v3.0\WindowsBase.dll"
      IntermediateOutputPath=".\obj\debug\"
      MSBuildBinPath="$(MSBuildBinPath)"
      ReferencePathTypeName="ReferencePath"/>
  </Target>
</Project>
```

## <a name="see-also"></a>Ayrıca bkz.
- [WPF MSBuild başvurusu](../msbuild/wpf-msbuild-reference.md)
- [Görev başvurusu](../msbuild/wpf-msbuild-task-reference.md)
- [MSBuild başvurusu](../msbuild/msbuild-reference.md)
- [Görev başvurusu](../msbuild/msbuild-task-reference.md)
- [Bir WPF uygulaması (WPF) oluşturma](/dotnet/framework/wpf/app-development/building-a-wpf-application-wpf)
- [WPF XAML tarayıcı uygulamalarına genel bakış](/dotnet/framework/wpf/app-development/wpf-xaml-browser-applications-overview)
