---
title: Yük Testlerini Çözümlemek için Grafik Görünümü Göstergesini Kullanma
ms.date: 10/19/2016
ms.topic: conceptual
helpviewer_keywords:
- Load Test Analyzer, graphs view legend
- load tests, graphs view legend
ms.assetid: 0f6ba8e4-1343-419c-8a9f-240cf50efed7
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 4c29620cad3333144d65386e509339e2f5eccddf
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62562682"
---
# <a name="use-the-graphs-view-legend-to-analyze-load-tests"></a>Yük testlerini çözümlemek için grafik görünümü göstergesini kullanma

Yük Testi Çözümleyicisinin Grafik görünümü seçili grafik ile ilişkili her performans sayacı bilgileri görüntüleyen bir gösterge paneli içerir.

![Grafik görünümü göstergesi](../test/media/load_viewlegend.png)

[!INCLUDE [web-load-test-deprecated](includes/web-load-test-deprecated.md)]

Aşağıdaki bilgiler, gösterge içinde yer alır:

- **Grafikte Göster:** Belirtmek için onay kutularını kullanın olmadığını belirli bir sayaç çizgi gibi **kullanıcı yükü** veya **Hatası/sn**, grafikte çizilir. Çizgi grafikte çizilmesini istiyorsanız onay kutusunu seçin. Graftan çizim satırı kaldırmak için bir onay kutusunu temizleyin. Çizim satırı kaldırıldığında, sayaç istatistikleri göstergede gösterilecek devam eder.

- **Aralığı:** Bu sütun, performans sayacının y ekseni aralığını gösterir. Varsayılan olarak, bu değeri otomatik olarak örnek veri değişikliklerini aralığı olarak ayarlar. Otomatik olarak ayarlanan bir aralık her zaman maksimum değerden fazla olan 10 sonraki gücünü olacaktır. Bu, negatif katları içerir. Bir grafik çeşitli sayaçları, her biri farklı bir aralık içerebilir. Bu nedenle, y ekseni ile belirli bir aralık Etiketlenmedi ancak bunun yerine her bir sayacın toplam aralığının yüzde temsil eden 0-100 değerleri ile etiketlenir. Örneğin, 1000 bir aralığı olan bir sayaç için bir veri noktasının y ekseninde 60 600 sayacının değerine karşılık gelir.

    > [!NOTE]
    > Belirli bir değer aralığına kilitleyerek otomatik aralık değeri ayarı kapatabilirsiniz. Aralık kilitlendiğinde aralığını aşan değerleri grafiğin üst kısmında belirtilen en yüksek değer olarak görüntülenir. Kullanım **Çizim Seçenekleri** belirli bir değerin aralığı kilitlemek için iletişim kutusu.

- **Sayaç:** Adlı dört sütun **sayacı**, **örneği**, **kategori**, ve **bilgisayar** birlikte performans sayacı benzersiz olarak tanımlanabilmesi.

- **Renk:** **Renk** sütun çizilen satır performans sayacı için renk ve çizgi stilini gösterir. Kullanım **Çizim Seçenekleri** grafikteki bir performans sayacı rengini veya çizgi stilini değiştirme iletişim kutusu. **Çizim Seçenekleri** iletişim kutusu gösterge kısayol menüsünden kullanılabilir.

- **İstatistikleri:** **Min**, **Max**, **ortalama** ve **son** sütunlar performans sayacı ilgili istatistikleri gösterir. Bu değerler grafı görünür bölgesine görüntülenen verilere karşılık gelir. Örneğin, bir bölgesine yakınlaştırma göstergesi istatistikleri yalnızca yakınlaştırılmış alan için değerleri ücreti yansıtılır. "Son" sütunu en son tamamlanan örnekleme aralıkta performans sayacı değeridir.

    > [!NOTE]
    > Yük testi çalışırken son sütunu, yalnızca Yük Testi Çözümleyicisi'nin göstergede görüntüler.

     Daha fazla bilgi için [nasıl yapılır: Grafiğin bir bölgesine yakınlaştırmak](../test/how-to-zoom-in-on-a-region-of-the-graph-in-load-test-results.md).

Bir öğenin göstergede seçilmesi şunları yapar:

- Gösterge ve grafik kaldırılacak öğe sağlar. Ya da öğeyi sağ tıklatıp seçin **Sil**, veya basın **Sil** anahtarı.

- Grafiği çizilen satırda vurgulanır.

- Seçili öğe için verileri görüntülemek veri kılavuzu neden olur.

- Erişmenizi sağlar **Çizim Seçenekleri** sayaç için iletişim kutusu.

> [!TIP]
> Kullanabileceğiniz **grafik seçenekleri aşağı açılan** düğmesine **Yük Testi Çözümleyicisi** araç çubuğu ve select **Göstergeyi Göster** göstermek veya gizlemek için **gösterge** graf görünümünü ile ilişkili bölmesi.

## <a name="see-also"></a>Ayrıca bkz.

- [Nasıl yapılır: Grafiğin bir bölgesine yakınlaştırma](../test/how-to-zoom-in-on-a-region-of-the-graph-in-load-test-results.md)
- [Grafik görünümünde yük testi sonuçlarını çözümleme](../test/analyze-load-test-results-in-the-graphs-view.md)
