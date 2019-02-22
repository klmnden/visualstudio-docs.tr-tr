---
title: CreateVisualBasicManifestResourceName görevi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- MSBuild, CreateVisualBasicManifestResourceName task
- CreateVisualBasicManifestResourceName task [MSBuild]
ms.assetid: 251c47b9-de32-414b-a138-bf45290af12e
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: ee1426c763b60325190a5d15744fabe5eaa1b3ae
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56640681"
---
# <a name="createvisualbasicmanifestresourcename-task"></a>CreateVisualBasicManifestResourceName görevi
Oluşturur bir [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)]-stili bildirim adından bir verilen *.resx* dosya adı veya diğer kaynak.

## <a name="parameters"></a>Parametreler
 Parametreleri aşağıdaki tabloda açıklanmıştır [CreateVisualBasicManifestResourceName görevi](../msbuild/createvisualbasicmanifestresourcename-task.md).


| Parametre | Açıklama |
| - | - |
| `ManifestResourceNames` | <xref:Microsoft.Build.Framework.ITaskItem> `[]` çıkış parametresi salt okunur.<br /><br /> Sonuçta elde edilen bildirim adları. |
| `ResourceFiles` | Gerekli `String` parametresi.<br /><br /> Oluşturulacağı kaynak dosyasının adı [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] bildirim adı. |
| `RootNamespace` | İsteğe bağlı `String` parametresi.<br /><br /> Genellikle proje dosyasından alınan kaynak dosyasının kök ad alanı. Olabilir `null`. |
| `PrependCultureAsDirectory` | İsteğe bağlı `Boolean` parametresi.<br /><br /> Varsa `true`, kültür adı bildirim kaynağı adına hemen önce bir dizin adı olarak eklenir. Varsayılan değer `true`. |
| `ResourceFilesWithManifestResourceNames` | İsteğe bağlı salt okunur `String` çıkış parametresi.<br /><br /> Artık bildirim kaynağı adına içeren kaynak dosyasının adını döndürür. |

## <a name="remarks"></a>Açıklamalar
 [CreateVisualBasicManifestResourceName görevi](../msbuild/createvisualbasicmanifestresourcename-task.md) atamak için uygun bildirim kaynak adını belirleyen bir verilen *.resx* veya başka bir kaynak dosyası. Görev, bir kaynak dosyası için mantıksal bir ad sağlar ve bir output parametresi olarak meta veriler ekler.

 Yukarıda listelenen parametrelerin yanı sıra, bu görev parametreleri devralan <xref:Microsoft.Build.Tasks.TaskExtension> kendisi sınıfının devraldığı <xref:Microsoft.Build.Utilities.Task> sınıfı. Bu ek parametrelerin ve Tanımlamaların bir listesi için bkz. [TaskExtension taban sınıfı](../msbuild/taskextension-base-class.md).

## <a name="see-also"></a>Ayrıca bkz.
- [Görevler](../msbuild/msbuild-tasks.md)
- [Görev başvurusu](../msbuild/msbuild-task-reference.md)