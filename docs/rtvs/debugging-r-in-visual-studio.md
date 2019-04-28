---
title: R kodu hata ayıklama
description: Visual Studio için R kesme noktaları da dahil olmak üzere tam bir hata ayıklama deneyimi sağlar, eklemek, yığın ve değişkenleri İnceleme çağırın.
ms.date: 01/24/2018
ms.topic: conceptual
author: kraigb
ms.author: kraigb
manager: jillfra
ms.workload:
- data-science
ms.openlocfilehash: 98dcbaaeb6f330cda3a14cf8c32afe403b50aa85
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62939293"
---
# <a name="debug-r-in-visual-studio"></a>Visual Studio'da R hata ayıklama

R araçları için Visual Studio (RTVS), Visual Studio'nun tam hata ayıklama deneyimi ile tümleştirilir (bkz [Visual Studio'da hata ayıklama](/visualstudio/debugger/debugger-feature-tour). Kesme noktaları, çağrı yığınını incelemek ve çalışan işlemleri, inceleme ve izleme değişkenleri eklemek destekler. Bu makalede, ardından, R ve RTVS özgü hata ayıklama bu özellikleri keşfediyor.

Projekt R R başlangıç dosyasında aynı diğer proje türleri için hata ayıklayıcı başlatılıyor: kullanın **hata ayıklama** > **hata ayıklamayı Başlat**, **F5** anahtarı veya **Kaynak başlangıç dosyası** hata ayıklama araç çubuğundaki:

![R için hata ayıklayıcı Başlat düğmesi](media/debugger-start-button.png)

Başlangıç dosyasını değiştirmek için Çözüm Gezgini'nde dosyaya sağ tıklayıp **kümesi olarak başlangıç R betiği**.

Tüm durumlarda, hata ayıklayıcı "Kaynaklar" Etkileşimli pencerede dosya başlatma yüklendikleri ve orada etkileşimli pencerenin çıktısında gösterilen şekilde çalıştığına anlamına gelir:

```output
> rtvs::debug_source("c:/proj/rproject1/rproject1/script.R")
Sourcing: c:\proj\rproject1\rproject1\script.R
Sourcing: c:\proj\rproject1\rproject1\Settings.R
```

Dikkat `rtvs::debug_source` işlevi komut dosyası kaynak için kullanılır. Bu işlev, kodunuzda hata ayıklama hazırlığı değiştirilecek RTVS gerektiğinden gereklidir. Herhangi bir RTVS kaynağını komutunu kullanıp bir hata ayıklayıcı eklendiğinde otomatik olarak Visual Studio kullanan `rtvs::debug_source`.

Hata ayıklayıcı kullanarak doğrudan etkileşimli penceresinden de el ile ekleyebilirsiniz **R Araçları** > **oturumu** > **hata ayıklayıcı iliştirmek** komutu, **hata ayıklama** > **ekleme R etkileşimli** komutu veya **hata ayıklayıcı iliştirmek** etkileşimli pencerenin araç çubuğundaki komutu. Bunu yaptıktan sonra kaynak, hata ayıklamak istediğiniz dosyaları sizin sorumluluğunuzdur. El ile kaynak dosyalarını istiyorsanız, kullandığınızdan emin olun `rtvs::debug_source` ve normal `source` r'deki komutu

Hata ayıklayıcı ve etkileşimli pencere arasındaki bu bağlantı arama (ve hata ayıklama) gibi şeyler kolaylaştırması farklı parametre değerleri ile bir işlev. Örneğin, aşağıdaki işlevi kaynaklı bir dosyada (oturuma yüklenmiş anlamına gelir) olduğunu varsayalım:

```R
add <- function(x, y) {
    return(x + y)
}
```

Üzerinde bir kesme noktası ayarlayın, sonra da `return` deyimi. Girme artık, etkileşimli pencerede, `add(4,5)` hata ayıklayıcı, kesme noktasına durdurur.

## <a name="environment-browser-in-the-interactive-window"></a>Etkileşimli pencerede ortam tarayıcı

Hata ayıklayıcıda durdurulduklarında, ayrıca ortam tarayıcı istemine durduruldu [etkileşimli pencere](interactive-repl-for-r-in-visual-studio.md). İstemi görünür `Browse[n]>` burada n, bir sayı.

Ortam tarayıcı özel komutları destekler:

| Komut | Açıklama |
| --- | --- |
| n | Sonraki: kod içinde sonraki deyimi çalıştırır (üzerinden adımla'olarak aynı) dosyası. |
| s | içine adımla: sonraki deyim işlev çağrısı ise bir işlev kapsamı Adımlama kod dosyasında, sonraki deyimi çalıştırır. |
| F | Son: geçerli işlev kapsamı geri kalanında çalıştırır ve çağıran (adım ile aynı) döndürür. |
| c, sürekli teslim | Devam Et: sonraki kesme noktasına kadar programı çalıştırır. |
| Q | sonlandırılıyor: hata ayıklama oturumu sona erer. |
| Burada | yığınını göster: çağrı yığını etkileşimli pencerede görüntüler. |
| Yardım | Yardımı Göster: kullanılabilir komutlar etkileşimli pencerede görüntüler. |
| &lt;ifade&gt; | İfade değerlendirme *expr*. |

![Etkileşimli pencerede ortam tarayıcı](media/debugger-environment-browser.png)
