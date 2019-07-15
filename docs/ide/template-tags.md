---
title: Ekleme veya proje şablonları etiketlere düzenleme
description: Visual Studio Proje şablonları etiketlere ekleyip öğrenin.
ms.date: 04/30/2019
author: minsa110
ms.author: somin
manager: jillfra
ms.topic: reference
helpviewer_keywords:
- item templates, updating
- Visual Studio templates, updating
- project templates, updating
- updating templates [Visual Studio]
- template tagging, updating
- template tags, updating
ms.openlocfilehash: 417b171a731224302e6dd2efa55b45d84455ca4b
ms.sourcegitcommit: 748d9cd7328a30f8c80ce42198a94a4b5e869f26
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/15/2019
ms.locfileid: "67891146"
---
# <a name="add-tags-to-project-templates"></a>Proje şablonları için etiketler ekleme

İtibariyle [Visual Studio 2019](https://visualstudio.microsoft.com/downloads/) sürüm 16.1 Preview 2'de, ekleyebileceğiniz dil, platform ve proje türü etiketleri için proje şablonları. 

Etiketler, iki yerde kullanılır **yeni proje** iletişim kutusunda:

- Etiketler, şablon açıklaması altında görünür.

   ![Proje şablonuyla yeni proje iletişim kutusundaki etiketler](media/npd-item-with-template-tags.png)

- Etiketler, arama ve filtre şablonu etkinleştirin.

   ![Arama ve filtre yeni proje iletişim kutusunda](media/npd-search-and-filter.png)

Güncelleştirerek etiketler ekleyebilirsiniz *.vstemplate* XML dosyası. Visual Studio'da yerleşik olarak bulunan şablon etiketler kullanabilir veya özel bir şablon etiketler oluşturma. Şablon etiketleri yalnızca Visual Studio 2019 içinde görünür **yeni proje** iletişim kutusu. Şablon etiketleri şablonu Visual Studio'nun önceki sürümlerinde nasıl işlediğini etkilemez.

## <a name="add-or-edit-tags"></a>Ekleme veya etiketleri Düzenle

Proje şablonunun etiketleri ekleyip isteyebileceğiniz *.vstemplate* aşağıdaki eylemlerden birini, XML:

* [Yeni bir proje şablonu oluşturma](/visualstudio/ide/how-to-create-project-templates) şablonu Dışarı Aktar Sihirbazı'nı kullanarak.
* [Var olan proje şablonunuzu güncelleştirme](/visualstudio/ide/how-to-update-existing-templates).
* [Yeni bir VSIX proje şablonu oluşturma](/visualstudio/extensibility/getting-started-with-the-vsix-project-template).

## <a name="syntax"></a>Sözdizimi

```xml
<LanguageTag> Language Name </LanguageTag>
<PlatformTag> Platform Name </PlatformTag>
<ProjectTypeTag> Project Type </ProjectTypeTag>
```

## <a name="attributes"></a>Öznitelikler

Gelişmiş Kullanıcı senaryolarda aşağıdaki isteğe bağlı öznitelikleri kullanabilirsiniz:

|Öznitelik|Açıklama|
|---------------|-----------------|
|`Package`|Visual Studio Paketi belirten bir GUID kimliği|
|`ID`|Visual Studio kaynak kimliğini belirtir.|

Sözdizimi:

```xml
<LanguageTag Package="{PackageID}" ID="ResourceID" />
<PlatformTag Package="{PackageID}" ID="ResourceID" />
<ProjectTypeTag Package="{PackageID}" ID="ResourceID" />
```

## <a name="elements"></a>Öğeler

### <a name="child-elements"></a>Alt öğeleri

Yok.

### <a name="parent-elements"></a>Üst öğeler

|Öğe|Açıklama|
|-------------|-----------------|
|[TemplateData](../extensibility/templatedata-element-visual-studio-templates.md)|(Gerekli) Şablonu kategorilere ayırır ve nasıl görüntülendiğini tanımlar **yeni proje** iletişim kutusu veya **Yeni Öğe Ekle** iletişim kutusu.|

## <a name="text-value"></a>Metin değeri

Kullandığınız sürece, bir metin değeri gereklidir `Package` ve `ID` öznitelikleri.

Metin şablonunun adını sağlar.

## <a name="built-in-tags"></a>Yerleşik etiketleri

Visual Studio yerleşik etiketlerin bir listesini sunar. Yerleşik bir etiket eklediğinizde, yerelleştirilmiş kaynak etiketi oluşturur. 

Aşağıdaki liste, Visual Studio'da kullanılabilen yerleşik etiketleri gösterir. Karşılık gelen değerler, parantez içinde gösterilmektedir.

| Dil | Platform | Proje türü |
| -- | -- | -- |
| C++ (`cpp`) | Android (`android`) | Cloud (`cloud`) |
| C#(`csharp`) | Azure (`azure`) | Konsolu (`console`) |
| F#(`fsharp`) | iOS (`ios`) | Masaüstü (`desktop`) |
| Java (`java`) | Linux (`linux`) | Uzantılar (`extension`) |
| JavaScript (`javascript`) | macOS (`macos`) | Oyunlar (`games`) |
| Python (`python`) | tvOS (`tvos`) | IOT (`iot`) |
| Sorgu Languate (`querylanguage`) | Windows (`windows`) | Kitaplık (`library`) |
| TypeScript (`typescript`) | Xbox (`xbox`) | Machine Learning (`machinelearning`) |
| Visual Basic (`visualbasic`) | | Mobile (`mobile`) |
| | | Office (`office`) |
| | | Diğer (`other`) |
| | | Hizmet (`service`) |
| | | Test (`test`) |
| | | UWP (`uwp`) |
| | | Web (`web`) |

## <a name="example"></a>Örnek

Aşağıdaki örnek, bir görsel için bir proje şablonu meta verileri gösterir C# uygulama:

```xml
<VSTemplate Type="Project" Version="3.0.0"
    xmlns="http://schemas.microsoft.com/developer/vstemplate/2005">
    <TemplateData>
        <Name>My template</Name>
        <Description>A basic template</Description>
        <Icon>TemplateIcon.ico</Icon>
        <ProjectType>CSharp</ProjectType>
        <LanguageTag>C#</LanguageTag>
        <PlatformTag>windows</PlatformTag>
        <PlatformTag>linux</PlatformTag>
        <PlatformTag>My Platform</PlatformTag>
        <ProjectTypeTag>console</ProjectTypeTag>
        <ProjectTypeTag>desktop</ProjectTypeTag>
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

- [Visual Studio Şablon Şeması Başvurusu](/visualstudio/extensibility/visual-studio-template-schema-reference)
- [Proje ve öğe şablonları oluşturma](/visualstudio/ide/creating-project-and-item-templates)
- [Proje ve öğe şablonlarını özelleştirme](/visualstudio/ide/customizing-project-and-item-templates)
- [VSIX proje şablonunu kullanmaya başlama](/visualstudio/extensibility/getting-started-with-the-vsix-project-template)
