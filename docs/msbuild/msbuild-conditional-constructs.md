---
title: MSBuild koşullu yapıları | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- <Choose> Element [MSBuild]
- Choose Element [MSBuild]
- conditional constructs [MSBuild]
- MSBuild, conditional constructs
- <When> Element [MSBuild]
- <Otherwise> Element [MSBuild]
- Otherwise Element [MSBuild]
- When Element [MSBuild]
ms.assetid: dd54258e-f4fb-448f-9da4-d1817e0cbaf2
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: ca2e1c99a8897dc80b30d8e91e48554ddce7451b
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53985913"
---
# <a name="msbuild-conditional-constructs"></a>MSBuild koşullu yapıları
[!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] için bir mekanizma sağlar / veya işlem ile [Seç](../msbuild/choose-element-msbuild.md), [olduğunda](../msbuild/when-element-msbuild.md), ve [Aksi takdirde](../msbuild/otherwise-element-msbuild.md) öğeleri.  
  
## <a name="use-the-choose-element"></a>Seç öğesi kullanma  
 `Choose` Öğesi içeren bir dizi `When` öğelerle `Condition` bir sonucunu verene kadar yukarıdan aşağıya sırasında test öznitelikleri `true`. Birden fazla ise `When` öğesi değerlendirilen `true`, yalnızca ilki kullanılır. Bir `Otherwise` öğesi, varsa değerlendirilir herhangi bir koşul, bir `When` öğesi değerlendirilen `true`.  
  
 `Choose` öğeleri alt öğeleri olarak kullanılabilir `Project`, `When` ve `Otherwise` öğeleri. `When` ve `Otherwise` öğeleri olabilir `ItemGroup`, `PropertyGroup`, veya `Choose` alt öğeleri.  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnekte `Choose` ve `When` öğeleri ya da / veya işleme. Projesi için öğeler ve özellikler bağlı olarak değeri ayarlanır `Configuration` özelliği.  
  
```xml  
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003" >  
    <PropertyGroup>  
        <Configuration Condition=" '$(Configuration)' == '' ">Debug</Configuration>  
        <OutputType>Exe</OutputType>  
        <RootNamespace>ConsoleApplication1</RootNamespace>  
        <AssemblyName>ConsoleApplication1</AssemblyName>  
        <WarningLevel>4</WarningLevel>  
    </PropertyGroup>  
    <Choose>  
        <When Condition=" '$(Configuration)'=='Debug' ">  
            <PropertyGroup>  
                <DebugSymbols>true</DebugSymbols>  
                <DebugType>full</DebugType>  
                <Optimize>false</Optimize>  
                <OutputPath>.\bin\Debug\</OutputPath>  
                <DefineConstants>DEBUG;TRACE</DefineConstants>  
            </PropertyGroup>  
            <ItemGroup>  
                <Compile Include="UnitTesting\*.cs" />  
                <Reference Include="NUnit.dll" />  
            </ItemGroup>  
        </When>  
        <When Condition=" '$(Configuration)'=='retail' ">  
            <PropertyGroup>  
                <DebugSymbols>false</DebugSymbols>  
                <Optimize>true</Optimize>  
                <OutputPath>.\bin\Release\</OutputPath>  
                <DefineConstants>TRACE</DefineConstants>  
            </PropertyGroup>  
        </When>  
    </Choose>  
    <!-- Rest of Project -->  
</Project>  
```  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Öğe Seç (MSBuild)](../msbuild/choose-element-msbuild.md)   
 [Zaman öğesi (MSBuild)](../msbuild/when-element-msbuild.md)   
 [Otherwise öğesi (MSBuild)](../msbuild/otherwise-element-msbuild.md)   
 [MSBuild başvurusu](../msbuild/msbuild-reference.md)