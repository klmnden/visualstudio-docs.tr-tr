---
title: SupportsMasterPage öğesi (Visual Studio şablonları) | Microsoft Docs
ms.date: 11/04/2016
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/vstemplate/2005#SupportsMasterPage
helpviewer_keywords:
- <SupportsMasterPage> element [Visual Studio Templates]
- SupportsMasterPage element [Visual Studio Templates]
ms.assetid: ce877a6a-9bba-4fd9-92fb-0a8dfec9e75b
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: fa55ed4344ab071d49b9f0e4030acb2a0762b2a9
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56691988"
---
# <a name="supportsmasterpage-element-visual-studio-templates"></a>SupportsMasterPage Öğesi (Visual Studio Şablonları)
Belirtir veya olmadığını **ana sayfa seçin** onay kutusunu etkin **Yeni Öğe Ekle** iletişim kutusu.

 \<VSTemplate > \<TemplateData > \<SupportsMasterPage >

## <a name="syntax"></a>Sözdizimi

```
<SupportsMasterPage> true/false </SupportsMasterPage>
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
|[TemplateData](../extensibility/templatedata-element-visual-studio-templates.md)|Şablonu kategorilere ayırır ve içinde biçimini tanımlar verileri belirtir **yeni proje** veya **yeni öğe** iletişim kutusu.|

## <a name="text-value"></a>Metin Değeri
 Bir metin değeri gereklidir.

 Metin olmalıdır `true` veya `false`gösteren olup olmadığını **ana sayfa seçin** onay kutusunu etkin **Yeni Öğe Ekle** iletişim kutusu.

## <a name="remarks"></a>Açıklamalar
 `SupportsMasterPage` İsteğe bağlı bir öğedir. Varsayılan değer `false` şeklindedir.

 `SupportsMasterPage` Öğesi, yalnızca Web öğesi şablonları için kullanılabilir.

## <a name="example"></a>Örnek
 Aşağıdaki örnek, bir ana sayfa desteği içeren bir Web projesi için meta verileri gösterir.

```
<VSTemplate Version="3.0.0" Type="Project"
    xmlns="http://schemas.microsoft.com/developer/vstemplate/2005">>
    <TemplateData>
        <Name>MyWebProjecStarterKit</Name>
        <Description>A simple Web template</Description>
        <Icon>icon.ico</Icon>
        <ProjectType>Web</ProjectType>
        <ProjectSubType>CSharp</ProjectSubType>
        <DefaultName>WebSite</DefaultName>
        <SupportsMasterPage>true</SupportsMasterPage>
    </TemplateData>
    <TemplateContent>
        <Project File="WebApplication.webproj">
            <ProjectItem>icon.ico</ProjectItem>
            <ProjectItem OpenInEditor="true">Default.aspx</ProjectItem>
            <ProjectItem>Default.aspx.cs</ProjectItem>
        </Project>
    </TemplateContent>
</VSTemplate>
```

## <a name="see-also"></a>Ayrıca Bkz.
- [Visual Studio Şablon Şeması Başvurusu](../extensibility/visual-studio-template-schema-reference.md)
- [Proje ve Öğe Şablonları Oluşturma](../ide/creating-project-and-item-templates.md)