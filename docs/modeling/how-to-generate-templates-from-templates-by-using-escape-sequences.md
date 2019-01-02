---
title: 'Nasıl Yapılır: Çıkış Sıraları Kullanarak Şablonlardan Şablon Oluşturma'
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- text templates, generating templates from templates
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.prod: visual-studio-dev15
ms.openlocfilehash: 8aa0d2203db6080260bc702429758fbd7f6b1a4a
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53938153"
---
# <a name="how-to-generate-templates-from-templates-by-using-escape-sequences"></a>Nasıl Yapılır: Çıkış Sıraları Kullanarak Şablonlardan Şablon Oluşturma
Oluşturulan metin çıktısı olarak başka bir metin şablonu oluşturan bir metin şablonu oluşturabilirsiniz. Bunu yapmak için metin şablon etiketleri ayırmak için kaçış dizileri kullanmanız gerekir. Kaçış dizileri kullanmayın, oluşturulan metin şablonunuzu önceden tanımlanmış bir anlamı olur. Metin şablonlarında çıkış sıraları kullanma hakkında daha fazla bilgi için bkz. [metin şablonlarında çıkış sıraları kullanarak](../modeling/using-escape-sequences-in-text-templates.md).

### <a name="to-generate-a-text-template-from-within-a-text-template"></a>Metin şablonu içindeki bir metin şablonu oluşturmak için

-   Ters eğik çizgi kullanın (\\) metin şablonu yönergeleri deyimleri, ifadelerin içinde gerekli işaretleme etiketleri oluşturmak ve Özellikler ayrı metin şablon dosyasına sınıf için bir kaçış karakteri olarak.

    ```
    \<#@ directive \#>
    \<# statement \#>
    \<#= expression \#>
    \<#+ classfeature \#>
    ```

## <a name="example"></a>Örnek
 Aşağıdaki örnek, bir metin şablonundan metin şablonu oluşturmak için kaçış karakterlerini kullanır. `output` Yönergesi, hedef dosya türü metin şablon dosyası türü (.tt) ayarlar.

```csharp
\<#@ output extension=".tt" \#>
\<#@ assembly name="System.Xml.dll" \#>
\<#@ import namespace="System.Xml" \#>
\<#
XmlDocument xDoc = new XmlDocument();
//System.Diagnostics.Debugger.Break();
    xDoc.Load(@"E:\CSharp\Overview.xml");
    XmlAttributeCollection attributes = xDoc.Attributes;
    if (attributes != null)
    {
       foreach (XmlAttribute attr in attributes)
       {\#>
           \<#= attr.Name \#>
       \<#}
     }
\#>
```

 Oluşturulan metin çıktısı bir metin şablonu budur.

```
<#@ output extension=".tt" #>
<#@ assembly name="System.Xml.dll" #>
<#@ import namespace="System.Xml" #>
<#
XmlDocument xDoc = new XmlDocument();
//System.Diagnostics.Debugger.Break();
    xDoc.Load(@"E:\CSharp\Overview.xml");
    XmlAttributeCollection attributes = xDoc.Attributes;
    if (attributes != null)
    {
       foreach (XmlAttribute attr in attributes)
       {#>
           <#= attr.Name #>
       <#}
     }
#>
```