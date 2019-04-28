---
title: MSBuild proje dosyası şema başvurusu | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- MSBuild, file schema
ms.assetid: d9a68146-1f43-4621-ac78-2c8c3f400936
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: c49c2198a4ecc40a40e3f5f6414bfd4af47279b8
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62842298"
---
# <a name="msbuild-project-file-schema-reference"></a>MSBuild proje dosyası şema başvurusu
Tüm bir tablo sağlar [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] XML Şeması öğeleri kullanılabilir öznitelikler ve alt öğeleri.

 [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] derleme ve oluşturma nasıl yapı altyapısının ne istemek için proje dosyalarını kullanır. [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] Proje dosyalardır izliyor XML dosyaları [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] XML şeması. Bu bölüm XML şema tanımı belge (*.xsd*) dosya [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)].

## <a name="msbuild-xml-schema-elements"></a>MSBuild XML Şeması öğeleri
 Aşağıdaki tabloda tüm listeler [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] XML Şeması öğeleri alt öğeleri ve öznitelikleri birlikte.

|Öğe|Alt öğeleri|Öznitelikler|
|-------------|--------------------|----------------|
|[Öğe Seç (MSBuild)](../msbuild/choose-element-msbuild.md)|Aksi takdirde<br /><br /> Ne zaman|--|
|[İçeri aktarma öğesi (MSBuild)](../msbuild/import-element-msbuild.md)|--|Koşul<br /><br /> Project|
|[Importgroup öğesi](../msbuild/importgroup-element.md)|İçeri Aktarma|Koşul|
|[Öğe unsuru (MSBuild)](../msbuild/item-element-msbuild.md)|*ItemMetaData*|Koşul<br /><br /> Hariç tutma<br /><br /> Şunları Dahil Et:<br /><br /> Kaldır|
|[Itemdefinitiongroup öğesi (MSBuild)](../msbuild/itemdefinitiongroup-element-msbuild.md)|*Öğesi*|Koşul|
|[ItemGroup öğesi (MSBuild)](../msbuild/itemgroup-element-msbuild.md)|*Öğesi*|Koşul|
|[Itemmetadata öğesi (MSBuild)](../msbuild/itemmetadata-element-msbuild.md)|*Öğesi*|Koşul|
|[OnError öğesi (MSBuild)](../msbuild/onerror-element-msbuild.md)|--|Koşul<br /><br /> ExecuteTargets|
|[Otherwise öğesi (MSBuild)](../msbuild/otherwise-element-msbuild.md)|Bunu seçin<br /><br /> ItemGroup<br /><br /> PropertyGroup|--|
|[Çıktı öğesi (MSBuild)](../msbuild/output-element-msbuild.md)|--|Koşul<br /><br /> ItemName<br /><br /> ÖzellikAdı<br /><br /> TaskParameter|
|[Parameter öğesi](../msbuild/parameter-element.md)|--|Çıkış<br /><br /> ParameterType<br /><br /> Gerekli|
|[ParameterGroup öğesi](../msbuild/parametergroup-element.md)|*Parametre*|--|
|[Proje öğesi (MSBuild)](../msbuild/project-element-msbuild.md)|Bunu seçin<br /><br /> İçeri Aktarma<br /><br /> ItemGroup<br /><br /> ProjectExtensions<br /><br /> PropertyGroup<br /><br /> Hedef<br /><br /> UsingTask|DefaultTargets<br /><br /> InitialTargets<br /><br /> ToolsVersion<br /><br /> TreatAsLocalProperty<br /><br /> xmlns|
|[ProjectExtensions öğesi (MSBuild)](../msbuild/projectextensions-element-msbuild.md)|--|--|
|[Özellik öğesi (MSBuild)](../msbuild/property-element-msbuild.md)|--|Koşul|
|[PropertyGroup öğesi (MSBuild)](../msbuild/propertygroup-element-msbuild.md)|*Özelliği*|Koşul|
|[SDK'sı öğesi (MSBuild)](../msbuild/sdk-element-msbuild.md)|--|Ad<br /><br /> Sürüm|
|[Hedef öğe (MSBuild)](../msbuild/target-element-msbuild.md)|OnError<br /><br /> *Görev*|AfterTargets<br /><br /> BeforeTargets<br /><br /> Koşul<br /><br /> DependsOnTargets<br /><br /> Girişler<br /><br /> KeepDuplicateOutputs<br /><br /> Ad<br /><br /> Çıktılar<br /><br /> Döndürür|
|[Görev öğesi (MSBuild)](../msbuild/task-element-msbuild.md)|Çıkış|Koşul<br /><br /> ContinueOnError<br /><br /> *Parametre*|
|[TaskBody öğesi (MSBuild)](../msbuild/taskbody-element-msbuild.md)|*Veri*|Değerlendir|
|[UsingTask öğesi (MSBuild)](../msbuild/usingtask-element-msbuild.md)|ParameterGroup<br /><br /> TaskBody|AssemblyFile<br /><br /> AssemblyName<br /><br /> Koşul<br /><br /> TaskFactory<br /><br /> TaskName|
|[Zaman öğesi (MSBuild)](../msbuild/when-element-msbuild.md)|Bunu seçin<br /><br /> ItemGroup<br /><br /> PropertyGroup|Koşul|

## <a name="see-also"></a>Ayrıca bkz.
- [Görev başvurusu](../msbuild/msbuild-task-reference.md)
- [Koşullar](../msbuild/msbuild-conditions.md)
- [MSBuild başvurusu](../msbuild/msbuild-reference.md)
- [MSBuild](../msbuild/msbuild.md)
