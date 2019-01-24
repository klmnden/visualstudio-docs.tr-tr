---
title: 'DA0501: Profil oluşturulan işlem tarafından ortalama CPU kullanımı. | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
f1_keywords:
- vs.performance.rules.DA0501
- vs.performance.DA0501
- vs.performance.501
ms.assetid: b01946b4-75e3-47d5-a1a1-cebfae66a3af
caps.latest.revision: 12
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 1462ac73e599b870f015a02998c069f7613be0ae
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54771960"
---
# <a name="da0501-average-cpu-consumption-by-the-process-being-profiled"></a>DA0501: Profil oluşturulan işlem tarafından ortalama CPU kullanımı.
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Kural Kimliği | DA501 |  
| Kategori | Kaynak İzleme |  
| Profil oluşturma yöntemi | Tüm |  
| İleti | Ortalama CPU kullanımının profili oluşturuluyor işlem. |  
| Kural türü | Bilgi |  
  
 Örnekleme, .NET bellek ve kaynak çekişmesi yöntemleri kullanılarak profili, bu kural tetiklemek için en az 10 örnekleri toplamanız gerekir.  
  
## <a name="rule-description"></a>Kural Tanımı  
 Bu ileti bir işlemci yönergeleri uygulamadan çalıştırmakla meşgul olduğu sürenin yüzdesini bildirir. Bildirilen değer profil oluşturulan işlem etkin olduğu tüm ölçüm aralıklarında bir ortalamadır. Değeri, birden çok işlemcili bir makinede % 100'den daha büyük olabilir.  
  
## <a name="how-to-use-rule-data"></a>Kural verileri kullanma  
 Kural değeri, farklı sürümlerin performans veya programın yapıları karşılaştırmak veya farklı test senaryoları altında uygulama performansını anlamak için kullanın.
