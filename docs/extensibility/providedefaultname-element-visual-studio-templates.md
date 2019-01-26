---
title: ProvideDefaultName öğesi (Visual Studio şablonları) | Microsoft Docs
ms.date: 11/04/2016
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/vstemplate/2005#ProvideDefaultName
helpviewer_keywords:
- ProvideDefaultName element [Visual Studio project templates]
ms.assetid: 7b0e7b20-fd6b-42e2-81d0-e5100cea0528
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 54f55731cd76fdeb1090eacfa42d3433ec5b323b
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55010031"
---
# <a name="providedefaultname-element-visual-studio-templates"></a>ProvideDefaultName öğesi (Visual Studio şablonları)
Belirtir olup olmadığını [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] proje sistemi, şablon için bir varsayılan ad oluşturacağını **Yeni Öğe Ekle** veya **yeni proje** iletişim kutusu.  
  
 \<VSTemplate >  
 \<TemplateData >  
 \<ProvideDefaultName >  
  
## <a name="syntax"></a>Sözdizimi  
  
```xml  
<ProvideDefaultName> true/false </ProvideDefaultName>  
```  
  
## <a name="attributes-and-elements"></a>Öznitelikler ve öğeler  
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.  
  
### <a name="attributes"></a>Öznitelikler  
 Yok.  
  
### <a name="child-elements"></a>Alt Öğeler  
 Yok.  
  
### <a name="parent-elements"></a>Üst öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[TemplateData](../extensibility/templatedata-element-visual-studio-templates.md)|Gerekli öğe.<br /><br /> Şablonu kategorilere ayırır ve nasıl görüntülendiğini tanımlar **yeni proje** veya **Yeni Öğe Ekle** iletişim kutusu.|  
  
## <a name="text-value"></a>Metin değeri  
 Bir metin değeri gereklidir.  
  
 Metin olmalıdır `true` veya `false`, şablon için varsayılan bir ad oluşturmak gerekip gerekmediğini belirten **Yeni Öğe Ekle** veya **yeni proje** iletişim kutusu.  
  
## <a name="remarks"></a>Açıklamalar  
 `ProvideDefaultName` İsteğe bağlı bir öğedir. Varsayılan değer `true` şeklindedir.  
  
 Varsa `ProvideDefaultName` öğesi `false`, **adı** kutularını **Yeni Öğe Ekle** ve **yeni proje** iletişim kutuları, bir değer içermemelidir `<Enter_name>`.  
  
 Kullanım [DefaultName](../extensibility/defaultname-element-visual-studio-templates.md) projenin varsayılan adı belirtin veya öğesi için öğe **Yeni Öğe Ekle** ve **yeni proje** iletişim kutuları. Zaman değerini `ProvideDefaultName` öğesi `true`, Java'daki `DefaultName` öğesi projeleri için iletişim kutusu şablonun adı, diğer bir deyişle, değerini doldurur [adı](../extensibility/name-element-visual-studio-templates.md) öğesi.
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnek kod `ProvideDefaultName` öğesine `false`.  
  
```  
<VSTemplate Type="Item" Version="3.0.0"  
    xmlns="http://schemas.microsoft.com/developer/vstemplate/2005">  
    <TemplateData>  
        <Name>MyClass</Name>  
        <Description>My custom C# class.</Description>  
        <Icon>Icon.ico</Icon>  
        <ProjectType>CSharp</ProjectType>  
        <ProvideDefaultName>false</ProvideDefaultName>  
    </TemplateData>  
    <TemplateContent>  
        <ProjectItem>MyClass.cs</ProjectItem>  
    </TemplateContent>  
</VSTemplate>  
```  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Visual Studio Şablon Şeması Başvurusu](../extensibility/visual-studio-template-schema-reference.md)   
 [Proje ve öğe şablonları oluşturma](../ide/creating-project-and-item-templates.md)
