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
ms.openlocfilehash: 28d9f3d43faa53731b101dfdf58fe1e68a0920c5
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68178297"
---
# <a name="using-memory-efficiently-when-you-build-large-projects"></a>Büyük Projeler Derlerken Belleği Verimli Şekilde Kullanma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Büyük projeler çoğunlukla çok sayıda alt projeleri ve diğer bağımlılıklar içerir ve bunlar sistem belleği çok sayıda derleme zamanında tüketebilir. Kullanılabilir sistem belleğini azaldıkça, sistem performansı da azaltılabilir. Eski sürümlerini [!INCLUDE[vstecmsbuild](../includes/vstecmsbuild-md.md)] projeleri kaldığını bellekte veya sürüm 3.5 projeleri kaldırıldı, ancak yapı sonuçlarını sonraki almak için bir önbellekte saklanır.  
  
 Sürüm 4.0 işleme bu bellek yönetimi otomatik olarak gibi özellikleri kullanmak zorunda kalmaktan projeleri kaydederek `UnloadProjectsOnCompletion` ve `UseResultsCache`.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Paralel Olarak Birden Çok Proje Derleme](../msbuild/building-multiple-projects-in-parallel-with-msbuild.md)
