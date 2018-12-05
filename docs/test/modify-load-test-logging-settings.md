---
title: Yük testi Visual Studio'da günlük ayarları
ms.date: 10/19/2016
ms.topic: conceptual
helpviewer_keywords:
- load tests, logging, modifying
ms.assetid: 9649226a-857d-41ef-8ec7-047b6e498033
author: gewarren
ms.author: gewarren
manager: douge
ms.prod: visual-studio-dev15
ms.technology: vs-ide-test
ms.openlocfilehash: d24bb1b3af468f35ae333407fc96c42f4f9e669b
ms.sourcegitcommit: ae46be4a2b2b63da7e7049e9ed67cd80897c8102
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2018
ms.locfileid: "52894891"
---
# <a name="modify-load-test-logging-settings"></a>Yük testi günlüğü ayarlarını değiştirme

Tamamlanan yük testi için yük testi sonucu performans sayaç örneklerini ve bir oturum açma, test altındaki bilgisayarlardan düzenli aralıklarla toplanan hata bilgilerini içerir. Çok sayıda performans sayacı örneği yük testi boyunca toplanabilir. Toplanan performans veri miktarı, çalıştırma, örnekleme aralığı, test edilen bilgisayar sayısına ve toplamak için sayaçları sayısı uzunluğuna bağlıdır. Bir büyük yük testi için toplanan performans veri miktarı kolaylıkla birkaç gigabayt olabilir; Bu nedenle, ne sıklıkta değiştirmeyi düşünebilirsiniz verileri günlüğe kaydedilir. Bkz: [Test denetleyicileri ve test aracılarını](configure-test-agents-and-controllers-for-load-tests.md).

[!INCLUDE [web-load-test-deprecated](includes/web-load-test-deprecated.md)]

*Test denetleyicisi* test çalışırken tüm toplanan yük testi örnek verileri bir veritabanına günlük biriktirir. Test tamamlandığında, zamanlama ayrıntılarını ve hata ayrıntılarının gibi ek veriler veritabanına yüklenir.

|Görev|İlişkili konular|
|-|-----------------------|
|**Bir yük testi başarısız olursa, günlükleri kaydedin:** bir yük testi başarısız olduğunda test günlüğü kaydetmek isteyip istemediğinizi belirtebilirsiniz.|-   [Nasıl yapılır: test başarısızlıklarının test günlüklerini kaydedilip kaydedilmediği belirleme](../test/how-to-specify-if-test-failures-are-saved-to-test-logs.md)|
|**Günlük dosyası için maksimum dosya boyutunu ayarlayın:** maksimum dosya boyutu için günlük dosyasına kullanmak istediğinizi belirtmek için test denetleyicisi hizmeti ile ilişkili XML yapılandırma dosyasını düzenleyebilirsiniz.|[Nasıl yapılır: günlük dosyası boyutu üst sınırı belirtin](../test/how-to-specify-the-maximum-size-for-the-log-file.md)|

## <a name="see-also"></a>Ayrıca bkz.

- [Yük testi çalıştırma ayarlarını yapılandırma](../test/configure-load-test-run-settings.md)