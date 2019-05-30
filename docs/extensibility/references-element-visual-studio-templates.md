---
title: Öğesi (Visual Studio şablonları) başvuruda | Microsoft Docs
ms.date: 11/04/2016
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/vstemplate/2005#References
helpviewer_keywords:
- <References> element [Visual Studio Templates]
- References element [Visual Studio Templates]
ms.assetid: 1969146d-46bf-422d-8d46-0e9493925003
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: e2ab5c3decc201958bd939a0a9d66dd65a5ef1c6
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66334415"
---
# <a name="references-element-visual-studio-templates"></a>References öğesi (Visual Studio şablonları)
Gruplar için proje şablonu ekleyen derleme başvuruları.

 \<VSTemplate > \<TemplateContent > \<başvuruları >

## <a name="syntax"></a>Sözdizimi

```xml
<References>
    <Reference>... </Reference>
    <Reference>... </Reference>
    ...
</References>
```

## <a name="attributes-and-elements"></a>Öznitelikler ve öğeler
 Aşağıdaki bölümlerde öznitelik, alt öğeler ve üst öğeler açıklanmaktadır.

### <a name="attributes"></a>Öznitelikler
 Yok.

### <a name="child-elements"></a>Alt öğeleri

|Öğe|Açıklama|
|-------------|-----------------|
|[Başvuru](../extensibility/reference-element-visual-studio-templates.md)|Gerekli öğe.<br /><br /> Öğe bir projeye eklendiğinde eklemek için derleme başvurusu belirtir. Bir veya daha fazla olmalıdır `Reference` öğelerinde bir `References` öğesi.|

### <a name="parent-elements"></a>Üst öğeler

|Öğe|Açıklama|
|-------------|-----------------|
|[TemplateContent](../extensibility/templatecontent-element-visual-studio-templates.md)|Şablonu içeriğini belirtir.|

## <a name="remarks"></a>Açıklamalar
 `References` bir isteğe bağlı bir alt öğesidir `TemplateContent`.

 `Reference` Ve `References` öğeleri yalnızca kullanılabilir *.vstemplate* sahip dosyalar bir `Type` öznitelik değerini `Item`.

## <a name="example"></a>Örnek
 Aşağıdaki örnekte gösterilmiştir `TemplateContent` öğe şablonu öğesidir. Bu XML başvuruları ekler *System.dll* ve *System.Data.dll* derlemeler.

```xml
<TemplateContent>
    <References>
        <Reference>
            <Assembly>
                System, Version=2.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089
            </Assembly>
        </Reference>
        <Reference>
            <Assembly>
                System.Data, Version=2.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089
            </Assembly>
        </Reference>
    </References>
    ...
</TemplateContent>
```

## <a name="see-also"></a>Ayrıca bkz.
- [Visual Studio Şablon Şeması Başvurusu](../extensibility/visual-studio-template-schema-reference.md)
- [Proje ve öğe şablonları oluşturma](../ide/creating-project-and-item-templates.md)
