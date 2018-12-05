---
title: Microsoft Word'ü kullanarak bir Visual Studio Yük testi başarım raporunu oluşturma
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
ms.technology: vs-ide-test
ms.openlocfilehash: 4a5dd85c56a57b6257041c129925703e8e91e050
ms.sourcegitcommit: ae46be4a2b2b63da7e7049e9ed67cd80897c8102
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2018
ms.locfileid: "52895619"
---
# <a name="how-to-manually-create-a-load-test-performance-report-using-microsoft-word"></a>Nasıl yapılır: Microsoft Word kullanılarak bir yük testi başarım raporunu el ile oluşturma

Grafik görünümü ve yük testi sonuçlarını Özet görünümü verileri yapıştırarak Microsoft Word yük testi raporları el ile oluşturabilirsiniz. Özet görünümü gösterilir ve grafikler görünümünde verileri, HTML biçiminde kopyalandığında uygulanır.

[!INCLUDE [web-load-test-deprecated](includes/web-load-test-deprecated.md)]

> [!TIP]
> Tablolar görünümü ve Microsoft Word için ekran Ayrıntılar görünümünü görüntüleri düz metni kopyalayın, ancak HTML biçiminde uygulanmaz ve biçimlendirme ve düzenleme ek gerektirir.

> [!TIP]
> Otomatik olarak düzenlenmiş Microsoft Excel raporları da oluşturabilirsiniz. Daha fazla bilgi için [nasıl yapılır: oluşturma yük testi başarım raporları kullanarak Microsoft Excel kullanarak](../test/how-to-create-load-test-performance-reports-using-microsoft-excel.md).

## <a name="copy-summary-view-data"></a>Özet görünümü verilerini kopyalama

1.  İçinde **yük testi sonuçları**, Özet görünümü şu anda görüntülenmiyorsa tıklayın **Özet** araç.

2.  Özet görünümünde, sağ tıklayıp **Tümünü Seç**.

3.  Özet görünümünde, sağ tıklayıp **kopyalama**. Bu, Özet görünümü verisini HTML biçiminde panoya olarak işler.

4.  Microsoft Word içinde Özet görünümü verileri istediğiniz yere yapıştırın.

5.  Artık, değiştirme, biçimlendirme ve raporlama ihtiyaçlarınızı karşılayacak şekilde kopyalanan içerik yönlerini silebilirsiniz.

## <a name="copy-graph-view-data"></a>Graf görünümü verilerini kopyalama

1.  İçinde **yük testi sonuçları**, görünüm şu anda görüntülenmez, grafik seçerseniz **grafikleri** araç.

2.  (İsteğe bağlı) Aşağıdaki çizimde gösterildiği gibi Microsoft Word belgesi için kopyalamak istediğiniz belirli grafik yakınlaştırın. Daha fazla bilgi için [nasıl yapılır: grafiğin bir bölgesine yakınlaştırmak](../test/how-to-zoom-in-on-a-region-of-the-graph-in-load-test-results.md).

     ![Graf görünümü yakınlaştırma denetimi](../test/media/ltest_zoomcontrol.png)

3.  Microsoft Word belgeniz için kopyalamak istediğiniz grafik üzerinde sağ tıklayıp **kopyalama**.

4.  Microsoft Word içinde grafik ve ilişkili tablo verilerini istenen konuma yapıştırın.

    > [!WARNING]
    > Uzak Masaüstü'nden grafiğe kopyalayın ve grafik ile ilişkili olan tablo bilgileri kopyaladığınızdan başka bir makineye yapıştırın ve graf görüntüsü değil. Graf görüntüsü, kopyalandığı makinedeki geçici dizinde depolanır ve ikinci makine o dizine başvuramaz.

## <a name="see-also"></a>Ayrıca bkz.

- [Rapor yük testi sonuçlarını test karşılaştırmaları veya eğilim analizi](../test/compare-load-test-results.md)
- [Nasıl yapılır: oluşturma yük testi başarım raporları kullanarak Microsoft Excel](../test/how-to-create-load-test-performance-reports-using-microsoft-excel.md)