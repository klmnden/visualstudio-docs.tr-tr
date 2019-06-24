---
title: Visual Studio 2019’daki yenilikler
titleSuffix: ''
description: Visual Studio 2019'deki yeni özellikler hakkında bilgi edinin.
ms.date: 05/22/2019
helpviewer_keywords:
- Visual Studio, what's new
- what's new [Visual Studio]
ms.assetid: 00bec66b-bcee-46f5-91d9-f73a2b469744
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.prod: visual-studio-windows
ms.technology: vs-ide-general
ms.topic: conceptual
ms.workload:
- multiple
ms.openlocfilehash: 7df082d8cf67a5c0eb4c6ecd5c017480c63a6b27
ms.sourcegitcommit: 7eb2fb21805d92f085126f3a820ac274f2216b4e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/22/2019
ms.locfileid: "67328825"
---
# <a name="whats-new-in-visual-studio-2019"></a>Visual Studio 2019’daki yenilikler

**İçin güncelleştirilmiş [16.1 sürüm](/visualstudio/releases/2019/release-notes/)**

>[!div class="button"]
>[Visual Studio 2019’u İndirin](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2019)

Visual Studio 2019 ile tüm geliştiriciler, herhangi bir uygulama ve herhangi bir platform için sınıfının en iyisi Araçlar ve hizmetler elde edersiniz. Visual Studio ilk kez kullanıyorsanız veya bu yıl için kullanmakta olduğunuz bu yeni sürümde beğenmek çok yoktur!

Yeniliklerin üst düzey bir özeti aşağıda verilmiştir:

* **[Geliştirme](#develop)** : Odaklı ve Gelişmiş performans, anında kod temizleme ve daha iyi arama sonuçları ile üretken kalın.
* **[İşbirliği](#collaborate)** : Bir Git öncelikli iş akışı, düzenleme ve hata ayıklama, gerçek zamanlı doğal işbirliği keyfini çıkarın ve sağa doğru Visual Studio'da kod incelemeleri.
* **[Hata ayıklama](#debug)** : Vurgulayın ve belirli değerlere gidin, bellek kullanımı iyileştirin ve uygulamanızın yürütme otomatik anlık.

Bu sürümdeki yenilikler tam listesini her şey için bkz: [sürüm notları](/visualstudio/releases/2019/release-notes/).

## <a name="develop"></a>Geliştirme

Yeni özelliklerle zaman kazandırır.
<br><br>
> [!VIDEO https://www.youtube.com/embed/n5sJ4EewKGk]

### <a name="improved-search"></a>Geliştirilmiş arama

Hızlı Başlatma eski adıyla bilinen yeni arama deneyimimizi daha hızlı ve daha etkili. Şimdi, siz yazarken arama sonuçlarını dinamik olarak görünür. Ve, böylece bunları gelecekte kullanım için daha kolay ezberleme arama sonuçları genellikle komutları için klavye kısayolları içerebilir.

   ![Visual Studio 2019 yeni arama deneyimini ilişkin bir animasyon](media/vs-2019/new-search-feature.gif)

Yeni belirsiz arama mantık hatalarını bağımsız olarak gereken her şeyi bulabilirsiniz. Komutlar, ayarları, belgeleri veya diğer faydalı bir şey için arıyorsanız, bu nedenle, yeni arama özelliğini aradığınızı bulmayı kolaylaştırır.

### <a name="refactorings"></a>Yeniden düzenlemeler

Çok sayıda yeni ve yüksek oranda yararlı yeniden düzenlemeler vardır C# kolaylaştırmak kodunuzu düzenleme şeklinizdir. Bunlar ampul, önerileri gösterme ve üyeleri arabirimi veya temel sınıfına taşımadan gibi eylemler dahil, ad alanları için ayarlama klasör yapısı, foreach döngü LINQ sorguları ve daha fazla bilgi için dönüştürme.

   ![Visual Studio 2019 yeniden düzenlemeler deneyiminin animasyon](media/vs-2019/refactorings.gif)

Tuşlarına basarak yeniden düzenlemeler yalnızca çağırma **Ctrl +.** ve gerçekleştirmek istediğiniz eylemi seçme.

### <a name="intellicode"></a>IntelliCode

[Visual Studio Intellicode](/visualstudio/intellicode/) yapay zeka (AI) kullanarak, yazılım geliştirme çalışmalarını geliştirir. GitHub üzerinde 2.000 açık kaynak projeler arasında Intellicode trenler&mdash;her 100'den fazla Yıldıza sahip&mdash;önerilerini oluşturmak için.

 ![Intellicode Visual Studio 2019 içinde'bir animasyon](media/vs-2019/IntelliCode.gif)

Visual Studio Intellicode üretkenliğinizi artırmaya yardımcı olabilir, birkaç yolu vardır:

* Bağlama duyarlı kod tamamlama sunun
* Ekip stillerini ve desenleri uyması için Geliştirici Kılavuzu
* Catch zor kod sorunlarını bulun
* Açısından gerçekten önemli olan alanlara dikkat çekmek tarafından odağı kod incelemeleri

Biz başlangıçta yalnızca desteklenen C# zaman biz öncelikle önizlemesi Intellicode bir uzantısı olarak Visual Studio için. Şimdi, **16.1 yeni**, için destek ekledik C# ve XAML "içinde hazır". (Desteği C++ ve TypeScript/JavaScript olan hala Önizleme aşamasındadır ancak.)

Ve kullanıyorsanız C#, kendi kod üzerinde özel bir model eğitip özelliği de ekledik.

Intellicode hakkında daha fazla bilgi için bkz. [Intellicode artı kısaca genel kullanıma sunulma Duyurusu](https://devblogs.microsoft.com/visualstudio/announcing-the-general-availability-of-intellicode-plus-a-sneak-peek/) ve [daha fazla kod, daha az Visual Studio Intellicode kaydırma](https://devblogs.microsoft.com/visualstudio/code-more-scroll-less-with-visual-studio-intellicode/) blog gönderilerimize göz atın.

### <a name="code-cleanup"></a>Kodu temizleme

Yeni bir belge sistem durumu göstergesi ile eşleştirilmiş bir yeni kod temizleme komutudur. Bu yeni komut belirlemek ve ardından uyarılar hem bir düğmeye tıklayarak önerileri gidermek için kullanabilirsiniz.

Temizleme kodunu biçimlendirmek ve herhangi kod düzeltmeleri tarafından önerilen uygulama [geçerli ayarları](code-styles-and-code-cleanup.md) ve [.editorconfig dosyalarını](create-portable-custom-editor-options.md).

   ![Visual Studio 2019 yeni kod temizleme denetimi görüntüsü](media/vs-2019/code-cleanup-profile.png)

Ayrıca, düzelticiden koleksiyonları bir profil kaydedebilirsiniz. Örneğin, küçük bir kod sık uygulanan hedeflenen düzelticiden sahip, ve ardından başka bir kapsamlı bir kod incelemesi önce uygulanacak düzelticiden varsa, profilleri bu farklı görevler ele almak için yapılandırabilirsiniz.

   ![Visual Studio 2019 yapılandırma kod temizleme denetimi görüntüsü](media/vs-2019/code-cleanup-profile-configure.png)

### <a name="per-monitor-aware-pma-rendering"></a>İzleyici başına kullanan (PMA) oluşturma

Farklı görüntüleme ölçek faktörlerle yapılandırılan izleyiciler kullanın veya ana cihazınızın farklı ekran ölçek faktörleri bir makineye uzaktan bağlanın, Visual Studio bulanık görünüyor veya yanlış ölçekte işler fark edebilirsiniz.

Visual Studio 2019'ın yayınlanmasıyla birlikte, uyumlu (PMA) uygulamasını İzle Visual Studio yapıyoruz. Artık, Visual Studio, kullandığınız görüntü ölçek Etkenler bağımsız olarak doğru şekilde işler.

   ![Visual Studio 2019 İzleyici başına kullanan (PMA) oluşturma](media/vs-2019/pma-dpi-scaling.png)

Daha fazla bilgi için [daha iyi bir Visual Studio 2019 çoklu monitör deneyimiyle](https://devblogs.microsoft.com/visualstudio/a-better-multi-monitor-experience-with-visual-studio-2019/) blog gönderisi.

## <a name="collaborate"></a>İşbirliği

Sorunları çözmek için güçlerini birleştirdi.
<br><br>
> [!VIDEO https://www.youtube.com/embed/dKLJsiK1QU8]

### <a name="cloud-first-workflow"></a>Bulut öncelikli iş akışı

Visual Studio 2019 açtığınızda fark edeceksiniz, yeni bir başlangıç penceresi bir şeydir.

   ![Yeni Visual Studio 2019 başlangıç penceresi görüntüsü](media/vs-2019/start-window-dark.png)

Başlangıç penceresi koduna hızlı bir şekilde almak için çeşitli seçenekler sunar. Biz, kopyalama veya bir depo koddan önce teslim seçeneği koyduğunuz.

   ![Visual Studio 2019 'Git-first' deneyiminin animasyon](media/vs-2019/git-first.gif)

Başlangıç penceresi, ayrıca bir projeyi veya çözümü açın, yerel bir klasöre açın veya yeni bir proje oluşturmak için seçenekleri içerir.

Daha fazla bilgi için [kodu alın: Yeni Visual Studio başlangıç penceresi nasıl tasarladığımız](https://devblogs.microsoft.com/visualstudio/get-to-code-how-we-designed-the-new-visual-studio-start-window/) blog gönderisi.

### <a name="live-share"></a>Live Share

[Visual Studio Canlı Paylaşım](https://visualstudio.microsoft.com/services/live-share/) bir kod temeli ve onun bağlamı arkadaşınızla paylaşın ve Visual Studio'dan doğrudan anlık çift yönlü işbirliği elde etmenize olanak tanıyan bir geliştirici hizmetidir. Live Share ile bir teammate okuma gidin, düzenlemek ve onlarla paylaştıktan bir projede hata ayıklamak ve sorunsuz ve güvenli bir şekilde bunu.

Ve Visual Studio 2019'ile bu hizmet, varsayılan olarak yüklenir.

![LiveShare işbirliği özelliği Visual Studio 2019 gösteren bir animasyonu](media/vs-2019/live-share.gif)

Daha fazla bilgi için [Visual Studio Live Share gerçek zamanlı kod incelemeleri ve etkileşimli eğitim için](https://devblogs.microsoft.com/visualstudio/visual-studio-live-share-for-real-time-code-reviews-and-interactive-education/) blog gönderisi ve [LiveShare artık ile Visual Studio 2019 dahil](https://devblogs.microsoft.com/visualstudio/live-share-now-included-with-visual-studio-2019/) blog gönderisi.

### <a name="integrated-code-reviews"></a>Tümleşik kod incelemeleri

Visual Studio 2019 ile kullanmak için indirebileceğiniz yeni bir uzantı kullanıma sunduğumuz. Bu yeni uzantısıyla gözden geçirin, çalıştırın ve bile çekme istekleri takımınız Visual Studio'dan ayrılmanıza gerek kalmadan hata ayıklama. Hem Azure DevOps, hem de GitHub depolarında kod destekliyoruz.

   ![Yeni Visual Studio 2019 başlangıç penceresi görüntüsü](media/vs-2019/pr-experience.png)

Daha fazla bilgi için [kod incelemeleri Visual Studio çekme istekleri uzantısını kullanarak](https://devblogs.microsoft.com/visualstudio/code-reviews-using-the-visual-studio-pull-requests-extension/) blog gönderisi.

## <a name="debug"></a>Hata ayıklama

Kesin hedefleyen oturum sıfır.
<br><br>
> [!VIDEO https://www.youtube.com/embed/hr72Fs8n_9c]

### <a name="performance-gains"></a>Performans kazancı elde edildi

Biz özel bir kez C++ veri kesme noktaları alınır ve bunları .NET Core uygulamaları için uyarlanmış.

   ![Hata ayıklama Visual Studio 2019 veri kesme noktaları gösteren bir animasyonu](media/vs-2019/debug-data-breakpoints.gif)

Veri kesme noktaları, mi, C++ veya .NET Core kodlamaya şekilde, yalnızca normal kesme noktaları yerleştirmek için iyi bir alternatif olabilir. Veri kesme noktaları ayrıca genel nesne değiştirildiği yerdir bulma gibi senaryoları veya eklenmesi veya bir listeden kaldırılması için mükemmel özellikler.

Ayrıca, kimin büyük uygulamalar geliştiren bir C++ geliştiricisiyseniz, Visual Studio 2019 simgeler dışında bellekle ilgili sorunları yaşayan olmadan bu uygulamalarda hata ayıklama olanak tanıyan proc yaptı.

### <a name="search-while-debugging"></a>Hata ayıklama sırasında arama

Büyük olasılıkla daha önce bir değerler kümesi arasında bir dize için izleme penceresinde bakarak o yollardan geçtik. Visual Studio 2019 ' nesneleri ve aradığınız değerlerini bulmanıza yardımcı olmak için izleme, Yereller ve Otomatikler windows Search'te ekledik.

   ![Visual Studio 2019 içinde hata ayıklama arama penceresini gösteren bir animasyonu](media/vs-2019/debug-window-search.gif)

Ayrıca, bir değer İzle, Yereller ve Otomatikler pencereleri içinde nasıl görüntüleneceğini biçimlendirebilirsiniz.  Herhangi bir windows öğelerden birine çift tıklayın ve bir virgül ekleyin (",") olası biçim belirticileri aşağı açılan listesi erişmek için her biri hedeflenen etkisini açıklamasını içerir.

   ![Yeni İzleme penceresi ve biçim değerleri özelliği Visual Studio 2019](media/search-watch-window.png)

Daha fazla bilgi için [geliştirilmiş Visual Studio 2019 içinde: Nesnelerle ve özelliklerle izleyin, Otolar ve yerel öğeler Windows Arama](https://devblogs.microsoft.com/visualstudio/enhanced-in-visual-studio-2019-search-for-objects-and-properties-in-the-watch-autos-and-locals-windows/) blog gönderisi.

### <a name="snapshot-debugger"></a>Anlık görüntü hata ayıklayıcısı

Bulutta tam olarak neler olduğunu görmek için uygulamanızın yürütmesini anlık görüntüsünü alın. (Bu özellik, yalnızca Visual Studio Enterprise'da kullanılabilir.)

   ![Visual Studio 2019 Enterprise'da Snapshot Debugger'ı gösteren bir animasyonu](media/vs-2019/snapshot-debugger.gif)

Bir Azure sanal makinesinde çalışan ASP.NET (Çekirdeği ve Masaüstü) uygulamaları hedeflemek için destek ekledik. Ayrıca, bir Azure Kubernetes Service'te çalışan uygulamalar için destek ekledik. Snapshot Debugger, üretim ortamlarında ortaya çıkan sorunları çözmek için gereken süreyi ciddi ölçüde azaltmaya yardımcı olabilir.

Daha fazla bilgi için bkz. [Snapshot Debugger'ı kullanarak canlı ASP.NET Azure uygulamaları için hata ayıklama](../debugger/debug-live-azure-applications.md) sayfasında ve [Giriş zaman seyahat hata ayıklamak için Visual Studio Enterprise 2019](https://devblogs.microsoft.com/visualstudio/introducing-time-travel-debugging-for-visual-studio-enterprise-2019/) blog gönderisi.

## <a name="whats-next"></a>Yenilikler

Visual Studio 2019 genellikle, geliştirme deneyimini daha da iyi hale getirebilir yeni özelliklerle güncelleştiriyoruz. Bizim en son yenilikler hakkında daha fazla bilgi edinmek için kullanıma [Visual Studio blogu](https://devblogs.microsoft.com/visualstudio/). Ve hangi tarih önizlemede yayımladık kayıt için göz atın [Preview sürüm notları](/visualstudio/releases/2019/release-notes-preview/).

Daha fazla Visual Studio 2019 işe ne hakkında olduğunu öğrenmek istiyorsunuz? Bkz: [Visual Studio yol haritası](/visualstudio/productinfo/vs-roadmap/).

## <a name="give-us-feedback"></a>Geri bildirimde bulunun

Neden Visual Studio ekibine geri bildirim gönderilsin mi? Size müşteri geri bildirimi ciddiye olduğundan. Ne yapıyoruz çoğunu yürütür.

* Visual Studio nasıl geliştirebileceğimizi ilgili öneride bulunmak istiyorsanız, bunu kullanarak yapabilirsiniz [özellik önerin](suggest-a-feature.md) aracı.

* Bir yanıt vermemesine, kilitlenme veya diğer performans sorunu yaşarsanız, kolayca yineleme adımları ve destekleyici dosyaları bizimle kullanarak paylaşabilirsiniz [sorun bildir](how-to-report-a-problem-with-visual-studio.md) aracı.

## <a name="see-also"></a>Ayrıca bkz.

* [Visual Studio 2019 Duyurusu](https://devblogs.microsoft.com/visualstudio/visual-studio-2019-code-faster-work-smarter-create-the-future/)
* [Visual Studio 2019 sürüm notları](/visualstudio/releases/2019/release-notes/)
* [Visual Studio 2019 SDK'da yenilikler nelerdir?](../extensibility/whats-new-visual-studio-2019-sdk.md)
* [Mac için Visual Studio 2019 kullanıma sunuldu](https://devblogs.microsoft.com/visualstudio/visual-studio-2019-for-mac-is-now-available/)
* [Microsoft yapı 2019 konferansı](https://www.microsoft.com/build)
* [Microsoft Connect(); 2018 conference](https://www.microsoft.com/connectevent)
