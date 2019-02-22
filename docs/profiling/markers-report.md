---
title: İşaretçiler raporu | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.cv.threads.report.markers
ms.assetid: 829ce099-172e-4c7e-bbd0-578b110c59bd
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 765fd6db153f30ad312ea873919a20e5f885b158
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56613888"
---
# <a name="markers-report"></a>İşaretçiler Raporu
İşaretçiler raporu görüntülenen zaman çerçevesi içinde işaretlerinin listeler.  Yatay yakınlaştırma veya kulvarları, gizleme görünmesini veya kaybolmasını işaretçileri neden olabilir. Rapor, her işaret hakkındaki bu bilgileri içerir:

- Bu, göreli izleme başlangıcını başladığında süre.

- Süresi. Süre bayrakları ve iletileri için sıfır çünkü bir anı temsil ederler.

- Oluşturulan iş parçacığı kimliği.

- Bu oluşturulan olay izleme için Windows (ETW) sağlayıcısı.

- İşaret serisi içinden yazılmıştır.

- Olayların ait kategori.

- Kendi önem düzeyi.

- (Aralık, bayrağı veya ileti) türü.

- Neyin temsil üst düzey açıklaması

  Seçin **dışarı** düğmesini işaretçiler raporu CSV dosyası olarak kaydedin. Diğer uygulamalar veya Araçlar CSV dosyasındaki verileri kullanabilirsiniz.

> [!NOTE]
>  İşaretçiler raporu 1.000 işaretleyicileri görüntüleyebilirsiniz. Tüm işaretleri görmek için bir CSV dosyasına tam raporu dışarı aktarın.