---
title: İşaretçiler raporu | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.cv.threads.report.markers
ms.assetid: 829ce099-172e-4c7e-bbd0-578b110c59bd
caps.latest.revision: 11
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 97705dab6f11ca0d9d51c27bfc56d315b454bc52
ms.sourcegitcommit: 75807551ea14c5a37aa07dd93a170b02fc67bc8c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/12/2019
ms.locfileid: "64837705"
---
# <a name="markers-report"></a>İşaretçiler Raporu
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

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
> İşaretçiler raporu 1.000 işaretleyicileri görüntüleyebilirsiniz. Tüm işaretleri görmek için bir CSV dosyasına tam raporu dışarı aktarın.
