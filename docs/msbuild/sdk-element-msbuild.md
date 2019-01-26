---
title: SDK'sı öğesi (MSBuild) | Microsoft Docs
ms.date: 01/25/2018
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/msbuild/2003#Project
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- Sdk element [MSBuild]
- <Sdk> element [MSBuild]
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 24392fe34069025209f0e2c02e1231d1cbbe3397
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54993280"
---
# <a name="sdk-element-msbuild"></a>SDK'sı öğesi (MSBuild)
Başvurular bir [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] SDK proje.  

 \<Proje >  
 \<Sdk>  


## <a name="syntax"></a>Sözdizimi  

```xml  
<Sdk Name="My.Custom.Sdk"
     Version="1.0.0" />  
```  

## <a name="attributes-and-elements"></a>Öznitelikler ve öğeler  
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.  

### <a name="attributes"></a>Öznitelikler  

|Öznitelik|Açıklama|  
|---------------|-----------------|  
|`Name`|Gerekli öznitelik.<br /><br /> SDK'sı projesinin adı.|  
|`Version`|İsteğe bağlı öznitelik.<br /><br /> ' % S'projesinin SDK sürümü|  

### <a name="child-elements"></a>Alt öğeleri  
 Yok.

### <a name="parent-elements"></a>Üst öğeler  

| Öğe | Açıklama |
| - | - |
| [Project](../msbuild/project-element-msbuild.md) | Gerekli kök öğesi bir [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] proje dosyası. |

## <a name="see-also"></a>Ayrıca bkz.  
 [Nasıl yapılır: Bir MSBuild proje SDK başvurusu](../msbuild/how-to-use-project-sdk.md)   
 [Proje dosyası şema başvurusu](../msbuild/msbuild-project-file-schema-reference.md)   
 [MSBuild](../msbuild/msbuild.md)
