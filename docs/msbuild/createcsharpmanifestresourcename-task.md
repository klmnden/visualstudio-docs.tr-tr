---
title: CreateCSharpManifestResourceName görevi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- MSBuild, CreateCSharpManifestResourceName task
- CreateCSharpManifestResourceName task [MSBuild]
ms.assetid: 2ace88c1-d757-40a7-8158-c1d3f5ff0511
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: b7ddede6870a982520b87cf8ec497788b4731244
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56640551"
---
# <a name="createcsharpmanifestresourcename-task"></a>CreateCSharpManifestResourceName görevi
Oluşturur bir [!INCLUDE[csprcs](../data-tools/includes/csprcs_md.md)]-stili bildirim adından bir verilen *.resx* dosya adı veya diğer kaynak.

## <a name="parameters"></a>Parametreler
 Parametreleri aşağıdaki tabloda açıklanmıştır [CreateCSharpManifestResourceName görevi](../msbuild/createcsharpmanifestresourcename-task.md).


| Parametre | Açıklama |
| - | - |
| `ManifestResourceNames` | <xref:Microsoft.Build.Framework.ITaskItem> `[]` çıkış parametresi salt okunur.<br /><br /> Sonuçta elde edilen bildirim adları. |
| `ResourceFiles` | Gerekli `String` parametresi.<br /><br /> Oluşturulacağı kaynak dosyasının adı [!INCLUDE[csprcs](../data-tools/includes/csprcs_md.md)] bildirim adı. |
| `RootNamespace` | İsteğe bağlı `String` parametresi.<br /><br /> Genellikle proje dosyasından alınan kaynak dosyasının kök ad alanı. Olabilir `null`. |
| `PrependCultureAsDirectory` | İsteğe bağlı `Boolean` parametresi.<br /><br /> Varsa `true`, kültür adı bildirim kaynağı adına hemen önce bir dizin adı olarak eklenir. Varsayılan değer `true`. |
| `ResourceFilesWithManifestResourceNames` | İsteğe bağlı salt okunur `String` çıkış parametresi.<br /><br /> Artık bildirim kaynağı adına içeren kaynak dosyasının adını döndürür. |

## <a name="remarks"></a>Açıklamalar
 [CreateVisualBasicManifestResourceName görevi](../msbuild/createvisualbasicmanifestresourcename-task.md) atamak için uygun bildirim kaynak adını belirleyen bir verilen *.resx* veya başka bir kaynak dosyası. Görev, bir kaynak dosyası için mantıksal bir ad sağlar ve bir output parametresi olarak meta veriler ekler.

 Yukarıda listelenen parametrelerin yanı sıra, bu görev parametreleri devralan <xref:Microsoft.Build.Tasks.TaskExtension> kendisi sınıfının devraldığı <xref:Microsoft.Build.Utilities.Task> sınıfı. Bu ek parametrelerin ve Tanımlamaların bir listesi için bkz. [TaskExtension taban sınıfı](../msbuild/taskextension-base-class.md).

## <a name="see-also"></a>Ayrıca bkz.
- [Görevler](../msbuild/msbuild-tasks.md)
- [Görev başvurusu](../msbuild/msbuild-task-reference.md)