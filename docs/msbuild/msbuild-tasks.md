---
title: MSBuild görevleri | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- tasks
- MSBuild, tasks
ms.assetid: 5d3cc4a7-e5db-4f73-b707-8b6882fddcf8
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 90b6731cf75a1825139aba57fe8491cd7cb0253f
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63004551"
---
# <a name="msbuild-tasks"></a>MSBuild görevleri
Bir yapı platformunu herhangi bir sayıda eylemleri derleme işlemi sırasında yürütme yeteneği gerekir. [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] kullanan *görevleri* bu eylemleri gerçekleştirmek için. Bir görev tarafından kullanılan yürütülebilir kod birimidir [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] CAN atomik yapı işlemleri gerçekleştirmek için.

## <a name="task-logic"></a>Görev mantığı
 [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] XML proje dosyası biçimi, proje dosyasının bunu kendi, görev mantıksal işlemleri uygulanan derleme tam olarak yürütülemiyor.

 Bir görevin yürütülme mantığı uygulayan bir .NET sınıfı uygulanır <xref:Microsoft.Build.Framework.ITask> tanımlanan arabirimi <xref:Microsoft.Build.Framework> ad alanı.

 Görev sınıfı proje dosyasında görev ayrıca giriş ve çıkış parametrelerini tanımlar. Görev sınıfı tarafından kullanıma sunulan tüm genel ayarlanabilir statik olmayan soyut olmayan özellikler üzerinde aynı ada sahip karşılık gelen bir öznitelik yerleştirerek proje dosyasında erişilebilir [görev](../msbuild/task-element-msbuild.md) öğesi.

 Yazma uygulayan yönetilen bir sınıf tarafından kendi görevinizi yazabilirsiniz <xref:Microsoft.Build.Framework.ITask> arabirimi. Daha fazla bilgi için [görev yazma](../msbuild/task-writing.md).

## <a name="execute-a-task-from-a-project-file"></a>Proje dosyasından bir görev yürütme
 Proje dosyanızda bir görev yürütülmeden önce görev adı ile görevi uygulayan derlemedeki tür ilk eşlenmelidir [UsingTask](../msbuild/usingtask-element-msbuild.md) öğesi. Böylece [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] proje dosyanızda bulduğunda, görevin yürütülme mantığı için aranacağı bildirin.

 Bir görev olarak çalıştırmak için bir [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] proje dosyası, bir alt öğesi olarak görev adı ile bir öğe oluşturmaya bir `Target` öğesi. Görev parametreleri kabul ediyorsa, bu öğenin öznitelikleri geçirilir.

 [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] öğe listeleri ve özellikleri parametre olarak kullanılabilir. Örneğin, aşağıdaki çağrıları kod `MakeDir` görev ve değerini ayarlar `Directories` özelliği `MakeDir` nesne değerine eşit `BuildDir` özelliği, önceki örnekte bildirilen.

```xml
<Target Name="MakeBuildDirectory">
    <MakeDir
        Directories="$(BuildDir)" />
</Target>
```

 Görevler, ayrıca öğeleri ya da daha sonra kullanmak için özellikler depolanabilir proje dosyasına bilgi döndürebilir. Örneğin, aşağıdaki çağrıları kod `Copy` bilgileri depolar ve görev `CopiedFiles` çıkış özelliğinde `SuccessfullyCopiedFiles` öğe listesi.

```xml
<Target Name="CopyFiles">
    <Copy
        SourceFiles="@(MySourceFiles)"
        DestinationFolder="@(MyDestFolder)">
        <Output
            TaskParameter="CopiedFiles"
            ItemName="SuccessfullyCopiedFiles"/>
     </Copy>
</Target>
```

## <a name="included-tasks"></a>Dahil edilen görevler
 [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] gibi birçok görevi ile birlikte gelen [kopyalama](../msbuild/copy-task.md), dosyaları kopyalayan [MakeDir](../msbuild/makedir-task.md), dizinler oluşturan ve [Csc](../msbuild/csc-task.md), hangi derler [!INCLUDE[csprcs](../data-tools/includes/csprcs_md.md)] kaynak kodu dosyaları. Kullanılabilir görevlerin ve kullanım bilgilerinin tam listesi için bkz: [görev başvurusu](../msbuild/msbuild-task-reference.md).

## <a name="overridden-tasks"></a>Geçersiz kılınan görevleri
 [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] Görevler çeşitli konumlarda arar. Uzantılı dosyalar ilk konumdur *. OverrideTasks* .NET Framework dizinlerinde depolanan. Bu dosyalar, görevler proje dosyasına görevler de dahil olmak üzere aynı ada sahip herhangi bir görevi geçersiz kılar. Dosya uzantısı olan ikinci konumdur *. Görevleri* .NET Framework dizinlerde. Görev bu konumlardan birini bulunamazsa, görev proje dosyasında kullanılır.

## <a name="see-also"></a>Ayrıca bkz.
- [MSBuild kavramları](../msbuild/msbuild-concepts.md)
- [MSBuild](../msbuild/msbuild.md)
- [Görev yazma](../msbuild/task-writing.md)
- [Satır içi görevleri](../msbuild/msbuild-inline-tasks.md)