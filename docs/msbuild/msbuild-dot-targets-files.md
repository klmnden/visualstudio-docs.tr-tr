---
title: MSBUILD. Hedef dosyalar | Microsoft Docs
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
ms.openlocfilehash: bacc58184d0ea78a5e54d7cc7b0b93df107b3300
ms.sourcegitcommit: 5694c5236fa32ba7f5bc1236a853f725ec7557e9
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/31/2019
ms.locfileid: "68681404"
---
# <a name="msbuild-targets-files"></a>MSBuild. targets dosyaları
[!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)]ortak senaryolar için öğeleri, özellikleri, hedefleri ve görevleri içeren birkaç *. targets* dosyası içerir. Bu dosyalar, bakım ve okunabilirlik işlemlerini [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] basitleştirmek üzere çoğu proje dosyasına otomatik olarak aktarılır.

 Projeler genellikle derleme işlemlerini tanımlamak için bir veya daha fazla *. targets* dosyasını içeri aktarır. Örneğin, tarafından [!INCLUDE[csprcs](../data-tools/includes/csprcs_md.md)] [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] oluşturulan bir proje *Microsoft. Common. targets*'ı içeri aktaran *Microsoft. CSharp. targets* içeri aktarır. Projenin kendisi bu projeye özgü öğeleri ve özellikleri tanımlar, ancak [!INCLUDE[csprcs](../data-tools/includes/csprcs_md.md)] projenin standart yapı kuralları içeri aktarılan *. targets* dosyalarında tanımlanır. [!INCLUDE[csprcs](../data-tools/includes/csprcs_md.md)]

 Değer `$(MSBuildToolsPath)` , bu ortak *. targets* dosyalarının yolunu belirtir. `ToolsVersion` 4,0 ise, dosyalar aşağıdaki konumdadır: *\<Windowsınstallationpath > \Microsoft.NET\Framework\v4.0.30319\\*

> [!NOTE]
> Kendi hedeflerinizi oluşturma hakkında daha fazla bilgi için bkz. [targets](../msbuild/msbuild-targets.md). Bir proje dosyasını başka bir proje dosyasına `Import` eklemek için öğesinin nasıl kullanılacağı hakkında bilgi için bkz. [Import element (MSBuild)](../msbuild/import-element-msbuild.md) ve [nasıl yapılır: Birden çok proje](../msbuild/how-to-use-the-same-target-in-multiple-project-files.md)dosyasında aynı hedefi kullanın.

## <a name="common-targets-files"></a>Ortak. targets dosyaları

| *. targets* dosyası | Açıklama |
|---------------------------------| - |
| *Microsoft. Common. targets* | [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] Ve[!INCLUDE[csprcs](../data-tools/includes/csprcs_md.md)] projeleri için standart derleme işlemindeki adımları tanımlar.<br /><br /> Aşağıdaki ifadeyi içeren *Microsoft. CSharp. targets* ve *Microsoft. VisualBasic. targets* dosyaları tarafından içeri aktarılır:`<Import Project="Microsoft.Common.targets" />` |
| *Microsoft. CSharp. targets* | Görsel C# projeler için standart derleme işlemindeki adımları tanımlar.<br /><br /> Aşağıdaki ifadeyi içeren C# görsel proje dosyaları ( *. csproj*) tarafından içeri aktarıldı:`<Import Project="$(MSBuildToolsPath)\Microsoft.CSharp.targets" />` |
| *Microsoft. VisualBasic. targets* | Visual Basic projeleri için standart derleme işlemindeki adımları tanımlar.<br /><br /> Aşağıdaki ifadeyi içeren Visual Basic proje dosyaları ( *. vbproj*) tarafından içeri aktarıldı:`<Import Project="$(MSBuildToolsPath)\Microsoft.VisualBasic.targets" />` |

## <a name="directorybuildtargets"></a>Directory. Build. targets
*Directory. Build. targets* , bir dizin altındaki projelere özelleştirmeler sağlayan Kullanıcı tanımlı bir dosyadır. **Importdirectorybuildtargets** özelliği **false**olarak ayarlanmadığı takdirde bu dosya *Microsoft. Common. targets* öğesinden otomatik olarak içeri aktarılır. Daha fazla bilgi için [yapınızı özelleştirin](customize-your-build.md).

## <a name="see-also"></a>Ayrıca bkz.
- [İçeri aktarma öğesi (MSBuild)](../msbuild/import-element-msbuild.md)
- [MSBuild başvurusu](../msbuild/msbuild-reference.md)
- [MSBuild](../msbuild/msbuild.md)
