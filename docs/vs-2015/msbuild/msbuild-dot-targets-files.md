---
title: MSBuild. Hedefler dosyaları | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: msbuild
ms.topic: reference
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- .Targets files
- MSBuild, .Targets files
ms.assetid: f6d98eb4-d2fa-49b7-8e3c-bae1ca3cf596
caps.latest.revision: 20
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: bab229a3246ac91eaa652be67e98a68aab40e820
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63439380"
---
# <a name="msbuild-targets-files"></a>MSBuild .Targets Dosyaları
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

[!INCLUDE[vstecmsbuild](../includes/vstecmsbuild-md.md)] öğeleri, özellikleri, hedefleri ve görevleri sık karşılaşılan senaryolara yönelik içeren birkaç .targets dosyaları içerir. Bu dosyaları en otomatik olarak içeri aktarılan [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] proje dosyaları, Bakım ve okunabilirliği kolaylaştırmak.  
  
 Projeleri genellikle yapı işlemlerini tanımlamak için bir veya daha fazla .targets dosyalarını içeri aktarın. Örneğin bir [!INCLUDE[csprcs](../includes/csprcs-md.md)] proje tarafından oluşturulan [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] , Microsoft.common.targets'ı aktarır Microsoft.CSharp.targets içeri aktaracak. [!INCLUDE[csprcs](../includes/csprcs-md.md)] Projenin kendisinin tanımlama öğeleri ve belirli özellikleri bu projeye, ancak standart derleme kuralları için bir [!INCLUDE[csprcs](../includes/csprcs-md.md)] proje içeri aktarılan .targets dosyalarında tanımlanır.  
  
 `$(MSBuildToolsPath)` Değeri bu ortak .targets dosyaları yolunu belirtir. Varsa `ToolsVersion` 4.0, dosyaları şu konumda: `WindowsInstallationPath\Microsoft.NET\Framework\v4.0.30319\`  
  
> [!NOTE]
> Kendi hedefleri oluşturma hakkında daha fazla bilgi için bkz: [hedefleri](../msbuild/msbuild-targets.md). Nasıl kullanılacağı hakkında daha fazla bilgi için `Import` öğesinin başka bir proje dosyasına bir proje dosyası eklemek için [içeri aktarma öğesi (MSBuild)](../msbuild/import-element-msbuild.md) ve [nasıl yapılır: Birden çok proje dosyasında aynı hedefi kullanma](../msbuild/how-to-use-the-same-target-in-multiple-project-files.md).  
  
## <a name="common-targets-files"></a>Ortak. MSBuild  
  
|. Hedef dosya|Açıklama|  
|-------------------|-----------------|  
|Microsoft.Common.targets|İçin standart derleme işlemindeki adımları tanımlar [!INCLUDE[vbprvb](../includes/vbprvb-md.md)] ve [!INCLUDE[csprcs](../includes/csprcs-md.md)] projeleri.<br /><br /> Aşağıdaki deyim içeren Microsoft.CSharp.targets ve Microsoft.VisualBasic.targets'daki dosyaları tarafından içe aktarılan: `<Import Project="Microsoft.Common.targets" />`|  
|Microsoft.CSharp.targets|Visual C# projeleri için standart derleme işlemindeki adımları tanımlar.<br /><br /> Aşağıdaki deyim içeren Visual C# proje dosyaları tarafından (.csproj) içeri aktarıldı: `<Import Project="$(MSBuildToolsPath)\Microsoft.CSharp.targets" />`|  
|Microsoft.VisualBasic.targets|Visual Basic projeleri için standart derleme işlemindeki adımları tanımlar.<br /><br /> Aşağıdaki deyim içeren Visual Basic proje dosyaları (.vbproj) içeri aktarıldı: `<Import Project="$(MSBuildToolsPath)\Microsoft.VisualBasic.targets" />`|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [İçeri aktarma öğesi (MSBuild)](../msbuild/import-element-msbuild.md)   
 [MSBuild Başvurusu](../msbuild/msbuild-reference.md)  
 [MSBuild](msbuild.md)
