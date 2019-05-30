---
title: TemplateContent öğesi (Visual Studio şablonları) | Microsoft Docs
ms.date: 11/04/2016
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/vstemplate/2005#TemplateContent
helpviewer_keywords:
- TemplateContent element [Visual Studio project templates]
ms.assetid: 90ae401c-b294-49ac-98da-e0d274f5bebb
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 71911ee480daa965dfbc3df43ea2e76cf2021d08
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66316633"
---
# <a name="templatecontent-element-visual-studio-templates"></a>TemplateContent Öğesi (Visual Studio Şablonları)

Şablonu içeriğini belirtir.

Öğe hiyerarşisi:

```xml
<VSTemplate>
  <TemplateContent>
```

## <a name="syntax"></a>Sözdizimi

```xml
<TemplateContent>
    ...
</TemplateContent>
```

## <a name="attributes-and-elements"></a>Öznitelikler ve Öğeler
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.

### <a name="attributes"></a>Öznitelikler

|Öznitelik|Açıklama|
|---------------|-----------------|
|[BuildOnLoad](../extensibility/buildonload-visual-studio-templates.md)|Bir proje şablondan oluşturulduğunda çözümü derlemek belirtir.|

### <a name="child-elements"></a>Alt Öğeler

|Öğe|Açıklama|
|-------------|-----------------|
|[ProjectCollection](../extensibility/projectcollection-element-visual-studio-templates.md)|İsteğe bağlı öğe.<br /><br /> Birden fazla projeli şablonların içeriğini ve düzenini belirtir.|
|[Project](../extensibility/project-element-visual-studio-templates.md)|İsteğe bağlı öğe.<br /><br /> Dosyaları veya dizinleri projeye eklemek için belirtir.|
|[Başvurular](../extensibility/references-element-visual-studio-templates.md)|İsteğe bağlı öğe.<br /><br /> Öğe şablonu için gerekli derleme başvurularını belirtir.|
|[ProjectItem](../extensibility/projectitem-element-visual-studio-item-templates.md)|İsteğe bağlı öğe.<br /><br /> Şablonda yer alan bir dosyayı belirtir.|
|[CustomParameters](../extensibility/customparameters-element-visual-studio-templates.md)|İsteğe bağlı öğe.<br /><br /> Şablondan bir proje veya öğe oluşturulduğunda kullanılacak olan herhangi bir özel parametre belirtir.|

### <a name="parent-elements"></a>Üst Öğeler

|Öğe|Açıklama|
|-------------|-----------------|
|[VSTemplate](../extensibility/vstemplate-element-visual-studio-templates.md)|Gerekli öğe.<br /><br /> Proje şablonu, öğe şablonu veya başlangıç Seti için meta veriler içerir.|

## <a name="remarks"></a>Açıklamalar
 `TemplateContent` gerekli bir öğedir.

## <a name="example"></a>Örnek
 Aşağıdaki örnek, bir proje şablonu için meta verileri gösterir. bir [!INCLUDE[csprcs](../data-tools/includes/csprcs_md.md)] uygulama.

```xml
<VSTemplate Type="Project" Version="3.0.0"
    xmlns="http://schemas.microsoft.com/developer/vstemplate/2005">
    <TemplateData>
        <Name>My template</Name>
        <Description>A basic starter kit</Description>
        <Icon>TemplateIcon.ico</Icon>
        <ProjectType>CSharp</ProjectType>
    </TemplateData>
    <TemplateContent>
        <Project File="MyStarterKit.csproj">
            <ProjectItem>Form1.cs<ProjectItem>
            <ProjectItem>Form1.Designer.cs</ProjectItem>
            <ProjectItem>Program.cs</ProjectItem>
            <ProjectItem>Properties\AssemblyInfo.cs</ProjectItem>
            <ProjectItem>Properties\Resources.resx</ProjectItem>
            <ProjectItem>Properties\Resources.Designer.cs</ProjectItem>
            <ProjectItem>Properties\Settings.settings</ProjectItem>
            <ProjectItem>Properties\Settings.Designer.cs</ProjectItem>
        </Project>
    </TemplateContent>
</VSTemplate>
```

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio Şablon Şeması Başvurusu](../extensibility/visual-studio-template-schema-reference.md)
- [Proje ve Öğe Şablonları Oluşturma](../ide/creating-project-and-item-templates.md)