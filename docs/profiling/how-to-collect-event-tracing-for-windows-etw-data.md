---
title: 'Nasıl Yapılır: Olay izleme için Windows (ETW) verilerini toplama | Microsoft Docs'
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
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 8a619820cd2c6a3a884c7279d4eb9ffc9741619d
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53863661"
---
# <a name="how-to-collect-event-tracing-for-windows-etw-data"></a>Nasıl Yapılır: Olay izleme için Windows (ETW) verileri toplama

Olay izleme için Windows (ETW), profil oluşturucu günlük çekirdek veya uygulama tarafından tanımlanan olayları sağlayan verimli çekirdek düzeyinde izleme sistemidir. Olay sağlayıcısı'ndan toplanan verileri yalnızca kullanılarak görüntülenebilir /**Summary: ETW** seçeneği [VSPerfReport](../profiling/vsperfreport.md) komut satırı aracı. Performans sorunlarını uygulamada nerede oluştuğunu belirlemek için bu raporu kullanabilirsiniz.

> [!NOTE]
> Windows 8 ve Windows Server 2012'deki Gelişmiş güvenlik özellikleri Visual Studio profil oluşturucu bu platformlarda veri toplayan bir şekilde önemli değişiklikler gerekmiştir. UWP uygulamaları, ayrıca yeni toplama teknikleri gerektirir. Bkz: [Windows 8 ve Windows Server 2012 uygulamalarında performans araçları](../profiling/performance-tools-on-windows-8-and-windows-server-2012-applications.md).

## <a name="to-enable-event-trace-providers"></a>Olay izleme sağlayıcılarını etkinleştirme

1. İçinde **performans Gezgini**performans oturumu sağ tıklayın ve ardından **özellikleri**.

2. İçinde **özellik sayfaları**, tıklayın **Windows olayları** özellikleri.

3. İçinde **verileri toplamak için Select olayı izleme sağlayıcısı** listesinde, uygulamanızın profilini için kullanmak istediğiniz olay sağlayıcılarını seçin.

## <a name="see-also"></a>Ayrıca bkz.

[Performans oturumlarını yapılandırma](../profiling/configuring-performance-sessions.md)