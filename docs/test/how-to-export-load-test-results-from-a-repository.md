---
title: Yük testi sonuçları Dışarı Aktar
ms.date: 10/19/2016
ms.topic: conceptual
helpviewer_keywords:
- results, load test
- load tests, exporting results
- Load Test Results Repository
- load test results, exporting
ms.assetid: 716c2af5-8737-4d31-956f-a0273f7c5c0c
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 477ab8ce86188af9a3db03b92e1ea0f574d8a6a3
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62949934"
---
# <a name="how-to-export-load-test-results-from-a-repository"></a>Nasıl yapılır: Yük testi sonuçlarını bir depodan dışarı aktarma

Çalıştırma sırasında toplanan bilgileri, bir yük testi çalıştırdığınızda, yük testi sonuçları deposunda depolanır. Yük testi sonuçları deposu, performans sayacı verileri ve hatalar hakkında bilgi içerir. Daha fazla bilgi için [Yönet yük testi sonuçları yük testi sonuçları deposunda](../test/manage-load-test-results-in-the-load-test-results-repository.md).

Kullanarak yük testi sonuçları Yük Testi Düzenleyicisi'nden yönetebilirsiniz **açık ve yük testi sonuçlarını yönetme** iletişim kutusu. Açın, içeri aktarma, dışarı aktarma ve yük testi sonuçları kaldırın.

[!INCLUDE [web-load-test-deprecated](includes/web-load-test-deprecated.md)]

## <a name="to-export-results-from-a-repository"></a>Sonuçlarını bir depodan dışarı aktarmak için

1. Bir web performansı ve yük testi projesinden, bir yük testi açın.

2. Gömülü araç çubuğunda **sonuçları Aç ve Yönet**.

     **Yönetme yük testi sonuçlarını Aç ve** iletişim kutusu görüntülenir.

3. İçinde **yük testi sonuçlarını bulmak için bir denetleyici adı girin**, bir denetleyici seçin. Seçin  **\<yerel - denetleyici yok >** yerel olarak depolanmış sonuçlara erişmek için.

4. İçinde **göstermek için aşağıdaki yükleme testi sonuçları**, yük testi sonuçları görüntülemek istediğinizi seçin. Seçin  **\<tüm testler için sonuçları Göster >** tüm testler için tüm sonuçları görmek için.

     Yük testi sonuçları kullanamıyorsanız, görünürler **yük testi sonuçları** listesi. Sütunların **zaman**, **süresi**, **kullanıcı**, **sonucu**, **Test**, ve  **Açıklama**. **Test** test adını içerir ve **açıklama** test çalıştırılmadan önce eklenir isteğe bağlı bir açıklama içerir. **Açıklama** sütunu içindeki girilen kısa açıklamaları görüntüler **analiz yorumları** bunun için test sonucu.

5. İçinde **yük testi sonuçları** listesinde, bir sonuç seçin. Kullanabileceğiniz **Shift** anahtar **Ctrl** anahtar ya da her ikisini birden fazla sonuç seçin ve bunları tek bir dosyaya dışarı aktarma.

6. Seçin **dışarı**.

     **Yük testi sonuçları dışa** iletişim kutusu görüntülenir.

7. İçinde **dosya adı** kutusuna bir ad yazın ve ardından **Kaydet**.

     Sonuçları bir arşiv dosyasına aktarılır.

    > [!NOTE]
    > **Yönetme yük testi sonuçlarını Aç ve** sonuçlar göründükten sonra iletişim kutusu açık kalır.

## <a name="see-also"></a>Ayrıca bkz.

- [Yük testi sonuçları deposu içindeki yük testi sonuçlarını yönetme](../test/manage-load-test-results-in-the-load-test-results-repository.md)
- [Nasıl yapılır: Yük testi sonuçlarını bir depodan silme](../test/how-to-delete-load-test-results-from-a-repository.md)
- [Yük testi sonuçlarını çözümleme](../test/analyze-load-test-results-using-the-load-test-analyzer.md)
- [Nasıl yapılır: Bir depoda alma yük testi sonuçları](../test/how-to-import-load-test-results-into-a-repository.md)