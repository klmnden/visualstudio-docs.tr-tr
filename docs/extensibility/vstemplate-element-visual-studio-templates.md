---
title: VSTemplate öğesi (Visual Studio şablonları) | Microsoft Docs
ms.date: 11/04/2016
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/vstemplate/2005#VSTemplate
helpviewer_keywords:
- VSTemplate element [Visual Studio project templates]
ms.assetid: f8ac561b-3b0b-4246-9ec9-118d2447e9a9
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: cdcbde9ab8e49d439ab909b4cd5563d6b8ec3afa
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66322862"
---
# <a name="vstemplate-element-visual-studio-templates"></a>VSTemplate öğesi (Visual Studio şablonları)
Proje şablonu, öğe şablonu veya başlangıç Seti hakkındaki meta verileri içerir.

## <a name="syntax"></a>Sözdizimi

```csharp
<VSTemplate Type="TemplateType" Version="x.x.x">
    <TemplateData>    </TemplateData>
    <TemplateContent>    </TemplateContent>
    ...
</VSTemplate>
```

## <a name="attributes-and-elements"></a>Öznitelikler ve öğeler
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.

### <a name="attributes"></a>Öznitelikler

| Öznitelik | Açıklama |
|-----------| - |
| `Type` | Şablonu proje şablonu veya bir öğe şablonu olarak tanımlar. Bu öznitelik değeri olabilir `Project` veya `Item`. |
| `Version` | Şablon için bir sürüm numarasını belirtir. Şablonlarda [!INCLUDE[vs_dev10_long](../code-quality/includes/vs_dev10_long_md.md)] ve [!INCLUDE[vs_dev11_long](../data-tools/includes/vs_dev11_long_md.md)] sahip bir `Version` öznitelik değerini `3.0.0`. |

### <a name="child-elements"></a>Alt öğeleri

|Öğe|Açıklama|
|-------------|-----------------|
|[TemplateData](../extensibility/templatedata-element-visual-studio-templates.md)|Gerekli öğe.<br /><br /> Şablonu kategorilere ayırır ve içinde biçimini tanımlar verileri belirtir **yeni proje** veya **Yeni Öğe Ekle** iletişim kutusu.|
|[TemplateContent](../extensibility/templatecontent-element-visual-studio-templates.md)|Gerekli öğe.<br /><br /> Şablonu içeriğini belirtir.|
|[WizardExtension](../extensibility/wizardextension-element-visual-studio-templates.md)|İsteğe bağlı öğe.|
|[WizardData](../extensibility/wizarddata-element-visual-studio-templates.md)|İsteğe bağlı öğe.|

### <a name="parent-elements"></a>Üst öğeler
 Yok.

## <a name="remarks"></a>Açıklamalar
 `VSTemplate` Öğedir kök öğesi *.vstemplate* dosyaları.

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
            <ProjectItem>Form1.cs</ProjectItem>
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
- [Proje ve öğe şablonları oluşturma](../ide/creating-project-and-item-templates.md)