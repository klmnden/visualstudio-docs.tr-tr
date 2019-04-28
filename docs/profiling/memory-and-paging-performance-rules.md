---
title: Bellek ve disk belleği performans kuralları | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: f37972b2-efe4-4a1c-a5d1-a246ccd76817
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 1f779a050c334e8f61d6d3711ed2be2a7b087e72
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62896692"
---
# <a name="memory-and-paging-performance-rules"></a>Bellek ve disk belleği performans kuralları
Uygulama performansını ve yanıt hızını etkileyebilir bir profil oluşturma çalıştırmasını etkinliğinde disk belleği bellek ve disk belleği kategorisi içindeki performans kuralları tanımlayın.

|||
|-|-|
|[DA0014: Çok yüksek oranda diske etkin bellek sayfalaması](../profiling/da0014-extremely-high-rates-of-paging-active-memory-to-disk.md)|Profil oluşturma çalışması boyunca yüksek oranda diske gelen ve giden etkin bellek Sayfalaması oluştu. Bu düzey genellikle Uygulama performansı etkileyebilir ve yanıt hızını oranlarda sayfalama. Algoritmalar düzeltilmesi tarafından bellek ayırmaları azaltmayı göz önünde bulundurun. Uygulamanızın bellek gereksinimlerini göz önünde bulundurun gerekebilir. Daha fazla belleğe sahip bir bilgisayarda yeniden profil çalıştırmayı deneyin. Bu kural, disk belleği etkinlik miktarı kuralının D0017 üst eşiği aştığında tetikler.|
|[DA0017: Yüksek oranda diske etkin bellek sayfalaması](../profiling/da0017-high-rates-of-paging-active-memory-to-disk.md)|Profil oluşturma çalışması boyunca görece yüksek oranda bir disk gelen ve giden etkin bellek Sayfalaması oluştu. Bu düzey genellikle Uygulama performansı etkileyebilir ve yanıt hızını oranlarda sayfalama. Algoritmalar düzeltilmesi tarafından bellek ayırmaları azaltmayı göz önünde bulundurun. Uygulamanızın bellek gereksinimlerini göz önünde bulundurun gerekebilir. Daha fazla belleğe sahip bir bilgisayarda yeniden profil çalıştırmayı deneyin.|