---
title: ProjectExtensions öğesi (MSBuild) | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: msbuild
ms.topic: conceptual
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
caps.latest.revision: 21
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 2a8241033be738e7f608f3a83531d6fde52e9361
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54801556"
---
# <a name="projectextensions-element-msbuild"></a>ProjectExtensions Öğesi (MSBuild)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
Sağlar [!INCLUDE[vstecmsbuild](../includes/vstecmsbuild-md.md)] proje dosyalarını içerecek olmayan[!INCLUDE[vstecmsbuild](../includes/vstecmsbuild-md.md)] bilgileri. Herhangi bir şey içinde bir `ProjectExtensions` öğesi tarafından yoksayılacak [!INCLUDE[vstecmsbuild](../includes/vstecmsbuild-md.md)].  
  
 \<Proje >  
 \<ProjectExtensions >  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
<ProjectExtensions>  
    Non-MSBuild information to include in file.  
</ProjectExtensions>  
```  
  
## <a name="attributes-and-elements"></a>Öznitelikler ve Öğeler  
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.  
  
### <a name="attributes"></a>Öznitelikler  
 Hiçbiri  
  
### <a name="child-elements"></a>Alt Öğeler  
 Hiçbiri  
  
### <a name="parent-elements"></a>Üst Öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[Project](../msbuild/project-element-msbuild.md)|Gerekli kök öğesi bir [!INCLUDE[vstecmsbuild](../includes/vstecmsbuild-md.md)] proje dosyası.|  
  
## <a name="remarks"></a>Açıklamalar  
 Yalnızca bir `ProjectExtensions` öğesi olarak kullanılabilir bir [!INCLUDE[vstecmsbuild](../includes/vstecmsbuild-md.md)] proje.  
  
## <a name="example"></a>Örnek  
 Aşağıdaki kod örneği bilgileri depolanıyor tümleşik geliştirme ortamından gösterir bir `ProjectExtensions` öğesi.  
  
```  
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
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Proje Dosyası Şema Başvurusu](../msbuild/msbuild-project-file-schema-reference.md)  
 [MSBuild](msbuild.md)
