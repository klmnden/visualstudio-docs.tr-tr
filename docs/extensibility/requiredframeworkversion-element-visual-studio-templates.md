---
title: RequiredFrameworkVersion öğesi (Visual Studio şablonları) | Microsoft Docs
ms.date: 11/04/2016
ms.technology: vs-ide-general
ms.topic: reference
helpviewer_keywords:
- <RequiredFrameworkVersion> (Visual Studio Templates)
- RequiredFrameworkVersion (Visual Studio Templates)
ms.assetid: 08a4f609-51a5-4723-b89f-99277fb18871
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 40eefc62eef318bcd9c52a1cbbb966377b3616f8
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54947003"
---
# <a name="requiredframeworkversion-element-visual-studio-templates"></a>RequiredFrameworkVersion öğesi (Visual Studio şablonları)

Şablon tarafından gerekli .NET Framework'ün en düşük sürümünü belirtir. Neden **hedef Framework sürümü** görüntülenecek açılan **yeni proje** iletişim. `RequiredFrameworkVersion` Öğesi, açılan listede kullanılabilir olan en düşük değer de belirler.

> [!IMPORTANT]
> Visual Studio 2017 sürüm 15.6, başlangıç **hedef Framework sürümü** açılan bir filtre görüntülenen şablonları için artık değil **şablonları** bölümünü **YeniProje** iletişim. Bunun yerine, seçilen şablonu için bir çerçeve Seçici açılan görür.

 \<VSTemplate > \<TemplateData > \<RequiredFrameworkVersion >

## <a name="syntax"></a>Sözdizimi

```xml
<RequiredFrameworkVersion> .... </RequiredFrameworkVersion>
```

## <a name="attributes-and-elements"></a>Öznitelikler ve öğeler
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.

### <a name="attributes"></a>Öznitelikler
 Yok.

### <a name="child-elements"></a>Alt öğeleri
 Yok.

### <a name="parent-elements"></a>Üst öğeler

|Öğe|Açıklama|
|-------------|-----------------|
|[TemplateData](../extensibility/templatedata-element-visual-studio-templates.md)|Gerekli öğe.<br /><br /> Şablonu kategorilere ayırır ve ya da nasıl görüntüleneceğini tanımlar **yeni proje** veya **Yeni Öğe Ekle** iletişim kutusu.|

## <a name="text-value"></a>Metin değeri
 Bir metin değeri gereklidir.

 Metin şablon için gerekli olan .NET Framework'ün en düşük sürüm numarası olmalıdır.

## <a name="remarks"></a>Açıklamalar

`RequiredFrameworkVersion` İsteğe bağlı bir öğedir. Şablonu yalnızca belirli bir en düşük sürümü (ve sonraki sürümleri varsa) destekliyorsa, bu öğeyi kullanın .NET Framework'ün. Belirtirseniz `RequiredFrameworkVersion` öğesi ve şablonunuzun belirli bir en düşük sürümü .NET Framework'ün desteklemiyor **hedef Framework sürümü** açılan uygun olmadığı durumlarda görüntülenir.

## <a name="example"></a>Örnek

Standart için meta veriler aşağıdaki örnekte [!INCLUDE[csprcs](../data-tools/includes/csprcs_md.md)] sınıf şablonu.

```xml
<VSTemplate Type="Item" Version="3.0.0"
    xmlns="http://schemas.microsoft.com/developer/vstemplate/2005">
    <TemplateData>
        <Name>MyClass</Name>
        <Description>My custom C# class template.</Description>
        <Icon>Icon.ico</Icon>
        <ProjectType>CSharp</ProjectType>
        <RequiredFrameworkVersion>3.0</RequiredFrameworkVersion>
        <MaxFrameworkVersion>4.7.1</MaxFrameworkVersion>
        <DefaultName>MyClass</DefaultName>
    </TemplateData>
    <TemplateContent>
        <ProjectItem>MyClass.cs</ProjectItem>
    </TemplateContent>
</VSTemplate>
```

Bu örnekte, şablon tarafından gerekli .NET Framework'ün en düşük sürüm temsil ettiği `RequiredFrameworkVersion`, 3. 0. Bu şablon kullanılarak oluşturulan bir proje .NET Framework sürüm 3.0 başlayarak hedefleyebilirsiniz.

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio Şablon Şeması Başvurusu](../extensibility/visual-studio-template-schema-reference.md)
- [Proje ve öğe şablonları oluşturma](../ide/creating-project-and-item-templates.md)
- [Belirli bir .NET Framework sürümünü hedefleme](../ide/visual-studio-multi-targeting-overview.md)
