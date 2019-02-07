---
title: Silme görevi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/msbuild/2003#Delete
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- Delete task [MSBuild]
- MSBuild, Delete task
ms.assetid: 916bb2e3-3017-4828-ae27-c0b5c99bbb48
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 0893ded1cd2eb40cc6004f90e29e0765ff48ca6a
ms.sourcegitcommit: 01334abf36d7e0774329050d34b3a819979c95a2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/07/2019
ms.locfileid: "55853810"
---
# <a name="delete-task"></a>Silme görevi
Belirtilen dosyaları siler.

## <a name="parameters"></a>Parametreler
Parametreleri aşağıdaki tabloda açıklanmıştır `Delete` görev.

|Parametre|Açıklama|
|---------------|-----------------|
|`DeletedFiles`|İsteğe bağlı <xref:Microsoft.Build.Framework.ITaskItem> `[]` çıkış parametresi.<br /><br /> Başarıyla silinen dosyaları belirtir.|
|`Files`|Gerekli <xref:Microsoft.Build.Framework.ITaskItem>`[]` parametresi.<br /><br /> Dosyaları silmek için belirtir.|
|`TreatErrorsAsWarnings`|İsteğe bağlı `Boolean` parametresi<br /><br /> Varsa `true`, hataları uyarı olarak kaydedilir. Varsayılan değer `false` şeklindedir.|

## <a name="remarks"></a>Açıklamalar
Yukarıda listelenen parametrelerin yanı sıra, bu görev parametreleri devralan <xref:Microsoft.Build.Tasks.TaskExtension> kendisi sınıfının devraldığı <xref:Microsoft.Build.Utilities.Task> sınıfı. Bu ek parametrelerin ve Tanımlamaların bir listesi için bkz. [TaskExtension taban sınıfı](../msbuild/taskextension-base-class.md).

## <a name="example"></a>Örnek
Aşağıdaki örnek dosyayı siler *MyApp.pdb*.

```xml
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">

    <PropertyGroup>
        <AppName>MyApp</AppName>
    </PropertyGroup>

    <Target Name="DeleteFiles">
        <Delete Files="$(AppName).pdb" />
    </Target>
</Project>
```

## <a name="see-also"></a>Ayrıca bkz.
[Görevler](../msbuild/msbuild-tasks.md)  
[Görev başvurusu](../msbuild/msbuild-task-reference.md)
