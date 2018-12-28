---
title: SolutionFolder öğesi (Visual Studio şablonları) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/vstemplate/2005#SolutionFolder
helpviewer_keywords:
- <SolutionFolder> element [Visual Studio Templates]
- SolutionFolder element [Visual Studio Templates]
ms.assetid: 963f0398-fb50-4d8e-879d-d48f8b7c6d80
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: c5e47729d55b9c248b81c5867175fed75e8b93a8
ms.sourcegitcommit: 35bebf794f528d73d82602e096fd97d7b8f82c25
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/18/2018
ms.locfileid: "53561596"
---
# <a name="solutionfolder-element-visual-studio-templates"></a>SolutionFolder Öğesi (Visual Studio Şablonları)
Birden fazla projeli şablonlardaki projeleri gruplandırır.  
  
 \<VSTemplate >  
 \<TemplateContent >  
 \<ProjectCollection >  
 \<SolutionFolder >  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
<SolutionFolder Name="DirectoryName">  
    ...  
</SolutionFolder>  
```  
  
## <a name="attributes-and-elements"></a>Öznitelikler ve Öğeler  
 Aşağıdaki bölümlerde öznitelik, alt öğeler ve üst öğeler açıklanmaktadır.  
  
### <a name="attributes"></a>Öznitelikler  
  
|Öznitelik|Açıklama|  
|---------------|-----------------|  
|`Name`|Gerekli öznitelik.<br /><br /> Çözüm klasör'ünün adı.|  
  
### <a name="child-elements"></a>Alt Öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[ProjectTemplateLink](../extensibility/projecttemplatelink-element-visual-studio-templates.md)|İsteğe bağlı öğe.<br /><br /> Birden fazla projeli bir şablonda, tek bir projenin .vstemplate dosyasının yolunu belirtir.|  
|`SolutionFolder`|İsteğe bağlı öğe.<br /><br /> Birden fazla projeli şablonlardaki projeleri gruplandırır.|  
  
### <a name="parent-elements"></a>Üst Öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[ProjectCollection](../extensibility/projectcollection-element-visual-studio-templates.md)|Birden fazla projeli şablonların içeriğini ve düzenini belirtir.|  
|`SolutionFolder`|Birden fazla projeli şablonlardaki projeleri gruplandırır.|  
  
## <a name="remarks"></a>Açıklamalar  
 Birden fazla projeli şablonlar, iki veya daha fazla proje için kapsayıcı olarak davranır. `SolutionFolder` Öğe şablonu projelerinde gruplar halinde düzenlemek için kullanılır. Tarafından belirtilen klasörler `SolutionFolder` çözüm klasörleri projede olarak oluşturulmuş öğelere [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)]. Birden fazla projeli Şablonlar hakkında daha fazla bilgi için bkz. [nasıl yapılır: Birden çok proje şablonu oluşturma](../ide/how-to-create-multi-project-templates.md).  
  
## <a name="example"></a>Örnek  
 Bu örnekte `SolutionFolder` birden çok proje şablonu iki gruplara bölmek için öğe `Math Classes` ve `Graphics Classes`. Bu şablon, ikisi her çözüm klasöründe yer alır, dört proje içerir.  
  
```  
<VSTemplate Version="3.0.0" Type="ProjectGroup"  
    xmlns="http://schemas.microsoft.com/developer/vstemplate/2005">  
    <TemplateData>  
        <Name>Multi-Project Template Sample</Name>  
        <Description>An example of a multi-project template</Description>  
        <Icon>Icon.ico</Icon>  
        <ProjectType>VisualBasic</ProjectType>  
    </TemplateData>  
    <TemplateContent>  
        <ProjectCollection>  
            <SolutionFolder Name="Math Classes">  
                <ProjectTemplateLink ProjectName="MathClassLib1">  
                    MathClassLib1\MyTemplate.vstemplate  
                </ProjectTemplateLink>  
                <ProjectTemplateLink ProjectName="MathClassLib2">  
                    MathClassLib2\MyTemplate.vstemplate  
                </ProjectTemplateLink>  
            </SolutionFolder>  
            <SolutionFolder Name="Graphics Classes">  
                <ProjectTemplateLink ProjectName="GraphicsClassLib1">  
                    GraphicsClassLib1\MyTemplate.vstemplate  
                </ProjectTemplateLink>  
                <ProjectTemplateLink ProjectName="GraphicsClassLib2">  
                    GraphicsClassLib2\MyTemplate.vstemplate  
                </ProjectTemplateLink>  
            </SolutionFolder>  
        </ProjectCollection>  
    </TemplateContent>  
</VSTemplate>  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Visual Studio Şablon Şeması Başvurusu](../extensibility/visual-studio-template-schema-reference.md)   
 [Proje ve öğe şablonları oluşturma](../ide/creating-project-and-item-templates.md)   
 [Nasıl yapılır: Birden çok proje şablonu oluşturma](../ide/how-to-create-multi-project-templates.md)