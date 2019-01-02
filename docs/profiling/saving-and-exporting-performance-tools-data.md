---
title: Kaydetme ve dışarı aktarma performans araçları verilerini | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- performance tools, saving and exporting reports
ms.assetid: 2e9b28fe-3ed2-4e1d-b9cb-0a5e384380b0
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 9bb2020ff396eef3dd9dad4c0ed2e2fd015e0fd6
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53838378"
---
# <a name="save-and-export-performance-tools-data"></a>Performans araçları verilerini kaydetme ve dışarı aktarma
Bu makalede, kaydedin ve performans veri dosyalarını dışarı aktarma açıklanır.  
  
## <a name="how-to-save-performance-data-files-as-analyzed-report-files"></a>Nasıl Yapılır: Performans veri dosyalarını analiz edilmiş raporu dosyaları olarak kaydedin.  
 Profil oluşturma veri filtrelenmiş veya filtrelenmemiş görünümlerini kaydedebilirsiniz (. *Vsp*) analiz gibi dosyaları bildirir (. *vsps*) dosyaları. Analiz edilen raporu dosya, rapor görünümü penceresindeki görüntülenebilir ve önemli ölçüde özgün değerinden daha küçüktür. *vsp* dosya. Ancak, veriler için bir filtre uygulanamıyor. bir. *vsps* dosya. Tümleşik geliştirme ortamında (IDE) dosyayı açmaya gerek kalmadan performans Gezgini'nden bir analiz edilmiş raporu dosyası oluşturabilir veya açın ve filtreleme. *vsp* dosya ve sonuçları kaydedin.  
  
#### <a name="to-save-an-analyzed-performance-report-from-the-performance-explorer"></a>Performans Gezgini'nden bir analiz edilen performans raporu kaydetmek için  
  
1.  Altında **raporları**, analiz edin ve ardından istediğiniz profil oluşturma veri dosyasını sağ tıklatın **Kaydet analiz**.  
  
2.  İçinde **analiz verilerini Kaydet** iletişim kutusunda, dizini belirtin ve ardından dosya adını yazın.  
  
3.  Tıklayın **kaydedin.**  
  
#### <a name="to-save-an-analyzed-performance-report-from-the-report-view-window"></a>Rapor Görünümü penceresinden bir performans analiz raporu kaydetmek için  
  
1.  Profil oluşturma verilerinin açın (. *Vsp*) dosyasında rapor görünümü penceresi.  
  
2.  (İsteğe bağlı) Verilere filtre uygulayın. Daha fazla bilgi için [performans raporu Görünüm Filtresi](../profiling/performance-report-view-filter.md).  
  
3.  Tıklayın **Kaydet analiz** rapor görünümü penceresi araç çubuğu üzerinde.  
  
4.  İçinde **analiz verilerini Kaydet** iletişim kutusunda, dizini belirtin ve ardından dosya adını yazın.  
  
5.  Tıklayın **kaydedin.**  
  
## <a name="how-to-export-profiling-tools-reports-to-an-xml-or-csv-file"></a>Nasıl Yapılır: Profil oluşturma araçları raporları bir .xml veya .csv dosyasına dışarı aktarma  
 Bir veya daha fazla rapor görünümlerini verebilirsiniz bir. *vsp* dosya veya. *vsps* virgülle ayrılmış olarak veri dosyası veya bir XML dosyası profil oluşturma. Rapor Görünümü penceresi verileri dışarı veya rapor görünümlerini tüm veri dosyasından dışarı aktarabilirsiniz önce filtreleyebilirsiniz **performans Gezgini** penceresi.  
  
> [!NOTE]
>  Ayrıca, kopyalayın ve rapor görünümü penceresi seçili satırları sekmeyle ayrılmış değerler olarak yapıştırın.  
  
#### <a name="to-export-performance-reports-from-the-performance-explorer-window"></a>Performans Gezgini penceresinden performans raporları dışarı aktarmak için  
  
1.  İçinde **performans Gezgini**, raporu seçin ve ardından sağ tıklayıp **dışarı**.  
  
     **Dışarı aktarma raporu** iletişim kutusu görüntülenir.  
  
2.  Dışarı aktarmak istediğiniz rapor görünümleri seçin.  
  
3.  Altında **önek raporu ile**, eklemek için rapor adı öneki belirtin.  
  
4.  Altında **dışarı aktarılan rapor konumu**, dizini belirtin.  
  
5.  Altında **dışarı aktarılan raporun biçimi**, (virgülle ayrılmış) seçin (\*.csv\), veya XML verisi (\*.xml\).  
  
6.  Tıklayın **dışarı**.  
  
     Her rapor görünümü adlı ayrı bir dosyaya kaydedilir \<önek > _\<rapor görünümü adı >.\< CSV&#124;xml >  
  
#### <a name="to-export-performance-reports-from-the-report-view-window"></a>Rapor Görünümü penceresinden performans raporları dışarı aktarmak için  
  
1.  Açık. *vsp* dosyasında rapor görünümü penceresi.  
  
2.  (İsteğe bağlı) Verilere filtre uygulayın. Daha fazla bilgi için [performans raporu Görünüm Filtresi](../profiling/performance-report-view-filter.md).  
  
3.  Tıklayın **dışarı aktarma raporu** rapor görünümü penceresi araç çubuğu üzerinde.  
  
4.  Dışarı aktarmak istediğiniz rapor görünümleri seçin.  
  
5.  Altında **önek raporu ile**, eklemek için rapor adı öneki belirtin.  
  
6.  Altında **dışarı aktarılan rapor konumu**, dizini belirtin.  
  
7.  Altında **dışarı aktarılan raporun biçimi**, (virgülle ayrılmış) seçin (\*.csv), veya XML verisi (\*.xml).  
  
8.  Tıklayın **dışarı**.  
  
     Her rapor görünümü adlı ayrı bir dosyaya kaydedilir \<önek > _\<rapor görünümü adı >.\< CSV&#124;xml >  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Performans Gezgini](../profiling/performance-explorer.md)   
 [Performans araçları verilerini analiz etme](../profiling/analyzing-performance-tools-data.md)   
 [Performans veri dosyalarını karşılaştırma](../profiling/comparing-performance-data-files.md)   
 [VSPerfReport](../profiling/vsperfreport.md)
