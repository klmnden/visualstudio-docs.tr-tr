---
title: Yük Testi Çözümleyicisinin Grafik Görünümünde Yük Testi Sonuçlarını Çözümleme
ms.date: 10/19/2016
ms.topic: conceptual
f1_keywords:
- vs.test.load.monitor.graph.view
helpviewer_keywords:
- graphs, analyzing load tests
- load tests, graphs in Load Test Viewer
- Load Test Viewer, graphs
- load tests, results graphs
- load tests, using graphs
- load test results, graphs
ms.assetid: 4a919cd8-541c-40ee-be3b-352fabc56140
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: c48fe67c8d52f962589c9f8628ff49f12f7770c5
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55970562"
---
# <a name="analyze-load-test-results-in-the-graphs-view-of-the-load-test-analyzer"></a>Yük Testi Çözümleyicisinin Grafik görünümünde yük testi sonuçlarını çözümleme

Bir yük testinin sonuçları, birkaç farklı bölmeler veri olarak görüntülenir.

[!INCLUDE [web-load-test-deprecated](includes/web-load-test-deprecated.md)]

Test sonuçlarını grafik şeklinde görüntülemek için seçin **grafikleri** üzerinde **yük testi** araç çubuğu. Her bir grafik en üstünde açılan listesinde grafik adıyla panelde görüntülenir. Başka bir grafiğe panelinde görüntülemek için listeden farklı bir grafik adı seçin.

En fazla dört grafik panelleri aynı anda görüntülenebilir. Farklı bir panel düzenleri kullanarak arasında geçiş yapabilirsiniz **panel düzenini** araç çubuğu düğmesi.

Birkaç yerleşik grafik sağlanır. Yerleşik kullanabileceğiniz grafikleri olduğu gibi veya bunları özelleştirebilirsiniz. Ayrıca, kendi grafiklerinizi oluşturabilirsiniz. Daha fazla bilgi için [nasıl yapılır: Grafiklerde sayaç ekleme ve silme](../test/how-to-add-and-delete-counters-on-graphs-in-load-test-results.md) ve [nasıl yapılır: Özel grafikler oluşturma](../test/how-to-create-custom-graphs-in-load-test-results.md).

## <a name="built-in-graphs"></a>Yerleşik grafikleri

Yük testi sonuçlarını analiz etmek kullanılabilen yerleşik grafikler aşağıdaki tabloda listelenmektedir.

|Grafik adı|Açıklama|
|-|-|
|Anahtar göstergesi|Kullanıcı yükü, aktarım hızı ve yanıt zamanı gibi performans sayaçları temel özelliklerini anlatan sınayın.|
|Test yanıt süresi|Çalıştırılacak testler süre miktarı hakkında veriler yararlanın.|
|Sayfa yanıt süresi|Web sayfaları için ortalama yanıt süresi, yükleme testi sırasında erişilir.|
|Test altındaki sistem|Üzerinde uygulama çalıştırmalarını test edilmesini bilgisayarlar hakkında bilgi. Bu, bellek kullanımı, işlemci, fiziksel disk, süreçleri hakkında veri içerir.<br /><br /> Varsayılan olarak, yalnızca kullanılabilir MBayt ve işlemci zamanı sayaçları toplanır.|
|Denetleyici ve aracılar|Yük testlerinin bilgisayarlar hakkında bilgi. Bu, bellek kullanımı, işlemci, fiziksel disk, süreçleri hakkında veri içerir.<br /><br /> Varsayılan olarak yalnızca kullanılabilir MBayt ve işlemci zamanı sayaçları toplanır.|
|İşlem yanıt süresi|Yük testi sırasında gerçekleştirilen işlemler için ortalama yanıt süresi.|

 Graf üzerinde hem çalışma zamanında hem de bir testi çalıştırdıktan sonra farklı sayaçlarını görüntüleyebilir.

> [!NOTE]
> Yalnızca yanıt süresi performans sayaçları için bir otomatik olarak üretilmiş bir yanıt süresi grafiği eklenebilir.

 Sayaç bilgileri hem de grafiğin altındaki grafikler göstergede görüntüler. Grafiğin bir bölümüne de yakınlaştırabilirsiniz. Daha fazla bilgi için [nasıl yapılır: Grafiğin bir bölgesine yakınlaştırmak](../test/how-to-zoom-in-on-a-region-of-the-graph-in-load-test-results.md).

## <a name="counters-displayed-in-graphs"></a>Grafiklerde Görüntülenen Sayaçlar

 Grafik görüntüleme *sayaçları*. Sayaçları testleri başına ikinci veya ortalama test süresi gibi bir yük testi sırasında toplanan verilere bakın. Sayaçları hakkında daha fazla bilgi için bkz. [sayaç kümelerini ve eşik kurallarını bilgisayarlar için bir yük testi içinde belirtme](../test/specify-counter-sets-and-threshold-rules-for-load-testing.md).

 Gösterge grafiklerde görüntülenen sayaçları için yük testi hakkında yararlı verileri çeşitli sütunları gösterir. Graftaki tüm verilerin görüntülenmesini devre dışı bırakmak için Göstergedeki satırındaki onay kutusunu temizleyin.

 Gösterge şu sütunları içerir:

|Sayaç|Sayaç adı|
|-|-|
|Örnek|Sayaç örneğinin adı.|
|Kategori|Sayacı kategori adı.|
|Bilgisayar|İçin sayaç toplandığı bilgisayarın adı.|
|Renk|Graftaki çizginin rengi.|
|Aralık|Bu sayaç için grafikteki 100 tarafından temsil edilen sayıyı belirtir. Örneğin, 10.000 üst değeri olan bir aralığı için 10.000 grafiğin üst kısmındaki 100 etiketi temsil eder.|
|Min.|Milisaniye cinsinden sayaç için minimum değeri gösterir.|
|Maks.|Sayaç milisaniye cinsinden en büyük değeri gösterir.|
|Ortalama|Milisaniye cinsinden sayacının ortalama değeri belirtir.|
|Son|Milisaniye cinsinden en son örnekleme aralığı sırasında sayaç değerini gösterir.|

## <a name="tasks"></a>Görevler

|Görevler|İlişkili konular|
|-|-|
|**Grafik gösterge kullanarak özelleştirin:** Grafikler, grafik ile ilişkili her performans sayacı için gösterge görüntüler bilgileri görüntüleyin. Gösterge, performans sayaçlarını kaldırmak, performans sayaçları grafiğe vurgulayın ve çizim seçenekleri özelleştirmek için kullanabilirsiniz.|-   [Yük testlerini çözümlemek için grafik görünümü göstergesini kullanma](../test/use-the-graphs-view-legend-to-analyze-load-tests.md)|
|**Grafiklerde sayaç görüntüle:** Grafik üzerinde sayaçları koyarak, bir yük testi sonuçları grafiği için farklı türlerde veri ekleyebilirsiniz.|-   [Nasıl Yapılır: Grafiklerde sayaç ekleme ve silme](../test/how-to-add-and-delete-counters-on-graphs-in-load-test-results.md)|
|**Grafiklerde yakınlaştırma:** Bir yük testi tamamlandıktan sonra yakınlaştırmak ve kaydırmak için grafiğin bir bölgesine yakınlaştırma çubukları kullanabilirsiniz. Yakınlaştırma tarafından ince ayrıntılı olarak yük testi sırasında oluşturulan verileri inceleyebilirsiniz.|-   [Nasıl Yapılır: Grafiğin bir bölgesine yakınlaştırma](../test/how-to-zoom-in-on-a-region-of-the-graph-in-load-test-results.md)|
|**Kutucuk grafikler:** Yük testi sonuç grafikleri herhangi çeşitli desenlerden düzenleyebilirsiniz. En fazla dört grafikleri döşeme.||
|**Özel grafikler oluşturma:** Yük testi sonuçları hakkında belirli bilgi görüntüleyen grafikleri tasarlayabilirsiniz. Özel bir grafik, graf görüntüleyen yük testi sayacı belirterek tasarlayın.|-   [Nasıl Yapılır: Özel grafikler oluşturma](../test/how-to-create-custom-graphs-in-load-test-results.md)|
|**Graftaki performans sayaçları verilerini dışarı aktarın:** Graf verileri kullanarak Microsoft Excel'e dışarı aktarabilirsiniz **grafik verilerini Excel'e dışarı aktar** düğmesini **Yük Testi Çözümleyicisi** içerikteyken araç **grafikleri** görünümü.||

## <a name="related-tasks"></a>İlişkili görevler

 [Yük testi sonuçlarını ve hatalarını Tablo görünümünde çözümleyin](../test/analyze-load-test-results-and-errors-in-the-tables-view.md)

 [Nasıl yapılır: Erişim yük testi sonuçlarını çözümleme](../test/how-to-access-load-test-results-for-analysis.md)

 [Yük testi sonuçlarını çözümleme](../test/analyze-load-test-results-using-the-load-test-analyzer.md)

## <a name="see-also"></a>Ayrıca bkz.

- [Nasıl yapılır: Grafiklerde sayaç ekleme ve silme](../test/how-to-add-and-delete-counters-on-graphs-in-load-test-results.md)
- [Nasıl yapılır: Özel grafikler oluşturma](../test/how-to-create-custom-graphs-in-load-test-results.md)
- [Nasıl yapılır: Grafiğin bir bölgesine yakınlaştırma](../test/how-to-zoom-in-on-a-region-of-the-graph-in-load-test-results.md)