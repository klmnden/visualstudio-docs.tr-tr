---
title: Büyük projeler derlerken belleği verimli şekilde kullanma | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- memory use (MSBuild)
- msbuild, efficient memory use building large trees
- caching (MSBuild)
ms.assetid: 853a21ed-69f7-4817-af00-57f73e2c74b5
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: ab3be342f31e5df018c14f84d30febd38c31c401
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56631659"
---
# <a name="use-memory-efficiently-when-you-build-large-projects"></a>Büyük projeler derlerken belleği verimli bir şekilde kullanın
Büyük projeler çoğunlukla birçok projeler ve sistem belleği çok sayıda derleme zamanında kullanabileceği diğer bağımlılıklar içerir. Kullanılabilir sistem belleğini azaldıkça, sistem performansı da azaltılabilir. Eski sürümlerini [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] proje bellekte kaldı. Sürüm 3.5 projeleri eski sürümlerini kaldırılır, ancak yapı sonuçlarını sonraki almak için bir önbellekte saklanır.

 Sürüm 4.0 işleme bu bellek yönetimi otomatik olarak gibi özellikleri kullanmak zorunda kalmaktan projeleri kaydederek `UnloadProjectsOnCompletion` ve `UseResultsCache`.

### <a name="see-also"></a>Ayrıca bkz.
- [Paralel olarak birden çok proje derleme](../msbuild/building-multiple-projects-in-parallel-with-msbuild.md)