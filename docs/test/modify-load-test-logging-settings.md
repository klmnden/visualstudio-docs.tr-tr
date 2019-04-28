---
title: Yük testi günlük oluşturma ayarlarını
ms.date: 10/19/2016
ms.topic: conceptual
helpviewer_keywords:
- load tests, logging, modifying
ms.assetid: 9649226a-857d-41ef-8ec7-047b6e498033
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 9751ce3b08a0ac963cccdf091ccb99001c6f2c9f
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62785779"
---
# <a name="modify-load-test-logging-settings"></a>Yük testi günlüğü ayarlarını değiştirme

Tamamlanan yük testi için yük testi sonucu performans sayaç örneklerini ve bir oturum açma, test altındaki bilgisayarlardan düzenli aralıklarla toplanan hata bilgilerini içerir. Çok sayıda performans sayacı örneği yük testi boyunca toplanabilir. Toplanan performans veri miktarı, çalıştırma, örnekleme aralığı, test edilen bilgisayar sayısına ve toplamak için sayaçları sayısı uzunluğuna bağlıdır. Bir büyük yük testi için toplanan performans veri miktarı kolaylıkla birkaç gigabayt olabilir; Bu nedenle, ne sıklıkta değiştirmeyi düşünebilirsiniz verileri günlüğe kaydedilir. Bkz: [Test denetleyicileri ve test aracılarını](configure-test-agents-and-controllers-for-load-tests.md).

[!INCLUDE [web-load-test-deprecated](includes/web-load-test-deprecated.md)]

*Test denetleyicisi* test çalışırken tüm toplanan yük testi örnek verileri bir veritabanına günlük biriktirir. Test tamamlandığında, zamanlama ayrıntılarını ve hata ayrıntılarının gibi ek veriler veritabanına yüklenir.

|Görev|İlişkili konular|
|-|-----------------------|
|**Bir yük testi başarısız olursa, günlükleri kaydedin:** Bir yük testi başarısız olduğunda test günlüğü kaydetmek isteyip istemediğinizi belirtebilirsiniz.|-   [Nasıl Yapılır: Test hata günlükleri test etmek için kaydedilip kaydedilmediği belirleme](../test/how-to-specify-if-test-failures-are-saved-to-test-logs.md)|
|**Günlük dosyası için maksimum dosya boyutunu ayarlayın:** Günlük dosyası için kullanmak istediğiniz maksimum dosya boyutunu belirtmek için test denetleyicisi hizmeti ile ilişkili XML yapılandırma dosyasını düzenleyebilirsiniz.|Değiştirme `<add key="LogSizeLimitInMegs" value="20"/>` içinde *QTCcontroller.exe.config* XML yapılandırma dosyası.|

## <a name="see-also"></a>Ayrıca bkz.

- [Yük testi çalıştırma ayarlarını yapılandırma](../test/configure-load-test-run-settings.md)