---
title: 'Nasıl yapılır: MSBuild.exe kullanarak çözümlerde belirli hedefleri derleme | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: msbuild
ms.topic: conceptual
helpviewer_keywords:
- MSBuild, building specific targets in a solution
- msbuild.exe, building specific targets in a solution
- MSBuild, msbuild.exe
ms.assetid: f46feb9b-4c16-4fec-b6e1-36a959692ba3
caps.latest.revision: 12
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 8bfef86b8ea82077ba7fe3f753f9835c06c3380a
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68156653"
---
# <a name="how-to-build-specific-targets-in-solutions-by-using-msbuildexe"></a>Nasıl yapılır: MSBuild.exe Kullanarak Çözümlerde Belirli Hedefleri Derleme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

MSBuild.exe belirli projelerin bir çözümde belirli hedefler oluşturmak için kullanabilirsiniz.  
  
### <a name="to-build-a-specific-target-of-a-specific-project-in-a-solution"></a>Belirli bir hedef bir çözümde belirli bir proje oluşturmak için  
  
1. Komut satırında `MSBuild.exe <SolutionName>.sln`burada `<SolutionName>` yürütmek istediğiniz hedef içeren çözüm dosya adına karşılık gelir.  
  
2. Sonra hedef belirtmek **/t** geçiş biçiminde *ProjectName*:*TargetName*.  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnek yürütür `Rebuild` hedefinin `NotInSlnFolder` proje ve sonra yürütür `Clean` hedefinin `InSolutionFolder` bulunan proje `NewFolder` Çözüm klasörü.  
  
```  
msbuild SlnFolders.sln /t:NotInSlnfolder:Rebuild;NewFolder\InSolutionFolder:Clean  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Komut satırı başvurusu](../msbuild/msbuild-command-line-reference.md)   
 [MSBuild başvurusu](../msbuild/msbuild-reference.md)   
 [MSBuild](msbuild.md)  
 [MSBuild Kavramları](../msbuild/msbuild-concepts.md)
