---
title: Visual Studio için Mac turu
description: Mac için Visual Studio, ASP.NET Core Web siteleri ve iOS, Android, Mac ve Xamarin.Forms için Xamarin projeleri dahil olmak üzere, macOS üzerinde .NET uygulama derlemek için bir tümleşik geliştirme ortamı sağlar.
author: conceptdev
ms.author: crdun
ms.date: 02/07/2019
ms.assetid: 7DC64A52-AA41-4F3A-A8A1-8A20BCD81CC7
ms.custom: video
ms.openlocfilehash: 4f3c868edb19cc45e25d73a11e7a65ead37c0b11
ms.sourcegitcommit: 752f03977f45169585e407ef719450dbe219b7fc
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2019
ms.locfileid: "56316736"
---
# <a name="visual-studio-2017-for-mac-preview-tour"></a>Visual Studio 2017 için Mac Önizleme turu

> [!NOTE]
> Mac için Visual Studio 2019 olduğunu [sunuldu](installation.md) test etmek için Önizleme olarak.

Mac için Visual Studio, bir .NET _tümleşik geliştirme ortamı_ düzenlemek için kullanılabilecek Mac üzerinde hata ayıklama ve kod derleme ve ardından bir uygulama yayımlayın. Standart Düzenleyici ve hata ayıklayıcı, gibi beklenen özelliklerine ek olarak Mac için Visual Studio derleyicileri, kod tamamlama araçları, grafik tasarımcıları ve ese yazılım geliştirme süreci için kaynak denetimi içerir.

Mac için Visual Studio destekleyen birçok Windows karşılığı ile aynı dosya türleri gibi `.csproj`, `.fsproj`, veya `.sln` dosyaları ve sizin için en uygun IDE'yi kullanabileceğiniz anlamına gelir, EditorConfig gibi özellikleri destekler.
Windows üzerinde Visual Studio önceden kullanılmış herkes için tanıdık bir deneyim, oluşturma, açma ve uygulama geliştirme olacaktır. Ayrıca, Mac için Visual Studio, çok güçlü bir IDE Windows çözümlemesiyle olun güçlü araçları kullanır. Roslyn derleyici platformu, yeniden düzenleme ve IntelliSense için kullanılır. MSBuild proje sistemi ve yapı altyapısı kullanın ve kaynak düzenleyicisinin TextMate paketi gruplarını destekler. Aynı hata ayıklayıcı altyapıları için Xamarin ve .NET Core uygulamaları ve aynı tasarımcıları Xamarin.iOS ve Xamarin.Android için kullanır.

## <a name="what-can-i-do-in-visual-studio-for-mac"></a>Visual Studio'da Mac için neler yapabilirim

Mac için Visual Studio geliştirme aşağıdaki türlerini destekler:

- ASP.NET Core web uygulamaları ile C#, F#ve Razor sayfaları, JavaScript ve TypeScript desteği
- .NET core konsol uygulamaları ile C# veyaF#
- Platformlar arası Unity oyunları ve uygulamalarıC#
- Xamarin ile Android, iOS, tvOS ve watchOS uygulamaları C# veya F# ve XAML
- Cocoa masaüstü uygulamalarında C# veyaF#

Bu makalede, bazı bu uygulamaları oluşturmak için güçlü bir araç hale getiren özellikler sağlayan Mac için Visual Studio çeşitli bölümlerini keşfediyor.

## <a name="ide-tour"></a>IDE turu

Mac için Visual Studio, uygulama dosyalarını ve ayarlarını yönetme, uygulama kodu oluşturma ve hata ayıklama için çeşitli bölümler halinde düzenlenmiştir.

## <a name="welcome-screen"></a>Hoş Geldiniz ekranı

Mac için Visual Studio başlatıldığında, görüntüler bir *Hoş Geldiniz ekranı*:

![Hoş Geldiniz ekranı](media/ide-tour-image1.png)

Hoş Geldiniz ekranında aşağıdaki bölümleri içerir:

- **Araç çubuğu** -Arama çubuğuna hızlı erişim sağlar. Bir çözüm yüklendiğinde, araç, hata ayıklama ve hataları görüntülemek için uygulama yapılandırmaları ayarlamak için kullanılır.
- **Başlarken** -Mac için Visual Studio ile çalışmaya başlama geliştiriciler için yararlı konularını hızlı erişim sağlar
- **Son çözümleri** -açın veya projeleri oluşturmak için uygun düğmeleri yanı sıra, en son açılan çözümleri hızlı erişim sağlar.
- **Geliştirici Haberleri** -en son Microsoft Developer bilgiler, güncel tutar bir haber akışı.

## <a name="solutions-and-projects"></a>Projeler ve Çözümler

Aşağıdaki görüntüde, Mac için Visual Studio ile yüklenen bir uygulama gösterilmektedir:

![Yüklü bir uygulama ile Mac için Visual Studio](media/ide-tour-image17.png)

Aşağıdaki bölümler, Mac için Visual Studio temel alanları genel bir bakış sağlar

## <a name="solution-pad"></a>Çözüm bölmesi

Çözüm panelinde bir çözümdeki projelerin düzenler:

![Çözüm panelinde düzenlenmiş projeleri](media/ide-tour-image18.png)

Dosya kaynak kodu, kaynakları, kullanıcı arabirimi ve bağımlılıkları için platforma özgü projelere burada düzenlenir budur.

Projeler ve çözümler, Mac için Visual Studio kullanarak daha fazla bilgi için bkz: [projeler ve çözümler](/visualstudio/mac/projects-and-solutions) makalesi.

## <a name="assembly-references"></a>Derleme başvuruları

Her proje için derleme başvuruları, başvuruları klasörünün altında mevcuttur:

![Çözüm Bölmesi'nde başvurular klasörünün](media/ide-tour-image19.png)

Ek başvurular kullanarak eklenir **başvuruları Düzenle** başvuruları klasörü çift tıklayarak ya da seçerek görüntülenen iletişim kutusunda **başvuruları Düzenle** kendi bağlam menüsünde eylemleri:

![Başvurular iletişim Düzenle](media/ide-tour-image20.png)

Başvurular, Mac için Visual Studio kullanarak daha fazla bilgi için bkz: [bir projedeki başvuruları yönetme](/visualstudio/mac/managing-references-in-a-project) makalesi.

## <a name="dependencies--packages"></a>Bağımlılıkları / paketleri

Uygulamanızda kullanılan tüm dış bağımlılıkları içinde bir.Net Core olmanıza bağlı olarak bağımlılıklar veya paketler klasöründe depolanır veya Xamarin.iOS/Xamarin.Android projesi. Bunlar, genellikle bir NuGet biçiminde sağlanır.

NuGet, .NET geliştirme için en popüler paket yöneticisidir. Visual Studio'nun NuGet desteği ile kolayca arayabilir ve paketleri uygulaması projenize ekleyin.

Uygulamanıza bir bağımlılık eklemek için bağımlı sağ / paketleri klasörünü açın ve seçin **paketleri Ekle**:

![Bir NuGet paketi ekleme](media/ide-tour-image21.png)

Bir uygulamada bir NuGet paketi kullanarak bilgi bulunabilir [projenizdeki bir NuGet dahil olmak üzere proje](/visualstudio/mac/nuget-walkthrough) makalesi.

## <a name="refactoring"></a>Yeniden Düzenle

Mac için Visual Studio, kodunuzu yeniden değiştirmenin iki kullanışlı yöntem sağlar: Bağlam Eylemler ve kaynak çözümleme. Daha fazla ilgili [yeniden düzenleme](/visualstudio/mac/refactoring) makalesi.

## <a name="debugging"></a>Hata Ayıklama

Mac için Visual Studio yerel hata ayıklayıcı bir izin verme hata ayıklama desteği Xamarin.iOS ve Xamarin.Mac Xamarin.Android uygulamaları için sahiptir. Mac için Visual Studio, Mono yazılım Mono çalışma zamanına uygulanan, IDE, tüm platformlar arasında hata ayıklama yönetilen kodu izin verme hata ayıklayıcıyı kullanır. Hata ayıklama hakkında ek bilgi için ziyaret edin [hata ayıklama](/visualstudio/mac/debugging) makalesi.

Hata ayıklayıcısı dizeleri, renkler, URL'ler, hem de boyutları, ortak ordinates ve bézier eğriler gibi özel türler için zengin görselleştiriciler içerir.

Hata Ayıklayıcı'nın veri görselleştirmeleri hakkında daha fazla bilgi için ziyaret [veri görselleştirmeleri](/visualstudio/mac/data-visualizations) makalesi.

## <a name="version-control"></a>Sürüm Denetimi

Mac için Visual Studio, Git, Subversion kaynak denetimi sistemleriyle tümleştirilir. Kaynak denetimi altında proje, çözüm adının yanında listelenen dal ile belirtilir:

![Kaynak denetimi altında proje belirtmek için dal adı](media/ide-tour-image22.png)

Dosyaları kaydedilmemiş değişikliklerle bir ek açıklama simgelerine çözüm bölmesinde üzerinde aşağıdaki görüntüde gösterildiği gibi sahiptir:

![Çözüm panelinde kaydedilmemiş dosyaları](media/ide-tour-image23.png)

Visual Studio'da sürüm denetimini kullanma ile ilgili daha fazla bilgi için bkz: [sürüm denetimi](/visualstudio/mac/version-control) makalesi.

## <a name="related-video"></a>İlgili Video

> [!Video https://channel9.msdn.com/Shows/Visual-Studio-Toolbox/Visual-Studio-for-Mac-Overview/player]


## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio IDE (üzerinde Windows)](/visualstudio/ide/visual-studio-ide)
