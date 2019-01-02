---
title: 'Nasıl Yapılır: İşaretlenmiş ikilileri yeniden Yerleştir | Microsoft Docs'
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
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: f8b50c5b76ea5b22bc9d734d32e433db1c7594d9
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53893084"
---
# <a name="how-to-relocate-instrumented-binaries"></a>Nasıl Yapılır: İşaretlenmiş ikilileri yeniden yerleştir

İzleme sırasında araştırmaları uygulama performansını ölçmek için ikili olarak eklenir. İşaretlenmiş ikilileri yeniden Yerleştir seçerek özgün ikilinin bir kopyası işaretlenir ve belirtilen konuma yerleştirin. Bu seçenek, özgün ikiliyi yeniden adlandırmak için profil oluşturucu istemiyorsanız yararlıdır. İkili konumlandırıldı değil, ikili dosya özgün sürümle üzerine yazılır.

## <a name="to-relocate-instrumented-binary"></a>İzleme eklenmiş ikili dışında yeniden konumlandırmakta

1. İçinde **performans Gezgini**performans oturumu sağ tıklayın ve ardından **özellikleri**.

2. İçinde **özellik sayfaları**, tıklayın **ikili** özellikleri.

3. Seçin **işaretlenmiş ikilileri yeniden Yerleştir** onay kutusu.

4. İzleme eklenmiş ikili dosya konumunu belirtin.

## <a name="see-also"></a>Ayrıca bkz.

[Performans oturumlarını yapılandırma](../profiling/configuring-performance-sessions.md)  
[VSInstr](../profiling/vsinstr.md)
