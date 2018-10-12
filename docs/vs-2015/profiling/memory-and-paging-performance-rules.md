---
title: Bellek ve disk belleği performans kuralları | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: f37972b2-efe4-4a1c-a5d1-a246ccd76817
caps.latest.revision: 13
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 7776daa85c176f95dd95a3d120d5c2471d10214a
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49183358"
---
# <a name="memory-and-paging-performance-rules"></a>Bellek ve Disk Belleği Performans Kuralları
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Uygulama performansını ve yanıt hızını etkileyebilir bir profil oluşturma çalıştırmasını etkinliğinde disk belleği bellek ve disk belleği kategorisi içindeki performans kuralları tanımlayın.  
  
|||  
|-|-|  
|[DA0014: Aşırı yüksek oranda diske etkin bellek sayfalaması gerçekleşiyor.](../profiling/da0014-extremely-high-rates-of-paging-active-memory-to-disk.md)|Profil oluşturma çalışması boyunca yüksek oranda diske gelen ve giden etkin bellek Sayfalaması oluştu. Bu düzey genellikle Uygulama performansı etkileyebilir ve yanıt hızını oranlarda sayfalama. Algoritmalar düzeltilmesi tarafından bellek ayırmaları azaltmayı göz önünde bulundurun. Uygulamanızın bellek gereksinimlerini göz önünde bulundurun gerekebilir. Daha fazla belleğe sahip bir bilgisayarda yeniden profil çalıştırmayı deneyin. Bu kural, disk belleği etkinlik miktarı kuralının D0017 üst eşiği aştığında tetikler.|  
|[DA0017: Yüksek oranda diske etkin bellek sayfalaması gerçekleşiyor.](../profiling/da0017-high-rates-of-paging-active-memory-to-disk.md)|Profil oluşturma çalışması boyunca görece yüksek oranda bir disk gelen ve giden etkin bellek Sayfalaması oluştu. Bu düzey genellikle Uygulama performansı etkileyebilir ve yanıt hızını oranlarda sayfalama. Algoritmalar düzeltilmesi tarafından bellek ayırmaları azaltmayı göz önünde bulundurun. Uygulamanızın bellek gereksinimlerini göz önünde bulundurun gerekebilir. Daha fazla belleğe sahip bir bilgisayarda yeniden profil çalıştırmayı deneyin.|



