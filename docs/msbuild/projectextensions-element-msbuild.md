---
title: ProjectExtensions öğesi (MSBuild) | Microsoft Docs
ms.date: 03/13/2017
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/msbuild/2003#ProjectExtensions
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- <ProjectExtensions> element [MSBuild]
- ProjectExtensions element [MSBuild]
ms.assetid: f95f312f-ff92-41eb-9469-ad99e236a307
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: c600d7756c83fb55a63a91e81b3d826aa9f3d747
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54996759"
---
# <a name="projectextensions-element-msbuild"></a>ProjectExtensions öğesi (MSBuild)
Sağlar [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] proje dosyalarını içerecek olmayan[!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] bilgileri. Herhangi bir şey içinde bir `ProjectExtensions` öğesi tarafından yoksayılacak [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)].  

 \<Proje >  
 \<ProjectExtensions >  

## <a name="syntax"></a>Sözdizimi  

```xml  
<ProjectExtensions>  
    Non-MSBuild information to include in file.  
</ProjectExtensions>  
```  

## <a name="attributes-and-elements"></a>Öznitelikler ve öğeler  
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.  

### <a name="attributes"></a>Öznitelikler  
 Hiçbiri  

### <a name="child-elements"></a>Alt öğeleri  
 Hiçbiri  

### <a name="parent-elements"></a>Üst öğeler  

| Öğe | Açıklama |
| - | - |
| [Project](../msbuild/project-element-msbuild.md) | Gerekli kök öğesi bir [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] proje dosyası. |

## <a name="remarks"></a>Açıklamalar  
 Yalnızca bir `ProjectExtensions` öğesi olarak kullanılabilir bir [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] proje.  

## <a name="example"></a>Örnek  
 Aşağıdaki kod örneği bilgileri depolanıyor tümleşik geliştirme ortamından gösterir bir `ProjectExtensions` öğesi.  

```xml  
<ProjectExtensions>  
    <VSIDE>  
        <External>  
            <!--  
            Raw XML passed to the IDE by an external source  
            -->  
        </External>  
    </VSIDE>  
</ProjectExtensions>  
```  

## <a name="see-also"></a>Ayrıca bkz.  
 [Proje dosyası şema başvurusu](../msbuild/msbuild-project-file-schema-reference.md)  
 [MSBuild](../msbuild/msbuild.md)
