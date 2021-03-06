---
title: Metin şablonu denetim blokları | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-modeling
ms.topic: conceptual
helpviewer_keywords:
- text templates, template code
ms.assetid: bad198b9-57a4-4777-bd5b-ab6336c825f3
caps.latest.revision: 34
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 2e2b21f69d0688f3554aec8cf751cf674c2b5e30
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63411469"
---
# <a name="text-template-control-blocks"></a>Metin Şablonu Denetim Blokları
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Denetim blokları çıktıyı değiştirmek için metin şablonunuza kod yazmanıza olanak sağlar. Denetim blokları, bunların açma köşeli parantez ayırt üç tür vardır:  
  
- `<# Standard control blocks #>` deyim içerebilir.  
  
- `<#= Expression control blocks #>` ifadeleri içerebilir.  
  
- `<#+ Class feature control blocks #>` yöntemler, alanlar ve özellikler içerebilir.  
  
## <a name="standard-control-block"></a>Standart denetim bloğu  
 Standart denetim blokları ifadeleri içerir. Örneğin, aşağıdaki standart bloğu tüm özniteliklerin adlarıyla XML belgesinde alır:  
  
```  
<#@ assembly name="System.Xml.dll" #>  
<#@ import namespace="System.Xml" #>  
  
<#  
    List<string> allAttributes = new List<string>();  
    XmlDocument xDoc = new XmlDocument();  
    xDoc.Load(@"E:\CSharp\Overview.xml");  
    XmlAttributeCollection attributes = xDoc.Attributes;  
    if (attributes.Count > 0)  
    {  
       foreach (XmlAttribute attr in attributes)  
       {  
           allAtributes.Add(attr.Name);  
       }  
     }    
#>  
```  
  
 Bileşik deyim içinde düz metin gibi ekleme `if` veya `for`. Örneğin, bu parça her döngü yinelemesinin bir çıkış satırı oluşturur:  
  
```  
<#  
       foreach (XmlAttribute attr in attributes)  
       {  
#>  
Found another one!  
<#  
           allAtributes.Add(attr.Name);  
       }  
#>  
```  
  
> [!WARNING]
> Her zaman {...}'ni kullanın Katıştırılmış düz metin içeren iç içe geçmiş deyimler sınırlandırmak için. Aşağıdaki örnek düzgün şekilde çalışmayabilir:  
>   
> `<# if (ShouldPrint) #> Some text. -- WRONG`  
>   
> Bunun yerine {küme ayraçları}, şu şekilde içermelidir:  
  
```  
  
<#  
 if (ShouldPrint)  
 {   //  "{" REQUIRED  
#>  
Some text.  
<#  
 }   
#>  
  
```  
  
## <a name="expression-control-block"></a>İfade denetim bloğu  
 İfade denetim blokları, çıktı dosyasına yazılması dizeleri sağlayan kod için kullanılır. Örneğin, yukarıdaki örnek ile kod bloğunu aşağıdaki şekilde değiştirerek öznitelikleri çıkış dosyasının adını yazdırabilir:  
  
```  
<#  
    XmlDocument xDoc = new XmlDocument();  
    xDoc.Load(@"E:\CSharp\Overview.xml");  
    XmlAttributeCollection attributes = xDoc.Attributes;  
    if (attributes != null)  
    {  
       foreach (XmlAttribute attr in attributes)  
       {   
#><#= attr.Name #><#  
       }  
    }  
#>  
```  
  
## <a name="class-feature-control-block"></a>Sınıf özelliği denetim bloğu  
 Sınıf özelliği denetim blokları, yöntemler, özellikler, alanlar veya bile iç içe geçmiş sınıflar, metin şablonunuza eklemek için kullanabilirsiniz. Sınıf özelliği bloklarını en yaygın kullanımı, diğer bölümlerinde metin şablonunun kod için yardımcı işlevleri sağlamaktır. Örneğin, aşağıdaki sınıf özelliği bloğu özniteliği adının ilk harfi büyük harfe dönüştürür (veya adı boşluk içeriyorsa, her sözcüğün ilk harfini büyük harfe):  
  
```  
<#@ import namespace="System.Globalization" #>  
```  
  
```  
<#+  
    private string FixAttributeName(string name)  
    {  
        return CultureInfo.CurrentCulture.TextInfo.ToTitleCase(name);  
    }  
#>  
```  
  
> [!NOTE]
> Bir sınıf özelliği denetim bloğu, standart denetim blokları aynı şablon dosyasında tarafından izlenmemelidir. Ancak, bu kısıtlama kullanarak sonucu için geçerli değildir `<#@include#>` yönergeleri. Eklenen her dosya, sınıf özelliği bloklarını tarafından izlenen standart blokları olabilir.  
  
 Bir sınıf özelliği denetim bloğu metin ve ifade bloklarında ekleyerek çıkış oluşturan bir işlev oluşturabilirsiniz. Örneğin:  
  
```  
<#+  
    private void OutputFixedAttributeName(string name)  
    {  
#>  
 Attribute:  <#= CultureInfo.CurrentCulture.TextInfo.ToTitleCase(name) #>  
<#+  // <<< Notice that this is also a class feature block.  
    }  
#>  
```  
  
 Bu işlev, standart bir blok veya başka bir sınıf özelliği bloğu çağırabilirsiniz:  
  
```  
<# foreach (Attribute attribute in item.Attributes)  
{  
  OutputFixedAttributeName(attribute.Name);  
}  
#>  
```  
  
## <a name="how-to-use-control-blocks"></a>Denetim blokları kullanma  
 Tüm standart ve ifade denetim blokları (kod dahil şablonlarında dahil) tek bir şablonda forma birlikte tüm kodu `TransformText()` yöntemi oluşturulan kod. (Diğer metin şablonları ile ekleme hakkında daha fazla bilgi için `include` yönergesine bakın [T4 metin şablonu yönergeleri](../modeling/t4-text-template-directives.md).)  
  
 Denetim blokları kullandığınızda aşağıdaki maddeler akılda tutulması:  
  
- **Dili.** C# veya Visual Basic kodu bir metin şablonunda kullanabilirsiniz. Varsayılan dil C# olmakla birlikte, Visual Basic ile belirttiğiniz `language` parametresinin `template` yönergesi. (Hakkında daha fazla bilgi için `template` yönergesine bakın [T4 metin şablonu yönergeleri](../modeling/t4-text-template-directives.md).)  
  
     Denetim blokları kullandığınız dil dil veya bir metin şablonunda oluşturmak metin biçimi ile yapmak için hiçbir şey vardır. C# Visual Basic kod veya bunun tersini de kullanarak oluşturabilirsiniz.  
  
     Dahil olan tüm metin şablonları dahil olmak üzere belirli bir metin şablonunda, yalnızca bir dil kullanabilirsiniz `include` yönergesi.  
  
- **Yerel değişkenler.** Standart ve ifade denetimindeki tüm kod engeller bu yana bir metin şablonu tek bir yöntem oluşturulur ve olduğundan yerel değişkenlerin adlarını ile çakışma olmadığından emin olmanız gerekir. Diğer metin şablonları dahil olmak üzere, tüm dahil şablonlarıyla değişken adlarının benzersiz olduğundan emin olmanız gerekir. Bu emin olmanın bir yolu, bir dize içinde bildirilen metin şablonunu tanımlayan her yerel değişkenin adı eklemektir.  
  
     Özellikle birden çok metin şablonları eklerken, bunları bildirdiğinizde, yerel değişkenleri mantıklı değerlere başlatmak için de iyi bir fikirdir.  
  
- **Denetim blokları iç içe geçmiş.** Denetim blokları diğer içinde bulunmayabilir. Başka bir açmadan önce her zaman belirli bir denetim bloğu sonlandırmanız gerekir. Örneğin, aşağıdaki standart denetim bloğu bir parçası olarak bir ifade bloğu metne nasıl gösterir.  
  
    ```  
    <#   
    int x = 10;  
    while (x-- > 0)  
    {  
    #>  
    <#= x #>  
    <# } #>  
    ```  
  
- **Yeniden düzenleme.** Metin şablonlarınızı kısa ve kolay anlaşılır tutulabilmesi için sınıf özelliği bloklarını yardımcı işlevler halinde yeniden kullanılabilir kod hesaba katarak veya devralınan kendi metin Şablon sınıfı oluşturarak yinelenen kodlardan kaçının önerilir Microsoft.VisualStudio.texttemplating.texttransformation ile sınıftan.
