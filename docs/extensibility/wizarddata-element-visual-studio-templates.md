---
title: WizardData öğesi (Visual Studio şablonları) | Microsoft Docs
ms.date: 11/04/2016
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/vstemplate/2005#WizardData
helpviewer_keywords:
- WizardData element [Visual Studio Templates]
- <WizardData> element [Visual Studio Templates]
ms.assetid: d0403a16-5d07-4fe5-b474-19ae3d9fd3ab
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: ad5ae7e2e83cb0f8db6cf0b2482547e66ab89497
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66350762"
---
# <a name="wizarddata-element-visual-studio-templates"></a>WizardData Öğesi (Visual Studio Şablonları)

Özel XML belirtir

```xml
\<VSTemplate>
\<WizardData>
```

## <a name="syntax"></a>Sözdizimi

```xml
<WizardData>
    <!-- XML to pass to the custom wizard extension -->
    ...
</WizardData>
```

## <a name="attributes-and-elements"></a>Öznitelikler ve Öğeler

Aşağıdaki bölümlerde öznitelik, alt öğeler ve üst öğeler açıklanmaktadır.

### <a name="attributes"></a>Öznitelikler

Yok.

### <a name="child-elements"></a>Alt Öğeler

Yok.

### <a name="parent-elements"></a>Üst Öğeler

|Öğe|Açıklama|
|-------------|-----------------|
|[VSTemplate](../extensibility/vstemplate-element-visual-studio-templates.md)|Gerekli öğe.<br /><br /> Proje şablonu, öğe şablonu veya başlangıç Seti için meta veriler içerir.|

## <a name="text-value"></a>Metin Değeri

Metin değeri isteğe bağlıdır.

Belirtilen özel sihirbaz uzantısı geçirmek için özel XML bu metni [WizardExtension](../extensibility/wizardextension-element-visual-studio-templates.md) öğesi.

## <a name="remarks"></a>Açıklamalar

Bu öğe, XML belirtilebilir. XML parametre olarak bu öğenin içeriğini kullanılacak uzantısı izin vermek için özel sihirbaz uzantısı geçirilir. Bu veriler üzerinde doğrulama gerçekleştirilir.

İçeriğini **WizardData** öğesi geçirilir, parametreleri dize sözlüğü içinde bir parametre olarak, değiştirilmeden `IWizard.RunStarted` yöntemi. Sözlük anahtarı adlı `$wizarddata$`.

## <a name="example"></a>Örnek

Standart proje şablonu için meta veriler aşağıdaki örnekte bir C# Windows uygulaması.

```xml
<VSTemplate Version="3.0.0" Type="Item"
    xmlns="http://schemas.microsoft.com/developer/vstemplate/2005">
    <TemplateData>
        <Name>MyTemplate</Name>
        <Description>Template using IWizard extension</Description>
        <Icon>TemplateIcon.ico</Icon>
        <ProjectType>CSharp</ProjectType>
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
    <WizardExtension>
        <Assembly>MyWizard, Version=1.0.3300.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a, Custom=null</Assembly>
        <FullClassName>MyWizard.CustomWizard</FullClassName>
    </WizardExtension>
    <WizardData>
        <!-- XML to pass to the custom wizard extension -->
    </WizardData>
</VSTemplate>
```

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio Şablon Şeması Başvurusu](../extensibility/visual-studio-template-schema-reference.md)
- [Proje ve Öğe Şablonları Oluşturma](../ide/creating-project-and-item-templates.md)
- [WizardExtension Öğesi (Visual Studio Şablonları)](../extensibility/wizardextension-element-visual-studio-templates.md)
- [Nasıl yapılır: Proje Şablonlarıyla Sihirbazlar Kullanma](../extensibility/how-to-use-wizards-with-project-templates.md)