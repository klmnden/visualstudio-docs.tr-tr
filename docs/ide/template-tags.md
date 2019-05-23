---
title: Ekleme veya proje şablonları etiketlere düzenleme
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
ms.openlocfilehash: 4a5113fa7f420d58892e2737ec9196422486490e
ms.sourcegitcommit: cd21b38eefdea2cdefb53e68e7a30b868e78dd6b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/22/2019
ms.locfileid: "66038664"
---
# <a name="add-tags-to-project-templates"></a>Proje şablonları için etiketler ekleme

İtibariyle [Visual Studio 2019](https://visualstudio.microsoft.com/downloads/) sürüm 16.1 Preview 2'de, ekleyebileceğiniz dil, platform ve proje türü etiketleri için proje şablonları. Etiketler, yeni proje iletişim kutusunda iki yerde kullanılır:

- Etiketler altında şablon açıklaması görünür.

   ![Proje şablonuyla yeni proje iletişim kutusu, etiketler](media/npd-item-with-template-tags.png)

- Arama ve filtre şablonu etiketlerini etkinleştir

   ![Arama ve filtre yeni proje iletişim kutusunda](media/npd-search-and-filter.png)

Güncelleştirerek etiketler ekleyebilirsiniz *.vstemplate* Visual Studio'ya veya özel bir şablon etiketler oluşturarak oluşturulan şablon etiketleri kullanarak XML dosyası. Şablon etiketleri yalnızca Visual Studio 2019 yeni proje iletişim kutusunda görüntülenir. Bunlar, Visual Studio'nun önceki sürümlerinde şablon işleme etkilemez.

## <a name="add-or-edit-tags"></a>Ekleme veya etiketleri Düzenle

Ekleme veya düzenleme, proje şablonunun etiketleri isteyebilirsiniz *.vstemplate* XML olduğunda:

* [Yeni bir proje şablonu oluşturma](/visualstudio/ide/how-to-create-project-templates) şablonu Dışarı Aktar Sihirbazı'nı kullanarak

* [Var olan proje şablonunuzu güncelleştirin](/visualstudio/ide/how-to-update-existing-templates)

* [Yeni bir VSIX proje şablonu oluşturma](/visualstudio/extensibility/getting-started-with-the-vsix-project-template)

## <a name="syntax"></a>Sözdizimi

```xml
<LanguageTag> Language Name </LanguageTag>
<PlatformTag> Platform Name </PlatformTag>
<ProjectTypeTag> Project Type </ProjectTypeTag>
```

## <a name="attributes"></a>Öznitelikler

Aşağıdaki öznitelikler isteğe bağlıdır ve gelişmiş kullanıcı senaryoları için.

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
|[TemplateData](../extensibility/templatedata-element-visual-studio-templates.md)|(Gerekli) Şablonu kategorilere ayırır ve nasıl görüntülendiğini tanımlar **yeni proje** veya **Yeni Öğe Ekle** iletişim kutusu.|

## <a name="text-value"></a>Metin değeri

Bir metin değeri sürece gereklidir `Package` ve `ID` öznitelikleri kullanılır.

Metin şablonunun adını sağlar.

## <a name="built-in-tags"></a>Yerleşik etiketleri

Yerelleştirilmiş kaynak işleme, yerleşik bir listesini, eklenen etiketler Visual Studio sunar. Yerleşik etiketleri ve parantez içinde bunlara karşılık gelen değerler listesi aşağıda verilmiştir.

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

Aşağıdaki örnek, bir görsel için bir proje şablonu meta verileri gösterir C# uygulama.

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
- [VSIX Proje Şablonunu Kullanmaya Başlama](/visualstudio/extensibility/getting-started-with-the-vsix-project-template)