---
title: NumberOfParentCategoriesToRollUp öğesi (Visual Studio şablonları)
ms.date: 11/04/2016
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/vstemplate/2005#NumberOfParentCategoriesToRollUp
helpviewer_keywords:
- NumberOfParentCategoriesToRollUp element [Visual Studio Templates]
- <NumberOfParentCategoriesToRollUp> element [Visual Studio Templates]
ms.assetid: 6f9d36f5-ae23-4a92-8132-b11799e2c21a
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: b733b65a62db3cb39197fbdbed4c471651eae49a
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56687954"
---
# <a name="numberofparentcategoriestorollup-element-visual-studio-templates"></a>NumberOfParentCategoriesToRollUp öğesi (Visual Studio şablonları)
Şablonda görüntüler üst kategori sayısını belirtir **yeni proje** iletişim kutusu.

 \<VSTemplate > \<TemplateData > \<NumberOfParentCategoriesToRollUp >

## <a name="syntax"></a>Sözdizimi

```xml
<NumberOfParentCategoriesToRollUp>
1
</NumberOfParentCategoriesToRollUp>
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
|[TemplateData](../extensibility/templatedata-element-visual-studio-templates.md)|Şablonu kategorilere ayırır ve nasıl görüntülendiğini tanımlar **yeni proje** veya **Yeni Öğe Ekle** iletişim kutusu.|

## <a name="text-value"></a>Metin değeri
 Bir `integer` değeri gereklidir.

 Bu değer, şablonda görüntüler üst kategori sayısını belirtir. **yeni proje** iletişim kutusu.

## <a name="remarks"></a>Açıklamalar
 `NumberOfParentCategoriesToRollUp` İsteğe bağlı bir öğedir.

## <a name="example"></a>Örnek
 Bu örnek için meta verileri gösterir. bir [!INCLUDE[csprcs](../data-tools/includes/csprcs_md.md)] Windows uygulaması. Bu meta veriler ile bir şablon iki klasör düzeyi en üst düzey yerleştirdiyseniz [!INCLUDE[csprcs](../data-tools/includes/csprcs_md.md)] düğümü, şablonu içinde üst düzey düğümünde görünür **yeni proje** iletişim kutusu. Varsa `NumberOfParentCategoriesToRollUp` ayarlanmazsa şablon yalnızca, BT konumlandırıldığını düğümünde görüntülenir.

```xml
<VSTemplate Type="Project" Version="3.0.0"
    xmlns="http://schemas.microsoft.com/developer/vstemplate/2005">
    <TemplateData>
        <Name>My template</Name>
        <Description>A basic starter kit</Description>
        <Icon>TemplateIcon.ico</Icon>
        <ProjectType>CSharp</ProjectType>
        <NumberOfParentCategoriesToRollUp>2</NumberOfParentCategoriesToRollUp>
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
- [Proje ve öğe şablonları oluşturma](../ide/creating-project-and-item-templates.md)