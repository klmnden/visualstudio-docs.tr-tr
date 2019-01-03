---
title: Itemmetadata öğesi (MSBuild) | Microsoft Docs
ms.date: 03/13/2017
ms.topic: reference
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- ItemMetadata Element [MSBuild]
- <ItemMetadata> Element [MSBuild]
ms.assetid: e3db5122-202d-43a9-b2f4-3e0ec4ed3d08
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 64786e5066476fcaca161fe0511f97a1fd2c7fd6
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53917533"
---
# <a name="itemmetadata-element-msbuild"></a>Itemmetadata öğesi (MSBuild)
Öğe meta veri değeri içeren bir kullanıcı tarafından tanımlanan öğe meta verileri anahtar içerir. Bir öğe meta verileri anahtar-değer çiftleri herhangi bir sayı olabilir.  

 \<Proje >  
 \<ItemGroup >  
 \<Öğesi >  

## <a name="syntax"></a>Sözdizimi  

```xml  
<ItemMetadataName> Item Metadata value</ItemMetadataName>  
```  

## <a name="attributes-and-elements"></a>Öznitelikler ve öğeler  
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.  

### <a name="attributes"></a>Öznitelikler  

|Öznitelik|Açıklama|  
|---------------|-----------------|  
|`Condition`|İsteğe bağlı öznitelik.<br /><br /> Değerlendirilecek koşul. Daha fazla bilgi için [koşullar](../msbuild/msbuild-conditions.md).|  

### <a name="child-elements"></a>Alt öğeleri  
 Yok.  

### <a name="parent-elements"></a>Üst öğeler  

|Öğe|Açıklama|  
|-------------|-----------------|  
|[Öğesi](../msbuild/item-element-msbuild.md)|Yapı işlemi için girişler tanımlayan bir kullanıcı tarafından tanımlanan öğe.|  

## <a name="text-value"></a>Metin değeri  
 Metin değeri isteğe bağlıdır.  

 Bu metin, metin veya XML olabilir öğesi meta veri değeri belirtir.  

## <a name="example"></a>Örnek  
 Aşağıdaki kod örneğinde nasıl ekleneceğini gösterir `Culture` meta veri değerine sahip `fr` öğesine `CSFile`.  

```xml  
<ItemGroup>  
    <CSFile Include="main.cs" >  
        <Culture>fr</Culture>  
    </CSFile>  
</ItemGroup>  
```  

## <a name="see-also"></a>Ayrıca bkz.  
 [Proje dosyası şema başvurusu](../msbuild/msbuild-project-file-schema-reference.md)   
 [Öğeler](../msbuild/msbuild-items.md)
