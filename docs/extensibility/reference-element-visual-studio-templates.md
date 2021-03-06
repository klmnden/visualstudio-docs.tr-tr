---
title: Başvuru öğesi (Visual Studio şablonları) | Microsoft Docs
ms.date: 11/04/2016
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/vstemplate/2005#Reference
helpviewer_keywords:
- Reference element [Visual Studio templates]
- <Reference> element [Visual Studio templates]
ms.assetid: 852772ea-c324-42e9-8c8a-6d565414a109
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 46c9cbde1186a0dd764c3075ef1566eb1fd5ea07
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66334387"
---
# <a name="reference-element-visual-studio-templates"></a>Reference öğesi (Visual Studio şablonları)
Öğe bir projeye eklendiğinde eklemek için derleme başvurusu belirtir.

 \<VSTemplate > \<TemplateContent > \<başvuruları > \<başvuru >

## <a name="syntax"></a>Sözdizimi

```xml
<Reference>
    <Assembly> ... </Assembly>
</Reference>
```

## <a name="attributes-and-elements"></a>Öznitelikler ve öğeler
 Aşağıdaki bölümlerde öznitelik, alt öğeler ve üst öğeler açıklanmaktadır.

### <a name="attributes"></a>Öznitelikler
 Yok.

### <a name="child-elements"></a>Alt öğeleri

|Öğe|Açıklama|
|-------------|-----------------|
|[Assembly](../extensibility/assembly-element-visual-studio-templates.md)|Gerekli öğe.<br /><br /> Projelere derlemeye bir başvuru eklemek için şablonu kullanan bir derlemeyle ilgili bilgileri belirtir. Olmalıdır `Assembly` öğesinde her `Reference` öğesi.|

### <a name="parent-elements"></a>Üst öğeler

|Öğe|Açıklama|
|-------------|-----------------|
|[Başvurular](../extensibility/references-element-visual-studio-templates.md)|Gruplar için proje şablonu ekleyen derleme başvuruları.|

## <a name="remarks"></a>Açıklamalar
 `Reference` gerekli alt öğesi olan `References`.

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
