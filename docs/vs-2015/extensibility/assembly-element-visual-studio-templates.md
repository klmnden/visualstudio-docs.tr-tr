---
title: Assembly öğesi (Visual Studio şablonları) | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/vstemplate/2005#Assembly
helpviewer_keywords:
- Assembly element [Visual Studio templates]
- <Assembly> element [Visual Studio templates]
ms.assetid: 9242f76a-1273-4b8a-8f26-6606f91829ef
caps.latest.revision: 11
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 10c894f3507ae760624b6ae18f785aae6016cd5e
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68184700"
---
# <a name="assembly-element-visual-studio-templates"></a>Assembly Öğesi (Visual Studio Şablonları)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Projelere derlemeye bir başvuru eklemek için şablonu kullanan bir derlemeyle ilgili bilgileri belirtir.  
  
 \<VSTemplate >  
 \<TemplateContent >  
 \<Başvuru >  
 \<Başvuru >  
 \<Derleme >  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
<Assembly> AssemblyName </Assembly>  
```  
  
## <a name="attributes-and-elements"></a>Öznitelikler ve Öğeler  
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.  
  
### <a name="attributes"></a>Öznitelikler  
 Yok.  
  
### <a name="child-elements"></a>Alt Öğeler  
 Yok.  
  
### <a name="parent-elements"></a>Üst Öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[Başvuru](../extensibility/reference-element-visual-studio-templates.md)|Öğe bir projeye eklendiğinde eklemek için derleme başvurusu belirtir.|  
  
## <a name="text-value"></a>Metin Değeri  
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
  
 `Reference`, `References,` Ve `Assembly` öğeleri olan .vstemplate dosyaları yalnızca kullanılabilir bir `Type` öznitelik değerini `Item`.  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnekte gösterilmiştir `TemplateContent` öğe şablonu öğesidir. Bu XML System.dll ve System.Data.dll derlemelerine başvurular ekler.  
  
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
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Visual Studio Şablon Şeması Başvurusu](../extensibility/visual-studio-template-schema-reference.md)   
 [Proje ve Öğe Şablonları Oluşturma](../ide/creating-project-and-item-templates.md)
