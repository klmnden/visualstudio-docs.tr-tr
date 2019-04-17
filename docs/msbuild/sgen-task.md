---
title: SGen görevi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/msbuild/2003#SGen
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- SGen task [MSBuild]
- MSBuild, SGen task
ms.assetid: 22c5ade4-4159-4667-b891-0c1aa06f4df5
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 7da05a71d5de4a8f1ec6ef5fbb27a2e74220a1ef
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/17/2019
ms.locfileid: "59666669"
---
# <a name="sgen-task"></a>SGen görevi
Bir XML serileştirme derleme türleri için belirtilen derlemesinde oluşturur. Bu görev sarmalar XML serileştiricisi Oluşturma Aracı (*Sgen.exe*). Daha fazla bilgi için [XML serileştiricisi Oluşturma Aracı (Sgen.exe)](/dotnet/framework/serialization/xml-serializer-generator-tool-sgen-exe).

## <a name="parameters"></a>Parametreler
 Parametreleri aşağıdaki tabloda açıklanmıştır `SGen` görev.

| Parametre | Açıklama |
|-----------------------------| - |
| `BuildAssemblyName` | Gerekli `String` parametresi.<br /><br /> Serileştirme kod oluşturmak için derleme. |
| `BuildAssemblyPath` | Gerekli `String` parametresi.<br /><br /> Serileştirme kod oluşturmak için derleme yolu. |
| `DelaySign` | İsteğe bağlı `Boolean` parametresi.<br /><br /> Varsa `true`, tam olarak imzalı bir derleme istediğinizi belirtir. Varsa `false`, yalnızca derleme içinde ortak anahtar yerleştirmek istediğinizi belirtir.<br /><br /> Bu parametre ile birlikte kullanılmadığı sürece hiçbir etkisi olmaz `KeyFile` veya `KeyContainer` parametresi. |
| `KeyContainer` | İsteğe bağlı `String` parametresi.<br /><br /> Anahtar çifti içeren bir kapsayıcıyı belirtir. Bu derleme bildirimine ortak anahtar ekleyerek derlemeyi imzalar. Görev, ardından son derlemeyi özel anahtarla imzalar. |
| `KeyFile` | İsteğe bağlı `String` parametresi.<br /><br /> Bir derlemeyi imzalamak için kullanılacak bir anahtar çifti veya bir ortak anahtar belirtir. Derleyici ortak anahtarı derleme bildirimine ekler ve ardından son derlemeyi özel anahtarla imzalar. |
| `Platform` | İsteğe bağlı `String` parametresi.<br /><br /> Alır veya çıkış derlemesi oluşturmak için kullanılan derleyici platformu ayarlar. Bu parametre değerini alabilir `x86`, `x64`, veya `anycpu`. Varsayılan değer `anycpu`. |
| `References` | İsteğe bağlı `String[]` parametresi.<br /><br /> XML serileştirme gerektiren türleri tarafından başvurulan bir derleme belirtir. |
| `SdkToolsPath` | İsteğe bağlı `String` parametresi.<br /><br /> SDK Araçları yolunu gibi belirtir *resgen.exe*. |
| `SerializationAssembly` | İsteğe bağlı <xref:Microsoft.Build.Framework.ITaskItem> `[]` çıkış parametresi.<br /><br /> Oluşturulan serileştirme bütünleştirilmiş kod içeriyor. |
| `SerializationAssemblyName` | İsteğe bağlı `String` parametresi.<br /><br /> Oluşturulan serileştirme bütünleştirilmiş kodun adını belirtir. |
| `ShouldGenerateSerializer` | Gerekli `Boolean` parametresi.<br /><br /> Varsa `true`, SGen görevi bir serileştirme derlemesi oluştur. |
| `Timeout` | İsteğe bağlı `Int32` parametresi.<br /><br /> Sonra yürütülebilir görev sonlandırıldığından, milisaniye cinsinden süre miktarını belirtir. Varsayılan değer `Int.MaxValue`, hiçbir zaman aşımı süresi olduğunu gösterir. |
| `ToolPath` | İsteğe bağlı `String` parametresi.<br /><br /> Temel alınan yürütülebilir dosya görev burada yükleyecek konumu belirtir (*sgen.exe*). Bu parametre belirtilmezse görev çalışıyor framework sürümüne karşılık gelen SDK yükleme yolunu kullanır. [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)]. |
| `Types` | İsteğe bağlı `String[]` parametresi.<br /><br /> Alır veya ayarlar için serileştirme kod oluşturmak için belirli türlerinin bir listesi. SGen bu tür için yalnızca serileştirme kod oluşturur. |
| `UseProxyTypes` | Gerekli `Boolean` parametresi.<br /><br /> Varsa `true`, SGen görevi XML Web hizmeti proxy türleri için yalnızca serileştirme kod oluşturur. |

## <a name="remarks"></a>Açıklamalar
 Yukarıda listelenen parametrelerin yanı sıra, bu görev parametreleri devralan <xref:Microsoft.Build.Tasks.ToolTaskExtension> kendisi sınıfının devraldığı <xref:Microsoft.Build.Utilities.ToolTask> sınıfı. Bu ek parametrelerin ve Tanımlamaların bir listesi için bkz. [ToolTaskExtension taban sınıfı](../msbuild/tooltaskextension-base-class.md).

## <a name="see-also"></a>Ayrıca bkz.
- [Görev başvurusu](../msbuild/msbuild-task-reference.md)
- [Görevler](../msbuild/msbuild-tasks.md)
- [MSBuild kavramları](../msbuild/msbuild-concepts.md)