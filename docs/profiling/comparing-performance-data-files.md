---
title: Performans veri dosyalarını karşılaştırma | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- profiling tools, comparing profiling tools report files
- profiling tools reports, comparing
ms.assetid: e6fda144-f21d-4912-9d16-1b8d3555a210
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: e75a5da65343a08f0c94be27837e70f4078192d5
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53893055"
---
# <a name="compare-performance-data-files"></a>Performans veri dosyalarını karşılaştırma
Profil oluşturma araçları veri dosyalarını karşılaştırma işlevi sayesinde iki rapor dosyası seçin (. *Vsp* ya. *vsps*) dosyaları ve farkları, performans gerilemeleri ve bir profil oluşturma oturumundan diğerine oluştu iyileştirmeleri gösteren bir rapor oluşturur.  
  
 Veri dosyalarını Karşılaştırma raporu [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] profil oluşturma araçları, başka bir veri dosyasındaki bir temel analiz sonuçları için bir profil oluşturma veri dosyasını içinde analiz sonuçlarını karşılaştırır. Her iki veri dosyalarını aynı profil oluşturma yöntemini kullanarak oluşturulmuş olmalıdır. Analiz edilen Karşılaştırma raporu olarak kaydedilmiş bir. *vsps* dosya.  
  
 Değiştirilen verileri içeren bir tablo görünümü karşılaştırma rapor görünümünü sunar. Tablo, delta veya taban çizgisinden Değiştir sunar. Delta eski değeri, temel değeri ve sonuç değeri arasındaki farkı yeni analiz belirleyerek hesaplanır.  
  
 Profil Oluşturucu veri karşılaştırmalarını temel işlevler kodu, uygulama, çizgiler, yönerge işaretçileri (IP) ve türleri modüllerde alabilir.  
  
 Profil oluşturma verisi karşılaştırma için kullanılabilir olan sütunları görüntülenen bilgileri içerir. Bu sütun adları tanımları için bkz: [performans raporu görünümleri](../profiling/performance-report-views.md).  
  
 Bir eşiği gürültüsünü azaltmak ve değişip değişmediğini satır karşılaştırma Tablo görünümünde herhangi bir veri filtrelemek için belirli bir miktarda ayarlanabilir.  
  
## <a name="in-this-section"></a>Bu bölümde  
 [Nasıl yapılır: Performans veri dosyalarını karşılaştırma](../profiling/how-to-compare-performance-data-files.md)