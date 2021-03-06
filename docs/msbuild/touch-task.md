---
title: Dokunma görevi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/msbuild/2003#Touch
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- MSBuild, Touch task
- Touch task [MSBuild]
ms.assetid: 8a978645-1393-4904-ae69-42afabd8c109
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 96bf92f6e0649a2d1eedda63d6159c3de95ae6bd
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62938862"
---
# <a name="touch-task"></a>Dokunma görevi
Dosya erişim ve değişiklik saatlerini ayarlar.

## <a name="parameters"></a>Parametreler
 Parametreleri aşağıdaki tabloda açıklanmıştır `Touch` görev.

|Parametre|Açıklama|
|---------------|-----------------|
|`AlwaysCreate`|İsteğe bağlı `Boolean` parametresi.<br /><br /> Varsa `true`, zaten mevcut olan tüm dosyaları oluşturur.|
|`Files`|Gerekli <xref:Microsoft.Build.Framework.ITaskItem>`[]` parametresi.<br /><br /> Dokunmaya dosya koleksiyonunu belirtir.|
|`ForceTouch`|İsteğe bağlı `Boolean` parametresi.<br /><br /> Varsa `true`, salt okunur dosyalar olsa bile dosya touch zorlar.|
|`Time`|İsteğe bağlı `String` parametresi.<br /><br /> Geçerli saat dışında bir süreyi belirtir. Biçim için kabul edilebilir bir biçimde olmalıdır <xref:System.DateTime.Parse%2A> yöntemi.|
|`TouchedFiles`|İsteğe bağlı <xref:Microsoft.Build.Framework.ITaskItem> `[]` çıkış parametresi.<br /><br /> Başarıyla dokunulan öğeleri koleksiyonunu içerir.|

## <a name="remarks"></a>Açıklamalar
 Yukarıda listelenen parametrelerin yanı sıra, bu görev parametreleri devralan <xref:Microsoft.Build.Tasks.TaskExtension> kendisi sınıfının devraldığı <xref:Microsoft.Build.Utilities.Task> sınıfı. Bu ek parametrelerin ve Tanımlamaların bir listesi için bkz. [TaskExtension taban sınıfı](../msbuild/taskextension-base-class.md).

## <a name="example"></a>Örnek
 Aşağıdaki örnekte `Touch` içinde belirtilen dosya erişim ve değişiklik saatlerini değiştirmek için görev `Files` öğe koleksiyonu ve başarıyla bilgiler dosyaların listesini koyar `FilesTouched` öğe koleksiyonu.

```xml
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">

<ItemGroup>
    <Files Include="File1.cs;File2.cs;File3.cs" />
</ItemGroup>

    <Target Name="TouchFiles">
        <Touch
            Files="@(Files)">
            <Output
                TaskParameter="TouchedFiles"
                ItemName="FilesTouched"/>
    </Touch>
</Target>
</Project>
```

## <a name="see-also"></a>Ayrıca bkz.
- [Görevler](../msbuild/msbuild-tasks.md)
- [Görev başvurusu](../msbuild/msbuild-task-reference.md)