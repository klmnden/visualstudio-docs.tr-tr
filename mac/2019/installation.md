---
title: Visual Studio 2019 Mac Önizleme yükleme
description: Visual Studio 2019 Mac Önizleme ve platformlar arası geliştirme için gereken ek bileşenlerini yükleme hakkında yönergeler.
author: conceptdev
ms.author: crdun
ms.date: 11/03/2018
ms.technology: vs-ide-install
ms.assetid: 22B1F2CD-32AE-464D-80AC-C8AB4786B015
ms.openlocfilehash: acd8f3bc4f5fefa0a0c8b273856579067fb33c6a
ms.sourcegitcommit: 5a65ca6688a2ebb36564657d2d73c4b4f2d15c34
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2019
ms.locfileid: "54316195"
---
# <a name="install-visual-studio-2019-for-mac-preview"></a>Visual Studio 2019 Mac Önizleme yükleme

> [!NOTE]
> Önizleme Mac için Visual Studio 2019 Mac için Visual Studio'nun en son kararlı sürüm ile yan yana yüklenebilir. Yükleme sırasında en son kararlı sürüm değilse, varolan bir Visual Studio güncelleştirmesi istenir.

## <a name="requirements-for-the-visual-studio-2019-for-mac-preview"></a>Mac için Visual Studio 2019 gereksinimleri Önizleme

- Mac ile macOS Sierra 10.13 yüksek veya üzeri.

İOS veya Mac OS x için Xamarin uygulamaları oluşturmak için ayrıca gerekir:

- Xcode 10.0 veya üzeri. En son kararlı sürüme genellikle önerilir.
- Bir Apple kimliği Bir Apple kimliği yoksa, yeni bir hesap oluşturabilirsiniz https://appleid.apple.com. Yükleme ve Xcode ile imzalamak için bir Apple Kimliği gereklidir.

## <a name="installing-the-preview"></a>Önizleme Yükleniyor

1. Önizleme Yükleyicisi'nden indirin [Önizleme sayfası Mac için Visual Studio](https://aka.ms/vs4mac-preview).
2. İndirme tamamlandıktan sonra tıklayın **VisualStudioforMacPreviewInstaller.dmg** yükleyici bağlamak için çalıştırın ve ok logosu çift tıklayarak:

    [![Yüklemeye başlamak için büyük oku](media/install-preview-installer-sml.png)](media/install-preview-installer.png#lightbox)

3. Internet'ten yüklenen uygulama hakkında bir uyarı ile sunulan. Tıklayın **açık**.
4. Yükleyicinin sisteminizi denetlerken bekleyin:

    [![Sisteminiz yüklü bileşenleri için yükleyici denetler](media/install-preview-checking-sml.png)](media/install-preview-checking.png#lightbox)

5. Gizlilik ve lisans koşullarını kabul etmek isteyen bir uyarı görüntülenir. Bunları okuyun ve sonra basın için bağlantıları izleyin **devam** kabul ediyorsanız:

    [![Koşulları ve gizlilik için bağlantıları izleyin, sonra kabul etmiyorsanız devam edin](media/install-preview-privacy-sml.png)](media/install-preview-privacy.png#lightbox)

6. Kullanılabilir iş yüklerinin listesi görüntülenir. Kullanmak için istediklerinizi seçin:

    [![İsteğe bağlı bir iş yükü özellikleri yüklemek istediğiniz seçin](media/install-preview-selection-sml.png)](media/install-preview-selection.png#lightbox)

    Mac için geçerli Visual Studio 2017 7.7 sürümden daha eski ise, (Bu, yan yana yükleme desteklemek için gerekli olan) en son kararlı sürüme yükseltme onaylamanız istenir. Tuşuna **devam** yükseltmeyi onaylamak için:

    ![Kararlı bir sürüm 7.7 için yükseltme gerekiyor](media/install-preview-older-upgrade.png)

7. Seçimlerinizi yaptıktan sonra basın **yükleme** düğmesi.
8. İndirir ve Mac ve seçilen iş yükleri için Visual Studio'yu yükler yükleyici ilerleme durumunu görüntüler. Yükleme için gerekli ayrıcalıklara vermek için parolanızı girmeniz istenebilir.
9. Kullanım **Visual Studio (Önizleme)** Önizleme sürümü test edebilir veya en son sürüme geçiş yapmak istediğiniz zaman üretim çalışmanız için Visual Studio kararlı. İki simgeyi burada gösterilir:

    ![Kararlı ve önizleme simgesinin farklılıklar](media/install-preview-icons-sml.png)

Bir Kurumsal ortamda yüklenirken ağ bulmakta güçlük çekiyorsanız, gözden [bir güvenlik duvarı veya proxy yüklemeye](https://docs.microsoft.com/visualstudio/mac/installation#install-visual-studio-for-mac-behind-a-firewall-or-proxy-server) yönergeleri.

Değişiklikleri hakkında daha fazla bilgi [sürüm notları](https://docs.microsoft.com/visualstudio/releasenotes/vs2019-mac-preview-relnotes).

> [!NOTE]
> Seçtiğiniz bir platform veya aracı özgün yükleme sırasında (bunu #6. adımda seçimini tarafından) değil yüklerseniz, bileşen daha sonra eklemek istiyorsanız, yükleyici yeniden çalıştırmanız gerekir.

## <a name="install-visual-studio-for-mac-behind-a-firewall-or-proxy-server"></a>Visual Studio Mac için bir güvenlik duvarı veya proxy sunucusunun arkasına yükleme

Güvenlik duvarının arkasında Mac için Visual Studio'yu yüklemek için belirli uç noktaları, yazılım güncelleştirmeleri ve gerekli araçları indirmeye izin ver için erişilebilir yapılması gerekir.

Şu konumlardan erişime izin vermek için ağ yapılandırın:

- [Visual Studio uç noktaları](/visualstudio/install/install-visual-studio-behind-a-firewall-or-proxy-server)

## <a name="next-steps"></a>Sonraki adımlar

Mac için Visual Studio yükleme, uygulamalarınız için kod yazmaya olanak tanır. Aşağıdaki kılavuzlarda yazma ve projelerinizi dağıtma sonraki adımlarda size rehberlik sağlanmaktadır.

### <a name="ios"></a>iOS

1. [Hello, iOS](https://developer.xamarin.com/guides/ios/getting_started/hello,_iOS/)
2. [Cihaz sağlama](https://developer.xamarin.com/guides/ios/getting_started/installation/device_provisioning)(cihazda uygulamanızı çalıştırmak için).

### <a name="android"></a>Android

1. [Xamarin Android SDK Yöneticisi'ni kullanma](https://developer.xamarin.com/guides/android/getting_started/installation/android-sdk/?ide=xs)
2. [Android SDK Emulator](https://developer.xamarin.com/guides/android/getting_started/installation/android-emulator/)
4. [Cihazı Dağıtım için Ayarlama](https://developer.xamarin.com/guides/android/getting_started/installation/set_up_device_for_development/)

### <a name="net-core-apps-aspnet-core-web-apps-unity-game-development"></a>.NET core uygulamaları, ASP.NET Core web uygulamaları, Unity oyun geliştirme

Diğer iş yükleri için başvurmak [iş yükleri](/visualstudio/mac/workloads) sayfası.

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio 2017 (Windows) yükleyin](/visualstudio/install/install-visual-studio)
