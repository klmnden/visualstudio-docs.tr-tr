---
title: MSBuild en iyi yöntemler | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: msbuild
ms.topic: reference
helpviewer_keywords:
- best practices, MSBuild
- MSBuild, best practices
ms.assetid: 90ef8693-e921-410a-a377-fe4d13f58c48
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: e597b10913ad495193545ab304b3b324d8f66b41
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68181123"
---
# <a name="msbuild-best-practices"></a>MSBuild En İyi Yöntemleri
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

MSBuild komut dosyaları yazmak için aşağıdaki en iyi yöntemleri öneririz:  
  
- Varsayılan özellik değerleri, kullanarak en iyi şekilde işlenir `Condition` özniteliği ve komut satırında bildirme varsayılan değerini geçersiz kılınabilir bir özellik tarafından. Örneğin, kullanın  
  
     `<MyProperty Condition="$(MyProperty)" == ''>`  
  
     `MyDefaultValue`  
  
     `</MyProperty>`  
  
- Öğe seçtiğinizde joker karakterler kaçının. Bunun yerine, dosyaları açıkça belirtin. Bu, eklediğinizde veya dosyaları silme oluşabilecek hatalar izlemenizi kolaylaştırır.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Gelişmiş Kavramlar](../msbuild/msbuild-advanced-concepts.md)
