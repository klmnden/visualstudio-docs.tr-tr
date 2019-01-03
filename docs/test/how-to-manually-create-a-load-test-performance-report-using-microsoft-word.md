---
title: Yük testi başarım raporunu Microsoft Word'ü kullanarak oluşturma
ms.date: 10/19/2016
ms.topic: conceptual
helpviewer_keywords:
- load tests, reporting
- load tests, creating Word reports
ms.assetid: 3b864c75-2699-48c1-a2b4-9651f108c267
author: gewarren
ms.author: gewarren
manager: douge
ms.prod: visual-studio-dev15
ms.openlocfilehash: 32cdb45a57b218645e6f9eaa84c5e198aeacc620
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53987647"
---
# <a name="how-to-manually-create-a-load-test-performance-report-using-microsoft-word"></a>Nasıl Yapılır: Microsoft Word kullanılarak bir yük testi başarım raporunu el ile oluşturma

Grafik görünümü ve yük testi sonuçlarını Özet görünümü verileri yapıştırarak Microsoft Word yük testi raporları el ile oluşturabilirsiniz. Özet görünümü gösterilir ve grafikler görünümünde verileri, HTML biçiminde kopyalandığında uygulanır.

[!INCLUDE [web-load-test-deprecated](includes/web-load-test-deprecated.md)]

> [!TIP]
> Tablolar görünümü ve Microsoft Word için ekran Ayrıntılar görünümünü görüntüleri düz metni kopyalayın, ancak HTML biçiminde uygulanmaz ve biçimlendirme ve düzenleme ek gerektirir.

> [!TIP]
> Otomatik olarak düzenlenmiş Microsoft Excel raporları da oluşturabilirsiniz. Daha fazla bilgi için [nasıl yapılır: Kullanarak Microsoft Excel kullanarak yük testi başarım raporları oluşturma](../test/how-to-create-load-test-performance-reports-using-microsoft-excel.md).

## <a name="copy-summary-view-data"></a>Özet görünümü verilerini kopyalama

1.  İçinde **yük testi sonuçları**, Özet görünümü şu anda görüntülenmiyorsa tıklayın **Özet** araç.

2.  Özet görünümünde, sağ tıklayıp **Tümünü Seç**.

3.  Özet görünümünde, sağ tıklayıp **kopyalama**. Bu, Özet görünümü verisini HTML biçiminde panoya olarak işler.

4.  Microsoft Word içinde Özet görünümü verileri istediğiniz yere yapıştırın.

5.  Artık, değiştirme, biçimlendirme ve raporlama ihtiyaçlarınızı karşılayacak şekilde kopyalanan içerik yönlerini silebilirsiniz.

## <a name="copy-graph-view-data"></a>Graf görünümü verilerini kopyalama

1.  İçinde **yük testi sonuçları**, görünüm şu anda görüntülenmez, grafik seçerseniz **grafikleri** araç.

2.  (İsteğe bağlı) Aşağıdaki çizimde gösterildiği gibi Microsoft Word belgesi için kopyalamak istediğiniz belirli grafik yakınlaştırın. Daha fazla bilgi için [nasıl yapılır: Grafiğin bir bölgesine yakınlaştırmak](../test/how-to-zoom-in-on-a-region-of-the-graph-in-load-test-results.md).

     ![Graf görünümü yakınlaştırma denetimi](../test/media/ltest_zoomcontrol.png)

3.  Microsoft Word belgeniz için kopyalamak istediğiniz grafik üzerinde sağ tıklayıp **kopyalama**.

4.  Microsoft Word içinde grafik ve ilişkili tablo verilerini istenen konuma yapıştırın.

    > [!WARNING]
    > Uzak Masaüstü'nden grafiğe kopyalayın ve grafik ile ilişkili olan tablo bilgileri kopyaladığınızdan başka bir makineye yapıştırın ve graf görüntüsü değil. Graf görüntüsü, kopyalandığı makinedeki geçici dizinde depolanır ve ikinci makine o dizine başvuramaz.

## <a name="see-also"></a>Ayrıca bkz.

- [Rapor yük testi sonuçlarını test karşılaştırmaları veya eğilim analizi](../test/compare-load-test-results.md)
- [Nasıl yapılır: Microsoft Excel kullanarak yük testi başarım raporları oluşturma](../test/how-to-create-load-test-performance-reports-using-microsoft-excel.md)