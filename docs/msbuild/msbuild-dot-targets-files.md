---
title: MSBuild. Hedefler dosyaları | Microsoft Docs
ms.date: 02/24/2017
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
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: c4053cd105bddf94644318ff7e06811e8d8cbbaf
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54961903"
---
# <a name="msbuild-targets-files"></a>MSBuild .targets dosyaları
[!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] birkaç içeren *.targets* öğeleri, özellikleri, hedefleri ve görevleri sık karşılaşılan senaryolara yönelik içeren dosyaları. Bu dosyaları en otomatik olarak içeri aktarılan [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] proje dosyaları, Bakım ve okunabilirliği kolaylaştırmak.  

 Projeleri genellikle bir veya daha fazla Al *.targets* yapı işlemlerini tanımlamak için dosyaları. Örneğin bir [!INCLUDE[csprcs](../data-tools/includes/csprcs_md.md)] proje tarafından oluşturulan [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] içeri aktaracak *Microsoft.CSharp.targets* hangi içeri aktarmalar *Microsoft.Common.targets*. [!INCLUDE[csprcs](../data-tools/includes/csprcs_md.md)] Projenin kendisinin tanımlama öğeleri ve belirli özellikleri bu projeye, ancak standart derleme kuralları için bir [!INCLUDE[csprcs](../data-tools/includes/csprcs_md.md)] proje tanımlanır, içeri aktarılan *.targets* dosyaları.  

 `$(MSBuildToolsPath)` Değeri bu ortak yolu belirtir *.targets* dosyaları. Varsa `ToolsVersion` 4.0, dosyaları şu konumda: *\<WindowsInstallationPath > \Microsoft.NET\Framework\v4.0.30319\\*  

> [!NOTE]
>  Kendi hedefleri oluşturma hakkında daha fazla bilgi için bkz: [hedefleri](../msbuild/msbuild-targets.md). Nasıl kullanılacağı hakkında daha fazla bilgi için `Import` öğesinin başka bir proje dosyasına bir proje dosyası eklemek için [içeri aktarma öğesi (MSBuild)](../msbuild/import-element-msbuild.md) ve [nasıl yapılır: Birden çok proje dosyasında aynı hedefi kullanma](../msbuild/how-to-use-the-same-target-in-multiple-project-files.md).  

## <a name="common-targets-files"></a>Ortak .targets dosyaları  

| *.targets* dosyası | Açıklama |
|---------------------------------| - |
| *Microsoft.Common.targets* | İçin standart derleme işlemindeki adımları tanımlar [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] ve [!INCLUDE[csprcs](../data-tools/includes/csprcs_md.md)] projeleri.<br /><br /> Tarafından alınan *Microsoft.CSharp.targets* ve *Microsoft.VisualBasic.targets* aşağıdaki deyim içeren dosyalar: `<Import Project="Microsoft.Common.targets" />` |
| *Microsoft.CSharp.targets* | Visual C# projeleri için standart derleme işlemindeki adımları tanımlar.<br /><br /> Visual C# proje dosyaları tarafından içe aktarılan (*.csproj*), aşağıdaki deyimi ekleyin: `<Import Project="$(MSBuildToolsPath)\Microsoft.CSharp.targets" />` |
| *Microsoft.VisualBasic.targets* | Visual Basic projeleri için standart derleme işlemindeki adımları tanımlar.<br /><br /> Visual Basic proje dosyaları tarafından içe aktarılan (*.vbproj*), aşağıdaki deyimi ekleyin: `<Import Project="$(MSBuildToolsPath)\Microsoft.VisualBasic.targets" />` |

## <a name="directorybuildtargets"></a>Directory.Build.targets
*Directory.Build.targets* özelleştirmeleri bir dizin altında projelerine sağlayan kullanıcı tanımlı bir dosya. Bu dosya gelen otomatik olarak içeri aktarılır *Microsoft.Common.targets* sürece özelliği **ImportDirectoryBuildTargets** ayarlanır **false**.

## <a name="see-also"></a>Ayrıca bkz.  
 [İçeri aktarma öğesi (MSBuild)](../msbuild/import-element-msbuild.md)   
 [MSBuild başvurusu](../msbuild/msbuild-reference.md)  
 [MSBuild](../msbuild/msbuild.md)
