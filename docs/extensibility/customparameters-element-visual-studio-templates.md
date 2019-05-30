---
title: CustomParameters öğesi (Visual Studio şablonları) | Microsoft Docs
ms.date: 11/04/2016
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/vstemplate/2005#CustomParameters
helpviewer_keywords:
- CustomParameters element [Visual Studio project templates]
ms.assetid: cf3efc91-1532-4022-bbb8-a18658424fee
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 8089e84f5414798fdf6a4707e8bde65e4df5e0a2
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66350201"
---
# <a name="customparameters-element-visual-studio-templates"></a>CustomParameters öğesi (Visual Studio şablonları)
Sihirbaz parametresi değişiklik yaptığında için Şablon Sihirbazı'nı geçirilecek özel parametreler gruplandırır.

## <a name="syntax"></a>Sözdizimi

```
<CustomParameters>
    <CustomParameter/>
    <CustomParameter/>
</CustomParameters>
```

## <a name="attributes-and-elements"></a>Öznitelikler ve öğeler
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.

### <a name="attributes"></a>Öznitelikler
 Yok.

### <a name="child-elements"></a>Alt öğeleri

|Öğe|Açıklama|
|-------------|-----------------|
|[CustomParameter](../extensibility/customparameter-element-visual-studio-templates.md)|İsteğe bağlı öğe.<br /><br /> Bir özel parametre adı ve şablondan bir proje veya öğe oluşturulduğunda kullanılacak değeri içerir. Sıfır veya daha fazla olabilir `CustomParameter` öğelerinde bir `CustomParameters` öğesi.|

### <a name="parent-elements"></a>Üst öğeler

|Öğe|Açıklama|
|-------------|-----------------|
|[TemplateContent](../extensibility/templatecontent-element-visual-studio-templates.md)|Şablonu içeriğini belirtir.|

## <a name="remarks"></a>Açıklamalar

## <a name="example"></a>Örnek
 Aşağıdaki örnek, şablonda birkaç özel parametreler kullanmayı gösterir. Bir proje veya öğe oluşturulduğunda aşağıdaki özel parametreleri, tüm örneklerini ile bir şablondan `$color1$` ve `$color2$` şablon dosyaları ile değiştirilecek `Red` ve `Blue`sırasıyla.

```
<CustomParameters>
    <CustomParameter Name="$color1$" Value="Red"/>
    <CustomParameter Name="$color2$" Value="Blue "/>
</CustomParameters>
```

## <a name="see-also"></a>Ayrıca bkz.
- [CustomParameter öğesi (Visual Studio şablonları)](../extensibility/customparameter-element-visual-studio-templates.md)
- [Şablon parametreleri](../ide/template-parameters.md)
- [Visual Studio Şablon Şeması Başvurusu](../extensibility/visual-studio-template-schema-reference.md)