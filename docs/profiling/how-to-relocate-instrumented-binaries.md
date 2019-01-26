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
ms.openlocfilehash: 394ac9b7f3a1a72485c8b435c776ca98c7c9fdb4
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54963469"
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
[VSInstr](../profiling/vsinstr.md)
