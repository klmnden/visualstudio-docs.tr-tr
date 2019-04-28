---
title: 'Nasıl yapılır: Olay izleme için Windows (ETW) verilerini toplama | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.performance.property.events
helpviewer_keywords:
- event trace providers, performance tools
- profiling tools, event trace providers
- performance tools, enabling event trace providers
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: d9734c75f078380649009d10da13ed8c926e5e16
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62973870"
---
# <a name="how-to-collect-event-tracing-for-windows-etw-data"></a>Nasıl yapılır: Olay izleme için Windows (ETW) verileri toplama

Olay izleme için Windows (ETW), profil oluşturucu günlük çekirdek veya uygulama tarafından tanımlanan olayları sağlayan verimli çekirdek düzeyinde izleme sistemidir. Olay sağlayıcısı'ndan toplanan verileri yalnızca kullanılarak görüntülenebilir /**Summary: ETW** seçeneği [VSPerfReport](../profiling/vsperfreport.md) komut satırı aracı. Performans sorunlarını uygulamada nerede oluştuğunu belirlemek için bu raporu kullanabilirsiniz.

> [!NOTE]
> Windows 8 ve Windows Server 2012'deki Gelişmiş güvenlik özellikleri Visual Studio profil oluşturucu bu platformlarda veri toplayan bir şekilde önemli değişiklikler gerekmiştir. UWP uygulamaları, ayrıca yeni toplama teknikleri gerektirir. Bkz: [Windows 8 ve Windows Server 2012 uygulamalarında performans araçları](../profiling/performance-tools-on-windows-8-and-windows-server-2012-applications.md).

## <a name="to-enable-event-trace-providers"></a>Olay izleme sağlayıcılarını etkinleştirme

1. İçinde **performans Gezgini**performans oturumu sağ tıklayın ve ardından **özellikleri**.

2. İçinde **özellik sayfaları**, tıklayın **Windows olayları** özellikleri.

3. İçinde **verileri toplamak için Select olayı izleme sağlayıcısı** listesinde, uygulamanızın profilini için kullanmak istediğiniz olay sağlayıcılarını seçin.

## <a name="see-also"></a>Ayrıca bkz.

[Performans oturumlarını yapılandırma](../profiling/configuring-performance-sessions.md)