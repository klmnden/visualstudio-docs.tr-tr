---
title: Assembly öğesi (Visual Studio şablonları) | Microsoft Docs
ms.date: 11/04/2016
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/vstemplate/2005#Assembly
helpviewer_keywords:
- Assembly element [Visual Studio templates]
- <Assembly> element [Visual Studio templates]
ms.assetid: 9242f76a-1273-4b8a-8f26-6606f91829ef
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 13c52b7f913e35ace3e0fd41227e27b6c00e90e2
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66352190"
---
# <a name="assembly-element-visual-studio-templates"></a>Assembly öğesi (Visual Studio şablonları)
Projelere derlemeye bir başvuru eklemek için şablonu kullanan bir derlemeyle ilgili bilgileri belirtir.

 \<VSTemplate > \<TemplateContent > \<başvuruları > \<başvuru > \<derleme >

## <a name="syntax"></a>Sözdizimi

```
<Assembly> AssemblyName </Assembly>
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
|[Başvuru](../extensibility/reference-element-visual-studio-templates.md)|Öğe bir projeye eklendiğinde eklemek için derleme başvurusu belirtir.|

## <a name="text-value"></a>Metin değeri
 Bir metin değeri gereklidir.

 Bu metin, öğe şablonu örneği oluşturulduğunda bir projeye Eklenecek derlemeyi belirtir. Bu derleme adı aşağıdaki yollardan birinde belirtilmelidir:

- Tam derleme adı. Örneğin:

    ```
    <Assembly>
        MyAssembly, Version=1.0.3300.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a, Custom = null.
    </Assembly>
    ```

- Basit metin başvuru olarak. Örneğin:

    ```
    <Assembly> System </Assembly>
    ```

## <a name="remarks"></a>Açıklamalar
 `Assembly` gerekli alt öğesi olan `Reference`.

 `Reference`, `References,` Ve `Assembly` öğeleri yalnızca kullanılabilir *.vstemplate* sahip dosyalar bir `Type` öznitelik değerini `Item`.

## <a name="example"></a>Örnek
 Aşağıdaki örnekte gösterilmiştir `TemplateContent` öğe şablonu öğesidir. Bu XML başvuruları ekler *System.dll* ve *System.Data.dll* derlemeler.

```
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