---
title: Kodlanmış UI Testleriyle Farklı Web Tarayıcıları Kullanma
ms.date: 11/04/2016
ms.topic: conceptual
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
author: gewarren
ms.openlocfilehash: 822ce0a2f0e8632706a4a1551cc53aafb23563ed
ms.sourcegitcommit: 4ffb7be5384ad566ce46538032bf8561754c61a4
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2019
ms.locfileid: "57983043"
---
# <a name="use-different-web-browsers-with-coded-ui-tests"></a>Kodlanmış UI testleriyle farklı web tarayıcıları kullanma

Kodlanmış UI testleri, web uygulamaları için Internet Explorer'ı kullanarak testlerinizi kaydederek sınamayı otomatikleştirebilirsiniz. Bu web uygulamaları için Internet Explorer veya başka tarayıcı türleri kullanarak testinizi özelleştirebilir ve geri oynatabilirsiniz.

[!INCLUDE [coded-ui-test-deprecation](includes/coded-ui-test-deprecation.md)]

İlk olarak, yükleme [Selenium bileşenlerini kodlanmış UI çapraz tarayıcı test etmek](https://marketplace.visualstudio.com/items?itemName=AtinBansal.SeleniumcomponentsforCodedUICrossBrowserTesting).

## <a name="whats-supported-across-all-web-browsers"></a>Ne tüm web tarayıcıları destekleniyor mu?

-   [Özellikleri denetlemek için özel kod ekleme](https://devblogs.microsoft.com/devops/coded-ui-test-configuring-search-properties-while-recording-on-internet-explorer/) properties, search ve playback waiters gibi.

-   Açılır pencereler ve iletişim kutuları

-   [Dönüş türü olmadan temel JavaScript yürütme](https://devblogs.microsoft.com/devops/introducing-javascript-execution-on-internetexplorer-and-crossbrowser-in-coded-ui-test/)

-   Arama (akıllı eşleşme kullanarak) esneklik ve [performans geliştirmeleri](https://devblogs.microsoft.com/devops/guidelines-on-improving-performance-of-coded-ui-test-playback/)

## <a name="why-should-i-use-coded-ui-tests-across-multiple-web-browser-types"></a>Birden çok web tarayıcı türleri arasında kodlanmış UI testleri neden kullanmalıyım?

Çeşitli web tarayıcı türleri kullanarak, web uygulamanızı test ederek, farklı tarayıcılar çalıştıran kullanıcıların kullanıcı arabirimi deneyimi daha iyi benzetirsiniz. Örneğin, uygulamanız diğer web tarayıcıları ile uyumlu olmayan Internet Explorer denetim veya kod içerebilir. Diğer tarayıcılar arasında kodlanmış UI testleri çalıştırarak, müşterilerinizi etkilemeden önce herhangi bir sorunu keşfedebilir ve düzeltebilirsiniz.

## <a name="how-do-i-record-and-play-back-coded-ui-tests-on-web-applications-using-the-supported-web-browsers"></a>Kodlanmış UI testleri desteklenen web tarayıcısı kullanarak web uygulamaları üzerinde nasıl kaydederim ve kayıttan yürütürüm?

**Kaydı:** Internet Explorer'ı kullanarak web uygulama testinizi kaydetmek için kodlanmış UI Test Oluşturucusu'nu kullanmanız gerekir. İsteğe bağlı olarak, doğrulama ve kodlanmış UI testleri için normalde yaptığınız gibi önceden tanımlanmış bir özellik kümesi kullanarak sınanmış denetimler için özel kod ekleyebilirsiniz. Daha fazla bilgi için [kodunuzu test etmek için kullanım UI Otomasyonu](../test/use-ui-automation-to-test-your-code.md).

> [!NOTE]
> Google Chrome veya Mozilla Firefox tarayıcısı kullanarak kodlanmış UI testleri kaydedemezsiniz.

 **Internet Explorer ile kayıttan yürütme:** Hiçbir tarayıcı açıkça belirtilmediğinde testler varsayılan olarak Internet Explorer'da çalışır. Açıkça ayarlayarak kullanılacak tarayıcı durum **BrowserWindow.CurrentBrowser** özelliğini test kodunuzda. Internet Explorer için bu özelliği ayarlanmalıdır **IE** veya **Internet Explorer**.

 **Geri Internet Explorer web tarayıcılarıyla çalma:** Internet Explorer web tarayıcılarında çalmak için BrowserWindow.CurrentBrowser özelliğini test kodunuzda ya da değiştirin **Firefox** veya **Chrome**.

 Testleri IE olmayan web tarayıcılarında çalmak için yüklemelisiniz **kodlanmış UI çapraz tarayıcı test etmek için Selenium bileşenlerini**.

### <a name="install-selenium-components"></a>Selenium bileşenlerini yükleme

::: moniker range="vs-2017"

1. Üzerinde **Araçları** menüsünde seçin **Uzantılar ve güncelleştirmeler**.

2. İçinde **Uzantılar ve güncelleştirmeler** iletişim kutusu, arama `Selenium components for Cross Browser Testing`.

::: moniker-end

::: moniker range=">=vs-2019"

1. Üzerinde **uzantıları** menüsünde seçin **uzantıları yönetme**.

2. İçinde **uzantıları yönetme** iletişim kutusu, arama `Selenium components for Cross Browser Testing`.

::: moniker-end

3. Uzantısını vurgulayın ve seçin **indirme**.

    > [!TIP]
    > Kodlanmış UI çapraz tarayıcı test etmek için Selenium bileşenlerini indirebilirsiniz [burada](https://marketplace.visualstudio.com/items?itemName=AtinBansal.SeleniumcomponentsforCodedUICrossBrowserTesting).

Daha fazla bilgi oluşturma ve kullanarak kodlanmış UI testleri için bkz. [Oluştur kodlanmış UI testleri](../test/use-ui-automation-to-test-your-code.md).

### <a name="enable-debugging"></a>Hata ayıklamayı etkinleştir

Web uygulamanızda hata ayıklamayı etkinleştirmek için aşağıdaki yapılandırma seçeneklerini tamamlamanız gerekir:

1.  Yalnızca Kendi Kodumu Etkinleştir:

    1.  Üzerinde **Araçları** menüsünde seçin **seçenekleri** seçip **hata ayıklama**.

    2.  Seçin **yalnızca kendi kodumu etkinleştir**.

2.  CLR özel durumları devre dışı bırakın:

    1.  Üzerinde **hata ayıklama** menüsünde seçin **özel durumları**.

    2.  İçin **ortak dil çalışma zamanı özel durumları**, onay kutusunu temizleyin **kullanıcı-işlenmemiş**.

Varsa değiştirme seçeneği görmüyorum `BrowserWindow.CurrentBrowser` kodlanmış UI testi, Visual Studio'nun çeşitli web tarayıcıları kullanarak kodlanmış UI testlerini desteklemeyen bir sürümünü kullanıyor olabilirsiniz. Bu tür kodlanmış UI testleri kullanmak için Visual Studio Enterprise edition'ı kullanmanız gerekir.

Bilmeniz gereken bazı işlemler aşağıda verilmiştir:

- Apple Safari web tarayıcısı desteklenmiyor.

- Web tarayıcısını başlatma eylemini, kodlanmış UI testi parçası olmalıdır.

   Internet Explorer kullanmadığınız sürece açık bir web tarayıcısına sahip ve adımlar üzerinde çalıştırmak istiyorsanız, kayıttan yürütme başarısız olur. Bu nedenle, web tarayıcınızı başlatması kodlanmış UI testleriniz bir parçası olarak dahil en iyi uygulamadır.

- Ekranı kapla, simge durumuna küçült, geri yükle gibi belirli tarayıcı tabanlı UI eylemlerini böyle otomatikleştirme desteklenmiyor.

## <a name="tips"></a>İpuçları

Çıktı kodlanmış UI günlüklerinde ekran görüntüleri dahil etmek için yapılandırabilirsiniz. Bunu yapmak için bazı yapılandırma ayarları kümesinde ihtiyacınız *QTAgent32.exe.config* dosya. Varsayılan olarak, bu dosya aşağıdaki konuma yüklenir:

*%ProgramFiles(x86)%\Microsoft Visual Studio\2017\Enterprise\Common7\IDE*

Aşağıdaki değerleri ayarlayın:

- `EqtTraceLevel` içinde `system.diagnostics` bölümü.

- `<add name="EqtTraceLevel" value="4" />`

   3 veya daha yüksek bir değere ayarlayarak, ekran görüntüleri her eylem için alınır. Değeri 1 veya 2'ye ayarlandığında, ekran görüntüleri yalnızca hata eylemleri alır.

Daha fazla bilgi için [Çözümle kodlanmış UI testleri, kodlanmış UI test günlüklerini kullanarak](../test/analyzing-coded-ui-tests-using-coded-ui-test-logs.md).

## <a name="video-resources"></a>Görüntü kaynakları

 [IE ve kayıttan yürütme her yerde kaydı](https://skydrive.live.com/redir?resid=AE5CD7309CCCC43C!183&authkey=!ANqaLtCZbtJrImU)

 [Çapraz tarayıcı testleri kodlanmış UI test Oluşturucusu ile yazar](https://skydrive.live.com/redir?resid=AE5CD7309CCCC43C!184&authkey=!AKG8CSow_qmeTq8)

 [Çapraz tarayıcı testleri UI eşlemesi düz el kodlama kullanarak Yazar](https://skydrive.live.com/redir?resid=AE5CD7309CCCC43C!186&authkey=!AJaEvxJnsefyAT4)

 [Çapraz tarayıcı sırayla birden çok tarayıcı üzerinde testler](https://skydrive.live.com/redir?resid=AE5CD7309CCCC43C!187&authkey=!ADI8eCQkxHnpOR8)

 [Tarayıcı test hatalarını giderme](https://skydrive.live.com/redir?resid=AE5CD7309CCCC43C!182&authkey=!AEpS48i295B49FI)

## <a name="see-also"></a>Ayrıca bkz.

- [UI otomasyonunu kullanarak kodunuzu test etme](../test/use-ui-automation-to-test-your-code.md)
- [Kodlanmış UI testleri ve eylem kayıtları için desteklenen yapılandırmalar ve platformlar](../test/supported-configurations-and-platforms-for-coded-ui-tests-and-action-recordings.md)
- [Kodlanmış UI test günlüklerini kullanarak kodlanmış UI testlerini analiz etme](../test/analyzing-coded-ui-tests-using-coded-ui-test-logs.md)
