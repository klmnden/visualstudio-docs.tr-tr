---
title: Visual Studio'yu yükleme
titleSuffix: ''
description: Visual Studio, adım adım yüklemeyi öğrenin.
ms.date: 02/11/2019
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
ms.openlocfilehash: 659f220936bd1a6273a27d63642534955a48c7aa
ms.sourcegitcommit: d78821f8c353e0102b1554719f549f32dffac71b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/27/2019
ms.locfileid: "58515268"
---
# <a name="install-visual-studio"></a>Visual Studio'yu yükleme

Visual Studio'yu yüklemek için yeni bir yolunu Hoş Geldiniz! Bu sürümde, seçin ve yalnızca gereksinim duyduğunuz özellikleri yüklemek daha kolay bir şekilde kolaylaştırdık. Daha hızlı ve daha önce hiç olmadığı kadar sistemi daha az etkileyerek yükler, böylece biz de Visual Studio'nun minimum ayak kısalttık.

> [!NOTE]
> Bu konu, Windows üzerinde Visual Studio için geçerlidir. Mac için Visual Studio için bkz: [Mac için Visual Studio](/visualstudio/mac/installation).

Else bu sürümdeki yenilikler hakkında daha fazla bilgi edinmek istiyorsunuz? Bkz. bizim [sürüm notları](/visualstudio/releasenotes/vs2017-relnotes).

Yüklenmeye hazır? Biz, bunu, adım adım konusunda rehberlik edelim.

## <a name="step-1---make-sure-your-computer-is-ready-for-visual-studio"></a>1. adım: bilgisayarınızın Visual Studio'ya hazır olduğundan emin olun

Visual Studio yükleme başlamadan önce:

1. Denetleme [sistem gereksinimleri](/visualstudio/productinfo/vs2017-system-requirements-vs). Bu gereksinimleri bilgisayarınıza Visual Studio 2017 destekleyip desteklemediğini bilmenize yardımcı olur.
2. En son Windows güncelleştirmelerini uygulayın. Bu güncelleştirmeler, bilgisayarınızda Visual Studio için en son güvenlik güncelleştirmelerini hem gerekli sistem bileşenlerine sahip olun.
3. Yeniden başlatma. Yeniden başlatma bekleyen yükleme veya güncelleştirmelerin Visual Studio yüklemesini engellememesini sağlar.
4. Alan boşaltın. Gereksiz dosyaları ve uygulamalar, % SYSTEMDRIVE %, örneğin, Disk Temizleme uygulamayı çalıştıran kaldırın.

Visual Studio 2017 ile yan yana Visual Studio'nun önceki sürümlerini çalıştıran hakkında sorular için bkz [Visual Studio uyumluluk ayrıntıları](/visualstudio/productinfo/vs2017-compatibility-vs#compatibility-with-previous-releases).

## <a name="step-2---download-visual-studio"></a>Adım 2 - Visual Studio indirme

Ardından, Visual Studio önyükleyicisi dosyasını indirin. Bunu yapmak için aşağıdaki düğmeyi seçin, seçmek istediğiniz Visual Studio 2017 sürümünü **Kaydet**ve ardından **Klasör Aç**.

 > [!div class="button"]
 > [Visual Studio 2017 İndir](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017)
<br/>

## <a name="step-3---install-the-visual-studio-installer"></a>3. adım - Visual Studio Yükleyicisi'ni yükleme

Ardından, Visual Studio Yükleyicisi'ni yüklemek için önyükleyici dosyasını çalıştırın. Yeni Basit yükleyicinin hem yüklemek ve Visual Studio 2017'yi özelleştirmek için ihtiyacınız olan her şeyi içerir.

1. Öğesinden, **indirir** klasöründe eşleşen veya benzer bir aşağıdaki dosyalar önyükleyici çift tıklayın:

   * **vs_enterprise.exe** için Visual Studio Enterprise
   * **vs_professional.exe** Visual Studio Professional
   * **vs_community.exe** Visual Studio Community için  <br><br>

   Bir kullanıcı hesabı denetimi bildirim alırsanız seçin **Evet**.

2. Microsoft onaylamak için isteriz [lisans koşulları](https://visualstudio.microsoft.com/license-terms/) ve Microsoft [gizlilik bildirimi](https://privacy.microsoft.com/privacystatement). Seçin **devam**.

   ![Lisans koşullarını ve gizlilik bildirimini](media/vs2017-privacy-and-license-terms.PNG "Microsoft lisans koşulları ve gizlilik bildirimi")

## <a name="step-4---select-workloads"></a>Adım 4 - Select iş yükleri

Yükleyici yüklendikten sonra bu özellik kümeleri seçerek yüklemenizi özelleştirmek için kullanabilirsiniz — veya iş yükleriniz — istediğiniz. İşte nasıl.

1. Bulmak istediğiniz iş yükünü **Visual Studio'yu** ekran.

   ![Visual Studio 2017 Kurulum iletişim kutusundan bir iş yükünü seçme](../install/media/install-visual-studio-community.png)

     Örneğin, ".NET masaüstü geliştirme" iş yükünü seçin. Bu, temel kod düzenleme açın ve projeye gerek kalmadan herhangi bir klasörden kodu düzenleme olanağı 20'den dil için destek içerir ve tümleşik kaynak kod denetimi varsayılan çekirdek Düzenleyicisi ile birlikte gelir.

2. İstediğiniz workload(s) seçtikten sonra seçin **yükleme**.

    Ardından, durum ekranları, Visual Studio yüklemenizin ilerleme durumunu gösteren görünür.

3. Yeni iş yükleri ve bileşenler yüklendikten sonra seçin **başlatma**.

> [!TIP]
> Yüklemeden sonra herhangi bir zamanda iş yükleri veya başlangıçta yüklenmedi bileşenleri yükleyebilirsiniz. Visual Studio'nun varsa **Araçları** > **araçları ve özellikleri Al...**  Visual Studio yükleyicisi açılır. Veya açık **Visual Studio yükleyicisi** Başlat menüsünden. Buradan yükleyin ve ardından istediğiniz bileşenleri ve iş yüklerini seçebileceğiniz **Değiştir**.

## <a name="step-5---select-individual-components-optional"></a>Adım 5 - tek bileşen seçin (isteğe bağlı)

Visual Studio yüklemenizi özelleştirmek için iş yüklerini özelliği kullanmayı istemiyorsanız, tek tek bileşenler yükleyerek bunu yapabilirsiniz. Tek tek bileşenleri seçmek için Seç **tek tek bileşenler** seçeneğini Visual Studio Yükleyicisi'nden, neleri istediğiniz ve daha sonra izleyin seçin yönergeleri.

  ![Visual Studio 2017 - tek tek bileşenleri yükle](media/vs2017-components.PNG "tek tek bileşenler Visual Studio'yu yükleyin")

## <a name="step-6---install-language-packs-optional"></a>6. adım - yükleme dil paketleri (isteğe bağlı)

Varsayılan olarak, yükleyici programı ilk kez çalıştığında işletim sisteminin dilini eşleştirmeye çalışır. Visual Studio 2017 bir dilde yüklemek için seçin **dil paketlerini** seçeneğini Visual Studio Yükleyicisi'nden ve yönergeleri izleyin.

  ![Visual Studio 2017 - yükleme dil paketlerini](media/vs2017-languages.PNG "Visual Studio'yu yükleyin dil paketleri")

### <a name="change-the-installer-language-from-the-command-line"></a>Komut satırından yükleyici dilini değiştirme

Varsayılan dilini değiştirme başka bir komut satırından yükleyiciyi çalıştırarak yoludur. Örneğin, aşağıdaki komutu kullanarak İngilizce olarak çalıştırmak için yükleyici zorlayabilirsiniz: `vs_installer.exe --locale en-US`. Yükleyici, sonraki açışınızda çalıştırdığınızda bu ayar hatırlanır. Aşağıdaki Dil belirteçler yükleyici destekler: zh-cn, zh-tw, cs-cz, en-us, es-es, fr-fr, de-de, it-IT, ja-jp, ko-kr, pl-pl, pt-br, ru-ru ve tr-tr.

## <a name="step-7---change-the-installation-location-optional"></a>7. adım - (isteğe bağlı) yükleme konumunu değiştirme

**15.7 sürümündeki yeni**: Artık, Visual Studio yükleme ayak izini sistem sürücünüzde azaltabilir. İndirme önbelleğini, paylaşılan bileşenler, SDK'ları ve araçları farklı sürücülere taşıma ve Visual Studio en hızlı çalışan sürücüde korumak seçebilirsiniz.

  ![2017 - Visual Studio yükleme konumunu değiştirmek](media/installation-options-by-location.png "yükleme konumunu değiştirme")

Daha fazla bilgi için [Visual Studio yükleme konumlarını değiştirme](change-installation-locations.md) sayfası.

## <a name="step-8---start-developing"></a>8. adım - geliştirmeye başlayın

::: moniker range="vs-2017"

1. Visual Studio yüklemesi tamamlandıktan sonra seçin **başlatma** Visual Studio ile geliştirmeye başlamak için düğme.

2. Seçin **dosya**ve ardından **yeni proje**.

3. Bir proje türü seçin.

   Örneğin, [bir C++ uygulaması derleme](../ide/getting-started-with-cpp-in-visual-studio.md), seçin **yüklü**, genişletme **Visual C++** ve sonra oluşturmak istediğiniz C++ proje türü seçin.

   İçin [yapı bir C# uygulama](../get-started/csharp/tutorial-wpf.md), seçin **yüklü**, genişletme **Visual C#** ve ardından C# proje derlemek istediğiniz türü.

::: moniker-end

::: moniker range="vs-2019"

1. Visual Studio yüklemesi tamamlandıktan sonra seçin **başlatma** Visual Studio ile geliştirmeye başlamak için düğme.

1. Pencerenin başlangıç seçin **yeni bir proje oluşturma**.

1. Arama kutusuna şablonlarının bir listesini görmek için oluşturmak istediğiniz uygulamanın türüne girin. (Örneğin, *WFP*.)

  > [!TIP]
  > Aramanızı belirli bir programlama dili kullanarak filtreleyebilirsiniz **dil** aşağı açılan listesi. Kullanarak filtreleyebilirsiniz **Platform** listesi ve **proje türü** listesi. 

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