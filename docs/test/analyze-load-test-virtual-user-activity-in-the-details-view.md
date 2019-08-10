---
title: Yük Testi Sanal Kullanıcı etkinliğini çözümleme
ms.date: 10/03/2016
ms.topic: conceptual
f1_keywords:
- vs.test.load.monitor.activitychart
helpviewer_keywords:
- virtual user activity chart
- load test, virtual user activity chart
ms.assetid: 63f4bd42-3cfb-4eee-af68-e8334976539e
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: a03096e92f2a5da98da2d1850f505c65eb5b6e27
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68918614"
---
# <a name="analyzing-load-test-virtual-user-activity-in-the-details-view-of-the-load-test-analyzer"></a>Yük Testi Çözümleyicisinin Ayrıntılar görünümünde Yük Testi Sanal Kullanıcı etkinliğini çözümleme

[!INCLUDE [web-load-test-deprecated](includes/web-load-test-deprecated.md)]

**Sanal Kullanıcı Etkinlik Grafiği**

![Sanal Kullanıcı Etkinlik Grafiği](../test/media/virtual_actchart.png)

**Ayrıntıları** görüntülemek görüntüler **sanal kullanıcı aktivite grafiği**, görsel olarak yük testi sırasında tek tek sanal kullanıcıların ne yaptığını analiz etmek için kullanılır. **Sanal kullanıcı aktivite grafiği** , kullanıcı etkinliğinin desenleri görmemizi, yük düzenleri, başarısız olan veya yavaş testleri ilişkilendirmenizi ve diğer sanal kullanıcı etkinliğini isteklerle olanak tanır. **Sanal kullanıcı aktivite grafiği** CPU kullanımı, saniye başına istek bırakmaları artış belirlemenizi de yapabilirsiniz ve hangi test veya sayfaları çalıştırma bırakmaları ve ani değişiklikleri sırasında.

> [!NOTE]
> Kullanmak istediğiniz yük testini çalıştırmadan önce **sanal kullanıcı etkinlik ayrıntıları grafiği**, doğrulamanız gerekir **Zamanlama Ayrıntıları Deposu** özelliği  **AllIndividualDetails** performans Yük Testi Düzenleyicisini kullanarak seçeneği.

**Ayrıntı göstergesi Panel**

![Ayrıntı göstergesi panel](../test/media/ltest_detailslegend.png)

Ayrıntı göstergesi panel görülebilir **sanal kullanıcı aktivite grafiği**. Ayrıntıları gösterge bölmesinde testler, sayfalar ve işlemleri birkaç farklı ölçütlere göre filtreleme yapmanızı sağlıyor. Örneğin, belirli testleri görünümden kaldır veya tüm başarılı testleri kaldırabilir veya bazı hatalarla başarısız olan testler kaldırın. Ayrıca, günlükleri olmayan tüm testleri de kaldırabilirsiniz.

Tüm başarısız testleri kırmızı renkte görüntüleyen, başarısız, testleri vurgulayabilirsiniz. Test günlüğü olan testleri de vurgulayabilirsiniz. Günlükleri ile testleri yeşil renkli.

**Sonuçlar paneli Filtrele**

![Sonuçlar paneli Filtrele](../test/media/ltest_filterresults.png)

Filtre sonuçlar paneli içinde görünen **sanal kullanıcı aktivite grafiği**. Filtre sonuçlar paneli aşağıdakilere göre filtreleyebilirsiniz:

- **Yalnızca Günlüklü sonuçları göster** yalnızca test test günlüklerinin ilişkili olan sonuçları görüntüler.

- **Başarılı sonuçları göster** başarılı sonuçları görüntüler.

- **Hatalı sonuçları göster** hata ayıklamaya yardımcı olabilecek hatalı sonuçları görüntüler.

## <a name="tasks"></a>Görevler

|Görevler|İlişkili konular|
|-|-|
|**Yük testinizi çalıştırın:** Bir yük testi oluşturduktan ve Sanal Kullanıcı etkinliği verilerini toplamayı etkinleştirecek şekilde yapılandırdıktan sonra, **Sanal Kullanıcı etkinliği grafiğini**görüntülemek için testi tamamlanana kadar testi çalıştırmanız gerekir.||
|**Sanal Kullanıcı etkinliği verilerini içeren yük testi sonuçlarını görüntüleyin:** Yük testiniz oluşturulduktan, yapılandırıldıktan ve çalışmayı tamamladıktan sonra, Sanal Kullanıcı **etkinlik grafiğini**kullanarak sanal kullanıcı etkinliği verilerini görüntüleyebilirsiniz.|-   [Yük testi sonuçlarını çözümleme](../test/analyze-load-test-results-using-the-load-test-analyzer.md)<br />-   [Nasıl Yapılır: Yük testi sırasında sanal kullanıcıların ne yaptığını çözümleyin](../test/how-to-analyze-virtual-user-activity-during-a-load-test.md)|
|**Yük testlerinde performans sorunlarını yalıtın:** Yük testinizde performans sorunlarını yalıtmaya yardımcı olması için **Sanal Kullanıcı etkinliği grafiğini** kullanabilirsiniz.|-   [Gidiş Sorunları yalıtmak için Sanal Kullanıcı etkinliği grafiğini kullanma](../test/walkthrough-use-the-virtual-user-activity-chart-to-isolate-issues.md)|

## <a name="see-also"></a>Ayrıca bkz.

- [Yük testi sonuçlarını çözümleme](../test/analyze-load-test-results-using-the-load-test-analyzer.md)
- [Yük testi sonuçlarını ve hatalarını Tablo görünümünde çözümleyin](../test/analyze-load-test-results-and-errors-in-the-tables-view.md)