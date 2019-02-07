---
title: Kopyalama görevi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/msbuild/2003#Copy
- MSBuild.Copy.SourceFileNotFound
- MSBuild.Copy.Retrying
- MSBuild.Copy.ExceededRetries
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- MSBuild, Copy task
- Copy task [MSBuild]
ms.assetid: a46ba9da-3e4e-4890-b4ea-09a099b6bc40
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 7f974cde33103f86aa7330600e87c856119f537c
ms.sourcegitcommit: 01334abf36d7e0774329050d34b3a819979c95a2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/07/2019
ms.locfileid: "55853553"
---
# <a name="copy-task"></a>Kopyalama görevi
Dosyaları, dosya sisteminde yeni bir konuma kopyalar.

## <a name="parameters"></a>Parametreler
Parametreleri aşağıdaki tabloda açıklanmıştır `Copy` görev.

|Parametre|Açıklama|
|---------------|-----------------|
|`CopiedFiles`|İsteğe bağlı <xref:Microsoft.Build.Framework.ITaskItem> `[]` çıkış parametresi.<br /><br /> Başarılıyla kopyalanan öğeleri içerir.|
|`DestinationFiles`|İsteğe bağlı <xref:Microsoft.Build.Framework.ITaskItem> `[]` parametresi.<br /><br /> Kaynak dosyaların kopyalanacağı dosyaların listesini belirtir. Bu listenin, `SourceFiles` parametresinde belirtilen liste ile bire bir eşlenir olması beklenir. Yani, `SourceFiles` içinde belirtilen ilk dosya `DestinationFiles` içinde belirtilen ilk konuma kopyalanır ve böyle devam eder.|
|`DestinationFolder`|İsteğe bağlı <xref:Microsoft.Build.Framework.ITaskItem> parametresi.<br /><br /> Dosyaları kopyalamak istediğiniz dizini belirtir. Bu, bir dosya değil, bir dizin olmalıdır. Eğer dizin yoksa otomatik olarak oluşturulur.|
|`OverwriteReadOnlyFiles`|İsteğe bağlı `Boolean` parametresi.<br /><br /> Salt okunur dosyalar olarak işaretlenmiş olsa bile dosyaların üzerine yaz|
|`Retries`|İsteğe bağlı `Int32` parametresi.<br /><br /> Eğer önceki tüm denemeler başarısız olursa, kopyalamanın kaç kere deneneceğini belirtir. Varsayılan olarak sıfırdır.<br /><br /> **Not:** Denemelerin kullanımı, yapılandırma işleminizdeki bir eşitleme sorununu gizleyebilir.|
|`RetryDelayMilliseconds`|İsteğe bağlı `Int32` parametresi.<br /><br /> Gerekli yeniden denemeler arasındaki gecikmeyi belirtir. Varsayılan olarak, CopyTask oluşturucusuna geçirilen RetryDelayMillisecondsDefault değerini kullanır.|
|`SkipUnchangedFiles`|İsteğe bağlı `Boolean` parametresi.<br /><br /> Eğer `true` ise, kaynak ve hedef arasında değişmeyen dosyaların kopyalanmasını atlar. `Copy` görevi, dosyalar aynı boyuta ve aynı son değiştirme tarihine sahipse bu dosyaları değişmemiş kabul eder. <br /><br /> **Not:**  Eğer bu parametreyi `true` olarak ayarlarsanız, içeren hedef üzerinde bağımlılık çözümlememesi kullanmamanız gerekir; çünkü bu, görevi sadece kaynak dosyalarının son değiştirme tarihleri hedef dosyaların son değiştirme tarihlerinden daha yeniyse çalıştırır.|
|`SourceFiles`|Gerekli <xref:Microsoft.Build.Framework.ITaskItem>`[]` parametresi.<br /><br /> Kopyalanacak dosyaları belirtir.|
|`UseHardlinksIfPossible`|İsteğe bağlı `Boolean` parametresi.<br /><br /> Eğer `true` ise, dosyaları kopyalamak yerine kopyalanan dosyalar için Sabit Bağlantılar oluşturur.|

## <a name="warnings"></a>Uyarılar
Uyarılar dahil olmak üzere kaydedilir:

- `Copy.DestinationIsDirectory`

- `Copy.SourceIsDirectory`

- `Copy.SourceFileNotFound`

- `Copy.CreatesDirectory`

- `Copy.HardLinkComment`

- `Copy.RetryingAsFileCopy`

- `Copy.FileComment`

- `Copy.RemovingReadOnlyAttribute`

## <a name="remarks"></a>Açıklamalar
`DestinationFolder` veya `DestinationFiles` parametresinin belirtilmesi gerekir, ancak ikisi birden belirtilmemelidir. Eğer her ikisi de belirtilirse görev başarısız olur ve bir hata günlüğe kaydedilir.

Yukarıda listelenen parametrelerin yanı sıra, bu görev parametreleri devralan <xref:Microsoft.Build.Tasks.TaskExtension> kendisi sınıfının devraldığı <xref:Microsoft.Build.Utilities.Task> sınıfı. Bu ek parametrelerin ve Tanımlamaların bir listesi için bkz. [TaskExtension taban sınıfı](../msbuild/taskextension-base-class.md).

## <a name="example"></a>Örnek
Aşağıdaki örnek, öğeler kopyalar `MySourceFiles` öğe koleksiyonundaki klasörüne *c:\MyProject\Destination*.

```xml
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">

    <ItemGroup>
        <MySourceFiles Include="a.cs;b.cs;c.cs"/>
    </ItemGroup>

    <Target Name="CopyFiles">
        <Copy
            SourceFiles="@(MySourceFiles)"
            DestinationFolder="c:\MyProject\Destination"
        />
    </Target>

</Project>
```

## <a name="example"></a>Örnek
Aşağıdaki örnek, yinelemeli bir kopyalamanın nasıl gerçekleştirileceğini gösterir. Bu projenin tüm dosyaları yinelemeli olarak kopyalar *c:\MySourceTree* içine *c:\MyDestinationTree*, dizin yapısını koruyarak.

```xml
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">

    <ItemGroup>
        <MySourceFiles Include="c:\MySourceTree\**\*.*"/>
    </ItemGroup>

    <Target Name="CopyFiles">
        <Copy
            SourceFiles="@(MySourceFiles)"
            DestinationFiles="@(MySourceFiles->'c:\MyDestinationTree\%(RecursiveDir)%(Filename)%(Extension)')"
        />
    </Target>

</Project>
```

## <a name="see-also"></a>Ayrıca bkz.
[Görevler](../msbuild/msbuild-tasks.md)  
[Görev başvurusu](../msbuild/msbuild-task-reference.md)
