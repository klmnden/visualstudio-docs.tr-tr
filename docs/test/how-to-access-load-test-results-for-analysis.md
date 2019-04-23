---
title: Yük testi sonuçlarını çözümleme
ms.date: 10/19/2016
ms.topic: conceptual
helpviewer_keywords:
- results, load test
- load test results, accessing
- Load Test Viewer
- load tests, accessing
- load tests, analyzing
- load tests, results
- Load Test Viewer, viewing
ms.assetid: b0a3e694-2894-479b-b270-7e61e9fafacd
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: e4b14be6df351a6975fb8a7cf6fa506a5d4f6041
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60087553"
---
# <a name="how-to-access-load-test-results-for-analysis"></a>Nasıl yapılır: Erişim yük testi sonuçlarını çözümleme

Yük Testi Düzenleyicisi'nden bir yük testi çalıştırdığınızda, yük testi sonuçları otomatik olarak açmak ve yük testi görüntülenen **Yük Testi Çözümleyicisi**. Komut satırından bir yük testi çalıştırdığınızda, yük testi sonuçları el ile erişmeniz gerekir.

Tamamlanan yük testi için yük testi sonucu performans sayaç örneklerini ve test altındaki bilgisayarlardan düzenli aralıklarla toplanan hata bilgilerini içerir. Çok sayıda performans sayacı örneği yük testi boyunca toplanabilir. Toplanan performans veri miktarı, test çalıştırması, örnekleme aralığı, test edilen bilgisayar sayısına, toplanmakta olan sayaç sayısı, yapılandırılmış veri toplayıcılarına ve günlüğe kaydetme düzeylerini uzunluğuna bağlıdır. Bir büyük yük testi için toplanan performans veri miktarı kolaylıkla birkaç gigabayt olabilir. Daha fazla bilgi için [Test denetleyicileri ve test aracılarını](configure-test-agents-and-controllers-for-load-tests.md).

[!INCLUDE [web-load-test-deprecated](includes/web-load-test-deprecated.md)]

## <a name="to-access-a-load-test-result"></a>Bir yük testi sonucu erişmek için

1. Bir web performansı ve yük testi projesinden, bir yük testi açın.

2. Yük Testi Düzenleyicisi'nin araç çubuğunda seçin **sonuçları Aç ve Yönet** düğmesi.

     **Sonuçları Aç ve Yönet** iletişim kutusu görüntülenir.

3. İçinde **yük testi sonuçlarını bulmak için bir denetleyici adı girin**, bir denetleyici seçin. Seçin  **\<yerel >-denetleyici yok** yerel olarak depolanmış sonuçlara erişmek için.

4. İçinde **göstermek için aşağıdaki yükleme testi sonuçları**, yük testi sonuçları görüntülemek istediğinizi seçin. Seçin  **\<tüm testler için sonuçları Göster >** tüm testler için tüm sonuçları görmek için.

     Yük testi sonuçları yoksa görünürler **yük testi sonuçları** listesi. Sütunların **zaman**, **süresi**, **kullanıcı**, **sonucu**, **Test**, ve  **Açıklama**. **Test** test adını içerir ve **açıklama** test çalıştırılmadan önce eklenir isteğe bağlı bir açıklama içerir.

    > [!NOTE]
    > En son sonuçları listenin üst kısmındaki sonuçlar görüntülenir.

5. İçinde **yük testi sonuçları** listesinde, istediğiniz çözümleyin ve yük testi sonuçlarını seçin **açık**.

6. **Yük Testi Çözümleyicisi** görünür. Seçilen yük testi sonucu Özet görünümünde görüntülenir. Daha fazla bilgi için [yük testi sonuçları özetine genel bakış](../test/load-test-results-summary-overview.md).

     Yük testi sonuçlarında diğer özelliklerini yönetebilir **sonuçları Aç ve Yönet** iletişim kutusu içeri aktarma, dışarı aktarma ve yük testi sonuçları kaldırma gibi. Daha fazla bilgi için [Yönet yük testi sonuçları Yük Testi Sonuçları Deposu](../test/manage-load-test-results-in-the-load-test-results-repository.md).

## <a name="see-also"></a>Ayrıca bkz.

- [Yük testi sonuçlarını çözümleme](../test/analyze-load-test-results-using-the-load-test-analyzer.md)