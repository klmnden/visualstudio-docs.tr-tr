---
title: Yüklü uygulama paketi (UWP) hata ayıklama | Microsoft Docs
ms.custom: H1Hack27Feb2017
ms.date: 07/17/2017
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.debug.installedapppackagelauncher
- vs.debug.remote.connection
dev_langs:
- C++
- FSharp
- CSharp
- JScript
- VB
helpviewer_keywords:
- app package, debug
ms.assetid: 5a94ad64-100d-43ca-9779-16cb5af86f97
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- uwp
ms.openlocfilehash: 3bb858f2ee20eb65c09dd4979f2bbba1470cbe0d
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49908255"
---
# <a name="debug-an-installed-app-package-in-visual-studio-uwp"></a>Yüklü uygulama paketi, Visual Studio (UWP) hata ayıklama

Tıklayarak tüm yüklü uygulama paketinin hatalarını ayıklayabilir **hata ayıklama > diğer hata ayıklama hedefleri > yüklenen uygulama paketinin hatalarını ayıklama**. Hata ayıklama bu yöntem, bu cihazlara Evrensel Windows uygulamaları (UWP) için kullanılabilir:

* Windows 10 (telefonlarda desteklenmez)
* XBox
* HoloLens
* IOT

Bu özellikler hakkında daha fazla bilgi için güncelleştirmeler için blog gönderisine bakın [hata ayıklama yüklü uygulama paketleri](https://blogs.msdn.microsoft.com/devops/2016/03/30/updates-for-debugging-installed-app-packages-in-visual-studio-2015-update-2/) ve gönderi [Evrensel Windows uygulamaları (UWP) oluşturma](https://blogs.msdn.microsoft.com/visualstudio/2016/08/02/universal-windows-apps-targeting-windows-10-anniversary-sdk/).

## <a name="debug-an-installed-app-package-or-running-app-on-a-local-machine-or-device"></a>Yüklü uygulama paketi ya da bir yerel makine veya cihazda çalışan uygulama hata ayıklama

1. Visual Studio'da açın, UWP projesi ile tıklayın **hata ayıklama > diğer hata ayıklama hedefleri > yüklenen uygulama paketinin hatalarını ayıklama**.

2. Şunlardan birini seçin **yerel makine** veya **cihaz**.

     Seçerseniz **cihaz**, bilgisayarınızın bir Windows 10 cihazına fiziksel olarak bağlı olması gerekir.

     ![DebugInstalledAppPackage](../debugger/media/debug-installed-app-pkg.png "DebugInstalledAppPackage")

     Yüklü uygulama paketleri gösterisini altında çalışmakta **çalıştıran** düğümü. Show altında çalışan olmayan uygulama paketlerinin yüklü **çalışmıyor**.

3. Altında hata ayıklamak istediğiniz uygulamanın adını seçin **çalıştıran** veya **çalışmıyor** ve **Başlat** veya uygulama zaten çalışıyorsa seçin **Ekle**.

     Seçerseniz **başlatma, ancak başlatıldığında kodumda Hata Ayıkla**, bu özel teker teker başlattığınızda uygulamanıza eklemek Visual Studio hata ayıklayıcı neden olur. Bu denetim yolları hata ayıklamak için etkili bir yoludur [farklı başlatma yöntemleri](/windows/uwp/xbox-apps/automate-launching-uwp-apps), özel parametrelerle protokolünü etkinleştirme gibi.

> [!NOTE]
> Visual Studio ayrıca iliştirebilirsiniz çalışan bir UWP uygulaması işleme seçerek **hata ayıklama**, ardından **iliştirme**. Çalışan bir işleme iliştirilmeyi özgün Visual Studio projesini gerektirmez, ancak işlemin semboller yükleniyor önemli ölçüde için özgün koda sahip olmayan bir işlemin hatalarını ayıklamaya yardımcı.
  
## <a name="remote"></a> Uzak bir bilgisayarda yüklü olan veya çalışan uygulama hata ayıklama 

Uzak bir bilgisayarda yüklü uygulama paketinin ilk kez hata ayıklaması yaparken, Visual Studio hedef cihazınız için Uzak Araçlar'ın doğru sürümü yükler. Hedef cihazınız Windows 10 bilgisayarı, XBox, HoloLens ve IOT cihazı olması gerekir.

1. Windows 10 Cihazınızda etkinleştirmek [Geliştirici modu](/windows/uwp/get-started/enable-your-device-for-development).

2. Windows 10 güncelleştirme sürümü öncesi-oluşturanın önce el ile çalışan uzak bir Bilgisayara bağlanıyorsanız [yükleme ve uzaktan hata ayıklayıcıyı başlatma](../debugger/remote-debugging.md).

     Bir XBox, HoloLens ve IOT cihaz ve Windows 10 Creator'ın Update çalıştıran Windows cihazlar için uzaktan hata ayıklayıcı el ile yüklemeniz gerekmez. Uzak Araçlar, uygulamayı dağıttığınızda otomatik olarak yüklenir.

3. Tıklayın **hata ayıklama > hata ayıklama hedefi sayısı diğer > yüklenen uygulama paketinin Hatalarını Ayıkla**.

4. İlk açılan listeden seçin **uzak makine**.

5. Adı veya eklemek istediğiniz bilgisayarın IP adresini yazın.

     ![ChooseRemoteComputer](../debugger/media/debug-remote-app-pkg.png "ChooseRemoteComputer")

     Bilgisayar adını kullanarak bağlanamıyorsa (seçtiğiniz sonra **Başlat**), bunun yerine IP adresi kullanın. IP adresi, XBox, HoloLens ve IOT cihazlar için kullanın.

6. Bir seçenek belirleyerek kimlik doğrulaması yapmayı seçin **kimlik doğrulama modu**.

    Çoğu uygulama için varsayılan değer tutmak **Evrensel (şifrelenmemiş Protokolü)**.

7. Altında hata ayıklamak istediğiniz uygulamanın adını seçin **çalıştıran** veya **çalışmıyor** ve **Başlat** veya (çalışan uygulamalar) **iliştirme**.

     Seçerseniz **başlatma, ancak başlatıldığında kodumda Hata Ayıkla**, bu özel teker teker başlattığınızda, uygulama paketi için Visual Studio hata ayıklayıcısının neden olur. Bu denetim yolları hata ayıklamak için etkili bir yoludur [farklı başlatma yöntemleri](/windows/uwp/xbox-apps/automate-launching-uwp-apps), özel parametrelerle protokolünü etkinleştirme gibi.

     İlk kez bağlı bir XBox, HoloLens ve IOT cihazda yüklü uygulama paketinin hata ayıklaması yaparken, Visual Studio uzaktan hata ayıklayıcı hedef cihazınız için doğru sürümünü yükler. Bu işlem biraz zaman alabilir ve bir ileti görürsünüz ``Starting remote debugger`` bu gerçekleştiği sırada.

     > [!NOTE]
   > Sunmak, XBox veya HoloLens cihaz uygulama zaten çalışıyorsa ayıklayıcıyı yeniden başlatılır.

[Dağıtma ve hata ayıklama UWP apps]((/windows/uwp/debug-test-perf/deploying-and-debugging-uwp-apps#advanced-remote-deployment-options). uzak dağıtımını UWP uygulamaları için Gelişmiş seçenekleri hakkında daha fazla bilgi için bkz. 
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Visual Studio’da hata ayıklama](../debugger/index.md)  
 [Hata ayıklayıcısı özellik turu](../debugger/debugger-feature-tour.md)  
 [Uzaktan Hata Ayıklama](../debugger/remote-debugging.md)  
 [Windows Güvenlik Duvarı’nı Uzaktan Hata Ayıklama İçin Yapılandırma](../debugger/configure-the-windows-firewall-for-remote-debugging.md)  
 [Uzaktan Hata Ayıklayıcı Bağlantı Noktası Atamaları](../debugger/remote-debugger-port-assignments.md)  
 [Uzaktan Hata Ayıklama Hataları ve Sorun Giderme](../debugger/remote-debugging-errors-and-troubleshooting.md)