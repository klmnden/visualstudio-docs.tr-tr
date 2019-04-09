---
title: Python ortamları penceresi başvurusu
description: Her Visual Studio'da Python ortamları penceresinde görünen sekmeler ayrıntıları.
ms.date: 03/18/2019
ms.topic: conceptual
author: JoshuaPartlow
ms.author: joshuapa
manager: jillfra
ms.custom: seodec18
ms.workload:
- python
- data-science
ms.openlocfilehash: 578f73aabfb8b5a4c8336c8611f634b8947c8885
ms.sourcegitcommit: 0e22ead8234b2c4467bcd0dc047b4ac5fb39b977
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59366529"
---
# <a name="python-environments-window-tabs-reference"></a>Python ortamları penceresi Sekme Başvurusu

Açmak için **Python ortamları** penceresi:

- Seçin **görünümü** > **diğer Windows** > **Python ortamları** menü komutu.
- Sağ **Python ortamları** bir proje için düğüm **Çözüm Gezgini** seçip **tüm Python ortamları görüntüleme**.

Genişletirseniz **Python ortamları** yetecek kadar geniş penceresinde bu seçenekler ile çalışmak daha kullanışlı bulabilirsiniz sekmeler olarak gösterilir. Daha anlaşılır olması için bu makaledeki sekmeleri Genişletilmiş görünümde gösterilir.

::: moniker range="vs-2017"
![Python ortamları penceresi Genişletilmiş Görünümü](media/environments/environments-expanded-view.png)
::: moniker-end
::: moniker range=">=vs-2019"
![Python ortamları penceresi Genişletilmiş Görünümü](media/environments/environments-expanded-view-2019.png)
::: moniker-end

## <a name="overview-tab"></a>Genel Bakış sekmesi

Ortam için temel bilgileri ve komutları sağlar:

::: moniker range="vs-2017"
![Python ortamları genel bakış sekmesi](media/environments/environments-overview-tab.png)
::: moniker-end
::: moniker range=">=vs-2019"
![Python ortamları genel bakış sekmesi](media/environments/environments-overview-tab-2019.png)
::: moniker-end

| Komut | Açıklama |
| --- | --- |
| **Bu ortama yeni projeler için varsayılan yapın.** | Visual Studio neden olabilecek etkin ortam ayarlar (2017 sürüm 15.5 ve öncesi) IntelliSense veritabanı yüklenirken kısa bir süreliğine duyuracağı olacak. Birçok paketleriyle ortamları daha uzun süre duyuracağı olabilir. |
| **Dağıtıcı Web sitesini ziyaret edin** | Python dağıtım tarafından sağlanan URL bir tarayıcı açar. Python 3.x, örneğin, için python.org gider. |
| **Açık etkileşimli penceresi** | Açılır [etkileşimli (REPL) penceresi](python-interactive-repl-in-visual-studio.md) Visual Studio'daki bu ortam için tüm uygulama [başlatma komut dosyaları (aşağıya bakın)](#startup-scripts). |
| **Etkileşimli betiklerini keşfedin** | Bkz: [başlatma komut dosyaları](#startup-scripts). |
| **Ipython etkileşimli modu kullanın** | Ayarlandığında, açılır **etkileşimli** Ipython penceresiyle varsayılan olarak. Satır içi çizimler ve bunun yanı sıra genişletilmiş Ipython söz dizimi gibi böylece `name?` yardımını görüntülemek için ve `!command` Kabuk komutları için. Bir Anaconda dağıtım olarak kullanarak ek paketler gerektirdiğinde bu seçeneği önerilir. Daha fazla bilgi için [kullanım Ipython etkileşimli pencerede](interactive-repl-ipython.md). |
| **PowerShell ile Aç** | Bir PowerShell komut penceresinde yorumlayıcı başlatır. |
| (Klasör ve program bağlantılar) | Ortamın yükleme klasörü, hızlı erişim sağlamak *python.exe* yorumlayıcısı ve *pythonw.exe* yorumlayıcı. Windows Gezgini'nde ilk açılır, sonraki iki konsol penceresi açın. |

### <a name="startup-scripts"></a>Başlatma komut dosyaları

Etkileşimli pencere, gündelik iş akışınızı kullandıkça, büyük olasılıkla düzenli olarak kullandığınız yardımcı işlevleri geliştirin. Örneğin, bir DataFrame Excel'de açılır bir işlev oluşturun ve her zaman kullanılabilir, böylece bu kod bir başlangıç dosyası olarak Kaydet **etkileşimli** penceresi.

Başlatma komut dosyası kodu içeren, **etkileşimli** penceresi yükler ve otomatik olarak içeri aktarmalar, işlev tanımları ve tam anlamıyla başka bir şey gibi çalışır. Bu komut iki yolla başvurulur:

1. Bir ortam yüklediğinizde Visual Studio, bir klasör oluşturur. *Documents\Visual Studio \<sürüm > \Python betikleri\\\<ortam >* burada &lt;sürümü&gt; (örneğin, 2017 veya 2019) Visual Studio sürümü ve &lt;ortam&gt; ortam adıyla aynıdır. Ortama özgü klasöre kolayca gezinebilirsiniz **etkileşimli betiklerini keşfedin** komutu. Başladığınızda **etkileşimli** penceresi bu ortam için bu yükler ve her şeyi çalıştırır *.py* dosyaları alfabetik sırayla burada bulunur.

1. **Betikleri** denetim **Araçları** > **seçenekleri** > **Python**  >  **Etkileşimli Windows** sekme (bkz [etkileşimli windows seçenekleri](python-support-options-and-settings-in-visual-studio.md#interactive-windows-options)) yüklenir ve tüm ortamlarda çalıştırabilirsiniz başlatma komut dosyaları için ek bir klasör belirtmek için tasarlanmıştır. Ancak, bu özellik şu anda çalışmıyor.

## <a name="configure-tab"></a>Yapılandır sekmesi

Varsa, **yapılandırma** sekmesi, aşağıdaki tabloda açıklandığı gibi ayrıntıları içerir. Bu sekme yoksa, Visual Studio otomatik olarak tüm ayrıntıları yönetiyor anlamına gelir.

::: moniker range="vs-2017"
![Python ortamları Yapılandır sekmesi](media/environments/environments-configure-tab.png)
::: moniker-end
::: moniker range=">=vs-2019"
![Python ortamları Yapılandır sekmesi](media/environments/environments-configure-tab-2019.png)
::: moniker-end

| Alan | Açıklama |
| --- | --- |
| **Açıklama** | Ortamı sağlamak için adı. |
| **Ön ek yolu** | Yorumlayıcı temel klasörün konumu. Bu değer doldurma ve tıklatarak **otomatik algıla**, Visual Studio sizin için diğer alanları doldurun dener. |
| **Cesta k interpretu** | Yolun yürütülebilir yorumlayıcı ön ek yolu tarafından yaygın olarak izlenen **python.exe** |
| **Pencereli yorumlayıcı** | Ön ek yolu ve ardından konsol içi yürütülebilir dosya yolu, genellikle **pythonw.exe**. |
| **Kitaplık yolu**<br/>(varsa) | Standart Kitaplığı'nın kökünü belirtir ancak bu değer, Visual Studio yorumlayıcı istek daha doğru bir yolu erişebiliyorsa yoksayılabilir. |
| **Dil sürümü** | Aşağı açılan menüden seçim. |
| **Mimari** | Normal olarak algılandı ve otomatik olarak doldurulur, aksi halde belirtir **32-bit** veya **64-bit**. |
| **PATH ortam değişkeni** | Ortam değişkenini yorumlayıcı arama yollarını bulmak için kullanır. Visual Studio, projenin arama yollarını içeren Python başlatırken değişkenin değerini değiştirir. Bu özellik genellikle ayarlanmalıdır **ise PYTHONPATH**, ancak bazı yorumlayıcılarını farklı bir değer kullanın. |

## <a name="packages-tab"></a>Paketleri sekmesi

*Ayrıca önceki sürümlerinde "pip" etiketli.*

PIP kullanarak ortamında yüklü paketleri yöneten ( **paketleri (Pypı)** sekmesi) ya da conda ( **paketleri (Conda)** conda ortamları Visual Studio 2017 sürüm 15.7 ve üzeri için sekmesinde). Bu sekmede arayın ve bağımlılıkları da dahil olmak üzere yeni paketlerini yükleyin.

Paket zaten yüklü olan paketleri denetimleri (yukarı ok) güncelleştirme ve kaldırma (daire içinde X) ile görünür:

![Python ortamları Paketleri sekmesi](media/environments/environments-pip-tab-controls.png)

Bir arama terimi filtreleri Pypı yüklü paketleri yanı sıra yüklü paketleri listesi giriliyor.

::: moniker range="vs-2017"
![Python ortamları paketleri sekmesinde "num" bir arama özelliğiyle](media/environments/environments-pip-tab.png)
::: moniker-end
::: moniker range=">=vs-2019"
![Python ortamları paketleri sekmesinde "num" bir arama özelliğiyle](media/environments/environments-pip-tab-2019.png)
::: moniker-end

Yukarıdaki görüntüde görebileceğiniz gibi arama sonuçlarının arama terimiyle eşleşen paket sayısı Göster; İlk listede, ancak bir komutu çalıştırmak için giriştir **pip yükleme \<adı >** doğrudan. Üzerinde kullanıyorsanız **paketleri (Conda)** sekmesinde, bunun yerine bkz **conda yükleme \<adı >**:

::: moniker range="vs-2017"
![Yükleme komutunu bir conda gösteren Conda Paketleri sekmesi](media/environments/environments-conda-tab-install.png)
::: moniker-end
::: moniker range=">=vs-2019"
![Yükleme komutunu bir conda gösteren Conda Paketleri sekmesi](media/environments/environments-conda-tab-install-2019.png)
::: moniker-end

Her iki durumda da, yükleme paket adından sonra arama kutusuna bağımsız değişken ekleyerek özelleştirebilirsiniz. Bağımsız değişkenler eklediğinizde gösterir arama sonuçlarının **pip yükleme** veya **conda yükleme** arama kutusuna içeriğine göre ve ardından:

::: moniker range="vs-2017"
![Pip ve conda yükleme komutları bağımsız değişkenleri kullanma](media/environments/environments-pip-tab-arguments.png)
::: moniker-end
::: moniker range=">=vs-2019"
![Pip ve conda yükleme komutları bağımsız değişkenleri kullanma](media/environments/environments-pip-tab-arguments-2019.png)
::: moniker-end

Bir paket yükleme oluşturur ortamın içindeki *LIB* dosya sisteminde klasör. Varsa, örneğin, Python 3.6 yüklü *c:\Python36*, içinde yüklü paketleri *c:\Python36\Lib*; yüklü Anaconda3 varsa *c:\Program Files\Anaconda3*paketleri yüklenmiş sonra *c:\Program Files\Anaconda3\Lib*. Conda ortamları için söz konusu ortamın klasöründe paketleri yüklenir.

### <a name="grant-administrator-privileges-for-package-install"></a>Yükleme paketi için yönetici ayrıcalıkları verme

Paketleri gibi dosya sistemi, korumalı bir alanda bulunan bir ortama yüklerken *c:\Program Files\Anaconda3\Lib*, Visual Studio çalıştırmanız gerekir `pip install` paket alt klasörler oluşturmak üzere izin vermek için yükseltilmiş. Yükseltme gerekli olduğunda, Visual Studio istemi görüntüler **yüklemek, güncelleştirmek veya bu ortam için paketleri kaldırmak için yönetici ayrıcalıkları gerekebilir**:

![Paket yüklemesi için yükseltme istemi](media/environments/environments-pip-elevate.png)

**Şimdi Yükselt** konu herhangi bir işletim sistemi için izinleri de ister. tek bir işlem için pip için yönetici ayrıcalıkları verir. Seçme **yönetici ayrıcalıkları olmadan devam** paketini yükleme ancak klasörleri gibi çıkış oluşturmaya çalışırken pip başarısız girişimleri **hata: değil oluşturabilirsiniz ' C:\Program Files\Anaconda3\Lib\ Site-packages\png.py': İzin reddedildi.**

Seçme **her zaman yüklerken veya paketlerini kaldırma yükseltmesine** iletişim ortamı için söz konusu görüntülenmesini engeller. İletişim kutusunu yeniden görünür hale getirmek için Git **Araçları** > **seçenekleri** > **Python** > **genel**düğmesini seçip **tüm kalıcı olarak gizli iletişim kutuları sıfırlama**.

Bu aynı **seçenekleri** sekmesinde de seçebilirsiniz **her zaman pip yönetici olarak çalıştır** tüm ortamlar için iletişim başlatmasını bastırmak için. Bkz: [seçenekleri - Genel sekmesi](python-support-options-and-settings-in-visual-studio.md#general-options).

### <a name="security-restrictions-with-older-versions-of-python"></a>Python'ın eski sürümleriyle birlikte güvenlik kısıtlamaları

3.1 ve 3.2, Python 2.6 kullanırken, Visual Studio uyarısı gösterir **yeni güvenlik kısıtlamaları nedeniyle internet'ten yükleme Python'ın bu sürümünde çalışmayabilir**:

![Python eski sürümü yükleme kısıtlamaları iletisi pip hakkında](media/environments/environments-old-version-restriction.png)

Uyarıya neden olan Python, bu eski sürümleriyle `pip install` desteği için Aktarım güvenliği Katmanı (TLS) 1.2, paket kaynağından paketleri yüklemek için gerekli olan içermiyor pypi.org. Özel bir Python yapılar destekleyebilir TLS 1.2 durumda `pip install` işe yarayabilir.

Uygun olabilir *get-pip.py* bir paket için [bootstrap.pypa.io](https://bootstrap.pypa.io/), el ile paket indirme [pypi.org](https://pypi.org/)ve ardından yükleme Bu yerel kopyayı paketi.

Ancak yalnızca Python 2.7 veya 3.3 durumu uyarısı görünmez + yükseltmek için önerilir.

::: moniker range="vs-2017"
## <a name="intellisense-tab"></a>IntelliSense sekmesi

IntelliSense tamamlanma veritabanı geçerli durumunu gösterir:

![Python ortamları IntelliSense sekmesi](media/environments/environments-intellisense-tab.png)

- Visual Studio 2017 sürüm 15.5 ve önceki sürümlerinde, IntelliSense tamamlamaları için bu kitaplığı derlenmiş olan bir veritabanı bağlıdır. Veritabanı oluşturma arka planda gerçekleştirilir, bu kitaplığa yüklendiğinde, ancak biraz zaman alabilir ve kod yazmaya başladığınızda tam olmayabilir.
- Visual Studio 2017 sürüm 15.6 ve daha sonra veritabanı üzerinde varsayılan olarak bağlı olmayan tamamlamaları sağlamak için daha hızlı bir yöntem kullanır. Bu nedenle sekme olarak etiketlenmiş **IntelliSense [veritabanı devre dışı]**. Veritabanı seçeneğini temizleyerek etkinleştirebilirsiniz **Araçları** > **seçenekleri** > **Python**  >   **Deneysel** > **ortamları için yeni stil IntelliSense kullanma**.

Visual Studio yeni bir ortam algılar (veya bir ekledikten sonra), veritabanı, kitaplık kaynak dosyalarını analiz ederek derlemek otomatik olarak başlar. Bu işlem, herhangi bir yere bir saat veya yüklenenler bağlı olarak daha fazla bilgi için bir dakika sürebilir. (Anaconda, örneğin, birçok kitaplıkları ile gelir ve veritabanını derlemek için biraz zaman alır.) Tamamlandıktan sonra size ayrıntılı IntelliSense ve veritabanını yeniden yenileme gerekmez (ile **Yenile DB** düğmesi) daha fazla kitaplıklarını yüklemek kadar.

Kendisi için veriler henüz derlenmiş kitaplıkları ile işaretlenmiş bir **!**; tam bir ortamın veritabanı yoksa bir **!** Ayrıca yanında ana ortam listesinde görünür.

::: moniker-end

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio'da Python ortamlarını yönetme](managing-python-environments-in-visual-studio.md)
- [Proje için yorumlayıcıyı seçme](selecting-a-python-environment-for-a-project.md)
- [Bağımlılıklar için Requirements.txt dosyasını kullanma](managing-required-packages-with-requirements-txt.md)
- [Arama yolları](search-paths.md)
