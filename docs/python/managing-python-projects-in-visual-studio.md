---
title: Python uygulaması projeleri yönetme
description: Visual Studio projeleri, dosyaları ve uygulama ilişkilerde karmaşıklığını arasındaki bağımlılıkları yönetin.
ms.date: 03/18/2019
ms.topic: conceptual
author: JoshuaPartlow
ms.author: joshuapa
manager: jillfra
ms.custom: seodec18
ms.workload:
- python
- data-science
ms.openlocfilehash: 2ee3b0d82251d01e8ede22be238dc1bca5a4e092
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59366230"
---
# <a name="python-projects-in-visual-studio"></a>Visual Studio'da Python projeleri

Python uygulamaları, genellikle yalnızca klasörleri ve dosyaları kullanılarak tanımlanır, ancak uygulamalar daha büyük hale gelir ve belki de JavaScript web uygulamaları için otomatik olarak oluşturulan dosyaları içeren vb. gibi bu yapı karmaşık hale gelebilir. Visual Studio projesi Bu karmaşıklığı yönetmenize yardımcı olur. Proje (bir *.pyproj* dosyası) kaynak ve projenizle ilişkili içerik dosyalarını tanımlar, her dosya için yapı bilgisi içerir, kaynak denetimi sistemleriyle tümleştirmeyi bilgilerini korur ve yardımcı olur mantıksal bileşenler uygulamanıza düzenleyin.

![Çözüm Gezgini'nde proje Python](media/projects-solution-explorer.png)

Projeleri Visual Studio'da her zaman ek olarak, yönetilen *çözüm*, herhangi bir sayıda birbirlerine başvurabilir projeleri içerebilir. Örneğin, bir Python projesi bir uzantı modülü uygulayan bir C++ projesi başvurabilir. Python projesi hata ayıklamaya başladığınızda bu ilişki ile Visual Studio C++ projesi (gerekirse) otomatik olarak oluşturur. (Genel tartışma için bkz: [Visual Studio'da projeler ve çözümler](../ide/solutions-and-projects-in-visual-studio.md).)

Visual Studio, çeşitli uygulama yapılarının bir projeden varolan bir klasör ağacı oluşturmak için bir şablon ve temiz, boş bir proje oluşturmak için bir şablon dahil olmak üzere, bir numarası hızlı bir şekilde ayarlamak için Python proje şablonları sağlar. Bkz: [proje şablonları](#project-templates) bir dizin için.

<a name="lightweight-usage-project-free"></a>

::: moniker range=">=vs-2019"
> [!Tip]
> Visual Studio 2019 Visual Studio'nun proje ve çözüm dosyaları oluşturmadan bu kodu çalıştıran ve Python kodu içeren bir klasörü açmayı destekler. Daha fazla bilgi için [hızlı başlangıç: Açın ve bir klasörde Python kodunu çalıştırma](quickstart-05-python-visual-studio-open-folder.md). Ancak, bu bölümde açıklandığı gibi bir proje dosyası kullanmanın avantajları vardır.
::: moniker-end

> [!Tip]
> Bir proje da ipucuyla Python kodunda Visual Studio'nun tüm sürümlerinde çalışır. Örneğin, bir Python dosyası kendisi tarafından ve otomatik tamamlama keyfini açık, IntelliSense ve hata ayıklama (Düzenleyicisi'nde sağ tıklatıp seçerek **ile hata ayıklama Başlat**). Bu tür kod her zaman varsayılan genel ortam kullandığından, kodu farklı bir ortam için tasarlanmıştır ancak yanlış tamamlama veya hataları görebilirsiniz. Ayrıca, Visual Studio, tüm dosyaları ve paketleri içinden tek dosya açıldığında, klasörde önemli miktarda CPU süresi kullanabilecek analiz eder.
>
> Bölümünde anlatıldığı gibi varolan koddan bir Visual Studio projesi oluşturmak için birkaç basit olan [var olan bir proje oluşturun](#create-project-from-existing-files).

|   |   |
|---|---|
| ![video kamera simgesini film](../install/media/video-icon.png "bir video izleyin") | [Yakından bakış: Python projeleri ile kaynak denetimi kullanın](https://youtu.be/Aq8eqApnugM) (youtube.com, 8 dk 55s). |

## <a name="add-files-assign-a-startup-file-and-set-environments"></a>Dosya ekleme, bir başlangıç dosyası atayın ve ortamlarını ayarlama

Uygulamanızı geliştirirken, genellikle farklı türdeki yeni dosyalar projeye eklemeniz gerekir. Bu tür dosyaları ekleyerek yapılır projeyi sağ tıklatıp seçerek **Ekle** > **var olan öğe** eklemek bir dosya için Gözat ile veya **Ekle**  >  **Yeni öğe**, öğe şablonları çeşitli olan bir iletişim getirir. Üzerinde açıklandığı [öğe şablonları](python-item-templates.md) başvuru seçenekleriniz boş Python dosyaları, bir Python sınıfı, bir birim testi ve web uygulamaları için ilgili çeşitli dosyaları. Hangi Visual Studio sürümünde kullanılabilir olduğunu öğrenmek için bu seçenekler bir test projesi ile keşfedebilirsiniz.

Kalın yazı tipinde gösterilen bir atanan başlangıç dosyasının her Python proje sahip **Çözüm Gezgini**. Başlangıç dosyası hata ayıklamaya başladığınızda çalıştırılan dosyasıdır (**F5** veya **hata ayıklama** > **hata ayıklamayı Başlat**) veya proje içinde çalıştırdığınızda**Etkileşimli** penceresi (**Shift**+**Alt**+**F5** veya **hataayıklama**  >  **Proje Python etkileşimli içinde Yürüt**). Bunu değiştirmek için yeni dosyaya sağ tıklayın ve seçin **başlangıç öğesi olarak ayarla** (veya **başlangıç dosyası olarak ayarla** Visual Studio'nun eski sürümlerinde).

> [!Tip]
> Seçilen başlangıç dosyasını projeden kaldırın ve yeni bir Visual Studio seçmeyin proje çalıştırmayı denediğinizde hangi Python dosyası ile başlaması bilmez. Bu durumda, Visual Studio 2017 sürüm 15.6 ve daha sonra bir hata gösterir. önceki sürümlerinde çalışan Python yorumlayıcısı ile ya da bir çıktı penceresini açın veya çıkış penceresine bakın görünür ancak hemen kaybolur. Bu davranışların karşılaşırsanız, bir atanan başlangıç dosyası olduğunu denetleyin.
>
> Çıkış penceresinde herhangi bir nedenle açık tutmak istiyorsanız, projenize sağ tıklayın, **özellikleri**seçin **hata ayıklama** sekmesine ve ardından eklemek `-i` için **yorumlayıcı bağımsız değişkenleri**  alan. Bu bağımsız değişken neden olur, böylece girdiğiniz kadar penceresi açık tutulması bir program tamamlandıktan sonra etkileşimli moduna geçin yorumlayıcı **Ctrl**+**Z**  >  **Enter** çıkmak için.

::: moniker range="vs-2017"
Yeni bir proje her zaman varsayılan global Python ortamı ile ilişkilidir. Proje (sanal ortamlar dahil) için farklı bir ortam ilişkilendirin, sağ **Python ortamları** seçin proje düğümü **Ekle/Kaldır Python ortamları**, ve istediklerinizi seçin.
::: moniker-end
::: moniker range=">=vs-2019"
Yeni bir proje her zaman varsayılan global Python ortamı ile ilişkilidir. Proje (sanal ortamlar dahil) için farklı bir ortam ilişkilendirin, sağ **Python ortamları** seçin proje düğümü **ortam Ekle...** , istediklerinizi seçin. Ayrıca ortamlar açılan denetimi seçmek için araç ve ortam kullanma veya başka bir projeye ekleyin.

![Python araç çubuğundaki ortam komut ekleme](media/environments/environments-toolbar-2019.png)
::: moniker-end

Etkin ortamı değiştirmek için istenen ortamında sağ **Çözüm Gezgini** seçip **etkinleştirme ortam** aşağıda gösterildiği gibi. Daha fazla bilgi için [bir proje için bir ortam seçin](selecting-a-python-environment-for-a-project.md).

![Python projesi için bir ortam etkinleştirme](media/projects-activate-environment.png)

<a name="project-types"></a>

## <a name="project-templates"></a>Proje şablonları

Visual Studio, bir Python projesi sıfırdan veya mevcut koddan ayarlamak için çeşitli yollarla sağlar. Bir şablon kullanmak için **dosya** > **yeni** > **proje** menü komutunu ya da çözüme sağ **çözümü Explorer** seçip **Ekle** > **yeni proje**, ikisi için de Getir **yeni proje** aşağıdaki iletişim. Python özel şablonları görmek için "Python" üzerinde arayın veya seçin **yüklü** > **Python** düğüm:

![Python şablonlarla yeni proje iletişim kutusu](media/projects-new-project-dialog.png)

Visual Studio 2017 ile kullanılabilir ve üzeri (tüm şablonları tüm önceki sürümlerinde mevcuttur) şablonları aşağıdaki tabloda özetlenmiştir:

| Şablon | Açıklama |
| --- | --- |
| [**Mevcut Python kodu**](#create-project-from-existing-files) | Visual Studio projesi klasörü yapısı içinde mevcut Python kodu oluşturur.  |
| **Python uygulaması** | Tek ve boş bir dosya ile yeni bir Python uygulaması için bir temel Proje yapısı. Varsayılan olarak, proje tarafından değiştirebileceğiniz varsayılan genel ortamın konsol yorumlayıcı çalışan [farklı bir ortama atama](selecting-a-python-environment-for-a-project.md). |
| [**Azure bulut hizmeti**](python-azure-cloud-service-project-template.md) | Python'da yazılmış bir Azure bulut hizmeti için bir proje. |
| [**Web projeleri**](python-web-application-project-templates.md) | Bottle, Django ve Flask gibi çeşitli çerçevelerini temel alan web apps için proje. |
| **Aplikace v Ironpythonu** | Benzer şekilde kullanır ancak Python uygulaması şablonu tarafından IronPython varsayılan etkinleştirme .NET birlikte çalışabilirlik ve karma mod .NET dilleri ile hata ayıklama. |
| **Aplikace WPF v Ironpythonu** | IronPython, Windows Presentation Foundation XAML dosyaları için uygulamanın kullanıcı arabirimini kullanarak bir proje yapısı. Visual Studio XAML Tasarımcısı sağlar, arka plan kod Python'da yazılabilir ve uygulama konsol görüntülemeden çalışır. |
| **IronPython Silverlight Web sayfası** | Silverlight'ı kullanarak bir tarayıcıda çalışan IronPython projesi. Uygulamanın Python kodu web sayfasına komut dosyası olarak dahil edilir. Ortak komut dosyası etiketi Python kodunuzu DOM ile etkileşim kurabilir Silverlight içinde çalışan IronPython başlatır miktar JavaScript kodu aşağı çeker |
| **IronPython Windows Formları uygulaması** | IronPython ile kullanıcı arabirimini kullanarak bir proje yapısı, kod ile Windows Forms kullanılarak oluşturulur. Uygulama, bir konsolu görüntülemeden çalışır. |
| **Arka plan uygulama (IOT)** | Arka plan Hizmetleri cihazlarda çalıştırmak için Python projeleri dağıtılmasını destekler. Ziyaret [Windows IOT Geliştirme Merkezi](https://dev.windows.com/en-us/iot) daha fazla bilgi için. |
| **Python uzantı Modülü** | Uygulamasını yüklediyseniz bu şablon Visual C++ altında görünür **Python yerel geliştirme araçları** Python iş yüküyle Visual Studio 2017 veya sonraki bir sürümde (bkz [yükleme](installing-python-support-in-visual-studio.md)). Çekirdek yapısı için C++ Uzantısı DLL, üzerinde açıklanana için benzer sağladığı [Python için C++ uzantısı oluşturma](working-with-c-cpp-python-in-visual-studio.md). |

> [!Note]
> Python yorumlanan bir dil olduğundan, Visual Studio'da Python projeleri bir tek başına yürütülebilir dosya gibi diğer derlenmiş dili projeler (C#, örneğin) üretmediği. Daha fazla bilgi için [sorularını ve yanıtlarını](overview-of-python-tools-for-visual-studio.md#questions-and-answers).

<a name="create-project-from-existing-files"></a>

### <a name="create-a-project-from-existing-files"></a>Var olan bir proje oluşturun

> [!Important]
> Burada açıklanan işlemi taşıma veya kopyalama orijinal kaynak dosyalarına desteklemez. Bir kopya ile çalışmak istiyorsanız, klasörü ilk çoğaltma.

[!INCLUDE[project-from-existing](includes/project-from-existing.md)]

## <a name="linked-files"></a>Bağlantılı dosyaları

Bağlı dosyalar projeye kapsama alınır, ancak genellikle uygulamanın proje klasörleri dışında bulunan dosyalardır. Görünürler **Çözüm Gezgini** Kaplanmış kısayol simge normal dosyalar: ![Bağlı dosya simgesi](media/projects-linked-file-icon.png)

İçinde belirtilen bağlantılı dosyaları *.pyproj* kullanarak dosya `<Compile Include="...">` öğesi. Bağlantılı dosyaları göreli bir yol dizin yapısı dışında kullanıyorlarsa örtük veya açık içindeki yollara kullanıyorlarsa **Çözüm Gezgini**:

```xml
<Compile Include="..\test2.py">
    <Link>MyProject\test2.py</Link>
</Compile>
```

Bağlantılı dosyaları aşağıdaki koşullardan herhangi biri altında göz ardı edilir:

- Bağlı dosya bağlantı meta verileri ve proje dizininden INCLUDE özniteliği olduğu belirtilen yolu içerir.
- Bağlı dosya proje hiyerarşisi içinde var olan bir dosya yineleme
- Bağlı dosya bağlantı meta verileri içeriyorsa ve bağlantı yolu göreli bir yol proje hiyerarşisi dışında
- Bağlantı yolunun kökü

### <a name="work-with-linked-files"></a>Bağlantılı dosyaları ile çalışma

Var olan bir öğeye bir bağlantı olarak eklemek istediğiniz dosyayı ekleyin, ardından seçin proje klasöre sağ tıklayın **Ekle** > **var olan öğe**. Görüntülenen iletişim kutusunda, bir dosya seçip **bağlantı olarak Ekle** açılır listeden **Ekle** düğmesi. Koşuluyla çakışan dosya yok, bu komut, seçili klasörde bulunan bir bağlantı oluşturur. Ancak, bu dosyanın bir bağlantısını projesinde zaten var veya aynı ada sahip bir dosya zaten var. bağlantı eklenmez.

Proje klasörleri zaten var olan bir bağlantı çalışırsanız, bir bağlantı değil de, normal bir dosya olarak eklenir. Bir dosya bir bağlantıya dönüştürülecek seçin **dosya** > **Kaydet** dosyası; proje hiyerarşisi dışındaki bir konuma kaydetmek için Visual Studio otomatik olarak bağlantıya dönüştürür. Benzer şekilde, bir bağlantı geri kullanarak dönüştürülebilir **dosya** > **Kaydet** dosyayı proje hiyerarşisi içinde herhangi bir yerde kaydetmek için.

Bir bağlı dosya taşırsanız **Çözüm Gezgini**, bağlantıyı taşınır, ancak gerçek dosyayı etkilenmez. Benzer şekilde, bir bağlantının silinmesi bağlantı dosyasını etkilemeden kaldırır.

Bağlantılı dosyaları yeniden adlandırılamaz.

## <a name="references"></a>Referanslar

Visual Studio projeleri projeler ve altında görünen uzantıları başvuruları ekleme desteği **başvuruları** düğümünde **Çözüm Gezgini**:

![Python projeleri uzantısı başvuruları](media/projects-extension-references.png)

Uzantı başvuruları genellikle projeleri arasındaki bağımlılıkları göstermek ve tasarım zamanı veya derleme zamanında bağlama IntelliSense sağlamak için kullanılır. Python projeleri benzer şekilde başvuruları kullanın, ancak Python dinamik doğası nedeniyle öncelikle tasarım zamanında geliştirilmiş IntelliSense sağlamak için kullanılırlar. Bunlar ayrıca Microsoft Azure'a dağıtılacak Ek Bağımlılıklar'ı yüklemek için kullanılabilir.

### <a name="extension-modules"></a>Uzantı modüllerini

Bir başvuru bir *.pyd* dosyası oluşturulan modülü için IntelliSense sağlar. Visual Studio yükler *.pyd* dosya Python yorumlayıcısı ve kendi türleri ve işlevleri içeriğini gözlemleyip. İmza Yardımı sağlamak işlevleri için belge dizelerini ayrıştırmak de çalışır.

Herhangi bir zamanda uzantı modülü diskte güncelleştirdiyseniz, Visual Studio arka planda modülü çözümlemeden. Bu eylem, çalışma zamanı davranışı üzerinde etkiye sahip değildir, ancak bazı tamamlamaları analiz tamamlanana kadar kullanılamaz.

Eklemeniz gerekebilir bir [arama yolu](search-paths.md) modülü içeren klasör.

### <a name="net-projects"></a>.NET projeleri

IronPython ile çalışırken, IntelliSense etkinleştirmek için .NET derlemelerine başvurular ekleyebilirsiniz. Çözümünüzdeki .NET projeleri için sağ **başvuruları** Python projenizin, seçme düğümünde **Başvuru Ekle**seçin **projeleri** sekmesini tıklatıp göz atın İstenen proje. Ayrı olarak yüklenen DLL'ler için seçin **Gözat** yerine sekmesini ve istenen DLL'ye göz atın.

IronPython başvuruları çağrısı kadar kullanılabilir değil çünkü `clr.AddReference('<AssemblyName>')` olan yapılan, ayrıca uygun bir ekleme gerekir `clr.AddReference` kodunuzun başında genellikle derleme arama. Örneğin, tarafından oluşturulan kodu **Windows Forms v Ironpythonu** Visual Studio'daki proje şablonu, üst dosyanın iki çağrısı içerir:

```python
import clr
clr.AddReference('System.Drawing')
clr.AddReference('System.Windows.Forms')

from System.Drawing import *
from System.Windows.Forms import *

# Other code omitted
```

### <a name="webpi-projects"></a>Webpı projeleri

Microsoft Azure bulut hizmetlerine Webpı aracılığıyla ek bileşenler yükleyebileceği dağıtım için Webpı ürün girişleri başvuruları ekleyebilirsiniz. Varsayılan olarak görüntülenen akış Python özgü olan ve Django CPython ve diğer temel bileşenleri içerir. Kendi akışınızı, aşağıda gösterildiği gibi de seçebilirsiniz. Microsoft Azure'a yayımlarken, Kurulum görev tüm başvurulan ürünleri yükler.

![Webpı başvuruları](media/projects-webPI-components.png)
