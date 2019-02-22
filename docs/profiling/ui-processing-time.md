---
title: UI işleme zamanı | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.cv.threads.timeline.uiprocessing
helpviewer_keywords:
- Concurrency Visualizer, UI Processing Time
ms.assetid: 0ddb05a3-8c6b-448b-8488-2751c1e5abcc
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 391b4582d03e32e738f0eade823326e72a662a43
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56615032"
---
# <a name="ui-processing-time"></a>UI işleme zamanı
Bu segmentlerde faaliyet zaman çizelgesi UI işleme sınıflandırılmış bir kez engelleme ile ilişkilidir. Bu, bir iş parçacığı Windows iletileri Pompalama veya diğer kullanıcı arabirimi (UI) iş yapılırken anlamına gelir. Bu süre boyunca, bir iş parçacığı UI işleme Concurrency Visualizer sayımını bir API'de engellendi. API'leri gibi `GetMessage()` ve `MsgWaitForMultipleObjects()` bu gruba girer.

 Önceden tanımlanmış hiçbir engelleme API belirlenirse, çağrı yığınları ve profil raporlarını gecikmesi temel nedenlerini belirlemek için gözden geçirin.

 UI işleme kategorisi, GUI uygulamalarının yanıtlama anlamanıza yardımcı olur ve kullanıcı Arabirimi yanıt hızı üzerinde bağlı uygulamalarda tercih edilir. Örneğin, bir uygulama kullanıcı Arabirimi iş parçacığında UI işleme % 100 sürede tutarsa büyük olasılıkla yanıt veriyor. Ancak, UI iş parçacığı diğer kategorilerde büyük miktarda zaman harcıyorsa, kök nedeni arayın ve iş parçacığı UI olmayan kategorilerindeki azaltma seçenekleri göz önünde bulundurun.

## <a name="see-also"></a>Ayrıca bkz.
- [İş Parçacıkları Görünümü](../profiling/threads-view-parallel-performance.md)