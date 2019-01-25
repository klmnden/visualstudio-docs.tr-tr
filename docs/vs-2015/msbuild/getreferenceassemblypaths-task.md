---
title: GetReferenceAssemblyPaths görevi | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: msbuild
ms.topic: reference
dev_langs:
- VB
- CSharp
- C++
- jsharp
ms.assetid: 178ef49c-5dee-405b-a14b-a37f41dc0609
caps.latest.revision: 7
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 4563e1c28c17a173c211f979d2ca46503a6d19a7
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54805136"
---
# <a name="getreferenceassemblypaths-task"></a>GetReferenceAssemblyPaths Görevi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
Başvuru bütünleştirilmiş kodu yolları çeşitli çerçevesini döndürür.  
  
## <a name="parameters"></a>Parametreler  
 Parametreleri aşağıdaki tabloda açıklanmıştır `GetReferenceAssemblyPaths` görev.  
  
|Parametre|Açıklama|  
|---------------|-----------------|  
|`ReferenceAssemblyPaths`|İsteğe bağlı `String[]` çıkış parametresi.<br /><br /> Temel yolunu döndürür `TargetFrameworkMoniker` parametresi. Varsa `TargetFrameworkMoniker` null veya boş, bu yolu olacak `String.Empty`.|  
|`FullFrameworkReferenceAssemblyPaths`|İsteğe bağlı `String[]` çıkış parametresi.<br /><br /> Temel yolunu döndürür `TargetFrameworkMoniker` ad profili bölümünü dikkate almadan parametresi. Varsa `TargetFrameworkMoniker` null veya boş, bu yolu olacak `String.Empty`.|  
|`TargetFrameworkMoniker`|İsteğe bağlı `String` parametresi.<br /><br /> Başvuru bütünleştirilmiş kodu yolları ile ilişkili olan hedef çerçeve adını belirtir.|  
|`RootPath`|İsteğe bağlı `String` parametresi.<br /><br /> Başvuru bütünleştirilmiş kod yolu oluşturmak için kullanılacak kök yolunu belirtir.|  
|`BypassFrameworkInstallChecks`|İsteğe bağlı [Boolean] (<!-- TODO: review code entity reference <xref:assetId:///Boolean?qualifyHint=False&amp;autoUpgrade=True>  -->) parametre.<br /><br /> Varsa `true`, temel denetimler atlar, `GetReferenceAssemblyPaths` belirli çalışma zamanı çerçeveleri, hedef Framework'ü bağlı olarak yüklendiğinden emin olmak için varsayılan olarak gerçekleştirir.|  
|`TargetFrameworkMonikerDisplayName`|İsteğe bağlı `String` çıkış parametresi.<br /><br /> Hedef Çerçeve adı için görünen adları belirtir.|  
  
## <a name="remarks"></a>Açıklamalar  
 Tabloda listelenen parametreleri sahip olmaya ek olarak, bu görev parametreleri devralan <xref:Microsoft.Build.Tasks.TaskExtension> kendisi sınıfının devraldığı <xref:Microsoft.Build.Utilities.Task> sınıfı. Bu ek parametrelerin ve Tanımlamaların bir listesi için bkz. [TaskExtension temel sınıfı](../msbuild/taskextension-base-class.md).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Görevleri](../msbuild/msbuild-tasks.md)   
 [Görev Başvurusu](../msbuild/msbuild-task-reference.md)
