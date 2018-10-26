---
title: Visual Studio yükleme için komut satırı parametresi örnekleri
description: Bu örnekleri kendi Visual Studio komut satırı yüklemesi oluşturmak için özelleştirin.
ms.date: 05/07/2018
ms.technology: vs-acquisition
ms.prod: visual-studio-dev15
ms.topic: conceptual
ms.assetid: 837F31AA-F121-46e9-9996-F8BCE768E579
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 7cd3c7a5b191ee74005eb79da0767223ca43de08
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49895491"
---
# <a name="command-line-parameter-examples-for-visual-studio-2017-installation"></a>Visual Studio 2017 yüklemesi için komut satırı parametresi örnekleri

Göstermek için nasıl [Visual Studio'yu yüklemek için komut satırı parametreleri kullanmak](use-command-line-parameters-to-install-visual-studio.md), ihtiyaçlarınıza uygun olarak özelleştirebileceğiniz bazı örnekleri aşağıda verilmiştir.

Her örnekte `vs_enterprise.exe`, `vs_professional.exe` ve `vs_community.exe` indirme işlemini başlatan küçük (yaklaşık 1 MB) dosyası Visual Studio önyükleyicisi ilgili sürümünü temsil eder. Farklı bir sürümü kullanıyorsanız, uygun önyükleyici adıyla değiştirin.

> [!NOTE]
> Tüm komutlar, yönetimsel ayrıcalık ve işlemin yükseltilmiş isteminden başlamamışsa istemi görüntülenecek olan bir kullanıcı hesabı denetimi gerektirir.
>
> [!NOTE]
>  Kullanabileceğiniz `^` birden fazla satır tek bir komutta birleştirmek için komut satırının sonunda karakter. Alternatif olarak, yalnızca bu satırlara birlikte tek bir satır yerleştirebilirsiniz. PowerShell'de vurgulamasını belirtir eşdeğerdir (`` ` ``) karakter.

## <a name="using---installpath"></a>--İnstallPath kullanma

* Visual Studio, en az bir örneğini hiçbir etkileşimli istemleri ancak görüntülenen ilerleme durumu ile yükleyin:

  ```cmd
  vs_enterprise.exe --installPath C:\minVS ^
   --add Microsoft.VisualStudio.Workload.CoreEditor ^
   --passive --norestart
  ```

* Hiçbir etkileşimli istemleri ancak görüntülenen ilerleme durumu ile komut satırını kullanarak bir Visual Studio örneği güncelleştirin:

  ```cmd
  vs_enterprise.exe --update --quiet --wait
  vs_enterprise.exe update --wait --passive --norestart --installPath "C:\installPathVS"
  ```

  > [!NOTE]
  > Her iki komut gereklidir. İlk komut, Visual Studio yükleyicisi güncelleştirir. İkinci komut, Visual Studio örneğini güncelleştirir. Bir kullanıcı hesabı denetimi iletişim önlemek için komut istemini yönetici olarak çalıştırın.

* Bir masaüstü Visual Studio örneğini sessiz bir şekilde, yalnızca ürün yüklendiğinde döndüren Fransızca Dil paketi yükleyin.

  ```cmd
  vs_enterprise.exe --installPath C:\desktopVS ^
   --addProductLang fr-FR ^
   --add Microsoft.VisualStudio.Workload.ManagedDesktop ^
   --includeRecommended --quiet --wait
  ```

  > [!NOTE]
  > `--wait` Parametresi, bir toplu iş dosyası kullanmak için tasarlanmıştır. Yükleme işlemi tamamlanana kadar bir toplu iş dosyasında İleri de komutu yürütmeye devam etmeyecek. `%ERRORLEVEL%` Açıklandığı gibi ortam değişkeni komut dönüş değeri içerecek [Visual Studio'yu yüklemek için komut satırı parametreleri kullanmak](use-command-line-parameters-to-install-visual-studio.md) sayfası.

## <a name="using---layout"></a>Kullanarak--düzeni

* Visual Studio çekirdek Düzenleyicisi'ni (en az Visual Studio yapılandırması) indirin. Yalnızca İngilizce dil paketi içerir:

  ```cmd
  vs_community.exe --layout C:\VS2017
   --lang en-US ^
   --add Microsoft.VisualStudio.Workload.CoreEditor
  ```

* .NET Masaüstü ve .NET web iş yüklerinin yanı sıra tüm önerilen bileşenleri ve GitHub uzantısı'nı indirin. Yalnızca İngilizce dil paketi içerir:

  ```cmd
  vs_community.exe --layout C:\VS2017 ^
   --lang en-US ^
   --add Microsoft.VisualStudio.Workload.NetWeb ^
   --add Microsoft.VisualStudio.Workload.ManagedDesktop ^
   --add Component.GitHub.VisualStudio ^
   --includeRecommended
  ```

## <a name="using---includerecommended"></a>--İncludeRecommended kullanma

* Etkileşimli bir yükleme, tüm iş yükleri ve Visual Studio 2017 Enterprise sürümünde kullanılabilir olan bileşenleri başlatın:

  ```cmd
  vs_enterprise.exe --all --includeRecommended --includeOptional
  ```

* Visual Studio 2017 Professional'ın ikinci, adlandırılmış bir örnek ile Visual Studio 2017 Community edition, Node.js geliştirme desteği ile yüklü bir makineye yükleyin:

  ```cmd
  vs_professional.exe --installPath C:\VSforNode ^
   --add Microsoft.VisualStudio.Workload.Node --includeRecommended --nickname VSforNode
  ```

## <a name="using---remove"></a>Kullanarak--Kaldır

* Profil oluşturma araçları bileşeni yüklü varsayılan Visual Studio örneği kaldırın:

  ```cmd
  vs_enterprise.exe modify ^
   --installPath "C:\Program Files (x86)\Microsoft Visual Studio\2017\Enterprise" ^
   --remove Microsoft.VisualStudio.Component.DiagnosticTools ^
   --passive
  ```

## <a name="using---path"></a>Kullanarak--yolu

Bu komut satırı parametreleri **15.7 sürümündeki yeni**. Bunlar hakkında daha fazla bilgi için bkz. [Visual Studio'yu yüklemek için komut satırı parametreleri kullanmak](use-command-line-parameters-to-install-visual-studio.md) sayfası.

* Yükleme, önbellek ve paylaşılan yollarını kullanarak:

  `vs_enterprise.exe --add Microsoft.VisualStudio.Workload.CoreEditor --path install="C:\VS" --path cache="C:\VS\cache" --path shared="C:\VS\shared"`

* Yalnızca yükleme ve önbellek yollarını kullanarak:

  `vs_enterprise.exe --add Microsoft.VisualStudio.Workload.CoreEditor --path install="C:\VS" --path cache="C:\VS\cache"`

* Yalnızca yükleme ve paylaşılan yolları kullanarak:

  `vs_enterprise.exe --add Microsoft.VisualStudio.Workload.CoreEditor --path install="C:\VS" --path shared="C:\VS\shared"`

* Yükleme yolu kullanarak:

  `vs_enterprise.exe --add Microsoft.VisualStudio.Workload.CoreEditor --path install="C:\VS"`

[!INCLUDE[install_get_support_md](includes/install_get_support_md.md)]

## <a name="see-also"></a>Ayrıca bkz.

* [Visual Studio Yönetici Kılavuzu](visual-studio-administrator-guide.md)
* [Komut satırı parametrelerini kullanarak Visual Studio'yu yükleme](use-command-line-parameters-to-install-visual-studio.md)
* [Visual Studio 2017'in çevrimdışı yüklemesini oluşturma](create-an-offline-installation-of-visual-studio.md)
