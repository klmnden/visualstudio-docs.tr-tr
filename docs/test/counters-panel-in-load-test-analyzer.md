---
title: Visual Studio'da yük testlerini çözümlemek için Sayaçlar paneli
ms.date: 10/19/2016
ms.topic: conceptual
helpviewer_keywords:
- load tests, counters panel
ms.assetid: e1a388d7-5d33-4631-931a-5653ac4aefdc
author: gewarren
ms.author: gewarren
manager: douge
ms.prod: visual-studio-dev15
ms.technology: vs-ide-test
ms.openlocfilehash: 229097b12e5b32e6be6af6b9614a628346780063
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49921489"
---
# <a name="use-the-counters-panel-in-graphs-view-and-tables-view"></a>Grafikler görünümünde ve Tablolar görünümünde Sayaçlar panelini kullanma

**Sayaçları** bir yük testi çalışırken ya da bir yük testi sonucu çözümlerken paneli grafikler görünümünde ve Tablolar görünümünde Yük Testi Çözümleyicisi'nde görünür. Daha fazla bilgi için [Çözümle yük testi sonuçlarını grafik görünümünde](../test/analyze-load-test-results-in-the-graphs-view.md), [yük testi sonuçlarını ve hatalarını Tablo görünümünde çözümlemek](../test/analyze-load-test-results-and-errors-in-the-tables-view.md) ve [nasıl yapılır: erişim yük testi sonuçlarını analiz](../test/how-to-access-load-test-results-for-analysis.md).

**Sayaçları** paneli yapılandırılmış bir yük testi sırasında toplanan performans sayaçlarının tümünü görünümünü görüntüler. Göster veya gizle **sayaçları** seçerek paneli **Sayaçlar panelini Göster** üzerinde **Yük Testi Çözümleyicisi** araç çubuğu.

Sayaçlar ve yaprak düğümlerin çizilebilir performans sayaç örnekleri nerede bir ağaç yapısı içinde düzenlenmiştir.

Sayaçlar paneli aşağıdaki özellikleri sağlar:

-   Eşik ihlali bilgileri iletişim kurar.

-   Sayaçları grafiğe aktarmak için seçimi.

-   Tüm performans sayaçlarını yapılandırılmış ağaç görünümünü aşağıdaki birincil dallar ile bir yük testi sırasında toplanan:

    -   **Genel:** tüm yük testi ve her test aracısı için Özet performans sayacı verilerini içerir.

    -   **Senaryo adı:** performans sayacı ağacında yük testi senaryo adları ile etiketlenmiş dalları, belirli bir yük testi senaryosu ile ilişkili tüm yük test sayaç örnekleri içerir. Çoğu yük testi sayacı senaryo dalında iç içe yer.

         Bir senaryo dal web performans testi düğümleri içerir. Sayfalar, istekler ve işlem web performans testi düğümleri içeren düğüm. Bu yapı herhangi bir yaprak düğüm grafiğe eklenen bir performans sayacıdır.

    -   **Bilgisayarlar:** bilgisayara göre gruplandırılan tüm olmayan yük testi sayacı örneklerini içerir. Bilgisayarlar dalı, şu anda seçilmiş test ayarlarının roller bölümünde belirtilen yük test denetleyicisi ile ilişkili olan her bilgisayar için bir düğüm içerir. Daha fazla bilgi için [Test denetleyicileri ve test aracılarını](configure-test-agents-and-controllers-for-load-tests.md).

         Her bilgisayar düğümü bu bilgisayardan toplanan performans sayacı kategorileri kümesi içerir. Sayaç kategorileri içerir ve performans sayacı örneği adları sayaçlar içerir.

    -   **Hata:** yük testi sırasında algılanan tüm hataları içerir. Hata düğümü birkaç alt kategori hata düğümü içerir. Alt kategoriler, çeşitli hatalar, örneğin, özel durumlar ve HTTP hataları özgüdür.

### <a name="scenario-name-node-in-counters-panel"></a>Sayaçlar paneli Senaryo adı düğümü

|Sayaçlar paneli|Açıklama|
|-|-|
|![Bölmenin Senaryo adı düğümü sayaç](../test/media/ltest__namenode.png)|1. Yük testi Senaryo1 ile ilişkili tüm performans sayaçlarını bu düğüm altında görünür.<br />2. Tüm testler bir senaryonun senaryo düğümün altında bulunur. Test adı belirtir.<br />3. Bir test düğümü altındaki yaprak düğümleri sayaç için örnek adını test adı olduğu yük testi test çalışması, sayaçlarıdır.<br />4. Tüm bir web performans testi dalla ilişkili test sayfası sayaç örnekleri yükleyin. Bu düğümde oturum açma (Raporlama adı) yük testinin Scenario1 IBuyBrowse web başarım testinde GET sayfayla ilişkili örnekleri Adım yük testi burada bulunur.<br />5. Yaprak düğümleri sayfasında düğümü altında yük testi sayfa sayaçlarıdır.<br />6. Tüm test istekleri sayaç örnekleri bir web performans testi ile ilişkili bir web performans test dalıyla yükleyin. Bu düğüm tüm örnekleri oturum açma (Raporlama adı) yük testi burada yer alan Scenario1 o IBuyBrowse web başarım testinde GET isteği ile ilişkili istek.<br />7. Yaprak düğümleri isteği düğümü altında yük testi isteği sayaçlarıdır.<br />8. Bir web performans testi ile ilişkili tüm yük testi işlem örnekleri, bir web performans testi dalında yer alır. Bu düğüm tüm işlem örnekleri yük testinin Scenraio1 IBuyBrowse web başarım testinde, adlandırılmış Transaction1 burada bulunur bir işlem ile ilişkilendirin.<br />9. Yaprak düğümleri işlem düğümü altında yük testi işlem sayaçlarıdır.<br />10. Birim test düğümü.|

## <a name="tasks"></a>Görevler

|Görevler|İlişkili konular|
|-|-----------------------|
|**Daha fazla performans sayaçlarının Grafik görünümünde bir grafik ekleyin:** içinde **sayaçları** panelinde ekleyebileceğiniz farklı türlerde veri bir yük testi grafiği için grafik üzerinde daha fazla performans sayaçlarını ekleyerek.|-   [Nasıl yapılır: grafiklerde sayaç ekleme ve silme](../test/how-to-add-and-delete-counters-on-graphs-in-load-test-results.md)|
|**İhlal edildi yük testi içinde belirtilen eşikler analiz:** **sayaçları** paneli, tablolar ve grafikler daha fazla analiz için daha sonra ekleyebilirsiniz Eşik ihlallerini temsil eden bir simge görüntüler.|-   [Nasıl yapılır: Sayaçlar panelini kullanılarak Eşik ihlallerini çözümleme](../test/analyze-threshold-rule-violations-in-load-tests.md)|
|**Yük testi çalıştırması sırasında algılanan hataları çözümleyin:** **sayaçları** paneli, hata kategorileri ve alt kategorileri gibi grafikler için hata eklemek için kullanabileceğiniz HTTP hataları içeren bir hata düğümü içerir Daha fazla analiz.|-   [Nasıl yapılır: Sayaçlar panelini kullanarak hataları çözümleme](../test/how-to-analyze-errors-using-the-counters-panel.md)|

## <a name="performance-counter-sampling-interval-considerations"></a>Performans sayacı örnekleme aralığı hakkında önemli noktalar

İçin bir değer seçin **örnek hızı** özelliği yük testinde çalışma ayarları yük testinizin uzunluğuna göre. Varsayılan değer olarak beş saniye gibi küçük bir örnekleme hızı yükleme testi sonuçları veritabanı daha fazla alan gerektirir. Daha uzun yük testleri için örnek hızı artırmak topladığınız veri miktarını azaltır. Daha fazla bilgi için [nasıl yapılır: örnek hızı belirtme](../test/how-to-specify-the-sample-rate-for-a-load-test.md).

Örnek hızlara ait bazı Kılavuzlar şunlardır:

|Yük testi süresi|Önerilen örnek hız|
|-|-----------------------------|
|\< 1 saat|5 saniye|
|1 - 8 saat|15 saniye|
|8 - 24 saat|30 saniye|
|> 24 saat|60 saniye|

## <a name="considerations-for-including-timing-details-to-collect-percentile-data"></a>Yüzdelik veri toplamak için zamanlama ayrıntılarını da dahil olmak üzere dikkat edilmesi gereken noktalar

Yük testi adlı Düzenleyicisi'nde çalışma ayarlarında bir özelliği yoktur **Zamanlama Ayrıntıları Deposu**. Varsa **Zamanlama Ayrıntıları Deposu** özelliği etkinse, sonra Yük testi sırasında her bir bireysel test, hareket ve sayfa yürütülme zamanı yükleme testi sonuçları deposunda depolanır. Bu 90'ıncı ve 95 yüzdelik veri Yük Testi Çözümleyicisi'nde testler, hareketler ve sayfalar tablolarında gösterilmesini sağlar.

Etkinleştirmek için iki seçeneğiniz vardır **Zamanlama Ayrıntıları Deposu** çalıştırma ayarları özellikleri özelliğinde: **StatisticsOnly** ve **AllIndividualDetails**. Her iki seçenek tüm bireysel testler, sayfalar ve hareketler zamanlanır ve bireysel zamanlama verisinden yüzdelik veri hesaplanır. Fark **StatisticsOnly** seçeneğini yüzdelik veri hesaplanır hemen sonra bireysel zamanlama verileri depodan silinir. Bu, zamanlama ayrıntılarını kullandığınızda depodaki gerekli alanı miktarını azaltır. Ancak, İleri düzey kullanıcılar SQL araçları kullanarak zamanlama ayrıntı verilerini farklı yollarla işlemek isteyebilirsiniz. Bu durum söz konusuysa **AllIndividualDetails** seçeneği kullanılmalıdır, böylece zamanlama ayrıntı verileri bu işlem için kullanılabilir. Ayrıca, özelliği ayarlamanız **AllIndividualDetails**, kullanan sanal kullanıcı etkinliğini çözümleyebilirsiniz **sanal kullanıcı etkinliği** grafik Yük Testi Çözümleyicisi'ndeki sonra Yük testi çalıştırma tamamlandı. Daha fazla bilgi için [Ayrıntılar görünümünde sanal kullanıcı etkinliğini çözümleme](../test/analyze-load-test-virtual-user-activity-in-the-details-view.md).

Zamanlama ayarları verisini saklamak için yük testi sonuçları deposunda gereken alan miktarı, özellikle daha uzun süre çalışan yük testleri için büyük olabilir. Bu veriler yük testi yürütmesini bitirene kadar yükleme testi aracısında depolanır çünkü Ayrıca, yük testi sonuçları deposu yük testinin sonunda bu verileri depolamak için uzun zamandır. Yük testi çalışmayı tamamladıktan sonra verilerin depoya saklandığı. Varsayılan olarak, **Zamanlama Ayrıntıları Deposu** özelliği etkin hale getirilir. Bu test ortamınızın sorunu ise, ayarlamak isteyebilirsiniz **Zamanlama Ayrıntıları Deposu** için **hiçbiri**.

Daha fazla bilgi için [nasıl yapılır: zamanlama ayrıntıları depolama özelliğini belirtme](../test/how-to-specify-the-timing-details-storage-property-for-a-load-test.md).

## <a name="see-also"></a>Ayrıca bkz.

- [Yük testi sonuçlarını çözümleme](../test/analyze-load-test-results-using-the-load-test-analyzer.md)