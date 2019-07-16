---
title: UI işleme zamanı | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.cv.threads.timeline.uiprocessing
helpviewer_keywords:
- Concurrency Visualizer, UI Processing Time
ms.assetid: 0ddb05a3-8c6b-448b-8488-2751c1e5abcc
caps.latest.revision: 10
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 4bbed9d8c4725b6bd497377d4a9dee22f2f8573d
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68145492"
---
# <a name="ui-processing-time"></a>UI İşleme Zamanı
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bu segmentlerde faaliyet zaman çizelgesi UI işleme sınıflandırılmış bir kez engelleme ile ilişkilidir. Bu, bir iş parçacığı Windows iletileri Pompalama veya diğer kullanıcı arabirimi (UI) iş yapılırken anlamına gelir. Bu süre boyunca, bir iş parçacığı UI işleme Concurrency Visualizer sayımını bir API'de engellendi. API'leri gibi `GetMessage()` ve `MsgWaitForMultipleObjects()` bu gruba girer.  
  
 Önceden tanımlanmış hiçbir engelleme API belirlenirse, çağrı yığınları ve profil raporlarını gecikmesi temel nedenlerini belirlemek için gözden geçirin.  
  
 UI işleme kategorisi, GUI uygulamalarının yanıt verme becerisini anlamak için önemlidir ve kullanıcı Arabirimi yanıt hızı üzerinde bağlı uygulamalarda tercih edilir. Örneğin, bir uygulama kullanıcı Arabirimi iş parçacığında UI işleme % 100 sürede tutarsa büyük olasılıkla çok yanıt veriyor. Ancak, UI iş parçacığı diğer kategorilerde büyük miktarda zaman harcıyorsa, kök nedeni arayın ve iş parçacığı UI olmayan kategorilerindeki azaltma seçenekleri göz önünde bulundurun.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [İş Parçacıkları Görünümü](../profiling/threads-view-parallel-performance.md)
