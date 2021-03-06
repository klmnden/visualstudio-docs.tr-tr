---
title: 'Nasıl yapılır: Bir yük testi sonuçları deposunu seçme'
ms.date: 10/19/2016
ms.topic: conceptual
f1_keywords:
- vs.test.load.dialog.connectstringmissing
- vs.test.load.dialog.databaseconnectstring
helpviewer_keywords:
- load tests, results repository
- results, load test
- load test results, repository
- Load Test Results Repository
- SQL, Load Test Results Store
ms.assetid: fa0c4dd9-612f-4a57-b8eb-458f129d9cda
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 602327d49733077e3c180c0e192027be6374afe6
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62950039"
---
# <a name="how-to-select-a-load-test-results-repository"></a>Nasıl yapılır: Bir yük testi sonuçları deposunu seçme

Bir yerel sonuç deposuyla sınırlı değildir. Sık, yük testleri Aracı bilgisayarların bir uzak kümesi üzerinde çalıştırılır. Aracıları, bir denetleyici ile birlikte tek bir bilgisayardan daha fazla benzetilmiş yük oluşturabilir. Daha fazla bilgi için [Test denetleyicileri ve test aracılarını](configure-test-agents-and-controllers-for-load-tests.md).

Test sonuçları, aracılarınız veya yerel bilgisayarınız bir yük testi sonuçları deposu oluşturmuş olduğunuz herhangi bir SQL Server'a kaydedilebilir. Her iki durumda da kullanarak yük testi sonuçlarını depolamak istediğiniz tanımlamalıdır **Test Denetleyicilerini Yönet** penceresi.

[!INCLUDE [web-load-test-deprecated](includes/web-load-test-deprecated.md)]

## <a name="identify-a-results-store-for-load-test-data"></a>Yük testi verileri için bir sonuç deposu tanımlayın

1. İçinde **Çözüm Gezgini**, yük testi dosyanızı açın.

2. Gelen **yük testi** araç seçin **Test Denetleyicilerini Yönet**. **Test denetleyicisini Yönet** iletişim kutusu görüntülenir. Aracıyı uzaktan kullanıyorsanız, bir denetleyici seçmeniz gerekir.

     ![Yük testi sonuçları deposunu bağlantı özellikleri](../test/media/loadtestconnectionproperties.png) yük testi sonuçları deposunu bağlantı özellikleri

3. İçinde **Yük Testi Sonuçları Deposu**, tıklayın **(...)**  görüntülenecek **bağlantı özellikleri** iletişim kutusu.

4. İçinde **sunucu adı**, çalıştırdığınız sunucunun adını yazın `LoadTest` betikler.

    > [!TIP]
    > Yük testi deposu için yerel makinenizde SQL Express kullanıyorsanız girin \<bilgisayaradı > \sqlexpress (örneğin, **Bilgisayarım\sqlexpress**).

5. Altında **sunucuda oturum açın**, seçebileceğiniz **Windows kimlik doğrulamasını kullan**. Kullanıcı adı ve parola belirtebilirsiniz, ancak bunu yaparsanız, seçeneğini belirlemeniz **parolamı Kaydet**.

6. Altında **veritabanına bağlan**, seçin **bir veritabanı adı seçin veya girin**. Seçin **LoadTest** aşağı açılan liste kutusundan.

7. Seçin **Tamam**. Bağlantıyı seçerek sınayabilirsiniz **Bağlantıyı Sına**.

8. Seçin **Kapat** içinde **Test denetleyicisini Yönet** iletişim kutusu.

## <a name="see-also"></a>Ayrıca bkz.

- [Yük testi sonuçları deposu içindeki yük testi sonuçlarını yönetme](../test/manage-load-test-results-in-the-load-test-results-repository.md)
- [Test denetleyicileri ve test aracıları](configure-test-agents-and-controllers-for-load-tests.md)