---
title: Visual Studio 2019’daki yenilikler
titleSuffix: ''
description: Visual Studio 2019'deki yeni özellikler hakkında bilgi edinin.
ms.date: 02/27/2019
helpviewer_keywords:
- Visual Studio, what's new
- what's new [Visual Studio]
ms.assetid: 00bec66b-bcee-46f5-91d9-f73a2b469744
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.prod: visual-studio-dev16
ms.topic: conceptual
ms.workload:
- multiple
ms.openlocfilehash: 5fdde6a34d3985c0e77cc9e84c58618a093ca365
ms.sourcegitcommit: 62149c96de0811415e99bb1e0194e76c320e1a1e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/28/2019
ms.locfileid: "57007286"
---
# <a name="whats-new-in-visual-studio-2019"></a>Visual Studio 2019’daki yenilikler

**İçin güncelleştirilmiş [Sürüm Adayı (RC)](/visualstudio/releases/2019/release-notes/)**

>[!div class="button"]
>[RC'yi indirin](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2019)

Visual Studio 2019 Geliştirici üretkenliği ve işbirliğini en iyi duruma getirme yeni özelliklerin yanı sıra birçok genel iyileştirmeler içerir. Visual Studio'yu ilk kez kullanıyorsanız veya bu yıl için kullanmakta olduğunuz geliştirme yaşam döngüsünün tüm yönleri için özelliklerinden yararlanmak mümkün olacaktır&mdash;Basitleştirilmiş proje oluşturma ve kod sistem durumu yönetimi team- ve açık kaynaklı işbirliğine dayalı iş akışları.<br/><br/>

>[!VIDEO https://channel9.msdn.com/Events/Connect/Microsoft-Connect--2018/D190/player]

Visual Studio sunmak olan, üst düzey bir özeti aşağıda verilmiştir:

* **[Kişisel ve takım üretkenliği](#personal-and-team-productivity)**. Üretkenliği en odaklamanızı herkes için.
* **[Modern geliştirme desteği](#modern-development-support)**. Geçerli projeleri ve gelecekteki çözümleri için destek.
* **[Sürekli yenilik](#continuous-innovation)**. Akıllı, bulut destekli desteğiyle akıllı kod.

> [!NOTE]
> Yeni özellikleri ve işlevleri Visual Studio 2019 tam listesi için bkz: [RC sürüm notları](/visualstudio/releases/2019/release-notes/) ve [Preview 4 sürüm notları](/visualstudio/releases/2019/release-notes-preview/). Hem bu yeni sürümleri hakkında daha fazla bilgi için bkz. [Visual Studio 2019 Sürüm Adayı sunuldu](https://devblogs.microsoft.com/visualstudio/visual-studio-2019-release-candidate-rc-now-available/) blog gönderisi.

## <a name="personal-and-team-productivity"></a>Kişisel ve takım üretkenliği

Bunun bir performans geliştirmeleridir önde gelen sorunlardır Visual Studio'nun her sürümü ile ancak bunu orada tam üretkenliğinizi artırmak koşuluyla. İşte nasıl ile yardımcı olabiliriz.

### <a name="new-start-window"></a>Yeni başlangıç penceresi

Visual Studio 2019 açtığınızda fark edeceksiniz ilk şey, yeni bir başlangıç penceredir.

   ![Yeni Visual Studio 2019 başlangıç penceresi](media/start-window.png)

Bu yeni başlangıç penceresi kopyalama veya kullanıma alma kodu, bir projeyi veya çözümü açın, yerel bir klasöre açın veya yeni bir proje oluşturmak için seçenekler sunar. Basit bir iletişim kutusunda Bu seçeneklere sahip iki yeni başlayanlar yardımcı olur ve hızlı bir şekilde kod Gelişmiş Visual Studio kullanıcılarına alın.

Daha fazla bilgi için [kodu alın: Yeni Visual Studio başlangıç penceresi nasıl tasarladığımız](https://devblogs.microsoft.com/visualstudio/get-to-code-how-we-designed-the-new-visual-studio-start-window/) blog gönderisi.

### <a name="better-search"></a>Daha iyi arama

Hızlı Başlatma eski adıyla bilinen yeni arama deneyimimizi daha hızlı ve daha etkili. Şimdi, siz yazarken arama sonuçlarını dinamik olarak görünür. Ve bunları gelecekte kullanım için daha kolay ezberleme komutları için klavye kısayolları arama sonuçlarını içerir.

   ![Visual Studio 2019 yeni arama özelliği](media/search-feature.png)

Komutlar, ayarları, belgeleri veya diğer faydalı bir şey için aradığınız olsun, yeni arama özelliğini aradığınızı bulmayı kolaylaştırır.

### <a name="one-click-code-cleanup"></a>Tek tıklamayla kod temizleme

Yeni bir belge sistem durumu göstergesi ile eşleştirilmiş bir yeni kod temizleme komutudur. Bu yeni komut belirlemek ve ardından uyarılar hem bir düğmeye tıklayarak önerileri gidermek için kullanabilirsiniz.

   ![Visual Studio 2019 yeni kod temizleme özelliği](media/code-cleanup.png)

Temizleme kodunu biçimlendirmek ve herhangi kod düzeltmeleri tarafından önerilen uygulama [geçerli ayarları](code-styles-and-quick-actions.md), [.editorconfig dosyalarını](create-portable-custom-editor-options.md), veya [Roslyn Çözümleyicileri](../code-quality/roslyn-analyzers-overview.md).

### <a name="debugger-improvements"></a>Hata ayıklayıcı geliştirmeleri

#### <a name="search-within-a-watch-window-and-format-watch-values"></a>Bir Gözcü penceresi içinde arama ve Gözcü değerlerini biçimlendirme

Büyük olasılıkla daha önce bir değerler kümesi arasında bir dize için izleme penceresinde bakarak o yollardan geçtik. Visual Studio 2019 ' nesneleri ve aradığınız değerlerini bulmanıza yardımcı olmak için izleme, Yereller ve Otomatikler windows Search'te ekledik.

Ayrıca, bir değer İzle, Yereller ve Otomatikler pencereleri içinde nasıl görüntüleneceğini biçimlendirebilirsiniz.  Herhangi bir windows öğelerden birine çift tıklayın ve bir virgül ekleyin (",") olası biçim belirticileri aşağı açılan listesi erişmek için her biri hedeflenen etkisini açıklamasını içerir.

   ![Yeni İzleme penceresi ve biçim değerleri özelliği Visual Studio 2019](media/search-watch-window.png)

Daha fazla bilgi için [geliştirilmiş Visual Studio 2019 içinde: Nesnelerle ve özelliklerle izleyin, Otolar ve yerel öğeler Windows Arama](https://devblogs.microsoft.com/visualstudio/enhanced-in-visual-studio-2019-search-for-objects-and-properties-in-the-watch-autos-and-locals-windows/) blog gönderisi.

### <a name="visual-studio-live-share"></a>Visual Studio Canlı Paylaşım

[Visual Studio Canlı Paylaşım](https://visualstudio.microsoft.com/services/live-share/) bir kod temeli ve onun bağlamı arkadaşınızla paylaşın ve Visual Studio'dan doğrudan anlık çift yönlü işbirliği elde etmenize olanak tanıyan bir geliştirici hizmetidir. Live Share ile bir teammate okuma gidin, düzenlemek ve onlarla paylaştıktan bir projede hata ayıklamak ve sorunsuz ve güvenli bir şekilde bunu.

Ve Visual Studio 2019'ile bu hizmet, varsayılan olarak yüklenir.

![LiveShare işbirliği özelliği Visual Studio 2019 gösteren animasyonlu GIF dosyası](media/live-share-collaboration.gif)

Daha fazla bilgi için [Visual Studio Live Share gerçek zamanlı kod incelemeleri ve Etkileşimli Eğitim](https://devblogs.microsoft.com/visualstudio/visual-studio-live-share-for-real-time-code-reviews-and-interactive-education/) blog gönderisi.

## <a name="modern-development-support"></a>Modern geliştirme desteği

### <a name="manage-pull-requests-prs-from-the-ide"></a>Çekme isteklerini (Pr'ler) IDE'den yönetme

Visual Studio 2019 ile kullanmak için indirebileceğiniz yeni bir uzantı kullanıma sunduğumuz. Bu yeni uzantı ile gözden geçirebilir, çalıştırma ve çekme istekleri Visual Studio IDE'den çıkmadan bile takımınızdan debug [(tümleşik geliştirme ortamı)](../get-started/visual-studio-ide.md). Biz, kod bugün Azure depolarda destekler, ancak genel deneyimini iyileştirmek ve GitHub'ı desteklemek için genişletme.

Hemen kullanmaya başlamak için Yükle [Visual Studio için çekme istekleri](https://aka.ms/pr4vs) Visual Studio Market'ten uzantı.

### <a name="develop-with-net-core-3-preview"></a>.NET Core 3 Preview ile geliştirin

Visual Studio 2019'ın Önizleme sürümüne yapı destekler [.NET Core 3](https://dotnet.microsoft.com/download/dotnet-core/3.0) herhangi bir platform için uygulamalar. İOS ve Android, Xamarin ile mobil geliştirme .NET yanı sıra, platformlar arası C++ geliştirme artırmak ve desteklemek devam edeceğiz.

   ![Visual Studio 2019'de .NET Core 3 Önizleme uygulamaları geliştirin](media/dot-net-core-three-dev.png)

Daha fazla bilgi için şu sayfalara bakın:

* [.NET core 3 Önizleme 1](https://github.com/dotnet/core/blob/master/release-notes/3.0/preview/3.0.0-preview1.md) ve [.NET Core 3 Önizleme 2](https://github.com/dotnet/core/blob/master/release-notes/3.0/preview/3.0.0-preview2.md) sürüm notları
* [.NET Core 3 Önizleme 1 Duyurusu](https://blogs.msdn.microsoft.com/dotnet/2018/12/04/announcing-net-core-3-preview-1-and-open-sourcing-windows-desktop-frameworks/) ve [.NET Core 3 Önizleme 2 Duyurusu](https://blogs.msdn.microsoft.com/dotnet/2019/01/29/announcing-net-core-3-preview-2/) blog gönderileri

## <a name="continuous-innovation"></a>Sürekli yenilik

### <a name="per-monitor-aware-pma-rendering"></a>İzleyici başına kullanan (PMA) oluşturma

Farklı görüntüleme ölçek faktörlerle yapılandırılan izleyiciler kullanın veya ana cihazınızın farklı ekran ölçek faktörleri bir makineye uzaktan bağlanın, Visual Studio bulanık görünüyor veya yanlış ölçekte işler fark edebilirsiniz.

Visual Studio 2019'ın yayınlanmasıyla birlikte, size Visual Studio kullanan (PMA) uygulamasını İzle bilgilerinizin ilk adımları sürüyor. Biz ne bağımsız olarak kullandığınız ölçek Etkenler görüntüleme doğru bir şekilde işlemek Visual Studio sağlayacak konusundaki temel çalışmalar yerleştirme.

   ![Visual Studio 2019 İzleyici başına kullanan (PMA) oluşturma](media/per-monitor-aware-dpi-scaling.png)

Daha fazla bilgi için [daha iyi bir Visual Studio 2019 çoklu monitör deneyimiyle](https://devblogs.microsoft.com/visualstudio/a-better-multi-monitor-experience-with-visual-studio-2019/) blog gönderisi.

### <a name="visual-studio-intellicode"></a>Visual Studio IntelliCode

[Visual Studio Intellicode](/visualstudio/intellicode/) artifical zeka (AI) kullanarak yazılım geliştirme çalışmalarınızı geliştiren bir uzantısıdır. GitHub üzerinde 2.000 açık kaynak projeler arasında Intellicode trenler&mdash;her 100'den fazla Yıldıza sahip&mdash;önerilerini oluşturmak için.

Visual Studio Intellicode üretkenliğinizi artırmaya yardımcı olabilir, birkaç yolu vardır:

* Bağlama duyarlı kod tamamlama sunun
* Ekip stillerini ve desenleri uyması için Geliştirici Kılavuzu
* Catch zor kod sorunlarını bulun
* Açısından gerçekten önemli olan alanlara dikkat çekmek tarafından odağı kod incelemeleri

 ![IntelliSense Öneri örneği](media/intellicode-intellisense-suggestion.png)

Biz başlangıçta yalnızca desteklenen C# zaman biz öncelikle önizlemesi Intellicode uzantısı için Visual Studio. Şimdi, C++ ve XAML desteği Visual Studio'da çok ekledik.

Ve kullanıyorsanız C#, kendi kod üzerinde özel bir model eğitip özelliği de ekledik.

En yeni güncelleştirmeleri hakkında daha fazla bilgi için bkz. [Visual Studio Intellicode, daha fazla dili destekleyen ve kodunuzdan öğrenir](https://devblogs.microsoft.com/visualstudio/visual-studio-intellicode-supports-more-languages-and-learns-from-your-code/) blog gönderisi. Ve uzantısı ve karşıdan yükleme hakkında daha fazla bilgi için bkz. [Visual Studio Intellicode - Preview](https://go.microsoft.com/fwlink/?linkid=872707) Microsoft DevLabs sayfasında.

## <a name="give-us-feedback"></a>Geri bildirimde bulunun

Neden Visual Studio ekibine geri bildirim gönderilsin mi? Size müşteri geri bildirimi ciddiye olduğundan. Ne yapıyoruz çoğunu yürütür.

* Visual Studio nasıl geliştirebileceğimizi ilgili öneride bulunmak istiyorsanız, bunu kullanarak yapabilirsiniz [bir öneride](talk-to-us.md#i-want-to-make-a-suggestion-about-visual-studio-features) aracı.

* Bir yanıt vermemesine, kilitlenme veya diğer performans sorunu yaşarsanız, kolayca yineleme adımları ve destekleyici dosyaları bizimle kullanarak paylaşabilirsiniz [sorun bildir](talk-to-us.md#i-want-to-report-a-problem-with-visual-studio) aracı.

## <a name="see-also"></a>Ayrıca bkz.

* [Visual Studio 2019 sürüm notları](/visualstudio/releases/2019/release-notes/)
* [Visual Studio 2019 SDK'da yenilikler nelerdir?](../extensibility/whats-new-visual-studio-2019-sdk.md)
* [Microsoft Connect(); 2018 conference](https://www.microsoft.com/connectevent)
* [Visual Studio 2017'deki yenilikler](whats-new-visual-studio-2017.md)
