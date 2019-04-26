---
title: 'Nasıl yapılır: İşaretlenmiş ikilileri yeniden Yerleştir | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.performance.property.binaries
helpviewer_keywords:
- binaries, instrumented
- instrumentation, instrumented binaries
- instrumented binaries and relocating
- profiling tools, instrumented binaries
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 96faf382145d7c4541f1fe66f872ad3622f64631
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62539312"
---
# <a name="how-to-relocate-instrumented-binaries"></a>Nasıl yapılır: İşaretlenmiş ikilileri yeniden yerleştir

İzleme sırasında araştırmaları uygulama performansını ölçmek için ikili olarak eklenir. İşaretlenmiş ikilileri yeniden Yerleştir seçerek özgün ikilinin bir kopyası işaretlenir ve belirtilen konuma yerleştirin. Bu seçenek, özgün ikiliyi yeniden adlandırmak için profil oluşturucu istemiyorsanız yararlıdır. İkili konumlandırıldı değil, ikili dosya özgün sürümle üzerine yazılır.

## <a name="to-relocate-instrumented-binary"></a>İzleme eklenmiş ikili dışında yeniden konumlandırmakta

1. İçinde **performans Gezgini**performans oturumu sağ tıklayın ve ardından **özellikleri**.

2. İçinde **özellik sayfaları**, tıklayın **ikili** özellikleri.

3. Seçin **işaretlenmiş ikilileri yeniden Yerleştir** onay kutusu.

4. İzleme eklenmiş ikili dosya konumunu belirtin.

## <a name="see-also"></a>Ayrıca bkz.

[Performans oturumlarını yapılandırma](../profiling/configuring-performance-sessions.md)
[Vsınstr](../profiling/vsinstr.md)
