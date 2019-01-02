---
title: BuildProjectOnload öğesi (Visual Studio şablonları) | Microsoft Docs
ms.date: 11/04/2016
ms.technology: vs-ide-general
ms.topic: reference
ms.assetid: b07d3074-0fc9-45e1-baf5-da6bd4f3f1c0
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 83fcafc765e6d4dbfdde865dd0ad66048370cb0c
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53850878"
---
# <a name="buildprojectonload-element-visual-studio-templates"></a>BuildProjectOnload öğesi (Visual Studio şablonları)
Yalnızca yeni projeler oluşturmak ve bunları bir çözüme eklemek gibi oluşturur. Tüm çözüm hazırladılar değil.

Öğe hiyerarşisi:

```xml
<VSTemplate>
  <TemplateData>
    <BuildProjectOnLoad>
```

## <a name="syntax"></a>Sözdizimi

```vb
<BuildProjectOnLoad> true/false </BuildProjectOnLoad>
```

## <a name="attributes-and-elements"></a>Öznitelikler ve öğeler
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.

### <a name="attributes"></a>Öznitelikler
 Yok.

### <a name="child-elements"></a>Alt öğeleri
 Yok.

### <a name="parent-elements"></a>Üst öğeler

|Öğe|Açıklama|
|-------------|-----------------|
|`TemplateData`|Şablonu kategorilere ayırır ve her ikisinde de görüntülenme şeklini tanımlayan **yeni proje** ve **Yeni Öğe Ekle** iletişim kutuları.|

## <a name="text-value"></a>Metin değeri
 Bir metin değeri gereklidir.

 Metin olmalıdır `true` veya `false` şablondan oluşturulduğunda, yalnızca yeni projeyi derlemek gösteren.

## <a name="remarks"></a>Açıklamalar
 `BuildProjectOnLoad` İsteğe bağlı bir öğedir. Varsayılan değer `false` şeklindedir.

## <a name="example"></a>Örnek
 Aşağıdaki örnek, bir Visual C# şablonu meta verileri gösterir.

```xml
<VSTemplate Type="Project" Version="3.0.0"
    xmlns="http://schemas.microsoft.com/developer/vstemplate/2005">
    <TemplateData>
        <Name>My template</Name>
        <Description>A basic template</Description>
        <Icon>TemplateIcon.ico</Icon>
        <ProjectType>CSharp</ProjectType>
        <BuildProjectOnload>true</BuildProjectOnLoad>
    </TemplateData>
    <TemplateContent>
        <Project File="MyTemplate.csproj">
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

- [BuildOnLoad özniteliği ve öğesi](buildonload-visual-studio-templates.md)
- [Proje ve öğe şablonları oluşturma](../ide/creating-project-and-item-templates.md)
- [Visual Studio Şablon Şeması Başvurusu](../extensibility/visual-studio-template-schema-reference.md)