---
title: ProjectType öğesi (Visual Studio şablonları) | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/vstemplate/2005#ProjectType
helpviewer_keywords:
- ProjectType element [Visual Studio project templates]
ms.assetid: ccf9d83f-c7f3-49c7-a31f-e1f22bec004c
caps.latest.revision: 20
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 8d9836702b00b51d1e2dbe1cd64687c892feaba4
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54765055"
---
# <a name="projecttype-element-visual-studio-templates"></a>ProjectType Öğesi (Visual Studio Şablonları)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Belirtilen grubun altında görünmesi proje şablonu kategorilere ayırır **yeni proje** veya **Yeni Öğe Ekle** iletişim kutusu.  
  
> [!WARNING]
>  Proje şablonları, c++, Visual Studio 2012'den itibaren desteklenir. C++'da Visual Studio 2010 ve önceki sürümleri için desteklenmez.  
  
 \<VSTemplate >  
 \<TemplateData >  
 \<ProjectType >  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
<ProjectType> CSharp/VisualBasic/VC/Web </ProjectType>  
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
|[TemplateData](../extensibility/templatedata-element-visual-studio-templates.md)|Şablonu kategorilere ayırır ve nasıl görüntülendiğini tanımlar **yeni proje** veya **Yeni Öğe Ekle** iletişim kutusu.|  
  
## <a name="text-value"></a>Metin Değeri  
 Bir metin değeri gereklidir.  
  
 Bu değer, türde bir proje şablonu oluşturur ve aşağıdaki değerlerden birini içermelidir belirtir:  
  
-   `CSharp`: Şablon oluşturur belirtir bir [!INCLUDE[csprcs](../includes/csprcs-md.md)] proje veya öğe.  
  
-   `VisualBasic`: Şablon oluşturur belirtir bir [!INCLUDE[vbprvb](../includes/vbprvb-md.md)] proje veya öğe.  
  
-   `Web`: Şablonu bir Web proje veya öğe oluşturup belirtir. Varsa `ProjectType` öğesi içerir, bu değer, dil proje veya öğe içinde tanımlanan [ProjectSubType öğesi (Visual Studio şablonları)](../extensibility/projectsubtype-element-visual-studio-templates.md).  
  
## <a name="remarks"></a>Açıklamalar  
 `ProjectType` gerekli alt öğesi olan `TemplateData`.  
  
 Değerini `ProjectType` öğeyi belirten bir şablon içinde bulunduğu **yeni proje** veya **Yeni Öğe Ekle** iletişim kutusu. Örneğin, bir şablonu ile bir `ProjectType` değerini `CSharp` altında görünür **Visual C#** düğümünde **yeni proje** iletişim kutusu.  
  
 Kullanarak şablon alt belirtilebilir [ProjectSubType](../extensibility/projectsubtype-element-visual-studio-templates.md) öğesi.  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnek, bir proje şablonu için meta verileri gösterir. bir [!INCLUDE[csprcs](../includes/csprcs-md.md)] uygulama.  
  
```  
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
 [Proje ve öğe şablonları oluşturma](../ide/creating-project-and-item-templates.md)   
 [ProjectSubType Öğesi (Visual Studio Şablonları)](../extensibility/projectsubtype-element-visual-studio-templates.md)
