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
ms.openlocfilehash: c326dc31f6ce80026f1c83c5b71f8e27faabf93e
ms.sourcegitcommit: 4dfe098ac0df294aad63e6b384d6575980798ca3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/11/2019
ms.locfileid: "70887635"
---
# <a name="sgen-task"></a>SGen görevi
Belirtilen derlemedeki türler için bir XML serileştirme bütünleştirilmiş kodu oluşturur. Bu görev, XML serileştirici Oluşturucu aracı 'nı (*SGen. exe*) sarmalanmış. Daha fazla bilgi için bkz. [XML serileştirici Oluşturucu aracı (SGen. exe)](/dotnet/framework/serialization/xml-serializer-generator-tool-sgen-exe).

## <a name="parameters"></a>Parametreler
 Aşağıdaki tablo, `SGen` görevin parametrelerini açıklar.

| Parametre | Açıklama |
|-----------------------------| - |
| `BuildAssemblyName` | Gerekli `String` parametre.<br /><br /> İçin serileştirme kodu oluşturulacak derleme. |
| `BuildAssemblyPath` | Gerekli `String` parametre.<br /><br /> İçin serileştirme kodu oluşturulacak derlemenin yolu. |
| `DelaySign` | İsteğe `Boolean` bağlı parametre.<br /><br /> `true`Yalnızca ortak anahtarı derlemeye yerleştirmek istediğinizi belirtir. İse `false`, tam olarak imzalanan bir derleme istediğinizi belirtir.<br /><br /> `KeyFile` Ya`KeyContainer` da parametresiyle kullanılmamışsa, bu parametrenin hiçbir etkisi yoktur. |
| `KeyContainer` | İsteğe `String` bağlı parametre.<br /><br /> Anahtar çifti içeren bir kapsayıcıyı belirtir. Bu, derleme bildirimine ortak anahtar ekleyerek derlemeyi imzalayacaktır. Görev daha sonra son derlemeyi özel anahtarla imzalayacaktır. |
| `KeyFile` | İsteğe `String` bağlı parametre.<br /><br /> Bir derlemeyi imzalamak için kullanılacak bir anahtar çifti veya ortak anahtar belirtir. Derleyici ortak anahtarı derleme bildirimine ekler ve ardından son derlemeyi özel anahtarla imzalar. |
| `Platform` | İsteğe `String` bağlı parametre.<br /><br /> Çıktı derlemesini oluşturmak için kullanılan derleyici platformunu alır veya ayarlar. Bu parametre `x86`, `x64`, veya `anycpu`değerine sahip olabilir. Varsayılan değer `anycpu`. |
| `References` | İsteğe `String[]` bağlı parametre.<br /><br /> XML serileştirme gerektiren türleri tarafından başvurulan bir derleme belirtir. |
| `SdkToolsPath` | İsteğe `String` bağlı parametre.<br /><br /> *Resgen. exe*gibi SDK araçlarının yolunu belirtir. |
| `SerializationAssembly` | İsteğe <xref:Microsoft.Build.Framework.ITaskItem> bağlı`[]` çıkış parametresi.<br /><br /> Oluşturulan serileştirme derlemesini içerir. |
| `SerializationAssemblyName` | İsteğe `String` bağlı parametre.<br /><br /> Oluşturulan serileştirme derlemesinin adını belirtir. |
| `ShouldGenerateSerializer` | Gerekli `Boolean` parametre.<br /><br /> İse `true`, SGen görevinin bir serileştirme derlemesi oluşturması gerekir. |
| `Timeout` | İsteğe `Int32` bağlı parametre.<br /><br /> Görev yürütülebilir dosyasının sonlandırılacağı süre (milisaniye cinsinden) sayısını belirtir. Varsayılan değer `Int.MaxValue`, zaman aşımı süresi olmadığını gösterir. |
| `ToolPath` | İsteğe `String` bağlı parametre.<br /><br /> Görevin temel alınan yürütülebilir dosyayı (*SGen. exe*) yükleneceği konumu belirtir. Bu parametre belirtilmezse, görev, çalıştıran [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)]çerçevenin sürümüne karşılık gelen SDK yükleme yolunu kullanır. |
| `Types` | İsteğe `String[]` bağlı parametre.<br /><br /> İçin serileştirme kodu oluşturmak üzere belirli türlerin bir listesini alır veya ayarlar. SGen yalnızca bu türler için serileştirme kodu oluşturur. |
| `UseProxyTypes` | Gerekli `Boolean` parametre.<br /><br /> İse `true`, SGen görevi yalnızca XML Web hizmeti proxy türleri için serileştirme kodu oluşturur. |

## <a name="remarks"></a>Açıklamalar
 Yukarıda listelenen parametrelere ek olarak, bu görev sınıfından devralınan <xref:Microsoft.Build.Tasks.ToolTaskExtension> <xref:Microsoft.Build.Utilities.ToolTask> parametreleri devralır. Bu ek parametrelerin ve açıklamalarının listesi için bkz. [ToolTaskExtension temel sınıfı](../msbuild/tooltaskextension-base-class.md).

## <a name="see-also"></a>Ayrıca bkz.
- [Görev başvurusu](../msbuild/msbuild-task-reference.md)
- [Görevler](../msbuild/msbuild-tasks.md)
- [MSBuild kavramları](../msbuild/msbuild-concepts.md)