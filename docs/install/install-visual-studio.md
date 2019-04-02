---
title: Visual Studio'yu yükleme
titleSuffix: ''
description: Visual Studio, adım adım yüklemeyi öğrenin.
ms.date: 03/30/2019
ms.custom: seodec18
ms.topic: conceptual
f1_keywords:
- vs.about
helpviewer_keywords:
- install Visual Studio
- dev15
- set up Visual Studio
- Visual Studio setup
- Visual Studio installer
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.prod: visual-studio-windows
ms.technology: vs-installation
ms.openlocfilehash: c76f7f151d10de791a8bcd0c50418d8775f51737
ms.sourcegitcommit: d4bea2867a4f0c3b044fd334a54407c0fe87f9e8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2019
ms.locfileid: "58790725"
---
# <a name="install-visual-studio"></a>Visual Studio'yu yükleme

::: moniker range="vs-2019"

Hoş Geldiniz Visual Studio 2019! Bu sürümde, seçin ve yalnızca gereksinim duyduğunuz özellikleri yüklemek kolaydır. Ve kendi kapladığı alan alt nedeniyle, hızlı ve sistemi daha az etkileyerek yükler.

::: moniker-end

::: moniker range="vs-2017"

Visual Studio'yu yüklemek için yeni bir yolunu Hoş Geldiniz! Bu sürümde, seçin ve yalnızca gereksinim duyduğunuz özellikleri yüklemek için daha kolay bir şekilde kolaylaştırdık. Daha hızlı ve daha önce hiç olmadığı kadar sistemi daha az etkileyerek yükler, böylece biz de Visual Studio'nun minimum ayak kısalttık.

::: moniker-end

> [!NOTE]
> Bu konu, Windows üzerinde Visual Studio için geçerlidir. Mac için Visual Studio için bkz: [Mac için Visual Studio](/visualstudio/mac/installation/).

::: moniker range="vs-2019"

Else bu sürümdeki yenilikler hakkında daha fazla bilgi edinmek istiyorsunuz? Bkz. bizim [sürüm notları](/visualstudio/releases/2019/release-notes/).

::: moniker-end

::: moniker range="vs-2017"

Else bu sürümdeki yenilikler hakkında daha fazla bilgi edinmek istiyorsunuz? Bkz. bizim [sürüm notları](/visualstudio/releasenotes/vs2017-relnotes).

::: moniker-end

Yüklenmeye hazır? Biz, bunu, adım adım konusunda rehberlik edelim.

## <a name="step-1---make-sure-your-computer-is-ready-for-visual-studio"></a>1. adım: bilgisayarınızın Visual Studio'ya hazır olduğundan emin olun

Visual Studio yükleme başlamadan önce:

::: moniker range="vs-2017"

1. Denetleme [sistem gereksinimleri](/visualstudio/productinfo/vs2017-system-requirements-vs). Bu gereksinimleri bilgisayarınıza Visual Studio 2017 destekleyip desteklemediğini bilmenize yardımcı olur.

1. En son Windows güncelleştirmelerini uygulayın. Bu güncelleştirmeler, bilgisayarınızda Visual Studio için en son güvenlik güncelleştirmelerini hem gerekli sistem bileşenlerine sahip olun.

1. Yeniden başlatma. Yeniden başlatma bekleyen yükleme veya güncelleştirmelerin Visual Studio yüklemesini engellememesini sağlar.

1. Alan boşaltın. Gereksiz dosyaları ve uygulamalar, % SYSTEMDRIVE %, örneğin, Disk Temizleme uygulamayı çalıştıran kaldırın.

::: moniker-end

::: moniker range="vs-2019"

1. Denetleme [sistem gereksinimleri](/visualstudio/releases/2019/system-requirements). Bu gereksinimleri bilgisayarınıza Visual Studio 2019 destekleyip desteklemediğini bilmenize yardımcı olur.

1. En son Windows güncelleştirmelerini uygulayın. Bu güncelleştirmeler, bilgisayarınızda Visual Studio için en son güvenlik güncelleştirmelerini hem gerekli sistem bileşenlerine sahip olun.

1. Yeniden başlatma. Yeniden başlatma bekleyen yükleme veya güncelleştirmelerin Visual Studio yüklemesini engellememesini sağlar.

1. Alan boşaltın. Gereksiz dosyaları ve uygulamalar, % SYSTEMDRIVE %, örneğin, Disk Temizleme uygulamayı çalıştıran kaldırın. 

::: moniker-end

::: moniker range="vs-2017"

Visual Studio 2017 ile yan yana Visual Studio'nun önceki sürümlerini çalıştıran hakkında sorular için bkz [Visual Studio uyumluluk ayrıntıları](/visualstudio/productinfo/vs2017-compatibility-vs#compatibility-with-previous-releases/).

::: moniker-end

::: moniker range="vs-2019"

Visual Studio 2019 ile yan yana Visual Studio'nun önceki sürümleri çalıştıran hakkında sorular için bkz [Visual Studio 2019 Platform hedefleme ve Uyumluluk](/visualstudio/releases/2019/compatibility/) sayfası.

::: moniker-end

## <a name="step-2---download-visual-studio"></a>Adım 2 - Visual Studio indirme

Ardından, Visual Studio önyükleyicisi dosyasını indirin. Bunu yapmak için aşağıdaki düğmeyi seçin, seçmek istediğiniz Visual Studio sürümünü **Kaydet**ve ardından **Klasör Aç**.

::: moniker range="vs-2017"

 > [!div class="button"]
 > [Visual Studio'yu indirin](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017)

::: moniker-end

::: moniker range="vs-2019"

 > [!div class="button"]
 > [Visual Studio'yu indirin](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2019+rc)

::: moniker-end

## <a name="step-3---install-the-visual-studio-installer"></a>3. adım - Visual Studio Yükleyicisi'ni yükleme

Visual Studio Yükleyicisi'ni yüklemek için önyükleyici dosyasını çalıştırın. Yeni Basit yükleyicinin hem yüklemek ve Visual Studio'yu özelleştirme için gereken her şeyi içerir.

1. Öğesinden, **indirir** klasöründe eşleşen veya benzer bir aşağıdaki dosyalar önyükleyici çift tıklayın:

   * **vs_community.exe** Visual Studio Community için
   * **vs_professional.exe** Visual Studio Professional
   * **vs_enterprise.exe** için Visual Studio Enterprise

   Bir kullanıcı hesabı denetimi bildirim alırsanız seçin **Evet**.

2. Microsoft onaylamak için isteriz [lisans koşulları](https://visualstudio.microsoft.com/license-terms/) ve Microsoft [gizlilik bildirimi](https://privacy.microsoft.com/privacystatement). Seçin **devam**.

   ![Lisans koşullarını ve gizlilik bildirimini](media/privacy-and-license-terms.png "Microsoft lisans koşulları ve gizlilik bildirimi")

## <a name="step-4---choose-workloads"></a>4. adım - iş yüklerini seçme

Yükleyici yüklendikten sonra bu özellik kümeleri seçerek yüklemenizi özelleştirmek için kullanabilirsiniz — veya iş yükleriniz — istediğiniz. İşte nasıl.

 ::: moniker range="vs-2017"

1. Bulmak istediğiniz iş yükünü **Visual Studio'yu** ekran.

   ![Visual Studio 2017: Bir iş yükünü yükleyin](../install/media/vs-installer-installing-workloads.png)

     Örneğin, ".NET masaüstü geliştirme" iş yükünü seçin. Bu, temel kod düzenleme açın ve projeye gerek kalmadan herhangi bir klasörden kodu düzenleme olanağı 20'den dil için destek içerir ve tümleşik kaynak kod denetimi varsayılan çekirdek Düzenleyicisi ile birlikte gelir.

1. Workload(s) seçtikten sonra seçmek istediğiniz **yükleme**.

    Ardından, durum ekranları, Visual Studio yüklemenizin ilerleme durumunu gösteren görünür.

 ::: moniker-end

::: moniker range="vs-2019"

1. Yeni iş yükleri ve bileşenler yüklendikten sonra seçin **başlatma**.

   ![Visual Studio 2019: Bir iş yükünü yükleyin](../install/media/vs-2019/vs-installer-workloads.png)

     Örneğin, "ASP.NET ve web geliştirme" iş yükünü seçin. Bu, temel kod düzenleme açın ve projeye gerek kalmadan herhangi bir klasörden kodu düzenleme olanağı 20'den dil için destek içerir ve tümleşik kaynak kod denetimi varsayılan çekirdek Düzenleyicisi ile birlikte gelir.

1. Workload(s) seçtikten sonra seçmek istediğiniz **yükleme**.

    Ardından, durum ekranları, Visual Studio yüklemenizin ilerleme durumunu gösteren görünür.

 ::: moniker-end

> [!TIP]
> Yüklemeden sonra herhangi bir zamanda iş yükleri veya başlangıçta yüklenmedi bileşenleri yükleyebilirsiniz. Visual Studio'nun varsa **Araçları** > **araçları ve özellikleri Al...**  Visual Studio yükleyicisi açılır. Veya açık **Visual Studio yükleyicisi** Başlat menüsünden. Burada, iş yükleri veya yüklemek istediğiniz bileşenleri seçebilirsiniz. Ardından, **Değiştir**.

## <a name="step-5---choose-individual-components-optional"></a>5. adım - (isteğe bağlı) bileşenleri tek tek seçme

Visual Studio yüklemenizi özelleştirmek için iş yüklerini özelliğini kullanmak istemediğiniz ya da bir iş yükü yükler çok daha fazla bileşen eklemek istediğiniz, yükleme veya tek tek bileşenleri ekleyerek bunu yapabilirsiniz **bağımsızbileşenler** sekmesi. Neleri istediğiniz ve daha sonra izleyin seçin yönergeleri.

::: moniker range="vs-2017"

  ![Visual Studio 2017 - tek tek bileşenleri yükle](media/vs-installer-installing-components.png "tek tek bileşenler Visual Studio'yu yükleyin")

::: moniker-end

::: moniker range="vs-2019"

  ![Visual Studio 2019 - tek tek bileşenleri yükle](media/vs-2019/vs-installer-individual-components.png "tek tek bileşenler Visual Studio'yu yükleyin")

::: moniker-end


## <a name="step-6---install-language-packs-optional"></a>6. adım - yükleme dil paketleri (isteğe bağlı)

Varsayılan olarak, yükleyici programı ilk kez çalıştığında işletim sisteminin dilini eşleştirmeye çalışır. Visual Studio bir dilde yüklemek için seçin **dil paketlerini** sekmesinde Visual Studio Yükleyicisi'nden ve ardından yönergeleri izleyin.

::: moniker range="vs-2017"

  ![Visual Studio 2017 - yükleme dil paketlerini](media/vs-installer-installing-language-packs.png "Visual Studio'yu yükleyin dil paketleri")

::: moniker-end

::: moniker range="vs-2019"

  ![Visual Studio 2019 - yükleme dil paketlerini](media/vs-2019/vs-installer-language-packs.png "Visual Studio'yu yükleyin dil paketleri")

::: moniker-end

### <a name="change-the-installer-language-from-the-command-line"></a>Komut satırından yükleyici dilini değiştirme

Varsayılan dilini değiştirme başka bir komut satırından yükleyiciyi çalıştırarak yoludur. Örneğin, aşağıdaki komutu kullanarak İngilizce olarak çalıştırmak için yükleyici zorlayabilirsiniz: `vs_installer.exe --locale en-US`. Yükleyici, sonraki açışınızda çalıştırdığınızda bu ayar hatırlanır. Aşağıdaki Dil belirteçler yükleyici destekler: zh-cn, zh-tw, cs-cz, en-us, es-es, fr-fr, de-de, it-IT, ja-jp, ko-kr, pl-pl, pt-br, ru-ru ve tr-tr.

## <a name="step-7---change-the-installation-location-optional"></a>7. adım - (isteğe bağlı) yükleme konumunu değiştirme

::: moniker range="vs-2017"

**15.7 sürümündeki yeni**: Artık, Visual Studio yükleme ayak izini sistem sürücünüzde azaltabilir. İndirme önbelleğini, paylaşılan bileşenler, SDK'ları ve araçları farklı sürücülere taşıma ve Visual Studio en hızlı çalışan sürücüde korumak seçebilirsiniz.

  ![Visual Studio 2017 - değişiklik yükleme konumlarını](media/installation-options-by-location.png "yükleme konumunu değiştirme")

::: moniker-end

::: moniker range="vs-2019"

Visual Studio yükleme ayak izini sistem sürücünüzde azaltabilir. İndirme önbelleğini, paylaşılan bileşenler, SDK'ları ve araçları farklı sürücülere taşıma ve Visual Studio en hızlı çalışan sürücüde korumak seçebilirsiniz.

  ![Visual Studio 2019 - değişiklik yükleme konumlarını](media/vs-2019/vs-installer-installation-locations.png "yükleme konumunu değiştirme")

::: moniker-end

> [!IMPORTANT]
> Yalnızca Visual Studio ilk kez yüklediğinizde, farklı bir sürücü seçebilirsiniz. Yüklemiş olduğunuz ve sürücüleri değiştirmek istiyorsanız, Visual Studio'yu kaldırın ve yeniden yükleyin.

Daha fazla bilgi için [seçin yükleme konumlarını](change-installation-locations.md) sayfası.

## <a name="step-8---start-developing"></a>8. adım - geliştirmeye başlayın

::: moniker range="vs-2017"

1. Visual Studio yüklemesi tamamlandıktan sonra seçin **başlatma** Visual Studio ile geliştirmeye başlamak için düğme.

2. Seçin **dosya**ve ardından **yeni proje**.

3. Bir proje türü seçin.

   Örneğin, [bir C++ uygulaması derleme](../ide/getting-started-with-cpp-in-visual-studio.md), seçin **yüklü**, genişletme **Visual C++** ve ardından oluşturmak istediğiniz C++ proje türünü seçin.

   İçin [yapı bir C# uygulama](../get-started/csharp/tutorial-console.md), seçin **yüklü**, genişletme **Visual C#** ve ardından C# proje derlemek istediğiniz türü.

::: moniker-end

::: moniker range="vs-2019"

1. Visual Studio yüklemesi tamamlandıktan sonra seçin **başlatma** Visual Studio ile geliştirmeye başlamak için düğme.

1. Pencerenin başlangıç seçin **yeni bir proje oluşturma**.

1. Arama kutusuna, kullanılabilir şablonların listesini görmek için oluşturmak istediğiniz uygulamanın türüne girin. Şablonlar listesinde, yükleme sırasında seçtiğiniz workload(s) bağlıdır. Farklı şablonları görmek için farklı iş yüklerini seçin.

   Kullanarak aramanızı belirli bir programlama dili için filtreleyebilirsiniz **dil** aşağı açılan listesi. Kullanarak filtreleyebilirsiniz **Platform** listesi ve **proje türü** çok listesi. 

1. Yeni projeniz Visual Studio açar ve kodu hazırsınız!

::: moniker-end

[!INCLUDE[install_get_support_md](includes/install_get_support_md.md)]

## <a name="see-also"></a>Ayrıca bkz.

* [Visual Studio’yu güncelleştirme](update-visual-studio.md)
* [Visual Studio’yu değiştirme](modify-visual-studio.md)
* [Visual Studio'yu kaldırma](uninstall-visual-studio.md)
* [Visual Studio’nun çevrimdışı yüklemesini oluşturma](create-an-offline-installation-of-visual-studio.md)
* [Komut satırı parametrelerini kullanarak Visual Studio'yu yükleme](use-command-line-parameters-to-install-visual-studio.md)
* [Mac için Visual Studio'yu yükleyin](/visualstudio/mac/installation)