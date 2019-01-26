---
title: WizardExtension öğesi (Visual Studio şablonları) | Microsoft Docs
ms.date: 11/04/2016
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/vstemplate/2005#WizardExtension
helpviewer_keywords:
- WizardExtension element [Visual Studio Templates]
- <WizardExtension> element [Visual Studio Templates]
ms.assetid: d54b01c1-50f5-4b65-828c-686e2321cc8c
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 4e3b2a01976dede37e3f20d5b9fcc8853e548502
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54986169"
---
# <a name="wizardextension-element-visual-studio-templates"></a>WizardExtension Öğesi (Visual Studio Şablonları)
Şablon Sihirbazı'nı özelleştirmek için kayıt öğeleri içerir.  
  
 \<VSTemplate >  
 ...  
 \<WizardExtension >  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
<WizardExtension>  
    <Assembly>... </Assembly>  
    <FullClassName>... </FullClassName>  
</WizardExtension>  
```  
  
## <a name="attributes-and-elements"></a>Öznitelikler ve Öğeler  
 Aşağıdaki bölümlerde öznitelik, alt öğeler ve üst öğeler açıklanmaktadır.  
  
### <a name="attributes"></a>Öznitelikler  
 Yok.  
  
### <a name="child-elements"></a>Alt Öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[Assembly](../extensibility/assembly-element-visual-studio-template-wizard-extension.md)|Gerekli öğe.<br /><br /> Adını veya genel derleme önbelleğinde görünen derlemenin tanımlayıcı adını belirtir. Mutlaka bir en az bir tane `Assembly` öğesinde bir `WizardExtension` öğesi.|  
|[FullClassName](../extensibility/fullclassname-element-visual-studio-template-wizard-extension.md)|Gerekli öğe.<br /><br /> Uygulayan sınıfın tam adını `IWizard` arabirimi. Mutlaka bir en az bir tane `FullClassName` öğesinde bir `WizardExtension` öğesi.|  
  
### <a name="parent-elements"></a>Üst Öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[VSTemplate](../extensibility/vstemplate-element-visual-studio-templates.md)|Proje şablonu, öğe şablonu veya başlangıç Seti için meta veriler içerir.|  
  
## <a name="remarks"></a>Açıklamalar  
 `WizardExtension` bir isteğe bağlı bir alt öğesidir `VSTemplate`.  
  
## <a name="example"></a>Örnek  
 Standart proje şablonu için meta veriler aşağıdaki örnekte bir [!INCLUDE[csprcs](../data-tools/includes/csprcs_md.md)] Windows uygulaması.  
  
```  
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
</VSTemplate>  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Visual Studio Şablon Şeması Başvurusu](../extensibility/visual-studio-template-schema-reference.md)   
 [Proje ve öğe şablonları oluşturma](../ide/creating-project-and-item-templates.md)   
 [Nasıl yapılır: Sihirbazları proje şablonlarıyla kullanma](../extensibility/how-to-use-wizards-with-project-templates.md)