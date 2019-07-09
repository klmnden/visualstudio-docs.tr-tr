---
title: Mac için Visual Studio 2019 yükleyin
description: Mac ve platformlar arası geliştirme için gereken ek bileşenleri için Visual Studio 2019'ı yükleme hakkında yönergeler.
author: asb3993
ms.author: amburns
ms.date: 04/02/2019
ms.technology: vs-ide-install
ms.assetid: 22B1F2CD-32AE-464D-80AC-C8AB4786B015
ms.custom: video
ms.openlocfilehash: 2086532f0602b4a2509358cbb6d57178a9a1a0d4
ms.sourcegitcommit: 7fbfb2a1d43ce72545096c635df2b04496b0be71
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/09/2019
ms.locfileid: "67691460"
---
# <a name="install-visual-studio-2019-for-mac"></a>Mac için Visual Studio 2019 yükleyin

MacOS üzerinde yerel, platformlar arası .NET uygulamalarını geliştirmeye başlamak için aşağıdaki adımları izleyerek Mac için Visual Studio 2019'ı yükleyin.

 > [!div class="button"]
 > [Mac için Visual Studio'yu indirin](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=navigation+cta&utm_content=download+vsmac2019)

## <a name="requirements"></a>Gereksinimler

- Mac ile macOS Sierra 10.12 yüksek veya üzeri.

İOS veya Mac OS x için Xamarin uygulamaları oluşturmak için ayrıca gerekir:

- Xcode 10.0 veya üzeri. En son kararlı sürüme genellikle önerilir.
- Bir Apple kimliği Bir Apple kimliği yoksa, yeni bir hesap oluşturabilirsiniz https://appleid.apple.com. Yükleme ve Xcode ile imzalamak için bir Apple Kimliği gereklidir.

## <a name="installation-instructions"></a>Yükleme yönergeleri

1. Yükleyici'den indirin [indirme sayfasında Mac için Visual Studio](https://aka.ms/vsmac).
2. İndirme tamamlandıktan sonra tıklayın **VisualStudioforMacInstaller.dmg** yükleyici bağlamak için çalıştırın ve ok logosu çift tıklayarak:

    [![Yüklemeye başlamak için büyük oku](media/install-installer-sml.png)](media/install-installer.png#lightbox)

3. Internet'ten yüklenen uygulama hakkında bir uyarı ile sunulan. Tıklayın **açık**.
4. Yükleyicinin sisteminizi denetlerken bekleyin:

    [![Sisteminiz yüklü bileşenleri için yükleyici denetler](media/install-checking-sml.png)](media/install-checking.png#lightbox)

5. Gizlilik ve lisans koşullarını kabul etmek isteyen bir uyarı görüntülenir. Bunları okuyun ve sonra basın için bağlantıları izleyin **devam** kabul ediyorsanız:

    [![Koşulları ve gizlilik için bağlantıları izleyin, sonra kabul etmiyorsanız devam edin](media/install-privacy-sml.png)](media/install-privacy.png#lightbox)

6. Kullanılabilir iş yüklerinin listesi görüntülenir. Kullanmak istediğiniz bileşenleri seçin:

    [![İsteğe bağlı bir iş yükü özellikleri yüklemek istediğiniz seçin](media/install-selection.png)](media/install-selection.png#lightbox)

   Tüm platformlara yüklemek istemiyorsanız, yüklemek için hangi platformların karar vermenize yardımcı olması için aşağıdaki kılavuzu kullanın:

   * **Xamarin kullanarak uygulamaları**:
      - Xamarin.Forms – seçin **Android** ve **iOS** platformlar.
      - iOS yalnızca – seçin **iOS** Platformu (yüklemeniz gerekecek Not [ **Xcode**](https://developer.apple.com/xcode/)).
      - Android yalnızca – seçin **Android** Platformu (ilgili bağımlılıkları da seçmeniz gerekir. Not).
      - Mac yalnızca – seçin **macOS** Platformu (yüklemeniz gerekecek Not [ **Xcode**](https://developer.apple.com/xcode/)).
      - Tam olarak platformlar arası Xamarin uygulamaları – seçin **Android**, **iOS**, ve **macOS** platformlar.
   * **.NET core uygulamaları** – Select **.NET Core** platform.
   * **ASP.NET Core Web uygulamaları** – Select **.NET Core** platform.
   * **Platformlar arası Unity oyun geliştirme** – Mac için Visual Studio dışında yüklenecek hiçbir ek platform gerekiyor Başvurmak [Unity Kurulum Kılavuzu](/visualstudio/mac/setup-vsmac-tools-unity) Unity uzantının yüklenmesi hakkında daha fazla bilgi.

7. Seçimlerinizi yaptıktan sonra basın **yükleme** düğmesi.
8. İndirir ve Mac ve seçilen iş yükleri için Visual Studio'yu yükler yükleyici ilerleme durumunu görüntüler. Yükleme için gerekli ayrıcalıklara vermek için parolanızı girmeniz istenebilir.

Bir Kurumsal ortamda yüklenirken ağ bulmakta güçlük çekiyorsanız, gözden [bir güvenlik duvarı veya proxy yüklemeye](https://docs.microsoft.com/visualstudio/mac/installation#install-visual-studio-for-mac-behind-a-firewall-or-proxy-server) yönergeleri.

Değişiklikleri hakkında daha fazla bilgi [sürüm notları](https://docs.microsoft.com/visualstudio/releasenotes/vs2019-mac-relnotes).

> [!NOTE]
> Bir platform veya aracı özgün yükleme sırasında (bunu #6. adımda seçimini tarafından) yüklemeyi seçerseniz, daha sonra bileşenleri eklemek isterseniz, yükleyici yeniden çalıştırmanız gerekir.

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

Diğer iş yükleri için başvurmak [iş yükleri](workloads.md) sayfası.

## <a name="related-video"></a>İlgili Video

> [!Video https://channel9.msdn.com/Shows/Visual-Studio-Toolbox/Visual-Studio-for-Mac-Acquisition/player]

## <a name="see-also"></a>Ayrıca bkz.

- [(Windows üzerinde) Visual Studio'yu yükleyin](/visualstudio/install/install-visual-studio)
