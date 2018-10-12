---
title: 'DA0004: Yüksek işlemci kullanımı | Microsoft Docs'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- vs.performance.rules.DAHighProcessorUsage
- vs.performance.rules.DA0004
- vs.performance.DA0004
- vs.performance.4
ms.assetid: 2c4fb569-929e-4f1d-8c50-b590ee371351
caps.latest.revision: 17
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 681905b5d57991bb647335184a334e82cbec4df4
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49179225"
---
# <a name="da0004-high-processor-usage"></a>DA0004: Yüksek işlemci kullanımı
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Kural Kimliği | DA0004 |  
| Kategori | Profil oluşturma araçları kullanım |  
| Profil oluşturma yöntemlerini | İzleme örnekleme |  
| İleti | Tutarlı bir şekilde işlemci kullanım %75 ' dir. CPU bağımlı uygulamalar için örnekleme modu kullanmayı düşünün. |  
| Kural türü | Bilgi |  
  
 Örnekleme, .NET bellek ve kaynak çekişmesi yöntemleri kullanılarak profili, bu kural tetiklemek için en az 10 örnekleri toplamanız gerekir.  
  
## <a name="cause"></a>Sebep  
 İşlemci (CPU) kullanımı, profil oluşturma Araçlar yöntemini kullanarak toplanan veriyi önemli ölçüde yüksek. Örnekleme profili oluşturma yöntemi bir CPU profili oluşturma uygulama bağlı kullanmayı düşünün.  
  
## <a name="rule-description"></a>Kural Tanımı  
 Bu profil oluşturma çalışması süresince, işlemci (veya işlemciler) tutarlı bir şekilde çok meşgul. Yüksek CPU kullanımı, CPU bağımlı uygulama belirtebilirsiniz. İzleme eklenmiş profil genellikle CPU kullanım senaryoları araştırmak için en etkili yolu değildir. Yönergeler işlemci üzerinde yürütme zamanlarının çoğunu harcama uygulamaları profil oluştururken örnekleme genellikle daha etkilidir.  
  
## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?  
 Yeniden örnekleme yöntemini işlevi zamanlamaları gerektiren veya işlemci performans sorunlarını anlama, giriş/çıkış daha ilgi sürece yerine izleme metodunu kullanarak uygulamanızın profilini oluşturmanız göz önünde bulundurun.




