---
title: LC görevi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/msbuild/2003#LC
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- MSBuild, LC task
- LC task [MSBuild]
ms.assetid: d5a53472-6f2a-42b8-a6db-593ca99c9790
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: fa9a210b61a1ba28d2dca2f81184b3d20a91ff7f
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56638707"
---
# <a name="lc-task"></a>LC görevi
Sarmalar *LC.exe*, oluşturduğu bir *.license* dosyasını bir *.licx* dosya. Daha fazla bilgi için *LC.exe*, bkz: [Lc.exe (lisans derleyici)](/dotnet/framework/tools/lc-exe-license-compiler).

## <a name="parameters"></a>Parametreler
Parametreler için aşağıdaki tabloda açıklanmıştır `LC` görev.

|Parametre|Açıklama|
|---------------|-----------------|
|`LicenseTarget`|Gerekli <xref:Microsoft.Build.Framework.ITaskItem> parametresi.<br /><br /> Yürütülebilir dosya için belirten *.licenses* dosyalar oluşturulur.|
|`NoLogo`|İsteğe bağlı `Boolean` parametresi.<br /><br /> Microsoft başlangıç başlığı görüntüsünü bastırır.|
|`OutputDirectory`|İsteğe bağlı `String` parametresi.<br /><br /> Çıkış yerleştirileceği dizini belirtir *.licenses* dosyaları.|
|`OutputLicense`|İsteğe bağlı <xref:Microsoft.Build.Framework.ITaskItem> çıkış parametresi.<br /><br /> Adını belirtir *.licenses* dosya. Adı bir ad belirtmezseniz *.licx* dosya kullanılır ve *.licenses* dosyasını içeren dizine yerleştirilir *.licx* dosya.|
|`ReferencedAssemblies`|İsteğe bağlı <xref:Microsoft.Build.Framework.ITaskItem> `[]` parametresi.<br /><br /> Oluştururken yüklemek için başvurulan bileşenlerini belirtir *.license* dosya.|
|`SdkToolsPath`|İsteğe bağlı `String` parametresi.<br /><br /> SDK Araçları yolunu gibi belirtir *resgen.exe*.|
|`Sources`|Gerekli <xref:Microsoft.Build.Framework.ITaskItem>`[]` parametresi.<br /><br /> Dahil etmek için lisanslı bileşenleri içeren öğelerini belirten *.licenses* dosya. Daha fazla bilgi için belgelerine bakın `/complist` anahtarının [Lc.exe (lisans derleyici)](/dotnet/framework/tools/lc-exe-license-compiler).|

 Yukarıda listelenen parametrelerin yanı sıra, bu görev parametreleri devralan <xref:Microsoft.Build.Tasks.ToolTaskExtension> kendisi sınıfının devraldığı <xref:Microsoft.Build.Utilities.ToolTask> sınıfı. Bu ek parametrelerin ve Tanımlamaların bir listesi için bkz. [ToolTaskExtension taban sınıfı](../msbuild/tooltaskextension-base-class.md).

## <a name="example"></a>Örnek
Aşağıdaki örnekte `LC` lisansları derlemek için bir görev.

```xml
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">
<!-- Item declarations, etc -->

    <Target Name="CompileLicenses">
        <LC
            Sources="@(LicxFile)"
            LicenseTarget="$(TargetFileName)"
            OutputDirectory="$(IntermediateOutputPath)"
            OutputLicenses="$(IntermediateOutputPath)$(TargetFileName).licenses"
            ReferencedAssemblies="@(ReferencePath);@(ReferenceDependencyPaths)">

            <Output
                TaskParameter="OutputLicenses"
                ItemName="CompiledLicenseFile"/>
        </LC>
    </Target>
</Project>
```

## <a name="see-also"></a>Ayrıca bkz.
- [Görevler](../msbuild/msbuild-tasks.md)
- [Görev başvurusu](../msbuild/msbuild-task-reference.md)
