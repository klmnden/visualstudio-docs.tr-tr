---
title: Büyük projeler derlerken belleği verimli şekilde kullanma | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: msbuild
ms.topic: conceptual
helpviewer_keywords:
- memory use (MSBuild)
- msbuild, efficient memory use building large trees
- caching (MSBuild)
ms.assetid: 853a21ed-69f7-4817-af00-57f73e2c74b5
caps.latest.revision: 15
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: b214ff057125b2921ec853fbee004cbb7d41f9e0
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54792773"
---
# <a name="using-memory-efficiently-when-you-build-large-projects"></a>Büyük Projeler Derlerken Belleği Verimli Şekilde Kullanma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
Büyük projeler çoğunlukla çok sayıda alt projeleri ve diğer bağımlılıklar içerir ve bunlar sistem belleği çok sayıda derleme zamanında tüketebilir. Kullanılabilir sistem belleğini azaldıkça, sistem performansı da azaltılabilir. Eski sürümlerini [!INCLUDE[vstecmsbuild](../includes/vstecmsbuild-md.md)] projeleri kaldığını bellekte veya sürüm 3.5 projeleri kaldırıldı, ancak yapı sonuçlarını sonraki almak için bir önbellekte saklanır.  
  
 Sürüm 4.0 işleme bu bellek yönetimi otomatik olarak gibi özellikleri kullanmak zorunda kalmaktan projeleri kaydederek `UnloadProjectsOnCompletion` ve `UseResultsCache`.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Paralel Olarak Birden Çok Proje Derleme](../msbuild/building-multiple-projects-in-parallel-with-msbuild.md)
