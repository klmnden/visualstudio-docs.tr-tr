---
title: T4 Derleme yönergesi | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-modeling
ms.topic: conceptual
ms.assetid: 44949749-ce3c-4fb5-8690-a17f1564ac2f
caps.latest.revision: 6
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: f81bdcad4f255585c2c554add59ed04dea5872d3
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54792913"
---
# <a name="t4-assembly-directive"></a>T4 Derleme Yönergesi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

İçinde bir [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] tasarım zamanı metin şablonu `assembly` yönergesi bir derleme yükler, böylece şablon kodunuz türlerini kullanabilir. Etkin bir derleme başvurusu eklemeye benzer bir [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] proje.  
  
 Metin şablonlarını yazmayla ilgili genel bilgiler için bkz: [T4 metin şablonu yazma](../modeling/writing-a-t4-text-template.md).  
  
> [!NOTE]
>  Gereksinim duymadığınız `assembly` çalışma zamanı (önceden işlenmiş) metin şablonunda yönergesi. Bunun yerine gerekli derlemeleri ekleyin **başvuruları** , uygulamanızın [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] proje.  
  
## <a name="using-the-assembly-directive"></a>Derleme Yönergesini Kullanma  
 Yönergenin sözdizimi aşağıdaki gibidir:  
  
```  
<#@ assembly name="[assembly strong name|assembly file name]" #>  
```  
  
 Derleme adı aşağıdakilerden biri olmalıdır:  
  
- Bir derlemenin GAC'deki tanımlayıcı adı gibi `System.Xml.dll`. Uzun biçimi gibi kullanabilir `name="System.Xml, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089"`. Daha fazla bilgi için bkz. <xref:System.Reflection.AssemblyName>.  
  
- Derlemenin mutlak yolu  
  
  Kullanabileceğiniz `$(variableName)` başvurmak için [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] gibi değişkenleri `$(SolutionDir)`, ve `%VariableName%` ortam değişkenlerine başvurmak için. Örneğin:  
  
```  
<#@ assembly name="$(SolutionDir)\MyProject\bin\Debug\SomeLibrary.Dll" #>  
```  
  
 Derleme yönergesinin önceden işlenmiş metin şablonu üzerinde etkisi yoktur. Bunun yerine gerekli dosyaları içeren **başvuruları** bölümünü, [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] proje. Daha fazla bilgi için [T4 metin şablonları ile çalışma süresi metni oluşturma](../modeling/run-time-text-generation-with-t4-text-templates.md).  
  
## <a name="standard-assemblies"></a>Standart Derlemeler  
 Aşağıdaki derlemeler otomatik olarak yüklenir, böylece onlar için derleme yönergelerini yazmanıza gerek yoktur:  
  
- `Microsoft.VisualStudio.TextTemplating.1*.dll`  
  
- `System.dll`  
  
- `WindowsBase.dll`  
  
  Özel bir yönerge kullanırsanız, yönerge işlemcisi ek derlemeler yükleyebilir. Örneğin, etki alanına özgü dil (DSL) için şablonlar yazarsanız, aşağıdaki derlemeler için derleme yönergeleri yazmak gerekmez:  
  
- `Microsoft.VisualStudio.Modeling.Sdk.1*.dll`  
  
- `Microsoft.VisualStudio.Modeling.Sdk.Diagrams.1*.dsl`  
  
- `Microsoft.VisualStudio.TextTemplating.Modeling.1*.dll`  
  
- DSL'nizi içeren derleme.  
  
##  <a name="msbuild"></a> Hem MSBuild hem Visual Studio'da proje özelliklerini kullanma  
 $(SolutionDir) gibi Visual Studio makroları MSBuild içinde çalışmaz. Şablonları yapı makinenizde dönüştürmek isterseniz, bunun yerine proje özelliklerini kullanmanız gerekir.  
  
 Proje özelliği tanımlamak için .csproj veya .vbproj dosyanızı düzenleyin. Bu örnek adlı bir özellik tanımlar `myLibFolder`:  
  
```xml  
<!-- Define a project property, myLibFolder: -->  
<PropertyGroup>  
    <myLibFolder>$(MSBuildProjectDirectory)\..\libs</myLibFolder>  
</PropertyGroup>  
  
<!-- Tell the MSBuild T4 task to make the property available: -->  
<ItemGroup>  
    <T4ParameterValues Include="myLibFolder">  
      <Value>$(myLibFolder)</Value>  
    </T4ParameterValues>  
  </ItemGroup>  
  
```  
  
 Artık proje özelliğinizi metin şablonlarında kullanabilirsiniz, böylece hem Visual Studio hem de MSBuild içinde doğru dönüştürme yapılır:  
  
```  
<#@ assembly name="$(myLibFolder)\MyLib.dll" #>  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [T4 Include Yönergesi](../modeling/t4-include-directive.md)
