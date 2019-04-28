---
title: Paket Framework sınıfları yönetilen | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: devlang-csharp
ms.topic: conceptual
helpviewer_keywords:
- managed package framework, helper classes
- managed package helper classes
- Visual Studio SDK, managed package helper classes
- classes [Visual Studio SDK], managed package framework
ms.assetid: 15aedcc3-c79a-460b-b620-43223f1ae81e
caps.latest.revision: 24
manager: jillfra
ms.openlocfilehash: 75f7cb153a976614ff790095141a820af80b5834
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63422763"
---
# <a name="managed-package-framework-classes"></a>Yönetilen paket Framework sınıfları
Yönetilen paket framework (MPF) sınıfları, yönetilen kod kullanarak VSPackage'ları oluşturmak için kullanılabilir. Bunlar, birçok VSPackage arabirimleri için varsayılan uygulamalarını sağlar. Uygulama Ayrıntıları ve karmaşıklık gizleyerek MPF oluşturmanızı sağlayan [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] minimum miktarda kod ürünleriyle tümleştirme.  
  
> [!WARNING]
> Visual Studio SDK'sı ile yönetilen paket çerçevesini sınıflar içeren derlemeler çoğunu gönderilir. Yönetilen paketlenmiş Framework projesi için kaynak kodunu indirebilirsiniz [projeleri için yönetilen paket çerçevesini](http://mpfproj11.codeplex.com/).  
  
## <a name="mpf-namespaces"></a>MPF ad alanları  
 Tarafından sağlanan MPF ad alanları aşağıdaki tabloda [!INCLUDE[vsipsdk](../includes/vsipsdk-md.md)].  
  
|Ad alanı|İçindekiler|  
|----------------|--------------|  
|<xref:Microsoft.VisualStudio>|COM hata işleme yararlı sınıfları içeren [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] sabitleri ve Win32 windows.|  
|<xref:Microsoft.VisualStudio.Package>|Yönetilen kod için sarmalayıcıları içerir [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] projeler ve düzenleyiciler MSBuild.|  
|<xref:Microsoft.VisualStudio.Shell>|Birçok yaygın Visual Studio nesne uygulaması türetilen MPF temel sınıflar içerir.|  
|<xref:Microsoft.VisualStudio.Shell.Design>|İçeren [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] Tasarımcı uzantıları.|  
|<xref:Microsoft.VisualStudio.Shell.Design.Serialization>|İçeren [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] serileştirme Tasarımcı uzantıları.|  
|<xref:Microsoft.VisualStudio.Shell.Design.Serialization.CodeDom>|İçeren [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] CodeDom Tasarımcı uzantıları.|  
|<xref:Microsoft.VisualStudio.Shell.Flavor>|Destekler subtypes (diğer adıyla "Özellikleri") projesi.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [VSPackages ve yönetilen paket çerçevesini](../misc/vspackages-and-the-managed-package-framework.md)   
 [Visual Studio ile birlikte çalışma bütünleştirilmiş kodlarını kullanma](../extensibility/internals/using-visual-studio-interop-assemblies.md)   
 [VSPackages ve yönetilen paket çerçevesini](../misc/vspackages-and-the-managed-package-framework.md)