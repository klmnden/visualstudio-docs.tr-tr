---
title: Öğe Seç (MSBuild) | Microsoft Docs
ms.date: 03/13/2017
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/msbuild/2003#Choose
dev_langs:
- VB
- CSharp
- C++
- jsharp
- xml
helpviewer_keywords:
- <Choose> Element [MSBuild]
- Choose Element [MSBuild]
ms.assetid: 7b8b025a-d944-4f5c-9018-c89fc2ef146d
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 316343e355f9cf3070f04660d89f9fbfd15484d1
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56609120"
---
# <a name="choose-element-msbuild"></a>Öğe Seç (MSBuild)
Bir grubu seçmek için alt öğeleri değerlendirir `ItemGroup` öğelerin ve/veya `PropertyGroup` değerlendirmek için öğeleri.

 \<Proje > \<seçin > \<olduğunda > \<seçin >... \<Aksi takdirde > \<seçin >...

## <a name="syntax"></a>Sözdizimi

```xml
<Choose>
    <When Condition="'StringA'=='StringB'">... </When>
    <Otherwise>... </Otherwise>
</Choose>
```

## <a name="attributes-and-elements"></a>Öznitelikler ve öğeler
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.

### <a name="attributes"></a>Öznitelikler
 Yok.

### <a name="child-elements"></a>Alt öğeleri

|Öğe|Açıklama|
|-------------|-----------------|
|[Aksi takdirde](../msbuild/otherwise-element-msbuild.md)|İsteğe bağlı öğe.<br /><br /> Kod bloğunun belirtir `PropertyGroup` ve `ItemGroup` değerlendirme öğeleri tüm koşullar `When` öğeleri değerlendirmek için `false`. Sıfır veya bir olabilir `Otherwise` öğelerinde bir `Choose` öğesi ve son öğesi olmalı.|
|[Ne zaman](../msbuild/when-element-msbuild.md)|Gerekli öğe.<br /><br /> Olası bir blok için kod belirtir `Choose` seçmek için öğesi. Bir veya daha fazla olabilir `When` öğelerinde bir `Choose` öğesi.|

### <a name="parent-elements"></a>Üst öğeler

| Öğe | Açıklama |
| - | - |
| [Aksi takdirde](../msbuild/otherwise-element-msbuild.md) | Belirtir, yürütülecek kod bloğu tüm koşullar `When` öğeleri değerlendirmek için `false`. |
| [Project](../msbuild/project-element-msbuild.md) | Gerekli kök öğesi bir [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] proje dosyası. |
| [Ne zaman](../msbuild/when-element-msbuild.md) | Olası bir blok için kod belirtir `Choose` seçmek için öğesi. |

## <a name="remarks"></a>Açıklamalar
 `Choose`, `When`, Ve `Otherwise` öğeleri birlikte bir dizi olası alternatifler dışında yürütülecek kodun bir bölümünü seçmek için bir yol sağlamak amacıyla kullanılır. Daha fazla bilgi için [koşullu yapılar](../msbuild/msbuild-conditional-constructs.md).

## <a name="example"></a>Örnek
 Aşağıdaki proje kullandığı `Choose` hangi özellik değerlerinde kümesini seçmek için öğe `When` ayarlamak için öğeleri. Varsa `Condition` her iki öznitelikleri `When` öğeleri değerlendirmek için `false`, özellik değerleri `Otherwise` öğesi ayarlanır.

```xml
<Project
    xmlns="http://schemas.microsoft.com/developer/msbuild/2003" >
    <PropertyGroup>
        <Configuration Condition="'$(Configuration)' == ''">Debug</Configuration>
        <OutputType>Exe</OutputType>
        <RootNamespace>ConsoleApplication1</RootNamespace>
        <AssemblyName>ConsoleApplication1</AssemblyName>
        <WarningLevel>4</WarningLevel>
    </PropertyGroup>
    <Choose>
        <When Condition=" '$(Configuration)'=='debug' ">
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
        <Otherwise>
            <PropertyGroup>
                <DebugSymbols>true</DebugSymbols>
                <Optimize>false</Optimize>
                <OutputPath>.\bin\$(Configuration)\</OutputPath>
                <DefineConstants>DEBUG;TRACE</DefineConstants>
            </PropertyGroup>
        </Otherwise>
    </Choose>
    <Import Project="$(MSBuildBinPath)\Microsoft.CSharp.targets" />
</Project>
```

## <a name="see-also"></a>Ayrıca bkz.
- [Koşullu yapılar](../msbuild/msbuild-conditional-constructs.md)
- [Proje dosyası şema başvurusu](../msbuild/msbuild-project-file-schema-reference.md)
