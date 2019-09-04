---
title: Visual Studio’yu güncelleştirme
titleSuffix: ''
description: Visual Studio en son sürümüne, adım adım güncelleştirmeyi öğrenebilirsiniz.
ms.date: 07/31/2019
ms.custom: seodec18
ms.topic: conceptual
ms.prod: visual-studio-windows
ms.technology: vs-installation
helpviewer_keywords:
- update [Visual Studio]
- change [Visual Studio]
f1_keywords:
- VS.ToolsOptionsPages.Environment.ProductUpdates
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 22b48cdb80f34a4bbf57626b9ffe6e4d753e5a55
ms.sourcegitcommit: 9c07ae6fb18204ea080c8248994a683fa12e5c82
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/04/2019
ms.locfileid: "70293685"
---
# <a name="update-visual-studio-to-the-most-recent-release"></a>Visual Studio 'Yu en son sürüme güncelleştirme

::: moniker range="vs-2017"

En son özellikleri, düzeltmeleri ve geliştirmeleri her zaman alabilmeniz için Visual Studio 2017 ' in en [son sürümüne](/visualstudio/releasenotes/vs2017-relnotes/) güncelleştirmeniz önerilir.

En yeni sürümü denemek istiyorsanız bunun yerine [Visual Studio 2019](https://visualstudio.microsoft.com/downloads) ' i indirip yüklemeyi göz önünde bulundurun.

> [!IMPORTANT]
> Yüklemek, güncelleştirmek veya Visual Studio değiştirmek için yönetici izinleri olan bir hesapla oturum açmalısınız. Daha fazla bilgi için [kullanıcı izinleri ve Visual Studio](../ide/user-permissions-and-visual-studio.md).
>
> [!NOTE]
> Bu konu, Windows üzerinde Visual Studio için geçerlidir. Mac için Visual Studio için bkz: [Mac için Visual Studio güncelleştirme](/visualstudio/mac/update).

## <a name="update-visual-studio-2017-version-156-or-later"></a>Visual Studio 2017 sürüm 15.6 veya sonraki bir sürümü güncelleştir

Biz rahat bir yükleme ve doğrudan IDE içinde kullanmak daha kolay hale getirmek için deneyim güncelleştirin. Sürüm 15.6 ve daha sonra yeniden daha yeni sürümlerini Visual Studio güncelleştirme açıklanmıştır.

### <a name="using-the-notifications-hub"></a>Bildirimler merkezini kullanma

Bir güncelleştirme olduğunda, Visual Studio 'da karşılık gelen bir bildirim bayrağı vardır.

1. Çalışmanızı kaydedin.

1. Bildirim bayrağına açmak için seçin **bildirimleri** hub'ı ve ardından yüklemek istediğiniz güncelleştirmeyi seçin.

   ![Bildirim hub'ı kullanarak Visual Studio 2017 güncelleştirmesi](media/vs-install-notifications-hub-15dot6.png "bildirim Merkezi'nde Visual Studio 2017")

      > [!TIP]
      > Visual Studio 2017 sürümüne yönelik bir güncelleştirme birikimlidir, bu nedenle her zaman en son sürüm numarasıyla yüklemeyi seçin.

1. Zaman **güncelleştirme** iletişim kutusu açılır öğesini **Şimdi Güncelleştir**.

    ![Bildirim hub'ından güncelleştirme iletişim kutusunu kullanarak Visual Studio 2017 güncelleştirmesi](media/vs-update-now-from-notifications-hub.png "güncelleştirme iletişim kutusunda bildirim Merkezi'nde Visual Studio")

     Kullanıcı erişim denetimi iletişim kutusunu açar, seçim **Evet**. Ardından, "Lütfen bekleyin." iletişim kutusu için biraz açabilir ve ardından güncelleştirilmesini başlatmak için Visual Studio yükleyicisi açılır.

     ![15.6 sürümündeki yeni Visual Studio yükleyicisi deneyimi](media/visual-studio-15dot6-installer.png "yeni Visual Studio yükleyicisi deneyiminde sürüm 15.6")

     Güncelleştirme devam ediyor. Tamamlandığında, daha sonra Visual Studio'yu yeniden başlatır.

     > [!NOTE]
     > Visual Studio'yu Yönetici modunda çalıştırdığınızda, el ile Visual Studio güncelleştirmeden sonra yeniden başlatmanız gerekir.

### <a name="using-the-ide"></a>IDE kullanma

Bir güncelleştirme olup olmadığını denetlemek ve ardından Visual Studio'da menü çubuğundan güncelleştirmeyi yükleyin.

1. Çalışmanızı kaydedin.

1. **Güncelleştirmeler için** **Yardım** > denetle ' yi seçin.

     ![Sürüm 15.6 Visual Studio'da yeni Yardım menüsü](media/vs-help-menu-check-for-updates.png "sürüm 15.6 Visual Studio'da yeni Yardım menüsü")

1. Zaman **güncelleştirme** iletişim kutusu açılır öğesini **Şimdi Güncelleştir**.

   Güncelleştirme, önceki bölümde sonra Visual Studio güncelleştirmesi başarıyla tamamlandıktan sonra yeniden başlatmaları açıklandığı gibi devam eder.

   > [!NOTE]
   > Visual Studio'yu Yönetici modunda çalıştırdığınızda, el ile Visual Studio güncelleştirmeden sonra yeniden başlatmanız gerekir.

### <a name="using-the-visual-studio-installer"></a>Visual Studio Yükleyicisi kullanma

Visual Studio 'nun önceki sürümlerinde olduğu gibi, bir güncelleştirmeyi yüklemek için Visual Studio Yükleyicisi kullanabilirsiniz.

1. Çalışmanızı kaydedin.

1. Yükleyici açın. Visual Studio yükleyicisi, devam etmeden önce güncelleştirme gerektirebilir.

   > [!NOTE]
   > Windows 10 çalıştıran bir bilgisayarda, yükleyici harfi altında bulabilirsiniz **V** olarak **Visual Studio yükleyicisi**, veya harf altında **M** olarak  **Microsoft Visual Studio yükleyicisi**.

1. Yükleyicideki **ürün** sayfasında, daha önce yüklediğiniz Visual Studio sürümünü arayın.

1. Bir güncelleştirme varsa, gördüğünüz bir **güncelleştirme** düğmesi. (Bir güncelleştirme kullanılabilir olup olmadığını belirlemek yükleyici için birkaç saniye sürebilir.)

   Seçin **güncelleştirme** güncelleştirmeleri yüklemek için düğme.

     ![Visual Studio Yükleyicisi'ni kullanarak Visual Studio 2017 güncelleştirmesi](media/update-visual-studio.png "güncelleştirme Visual Studio 2017 Visual Studio Yükleyicisi'ni kullanarak")

## <a name="update-visual-studio-2017-version-155-or-earlier"></a>Visual Studio 2017 sürüm 15.5 veya önceki bir sürümünü güncelleştirme

Önceki bir sürümü kullanıyorsanız, Visual Studio 2017 sürüm 15,0 ' den sürüm 15,5 aracılığıyla bir güncelleştirme uygulama hakkında daha fazla bilgiyi burada bulabilirsiniz.

### <a name="update-by-using-the-notifications-hub"></a>Bildirim hub'ı kullanarak güncelleştirme

1. Güncelleştirmeler olduğunda, Visual Studio ile ilgili bir bildirim bayrağı yok.

   ![Bildirim hub'ı kullanarak Visual Studio 2017 güncelleştirmesi](media/notification-flag.png "Visual Studio'daki bildirim bayrağı güncelleştirmenin")

   Bildirim bayrağına açmak için seçin **bildirimleri** hub.

   ![Bildirim hub'ı kullanarak Visual Studio 2017 güncelleştirmesi](media/notifications-hub.png "bildirim Merkezi'nde Visual Studio")

      > [!TIP]
      > Visual Studio 2017 sürümüne yönelik bir güncelleştirme birikimlidir, bu nedenle her zaman en son sürüm numarasıyla yüklemeyi seçin.

1. Seçin **"Visual Studio güncelleştirme" kullanılabilir**, açan **Uzantılar ve güncelleştirmeler** iletişim kutusu.

   ![Bildirim hub'ı kullanarak Visual Studio 2017 güncelleştirmesi](media/notifications-hub-select.png "bildirim Merkezi'nde Visual Studio")

1. İçinde **Uzantılar ve güncelleştirmeler** iletişim kutusunda **güncelleştirme** düğmesi.

   ![Bildirim hub'ı kullanarak Visual Studio 2017 güncelleştirmesi](media/notifications-extensions-and-updates.png "Visual Studio'da Uzantılar ve güncelleştirmeler iletişim kutusu")

#### <a name="more-about-visual-studio-notifications"></a>Visual Studio bildirimleri hakkında daha fazla bilgi

Visual Studio bildirir, size, herhangi bir bileşeni için veya Visual Studio'nun kendisi için bir güncelleştirme kullanılabilir olduğunda ve ayrıca belirli olaylar gerçekleştiğinde Visual Studio ortamında.

* Bildirim bayrağı sarı olduğunda, yüklemek için kullanabileceğiniz bir Visual Studio ürün güncelleştirmesi vardır.
* Bildirim bayrağı kırmızı olduğunda, lisansınızın bir sorunu vardır.
* Bildirim bayrağına siyah olduğunda, gözden geçirmek için isteğe bağlı veya bilgilendirme iletileri vardır.

Açmak için bildirimler bayrağına seçin **bildirimleri** hub üzerinde çalışmasını istediğiniz bildirimleri seçin. Veya Yoksay veya bir bildirimi kapatmak seçin.

 ![Bildirim hub'ında bir isteğe bağlı veya bilgilendirme iletisi görüntülemek](media/notification-flag-optional.png "isteğe bağlı veya bilgilendirme iletisi Visual Studio'daki bildirim bayrağı")

Bir bildirim yoksaymayı seçerseniz, Visual Studio göstermeyi durdurur. Yoksayılan bildirimleri listesi sıfırlamak istiyorsanız, seçin **ayarları** bildirim hub'ında düğmesi.

   ![Bildirim seçenekleri görmek için bildirim Merkezi'nde Ayarlar düğmesini](media/vs-notifications-hub-settings-button.png "bildirim seçeneklerini görüntülemek için bildirim Merkezi'nde Ayarlar düğmesini seçin")

### <a name="update-by-using-the-visual-studio-installer"></a>Visual Studio Yükleyicisi'ni kullanarak güncelleştirme

1. Yükleyici açın. Yükleyici, devam etmeden önce güncelleştirmeniz gerekebilir. Böyle bir durum söz konusu olduğunda bunu yapmanız istenir.

   > [!NOTE]
   > Windows 10 çalıştıran bir bilgisayarda, yükleyici harfi altında bulabilirsiniz **V** olarak **Visual Studio yükleyicisi**, veya harf altında **M** olarak  **Microsoft Visual Studio yükleyicisi**.

1. Yükleyicideki **ürün** sayfasında, daha önce yüklenen Visual Studio sürümünü arayın.

1. Bir güncelleştirme varsa, gördüğünüz bir **güncelleştirme** düğmesi. (Bir güncelleştirme kullanılabilir olup olmadığını belirlemek yükleyici için birkaç saniye sürebilir.)

   Seçin **güncelleştirme** güncelleştirmeleri yüklemek için düğme.

     ![Visual Studio yükleyicisi kullanarak Visual Studio 2017](media/update-visual-studio.png "i güncelleştirin Visual Studio yükleyicisi kullanarak Visual Studio 'Yu güncelleştirme")

::: moniker-end

::: moniker range="vs-2019"

En son özellikleri, düzeltmeleri ve geliştirmeleri her zaman alabilmeniz için Visual Studio 2019 ' in en [son sürümüne](/visualstudio/releases/2019/release-notes/) güncelleştirmeniz önerilir.

Visual Studio 2019 ' ı henüz yüklemediyseniz, [Visual Studio İndirmeleri](https://visualstudio.microsoft.com/downloads) sayfasına giderek ücretsiz olarak yükleme yapın.

> [!IMPORTANT]
> Yüklemek, güncelleştirmek veya Visual Studio değiştirmek için yönetici izinleri olan bir hesapla oturum açmalısınız. Daha fazla bilgi için [kullanıcı izinleri ve Visual Studio](../ide/user-permissions-and-visual-studio.md).
>
> [!NOTE]
> Bu konu, Windows üzerinde Visual Studio için geçerlidir. Mac için Visual Studio için bkz: [Mac için Visual Studio güncelleştirme](/visualstudio/mac/update).

Visual&nbsp;Studio&nbsp;2019 ' i güncelleştirme.

## <a name="use-the-visual-studio-installer"></a>Visual Studio Yükleyicisi'ni kullanın

1. Yükleyici açın.

     ![Visual Studio yükleyicisi Windows 'Tan açın](media/vs-2019/vs-installer-windows-start.png "Visual Studio yükleyicisi açın")

   Devam etmeden önce yükleyiciyi güncelleştirmeniz gerekebilir. Bu durumda, istemleri izleyin.

1. Yükleyicide, yüklediğiniz Visual Studio sürümünü arayın.

   Örneğin, daha önce Visual&nbsp;Studio Community&nbsp;2019 ' i yüklediyseniz ve bu güncelleştirme için bir güncelleştirme varsa, yükleyicide bir **güncelleştirme kullanılabilir** iletisi görüntülenir.

     ![Güncelleştirmek Istediğiniz Visual Studio 2019 sürümünü seçin](media/vs-2019/vs-installer-update-visual-studio-community.png "Güncelleştirmek Istediğiniz Visual Studio 2019 sürümünü seçin")

1. Güncelleştirmeleri yüklemek için **Güncelleştir** ' i seçin.

    ![Güncelleştirmeleri yüklemek Için Güncelleştir düğmesini seçin](media/vs-2019/vs-installer-choose-update-visual-studio-community.png "Güncelleştirmeleri yüklemek Için Güncelleştir düğmesini seçin")

1. Güncelleştirme tamamlandıktan sonra bilgisayarınızı yeniden başlatmanız istenebilir. Varsa, bunu yapın ve ardından Visual Studio 'Yu genellikle yaptığınız gibi başlatın.

   Bilgisayarınızı yeniden başlatmanız istenmezse, yükleyiciden Visual Studio 'yu başlatmak için **Başlat** ' ı seçin.

    ![Visual Studio 'yu başlatmak Için Başlat düğmesini seçin](media/vs-2019/choose-launch-visual-studio-community.png "Visual Studio 'yu başlatmak Için Başlat düğmesini seçin")

## <a name="use-the-ide"></a>IDE'yi kullanın

Bir güncelleştirmeyi denetleyebilir ve ardından menü çubuğunu veya Visual Studio 2019 arama kutusunu kullanarak yükleyebilirsiniz.

### <a name="open-visual-studio"></a>Visual Studio 'Yu aç

1. Windows **Başlat** menüsünde **Visual Studio 2019**' ı seçin.

    ![Visual Studio 2019 'Yi açın](media/vs-2019/vs-installer-visual-studio-2019.png "Windows 'Dan Visual Studio 2019 'Yi açın")

1. **Kullanmaya**başlayın ' ın altında, IDE 'yi açmak için herhangi bir seçeneği belirleyin.

    ![Visual Studio yükleyicisi açın](media/vs2019-choose-option-from-get-started.png "Visual Studio yükleyicisi açın")

    Visual Studio açılır. IDE 'de bir **Visual Studio 2019 güncelleştirme** iletisi görüntülenir.

    ![IDE 'deki ' Visual Studio 2019 Güncelleştirmesi ' iletisi](media/vs-2019/update-visual-studio-ide-message.png "IDE 'deki ' Visual Studio 2019 Güncelleştirmesi ' iletisi")

1. **Visual Studio 2019 güncelleştirme** Iletisinde **Ayrıntıları görüntüle**' yi seçin.

   ![Visual Studio 2019 IDE güncelleştirme Iletisinde ayrıntıları görüntüle düğmesini seçin](media/vs-2019/update-visual-studio-ide-view-details.png "Visual Studio 2019 güncelleştirme Iletisindeki ayrıntıları görüntüle düğmesini seçin")

1. **Güncelleştirme indirildi ve yüklemeye hazırlanıyor** Iletişim kutusunda **Güncelleştir**' i seçin.

     ![' Güncelleştirme indirilmiş ve yüklenmeye hazırlanıyor ' iletişim kutusunda Güncelleştir düğmesini seçin](media/vs-2019/update-ready-install-visual-studio-community-from-ide.png "' Güncelleştirme indirilmiş ve yüklenmeye hazırlanıyor ' iletişim kutusunda Güncelleştir düğmesini seçin")

   Visual Studio güncelleştirmeleri, kapanır ve sonra yeniden açılır.

### <a name="in-visual-studio"></a>Visual Studio 'da

1. Menü çubuğundan **Yardım**' ı seçin ve ardından **Güncelleştirmeleri denetle**' yi seçin.

     ![Yardım menüsünden ' güncelleştirmeleri denetle 'Yi seçin](media/vs-2019/vs-ide-check-updates-help-menu.png "Yardım menüsünden ' güncelleştirmeleri denetle 'Yi seçin")

    > [!NOTE]
    > Ayrıca, güncelleştirmeleri denetlemek için IDE 'deki arama kutusunu da kullanabilirsiniz. **CTRL**+**Q**tuşlarına basın, "güncelleştirmeleri denetle" yazın ve ardından eşleşen arama sonucunu seçin.

1. **Kullanılabilir güncelleştirme** Iletişim kutusunda **Güncelleştir**' i seçin.

     ![Güncelleştirme indirilmiş ve yüklenmeye hazırlanıyor ' iletişim kutusunda Güncelleştir düğmesini seçin](media/vs-2019/update-visual-studio-community-from-ide.png "Güncelleştirme indirilmiş ve yüklenmeye hazırlanıyor ' iletişim kutusunda Güncelleştir düğmesini seçin")

   Visual Studio güncelleştirmeleri, kapanır ve sonra yeniden açılır.

## <a name="use-the-notifications-hub"></a>Bildirim hub'ı kullanın

1. Visual Studio 'da çalışmanızı kaydedin.

1. **Bildirimler** merkezini açmak Için VISUAL Studio IDE 'nin sağ alt köşesindeki bildirim simgesini seçin.

   ![Visual STUDIO IDE 'deki bildirim simgesi](media/vs-2019/notification-bar.png "Visual STUDIO IDE 'deki bildirim simgesi")

1. **Bildirimler hub 'ında**, yüklemek istediğiniz güncelleştirmeyi seçin ve ardından **Ayrıntıları görüntüle**' yi seçin.

     ![Visual Studio 2019 ' de Bildirim Hub 'ı](media/vs-2019/notification-hub-update.png "Visual Studio 2019 ' de Bildirim Hub 'ı")

      > [!TIP]
      > Visual Studio 2019 sürümüne yönelik bir güncelleştirme birikimlidir, bu nedenle her zaman en son sürüm numarasıyla yüklemeyi seçin.

1. **Kullanılabilir güncelleştirme** Iletişim kutusunda **Güncelleştir**' i seçin.

   Visual Studio güncelleştirmeleri, kapanır ve sonra yeniden açılır.

## <a name="customize-update-settings"></a>Güncelleştirme ayarlarını özelleştirme

Visual Studio 'daki güncelleştirme ayarlarını, yükleme modunu değiştirerek ve otomatik indirmeleri seçerek gibi çeşitli yollarla özelleştirebilirsiniz.

Aralarından seçim yapabileceğiniz iki yükleme modu vardır:

* **İndirme sırasında yükleme**
* **Tümünü İndir, sonra Yükle**

Ayrıca, makineniz boşta kaldığında güncelleştirmelerin indirilmesine izin veren **güncelleştirme ayarlarını otomatik olarak indir** seçeneğini de belirleyebilirsiniz.

Şöyle:

1. Menü çubuğunda **Araçlar** > **Seçenekler**' i seçin.

2. **Ortam**' ı genişletin ve **ürün güncelleştirmeleri**' ni seçin.

    ![Visual Studio 'da güncelleştirme ayarları](media/vs-2019/update-settings-options.png)

3. Visual Studio güncelleştirmelerinizde yükleme modunu ve otomatik indirme seçeneklerini belirleyin.

::: moniker-end

[!INCLUDE[install_get_support_md](includes/install_get_support_md.md)]

## <a name="see-also"></a>Ayrıca bkz.

* [Visual Studio sürümlerini yan yana yükler](install-visual-studio-versions-side-by-side.md)
* [Visual Studio’nun ağ tabanlı yüklemesini güncelleştirme](update-a-network-installation-of-visual-studio.md)
* [Bakım temeliyle Visual Studio 'Yu güncelleştirme](update-servicing-baseline.md)
* [Ağ tabanlı Visual Studio dağıtımlarına yönelik güncelleştirmeleri denetleme](controlling-updates-to-visual-studio-deployments.md)
* [Visual Studio’yu değiştirme](modify-visual-studio.md)
* [Visual Studio'yu kaldırma](uninstall-visual-studio.md)
