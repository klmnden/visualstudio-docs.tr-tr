---
title: Özellik öğesi (MSBuild) | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: msbuild
ms.topic: conceptual
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- <Property> Element [MSBuild]
- Property Element [MSBuild]
ms.assetid: 69ab08ab-3e76-41dd-a01b-49aa1d2e0cac
caps.latest.revision: 20
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 958692d9227017eba0901ddb48a19502af9ec452
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54769209"
---
# <a name="property-element-msbuild"></a>Özellik Öğesi (MSBuild)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
Bir kullanıcı tanımlı özellik adını ve değerini içerir. Kullanılan her bir özellik bir [!INCLUDE[vstecmsbuild](../includes/vstecmsbuild-md.md)] alt öğesi olarak proje belirtilen bir `PropertyGroup` öğesi.  
  
 \<Proje >  
 \<PropertyGroup >  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
<Property Condition="'String A' == 'String B'">  
    Property Value  
</Property>  
```  
  
## <a name="attributes-and-elements"></a>Öznitelikler ve Öğeler  
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.  
  
### <a name="attributes"></a>Öznitelikler  
  
|Öznitelik|Açıklama|  
|---------------|-----------------|  
|`Condition`|İsteğe bağlı öznitelik.<br /><br /> Değerlendirilecek koşul. Daha fazla bilgi için [koşullar](../msbuild/msbuild-conditions.md).|  
  
### <a name="child-elements"></a>Alt Öğeler  
 Yok.  
  
### <a name="parent-elements"></a>Üst Öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[PropertyGroup](../msbuild/propertygroup-element-msbuild.md)|Özellikler için gruplandırma öğesi.|  
  
## <a name="text-value"></a>Metin Değeri  
 Metin değeri isteğe bağlıdır.  
  
 Bu metin değerini belirtir ve XML içeriyor olabilir.  
  
## <a name="remarks"></a>Açıklamalar  
 Özellik adları yalnızca ASCII karakterleri sınırlıdır. Özellik değerlerini başvurulan projede arasında özellik adı girerek "`$(`"ve"`)`". Örneğin, `$(builddir)\classes` "build\classes", çözümlemek `builddir` özellik değeri olan `build`. Özellikler hakkında daha fazla bilgi için bkz. [MSBuild özellikleri](msbuild-properties1.md).  
  
## <a name="example"></a>Örnek  
 Aşağıdaki kod kümeleri `Optimization` özelliğini `false` ve `DefaultVersion` özelliğini `1.0` varsa `Version` özelliği boşsa.  
  
```  
<PropertyGroup>  
    <Optimization>false</Optimization>  
    <DefaultVersion Condition="'$(Version)' == ''" >1.0</DefaultVersion>  
</PropertyGroup>  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.
[MSBuild Özellikleri](msbuild-properties1.md)  
 [Proje Dosyası Şema Başvurusu](../msbuild/msbuild-project-file-schema-reference.md)
