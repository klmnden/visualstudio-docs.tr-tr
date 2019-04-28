---
title: 'Nasıl yapılır: Performans veri dosyalarını karşılaştırma | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vsperf.choosediffbinaries
helpviewer_keywords:
- profiling tools, how to compare profiler result files
- profiler result files, how to compare
ms.assetid: 1905b45d-c6b3-43c8-87b1-1aee734f37f9
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 101512cb15bca022e5e3b473c84bd433a7269e15
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62973909"
---
# <a name="how-to-compare-performance-data-files"></a>Nasıl yapılır: Performans veri dosyalarını karşılaştırma
İki farklı profil oluşturucu veri dosyalarının sonuçları karşılaştırmak (. *Vsp* veya. *vsps*) bir karşılaştırması ("fark") oluşturarak, rapor veya görüntüleyin. Farklar, performans gerilemeleri ve bir profil oluşturma oturumundan diğerine oluştu iyileştirmeleri karşılaştırmasını gösterir.

 Fark rapor verilerin tablo bir görünümünü sunar. Tablo, delta veya taban çizgisinden Değiştir sunar. Bu, eski değeri, temel değeri ve sonuç değeri arasındaki farkı yeni analiz belirleyerek hesaplanır.

 Profil Oluşturucu veri karşılaştırmalarını temel işlevler kodu, uygulama, çizgiler, yönerge işaretçileri (IP) ve türleri modüllerde alabilir.

 Bir eşiği gürültüsünü azaltmak ve Tablo görünümünde değişip değişmediğini satırların herhangi bir veri filtrelemek için belirli bir miktarda ayarlanabilir.

### <a name="to-create-comparison-file-view-for-a-project-in-performance-explorer"></a>Performans Gezgini içinde bir proje için karşılaştırma dosya görünümü oluşturmak için

1. İçinde **performans Gezgini**altında **raporları**seçin. *Vsp* veya. *vsps* taban çizgisi değerlerini karşılaştırma için kullanmak istediğiniz rapor dosyası.

2. Seçin. *vsp* veya. *vsps* rapor karşılaştırmak istediğiniz dosyaları.

3. Seçilen dosyalardan birine sağ tıklayın ve ardından **karşılaştırma raporları**.

### <a name="to-compare-values"></a>Değerleri karşılaştırmak için

1. Seçin **Karşılaştırma raporu** rapor görünümü penceresindeki sekmesi.

2. İçinde **tablo** aşağı açılan listesinde, işlev veya karşılaştırmak için modülleri seçin.

3. İçinde **sütun** aşağı açılan listesinde, karşılaştırmak istediğiniz değer seçin.

4. (isteğe bağlı) İçin bir değer yazın **eşiği**.

5. **Uygula**'ya tıklayın.

### <a name="to-compare-report-files"></a>Rapor dosyalarını karşılaştırma

1. Üzerinde **Çözümle** menüsünde **Performans raporlarını Karşılaştır**.

2. İçinde **seçin analiz dosyaları karşılaştırma** penceresinde, Gözat ve Seç **ana hat dosyası** analiz dosyası (. *Vsp* veya. *vsps*) ve **karşılaştırma dosyası** (. *Vsp* veya. *vsps*).

3. **Tamam**'ı tıklatın.