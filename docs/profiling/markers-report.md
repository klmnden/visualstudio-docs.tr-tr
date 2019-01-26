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
ms.openlocfilehash: 726dc50032cd276c23f9fc3f988a8553e23bde17
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54924969"
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