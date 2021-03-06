---
title: LocationField öğesi (Visual Studio Proje şablonları) | Microsoft Docs
ms.date: 11/04/2016
ms.technology: vs-ide-general
ms.topic: conceptual
f1_keywords:
- http://schemas.microsoft.com/developer/vstemplate/2005#LocationField
helpviewer_keywords:
- LocationField element [Visual Studio project templates]
ms.assetid: 6aaaa155-6ce0-4f7f-aa50-8d63d7a7c992
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: b440595207cee6a146e6d85ee5e9f7c492ee3eee
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66309165"
---
# <a name="locationfield-element-visual-studio-project-templates"></a>LocationField öğesi (Visual Studio Proje şablonları)
Belirtir olup olmadığını **konumu** metin kutusu **yeni proje** iletişim kutusu etkin, devre dışı veya gizli proje şablonu.

 \<VSTemplate > \<TemplateData > \<LocationField >

## <a name="syntax"></a>Sözdizimi

```
<LocationField> Enabled/Disabled/Hidden </LocationField>
```

## <a name="attributes-and-elements"></a>Öznitelikler ve öğeler
 Aşağıdaki bölümlerde öznitelik, alt öğeler ve üst öğeler açıklanmaktadır.

### <a name="attributes"></a>Öznitelikler
 Yok.

### <a name="child-elements"></a>Alt öğeleri
 Yok.

### <a name="parent-elements"></a>Üst öğeler

|Öğe|Açıklama|
|-------------|-----------------|
|[TemplateData](../extensibility/templatedata-element-visual-studio-templates.md)|Gerekli öğe.<br /><br /> Şablonu kategorilere ayırır ve nasıl görüntülendiğini tanımlar **yeni proje**.|

## <a name="text-value"></a>Metin değeri
 Bir metin değeri gereklidir.

 Geçerli bir metin değerleri şunlardır:

- `Enabled`, hangi belirtir **konumu** kutusunun **yeni proje** iletişim kutusu etkin.

- `Disabled`, hangi belirtir **konumu** kutusunun **yeni proje** iletişim kutusu devre dışı bırakıldı.

- `Hidden`, hangi belirtir **konumu** kutusunun **yeni proje** iletişim kutusu gizlenir.

## <a name="remarks"></a>Açıklamalar
 Varsayılan değer `Enabled` şeklindedir.

 **Konumu** metin kutusu **yeni proje** iletişim kutusu yeni projeler kaydedilir varsayılan dizinini değiştirme olanağı sağlar.

 İçinde belirtilen değerle `Location` temel proje sistemi destekliyorsa öğesi iletişim kutusu tarafından yalnızca kabul.

## <a name="example"></a>Örnek
 Meta veriler için aşağıdaki örnekte bir [!INCLUDE[csprcs](../data-tools/includes/csprcs_md.md)] şablonu.

```
<VSTemplate Type="Project" Version="3.0.0"
    xmlns="http://schemas.microsoft.com/developer/vstemplate/2005">
    <TemplateData>
        <Name>My template</Name>
        <Description>A basic template</Description>
        <Icon>TemplateIcon.ico</Icon>
        <ProjectType>CSharp</ProjectType>
        <LocationField>Disabled</LocationField>
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
- [Visual Studio Şablon Şeması Başvurusu](../extensibility/visual-studio-template-schema-reference.md)
- [Proje ve öğe şablonları oluşturma](../ide/creating-project-and-item-templates.md)