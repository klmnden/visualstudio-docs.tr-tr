---
title: CreateNewFolder öğesi (Visual Studio şablonları) | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/vstemplate/2005#CreateNewFolder
helpviewer_keywords:
- CreateNewFolder element [Visual Studio project templates]
ms.assetid: acef2016-4140-45d6-ace8-b8160eabd676
caps.latest.revision: 15
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 7401ed7ed097c6e20bf4cd0bbf30820bcb33b514
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54794626"
---
# <a name="createnewfolder-element-visual-studio-templates"></a>CreateNewFolder Öğesi (Visual Studio Şablonları)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Projenin oluşturulacak olduğu hedef dizini yok denetlenip denetlenmeyeceğini belirler. Dizini mevcut değilse, proje için yeni bir dizin oluşturulabilir. Bu ayar genellikle tarafından geçersiz kılınır `NewProjectRequiresNewFolder(VsTemplate)` kayıt bayrağı (`HKEY_LOCAL_MACHINE/SOFTWARE(/Wow6432Node)/Microsoft/VisualStudio/<version number>/Projects/<project GUID>`) tüm ortak proje türleri, yeni bir dizinde yeni bir proje oluşturmak karar vermek için kullanın.  
  
 \<VSTemplate >  
 \<TemplateData >  
 \<CreateNewFolder >  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
<CreateNewFolder>  
    true/false  
</CreateNewFolder>  
```  
  
## <a name="type"></a>Tür  
 `Boolean`  
  
## <a name="attributes-and-elements"></a>Öznitelikler ve Öğeler  
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.  
  
### <a name="attributes"></a>Öznitelikler  
 Yok.  
  
### <a name="child-elements"></a>Alt Öğeler  
 Yok.  
  
### <a name="parent-elements"></a>Üst Öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[TemplateData](../extensibility/templatedata-element-visual-studio-templates.md)|Gerekli öğe.<br /><br /> Şablonu kategorilere ayırır ve nasıl görüntülendiğini tanımlar **yeni proje** veya **Yeni Öğe Ekle** iletişim kutusu.|  
  
## <a name="text-value"></a>Metin Değeri  
 Bir metin değeri gereklidir.  
  
 Metin olmalıdır `true` veya `false`gösteren bir proje şablondan oluşturulduğunda yeni bir kapsayıcı klasör olup olmadığını oluşturulmalıdır.  
  
## <a name="remarks"></a>Açıklamalar  
 `CreateNewFolder` İsteğe bağlı bir öğedir. Varsayılan değer `true` şeklindedir.  
  
 İçinde belirtilen değerle `CreateNewFolder` öğesi tarafından kabul yalnızca [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] temel proje sistemi destekliyorsa.  
  
## <a name="example"></a>Örnek  
 Aşağıdaki kod örneği, bir proje şablondan oluşturulduğunda yeni bir klasör oluşturmasını belirtir.  
  
```  
<VSTemplate Type="Project" Version="3.0.0"  
    xmlns="http://schemas.microsoft.com/developer/vstemplate/2005">  
    <TemplateData>  
        <Name>My template</Name>  
        <Description>A basic template</Description>  
        <Icon>TemplateIcon.ico</Icon>  
        <ProjectType>CSharp</ProjectType>  
        <CreateNewFolder>false</CreateNewFolder>  
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
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Visual Studio Şablon Şeması Başvurusu](../extensibility/visual-studio-template-schema-reference.md)   
 [Proje ve Öğe Şablonları Oluşturma](../ide/creating-project-and-item-templates.md)
