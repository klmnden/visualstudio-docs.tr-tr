---
title: 'Nasıl yapılır: MSBuild özel karakterleri kaçış | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: msbuild
ms.topic: conceptual
helpviewer_keywords:
- special characters, escaping
- characters, escapes
- escape characters
- MSBuild, escaping special characters
ms.assetid: 1aa3669c-1647-4960-b770-752e2532102f
caps.latest.revision: 15
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 291b8a33b5cf8777259be6325be9596bd9dc95e2
ms.sourcegitcommit: a83c60bb00bf95e6bea037f0e1b9696c64deda3c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/19/2019
ms.locfileid: "54834606"
---
# <a name="how-to-escape-special-characters-in-msbuild"></a>Nasıl yapılır: MSBuild'de Kaçış Özel Karakterleri
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
Belirli karakterler özel bir anlamı olmayan [!INCLUDE[vstecmsbuild](../includes/vstecmsbuild-md.md)] proje dosyaları. Karakterler örnekleri noktalı virgül (;) ve yıldız işareti (*) içerir. Bu özel karakterlerin tam bir listesi için bkz. [MSBuild özel karakterleri](../msbuild/msbuild-special-characters.md).  
  
 Bu özel karakterlerin bir proje dosyasında sabit değer olarak kullanmak için söz dizimi % kullanarak belirtilmelidir*xx*burada *xx* karakter ASCII onaltılık değerini temsil eder.  
  
## <a name="msbuild-special-characters"></a>MSBuild Özel Karakterleri  
 Bir özel karakter kullanıldığı örnek konusu `Include` öğesi listeleri özniteliği. Örneğin, aşağıdaki madde listesini iki öğe bildirir: `MyFile.cs` ve `MyClass.cs`.  
  
```  
<Compile Include="MyFile.cs;MyClass.cs"/>  
```  
  
 Adında bir noktalı virgül içeren bir öğe bildirmek istiyorsanız, % kullanmalısınız*xx* noktalı virgül kaçış ve önlemek için söz dizimi [!INCLUDE[vstecmsbuild](../includes/vstecmsbuild-md.md)] gelen iki ayrı öğeleri bildirme. Örneğin, aşağıdaki öğe noktalı virgül çıkışları ve bir öğe adlı bildirir `MyFile.cs;MyClass.cs`.  
  
```  
<Compile Include="MyFile.cs%3BMyClass.cs"/>  
```  
  
#### <a name="to-use-an-msbuild-special-character-as-a-literal-character"></a>MSBuild özel karakter değişmez değer olarak kullanmak için  
  
-   Gösterim % kullanmak*xx* özel karakter yerine burada *xx* ASCII karakter onaltılık değerini temsil eder. Örneğin, sabit karakter olarak yıldız işareti (*) kullanmak için değerini kullanın. `%2A`.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [MSBuild kavramları](../msbuild/msbuild-concepts.md)   
 [MSBuild](msbuild.md) [öğeleri](../msbuild/msbuild-items.md)
