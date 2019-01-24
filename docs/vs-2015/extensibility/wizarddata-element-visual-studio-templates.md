---
title: WizardData öğesi (Visual Studio şablonları) | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/vstemplate/2005#WizardData
helpviewer_keywords:
- WizardData element [Visual Studio Templates]
- <WizardData> element [Visual Studio Templates]
ms.assetid: d0403a16-5d07-4fe5-b474-19ae3d9fd3ab
caps.latest.revision: 10
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: d7cd59266a69140ba2ea5a7fd1d1b0b0c72f14c2
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54790249"
---
# <a name="wizarddata-element-visual-studio-templates"></a>WizardData Öğesi (Visual Studio Şablonları)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Özel XML belirtir  
  
 \<VSTemplate >  
 \<WizardData >  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
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
  
 İçeriğini `WizardData` öğesi geçirilir, parametreleri dize sözlüğü içinde bir parametre olarak, değiştirilmeden `IWizard.RunStarted` yöntemi. Parametre $WizardData$ adlandırılır.  
  
## <a name="example"></a>Örnek  
 Standart proje şablonu için meta veriler aşağıdaki örnekte bir [!INCLUDE[csprcs](../includes/csprcs-md.md)] Windows uygulaması.  
  
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
    <WizardData>  
        <!-- XML to pass to the custom wizard extension -->  
    </WizardData>  
</VSTemplate>  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Visual Studio Şablon Şeması Başvurusu](../extensibility/visual-studio-template-schema-reference.md)   
 [Proje ve öğe şablonları oluşturma](../ide/creating-project-and-item-templates.md)   
 [WizardExtension öğesi (Visual Studio şablonları)](../extensibility/wizardextension-element-visual-studio-templates.md)   
 [Nasıl yapılır: Sihirbazları proje şablonlarıyla kullanma](../extensibility/how-to-use-wizards-with-project-templates.md)
