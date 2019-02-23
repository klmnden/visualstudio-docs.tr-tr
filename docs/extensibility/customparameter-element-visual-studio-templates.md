---
title: CustomParameter öğesi (Visual Studio şablonları) | Microsoft Docs
ms.date: 11/04/2016
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/vstemplate/2005#CustomParameter
helpviewer_keywords:
- CustomParameters element [Visual Studio project templates]
ms.assetid: 743c4489-74ac-403a-bbaa-eed7d785a3ac
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: dc0ac3d936037e9b92567a6fcf20b26c25cb5d3f
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56705943"
---
# <a name="customparameter-element-visual-studio-templates"></a>CustomParameter öğesi (Visual Studio şablonları)
Bir özel parametre adı ve şablondan bir proje veya öğe oluşturulduğunda kullanılacak değeri içerir.

## <a name="syntax"></a>Sözdizimi

```
<CustomParameter Name="name" Value="value">
```

## <a name="attributes-and-elements"></a>Öznitelikler ve öğeler
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.

### <a name="attributes"></a>Öznitelikler

|Öznitelik|Açıklama|
|---------------|-----------------|
|`Name`|Gerekli. Parametrenin adı. Parametre biçimi $*adı*$.|
|`Value`|Gerekli. Parametre değiştirme değeri.|

### <a name="child-elements"></a>Alt öğeleri
 Yok.

### <a name="parent-elements"></a>Üst öğeler

|Öğe|Açıklama|
|-------------|-----------------|
|[CustomParameters](../extensibility/customparameters-element-visual-studio-templates.md)|Sihirbaz parametresi değişiklik yaptığında için Şablon Sihirbazı'nı geçirilecek özel parametreler gruplandırır.|

## <a name="remarks"></a>Açıklamalar
 Bir şablon içerdiğinde `CustomParameter` öğeleri, her örnek `Name` özniteliği ile değiştirilir `Value` oluşturulan proje veya öğe dosya özniteliği.

## <a name="example"></a>Örnek
 Aşağıdaki örnek, şablonda birkaç özel parametreler kullanmayı gösterir. Bir proje veya öğe oluşturulduğunda aşağıdaki özel parametreleri, tüm örneklerini ile bir şablondan `$color1$` ve `$color2$` şablon dosyaları ile değiştirilecek `Red` ve `Blue`sırasıyla.

```
<CustomParameters>
    <CustomParameter Name="$color1$" Value="Red"/>
    <CustomParameter Name="$color2$" Value="Blue "/>
</CustomParameters>
```

## <a name="see-also"></a>Ayrıca bkz.
- [CustomParameters öğesi (Visual Studio şablonları)](../extensibility/customparameters-element-visual-studio-templates.md)
- [Şablon parametreleri](../ide/template-parameters.md)
- [Visual Studio Şablon Şeması Başvurusu](../extensibility/visual-studio-template-schema-reference.md)