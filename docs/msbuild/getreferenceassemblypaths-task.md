---
title: GetReferenceAssemblyPaths görevi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
dev_langs:
- VB
- CSharp
- C++
- jsharp
ms.assetid: 178ef49c-5dee-405b-a14b-a37f41dc0609
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: e752e345de9211a2b6c8d8fe076be863a04c70ca
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56610274"
---
# <a name="getreferenceassemblypaths-task"></a>GetReferenceAssemblyPaths görevi
Başvuru bütünleştirilmiş kodu yolları çeşitli çerçevesini döndürür.

## <a name="parameters"></a>Parametreler
 Parametreleri aşağıdaki tabloda açıklanmıştır `GetReferenceAssemblyPaths` görev.

|Parametre|Açıklama|
|---------------|-----------------|
|`ReferenceAssemblyPaths`|İsteğe bağlı `String[]` çıkış parametresi.<br /><br /> Temel yolunu döndürür `TargetFrameworkMoniker` parametresi. Varsa `TargetFrameworkMoniker` null veya boş, bu yolu olacak `String.Empty`.|
|`FullFrameworkReferenceAssemblyPaths`|İsteğe bağlı `String[]` çıkış parametresi.<br /><br /> Temel yolunu döndürür `TargetFrameworkMoniker` ad profili bölümünü dikkate almadan parametresi. Varsa `TargetFrameworkMoniker` null veya boş, bu yolu olacak `String.Empty`.|
|`TargetFrameworkMoniker`|İsteğe bağlı `String` parametresi.<br /><br /> Başvuru bütünleştirilmiş kodu yolları ile ilişkili olan hedef çerçeve adını belirtir.|
|`RootPath`|İsteğe bağlı `String` parametresi.<br /><br /> Başvuru bütünleştirilmiş kod yolu oluşturmak için kullanılacak kök yolunu belirtir.|
|`BypassFrameworkInstallChecks`|İsteğe bağlı <xref:System.Boolean> parametresi.<br /><br /> Varsa `true`, temel denetimler atlar, `GetReferenceAssemblyPaths` belirli çalışma zamanı çerçeveleri, hedef Framework'ü bağlı olarak yüklendiğinden emin olmak için varsayılan olarak gerçekleştirir.|
|`TargetFrameworkMonikerDisplayName`|İsteğe bağlı `String` çıkış parametresi.<br /><br /> Hedef Çerçeve adı için görünen adları belirtir.|

## <a name="remarks"></a>Açıklamalar
 Tabloda listelenen parametreleri sahip olmaya ek olarak, bu görev parametreleri devralan <xref:Microsoft.Build.Tasks.TaskExtension> kendisi sınıfının devraldığı <xref:Microsoft.Build.Utilities.Task> sınıfı. Bu ek parametrelerin ve Tanımlamaların bir listesi için bkz. [TaskExtension taban sınıfı](../msbuild/taskextension-base-class.md).

## <a name="see-also"></a>Ayrıca bkz.
- [Görevler](../msbuild/msbuild-tasks.md)
- [Görev başvurusu](../msbuild/msbuild-task-reference.md)