---
title: İşaretçiler raporu | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- vs.cv.threads.report.markers
ms.assetid: 829ce099-172e-4c7e-bbd0-578b110c59bd
caps.latest.revision: 11
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: a1777f2f9fbd63ba659e74d0ce471962b29b15fd
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49811080"
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
>  İşaretçiler raporu 1.000 işaretleyicileri görüntüleyebilirsiniz. Tüm işaretleri görmek için bir CSV dosyasına tam raporu dışarı aktarın.



