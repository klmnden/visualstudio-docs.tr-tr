---
title: MSBuild en iyi yöntemler | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- best practices, MSBuild
- MSBuild, best practices
ms.assetid: 90ef8693-e921-410a-a377-fe4d13f58c48
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 622d7b087e94d21f86691b88c3af4891aa533e9a
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55013216"
---
# <a name="msbuild-best-practices"></a>MSBuild en iyi uygulamalar
MSBuild komut dosyaları yazmak için aşağıdaki en iyi yöntemleri öneririz:  
  
-   Varsayılan özellik değerleri, kullanarak en iyi şekilde işlenir `Condition` özniteliği ve komut satırında bildirme varsayılan değerini geçersiz kılınabilir bir özellik tarafından. Örneğin, kullanın  
  
```xml
<MyProperty Condition="'$(MyProperty)' == ''">
   MyDefaultValue
</MyProperty>
```
  
-   Öğe seçtiğinizde joker karakterler kaçının. Bunun yerine, dosyaları açıkça belirtin. Bu, eklediğinizde veya dosyaları silme oluşabilecek hatalar izlemenizi kolaylaştırır.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Gelişmiş kavramlar](../msbuild/msbuild-advanced-concepts.md)
