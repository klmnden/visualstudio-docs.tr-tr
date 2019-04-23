---
title: 'Nasıl yapılır: İşaretlenmiş ikilileri yeniden Yerleştir | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.performance.property.binaries
helpviewer_keywords:
- binaries, instrumented
- instrumentation, instrumented binaries
- instrumented binaries and relocating
- profiling tools, instrumented binaries
ms.assetid: 258f49e8-4b09-477e-a132-8fad685b66f4
caps.latest.revision: 23
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 00b39b91b0a776438199d1df3c212cb9fe40f338
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60048384"
---
# <a name="how-to-relocate-instrumented-binaries"></a>Nasıl yapılır: İşaretlenmiş ikilileri yeniden Yerleştir
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

İzleme sırasında araştırmaları uygulama performansını ölçmek için ikili olarak eklenir. İşaretlenmiş ikilileri yeniden Yerleştir seçerek özgün ikilinin bir kopyası işaretlenir ve belirtilen konuma yerleştirin. Bu seçenek, özgün ikiliyi yeniden adlandırmak için profil oluşturucu istemiyorsanız yararlıdır. İkili konumlandırıldı değil, ikili dosya özgün sürümle üzerine yazılır.  
  
 **Gereksinimler**  
  
- [!INCLUDE[vsUltLong](../includes/vsultlong-md.md)], [!INCLUDE[vsPreLong](../includes/vsprelong-md.md)], [!INCLUDE[vsPro](../includes/vspro-md.md)]  
  
### <a name="to-relocate-instrumented-binary"></a>İzleme eklenmiş ikili dışında yeniden konumlandırmakta  
  
1. İçinde **performans Gezgini**performans oturumu sağ tıklayın ve ardından **özellikleri**.  
  
2. İçinde **özellik sayfaları**, tıklayın **ikili** özellikleri.  
  
3. Seçin **işaretlenmiş ikilileri yeniden Yerleştir** onay kutusu.  
  
4. İzleme eklenmiş ikili dosya konumunu belirtin.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Performans oturumlarını yapılandırma](../profiling/configuring-performance-sessions.md)   
 [VSInstr](../profiling/vsinstr.md)
