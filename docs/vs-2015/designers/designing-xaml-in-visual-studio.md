---
title: XAML tasarlama
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology: vs-ide-general
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 288e2415-9fcf-408e-bc35-9848315e14fd
caps.latest.revision: 6
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: a1c58ca9d567db88fb8267d56e071c11ba8aef27
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53870235"
---
# <a name="designing-xaml-in-visual-studio"></a>Visual Studio'da XAML tasarlama
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Visual Studio hem de visual araçları sağlayan için ilgi çekici kullanıcı arabirimleri oluşturma ve zengin medya deneyimlerini XAML tabanlı Windows Masaüstü için Visual Studio'da ve Blend'de Web'de [Windows Phone](http://msdn.microsoft.com/library/windowsphone/develop/jj683071.aspx), ve [Windows Store](http://msdn.microsoft.com/library/windows/apps/jj129478.aspx)uygulamalar. Hem de ortak tasarım ve araç pencereleri ve bir XAML Düzenleyicisi sahip, ancak Visual Studio için Blend, animasyon ve davranışlar gibi daha gelişmiş görevler için diğer tasarım araçları sağlar.

## <a name="choosing-the-right-tool"></a>Doğru aracı seçme
 Tasarım araçlarını tercih ettiğiniz beceri kümenizi bulunmadığına bağlıdır. Daha fazla kod odaklı varsa, daha gelişmiş tasarım görevini gerçekleştirmek için Visual Studio'da XAML kod yazabilirsiniz. Tasarım odaklı fazla varsa, Visual Studio için Blend kod yazmaya gereksinim duymadan gelişmiş görevleri gerçekleştirmenize olanak tanır.

 Visual Studio ve Visual Studio için Blend arasında ileri ve geri geçiş yapabilirsiniz ve aynı anda hem de aynı projeyi bile olabilir. Bir IDE için geçiş yaptığınızda otomatik yeniden tek bir IDE XAML dosyalarında yapılan değişiklikler uygulanabilir. Seçenekleri üzerinden yeniden yükleme davranışını kontrol edebilirsiniz **Araçları**, **seçenekleri** IDE ya da iletişim kutusunda.

### <a name="shared-capabilities"></a>Paylaşılan Özellikler
 En temel görevler için Visual Studio IDE ve Visual Studio için Blend paylaşın aynı dizi windows ve özellikleri, bazı farklar. Bazı önemli noktalar şunlardır:

-   **Tutarlı bir kullanıcı arabirimi:** Uygulamalarınızı tanıdık bağlam içinde daha eğlenceli ve üretken bir deneyim IDE'ler arasında geçiş yapar Visual Studio kullanıcı arabiriminin tasarlayabilirsiniz. Visual Studio kullanımlar odaklanmanıza yardımcı olan Visual Studio koyu tema içeriğinizi ve kullanıcı arabirimi arasındaki kontrastı geliştirerek tasarlarken içerik üzerinde karışır. Bkz: [XAML Tasarımcısını kullanarak kullanıcı Arabirimi oluşturma](../designers/creating-a-ui-by-using-xaml-designer-in-visual-studio.md).

     ![Visual Studio IDE için Blend](../designers/media/blendide.png "BlendIDE")

-   **XAML IntelliSense:** Her iki IDE'ler deyim tamamlama, açıklama ve kod ve gezinme kaynakları, bağlama ve kod biçimlendirme gibi Düzenleyici işlemleri ortak desteği dahil olmak üzere ıntellisense'ten beklediğiniz genel özelliklerin tümünü destekler.

-   **Temel hata ayıklama özellikleri:** Artık çalışan uygulamanızda hata ayıklama için kodunuzda ayarı kesme noktaları da dahil olmak üzere blend'de ayıklayabilirsiniz. Visual Studio ile hata ayıklama tutarlı bir deneyim sağlamak için Visual Studio için Blend çoğu Visual Studio hata ayıklama windows ve araç çubuklarını içerir. Gelişmiş hata ayıklama yetenekleri gibi tanılama ve Kod Analizi yalnızca Visual Studio içinde kullanılabilir. Bkz: [Visual Studio'da hata ayıklama](../debugger/debugging-in-visual-studio.md).

-   **Dosya yeniden yükleme deneyimi:** Her iki Visual Studio için Blend ya da Visual Studio XAML dosyalarınızı düzenleyin ve bunlar arasında geçiş yaparken otomatik olarak yeniden düzenlenmiş dosyalarınız. İş akışı kesintilerini en aza indirmek için artık dosyanızı yeniden tercihleri dosyası Yükle iletişim kutusunda ayarlayabilirsiniz.

     ![Dosya yeniden yükleme deneyimi](../designers/media/blendfilereload.png "BlendFileReload")

-   **Eşitlenmiş düzenler ve ayarları:** Özel düzenleri kaydedebilir ve araç penceresi düzeni özelleştirmeleri uygulayabilirsiniz olanak sağlar. Aynı Microsoft hesabıyla oturum açtığınızda visual Studio bu özelleştirmeler ve hem Visual Studio ve Visual Studio için Blend tercihlerini makinelerdeki eşitler. Bkz: [Visual Studio'da geliştirme ayarlarını özelleştirme](http://msdn.microsoft.com/en-us/22c4debb-4e31-47a8-8f19-16f328d7dcd3).

-   **Ortak Çözüm Gezgini için:** Çözüm Gezgini'nde, projelerinizi ve kendi dosyaları, hem de kendileriyle ilişkili komutların hazır erişimi düzenli bir görünümünü sağlar. Çözüm Gezgini ile büyük kurumsal projeleriyle çalışmak kolaydır. Bkz: [çözümler ve projeler](../ide/solutions-and-projects-in-visual-studio.md).

-   **Takım Gezgini için:** Takım Gezgini ile projelerinizi takım işbirliğini kolaylaştırmak için GIT veya TFS depoları ile yönetebilirsiniz. Bkz: [Takım Gezgini'nde iş](http://msdn.microsoft.com/library/fd7a5cf7-7916-4fa0-b5e6-5a83cf377a02).

-   **NuGet:** Visual Studio ve Visual Studio için Blend hem NuGet paketlerini yönetebilirsiniz. NuGet paketleri bir çözümden kaldırılması ve yüklenmesine basitleştirir .NET Framework için bir paket yöneticisidir.

## <a name="advanced-capabilities-in-blend-for-visual-studio"></a>Visual Studio için blend'de Gelişmiş Özellikler
 Üretkenliğinizi artırmak için aşağıdaki görevler için Visual Studio için Blend kullanarak göz önünde bulundurun. Bu, Visual Studio için Blend, daha fazla hız ve Visual Studio Tasarımcısı veya tek başına bir kod işlevsellik burada sunar alanlardır.

|Bitiş|Visual Studio|Visual Studio için Blend|Daha fazla bilgi|
|--------|-------------------|-----------------------------|----------------------|
|**Animasyonlar oluşturma**|Animasyon için tasarım aracı yoktur; bunları programlı olarak oluşturmanız gerekir. Bu, animasyon ve zamanlama sistemine WPF ve kodlama kapsamlı uzmanlığını'nın bilinmesini gerektirir.|Görsel animasyonlar oluşturur ve bunları Visual Studio için blend'de önizlemesini görebilirsiniz. Bu daha hızlı ve kod içinde animasyonları oluşturmak daha kesin değildir. Kullanıcı etkileşimi işlemek için Tetikleyiciler ekleyebilir ve olay işleyicileri ve diğer işlevler eklemek için kod geçiş yapabilirsiniz.|[Nesnelere animasyon ekleme](../designers/animate-objects-in-xaml-designer.md)|
|**Şekil ve metinler yolları daha kolay düzenlemesi için dönüştürün**|Desteklenmez.|Daha iyi düzenleme denetimi sağlayan yollar dönüştürerek (örneğin, dikdörtgenler ve elipsler) şekillere ince veya çarpıcı değişiklikler yapabilirsiniz.  Şekillendirmek veya yolları birleştirme ve birden çok şekillerden bileşik yollar oluşturabilir.<br /><br /> Ayrıca metin blokları vektör görüntüleri yönetileceğini yolları dönüştürebilirsiniz.|[Şekiller ve yollar çizme](../designers/draw-shapes-and-paths.md)|
|**UI tasarımlarınızı etkileşim ekleme**|C#, Visual Basic veya C++ kod gerektirir.|Davranışlar statik tasarımlarınızı etkileşim eklemek için denetimleri üzerine sürükleyip yeniden açın. Davranışlar, sürükle ve bırak, yakınlaştırma ve görsel durum değişiklikleri gibi işlevi kapsülleyen kullanıma hazır kod parçacıkları verilmiştir. Aralarından seçim yapabileceğiniz davranışları büyüyen bir dizi yoktur ve kendi oluşturabilirsiniz.<br /><br /> Her davranışı, Visual Studio için blend'de özelliklerini değiştirerek veya olay işleyicileri ekleme kodu daha sonra özelleştirebilirsiniz.|[Denetimler ekleme ve bunların davranışlarını değiştirme](../designers/insert-controls-and-modify-their-behavior-in-xaml-designer.md)|
|**Adobe resmi kullanın**|Desteklenmez.|Adobe FXG, PhotoShop veya Illustrator resmi almak ve Visual Studio için blend'de kullanıcı arabirimini uygulayın.|[Görüntü, video ve ses klipleri ekleme](../designers/insert-images-videos-and-audio-clips-in-xaml-designer.md)|
|**Denetimleri, şablonlar ve stiller Düzenle**|Kodlama ve WPF stilleri ve şablonları bilinmesini gerektirir.|Herhangi bir görüntü denetime açın.<br /><br /> Denetimleri, stilleri ve şablonları ile yalnızca birkaç tıklamayla değişiklik yapmak için şablon düzenleme araçlarını kullanın.<br /><br /> Örneğin, Visual Studio stili kaynak için Blend (örneğin, düğmeler, liste kutuları, kaydırma çubukları, menüler, vb.) ortak WPF denetimleri uygulayın ve bunların renk, stil veya doğrudan Visual Studio için blend'de temel alınan şablonu değiştirmek için kullanabilirsiniz. İsterseniz daha sonra Son dokunuşları kodunu geçiş yapabilirsiniz.|[Nesnelerin stilini değiştirme](../designers/modify-the-style-of-objects-in-blend.md)|
|**Kullanıcı Arabirimi verilere bağlanma**|SQL Server veritabanları, WCF veya web Hizmetleri, nesneler veya SharePoint listeleri gibi bir veri kaynağı oluşturun ve veri kaynağı, kullanıcı Arabirimi denetimlerine bağlama.<br /><br /> Tasarım zamanı veri bir etkileşimli bir tasarımı deneyimi için el ile oluşturulması gerekir.|Örnek veriler prototip oluşturma ve sınama için kolayca oluşturun. Hazır olduğunuzda Canlı verilere geçme.<br /><br /> Blend için Visual Studio'nun veri oluşturma özellikleri bekleyen (ekleyebileceğiniz adlar, sayılar, URL'ler, hareket halindeyken için bir kolayca fotoğraf), çok zaman tasarruf edebilirsiniz.<br /><br /> Canlı verileri için bir XML dosyasına veya herhangi bir CLR veri kaynağı için kullanıcı Arabirimi denetimleri bağlayabilirsiniz.|[Verileri görüntüleme](../designers/display-data-in-blend.md)|

 Gelişmiş XAML tasarımı hakkında daha fazla bilgi için bkz. [Visual Studio için Blend’i kullanarak kullanıcı arabirimi oluşturma](../designers/creating-a-ui-by-using-blend-for-visual-studio.md)
