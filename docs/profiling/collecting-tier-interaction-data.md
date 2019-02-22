---
title: Katman etkileşim verileri toplama | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.performance.property.tierinteraction
helpviewer_keywords:
- Profiling Tools,ADO.NET profiling
- tier interaction profiling method
- Profiling Tools,tier-interaction method
- ADO.NET performance profiling
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: fcdab1fcb776a729d00a143dfc318053b74c5cf5
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56600122"
---
# <a name="collect-tier-interaction-data"></a>Katman etkileşim verileri toplama

Katman etkileşim profili oluşturma, ADO.NET Hizmetleri aracılığıyla veritabanları ile iletişim kuran çok katmanlı uygulamaların işlevlerini yürütme sürelerini hakkında ek bilgi sağlar. Verileri yalnızca zaman uyumlu işlev çağrıları için toplanır.

**Visual Studio sürümleri**

Katman etkileşimli profil oluşturma verileri, herhangi bir Visual Studio sürümünü kullanarak toplanabilir. Ancak, yalnızca Visual Studio Enterprise'da katman etkileşimli profil oluşturma veri görüntülenebilir.

**Windows 8 ve Windows Server 2012**

Masaüstü uygulamalarını Windows 8 ve Windows Server 2012 uygulamalar üzerinde katman etkileşim verileri toplamak için Araçlar yöntemini kullanmanız gerekir. UWP uygulamaları için katman etkileşim verileri toplanamıyor. Bkz: [Windows 8 ve Windows Server 2012 uygulamalarında performans araçları](../profiling/performance-tools-on-windows-8-and-windows-server-2012-applications.md). Desteklenen diğer Windows sürümünde tüm profil oluşturma yöntemlerini katman etkileşim verileri içerebilir.

**Performans Sihirbazı**

Performans Sihirbazı bir hata nedeniyle, bir profil oluşturma yürütmesine katman etkileşim verileri toplama seçeneği performans Gezgini'nden eklemelisiniz. Ayrıca proje, yürütülebilir dosya veya Web performans Gezgini hedef düğüme eklemeniz gerekir.

## <a name="to-add-tier-interaction-data-to-a-profiling-run-by-using-the-performance-session-property-pages"></a>Bir performans oturumu özellik sayfaları kullanarak profil oluşturma için katman etkileşim verileri ekleme

1. Performans Gezgini'nde **özellikleri** bağlam menüsünden.

2. Seçin **katman etkileşimleri** sayfasında ve ardından **Katman etkileşimi profili oluşturmayı etkinleştir** onay kutusu.

3. Performans Gezgini içinde seçin **hedefleri** düğümünü ve ardından Proje, yürütülebilir dosya veya profil oluşturmak istediğiniz web sitesi belirtin.

## <a name="see-also"></a>Ayrıca bkz.

[Katman etkileşimleri görünümü](../profiling/tier-interactions-view.md)