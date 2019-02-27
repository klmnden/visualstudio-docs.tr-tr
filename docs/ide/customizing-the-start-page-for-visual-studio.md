---
title: Değişiklik başlangıç deneyimi
ms.date: 02/01/2017
ms.topic: conceptual
f1_keywords:
- vs.ToolsOptionsPages.Startup
helpviewer_keywords:
- Start Page [Visual Studio]
- customizing Start Page [Visual Studio]
- Visual Studio Start Page
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: c15824ec28547cbdb18fdfebc4ebcee1bdd1d387
ms.sourcegitcommit: cea6187005f8a0cdf44e866a1534a4cf5356208c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/27/2019
ms.locfileid: "56953388"
---
# <a name="customize-startup"></a>Başlangıç'ı özelleştirme

Visual Studio için başlangıç deneyimini çözümünüzün en son ya da boş bir geliştirme ortamı yalnızca bir açma gibi birçok farklı şekilde özelleştirebilirsiniz.

::: moniker range="vs-2017"

Araç penceresinde çalışan ve Visual Studio'ya özel dahili komutları çalıştıran bir Windows Presentation Foundation (WPF) XAML sayfası olarak, özel bir başlangıç sayfası da gösterebilirsiniz.

::: moniker-end

## <a name="to-change-the-startup-item"></a>Başlangıç öğesini değiştirmek için

1. Menü çubuğunda, **Araçları** > **seçenekleri**.

2. Genişletin **ortam**ve ardından **başlangıç**.

::: moniker range="vs-2017"

3. İçinde **başlangıçta** listesinde, Visual Studio'yu başlattıktan sonra görüntülenecek öğeyi seçin.

::: moniker-end

::: moniker range=">=vs-2019"

3. İçinde **, başlangıçta açılması** listesinde, Visual Studio'yu başlattıktan sonra olmasını istediğinizi seçin. Aralarından seçim yapabileceğiniz **başlangıç penceresi** (olanak sağlayan yeni veya mevcut bir projeyi açmayı), **en son çözüm**, veya **boş ortam**.

::: moniker-end

::: moniker range="vs-2017"

## <a name="to-show-a-custom-start-page"></a>Özel başlangıç sayfası göstermek için

Yapabilecekleriniz [kendi özel başlangıç sayfası oluşturma](../extensibility/creating-a-custom-start-page.md) Visual Studio SDK'sını kullanarak veya bir başkası zaten oluşturduğu kullanın. Örneğin, özel başlangıç sayfalarda bulabilirsiniz [Visual Studio Market](https://marketplace.visualstudio.com/search?target=VS&category=Tools&vsVersion=&subCategory=Start%20Pages&sortBy=Downloads).

Özel başlangıç sayfası yüklemek için açın *.vsix* dosyası veya kopyalayın ve başlangıç sayfası dosyalarına yapıştırın *%USERPROFILE%\Documents\Visual Studio 2017\StartPages* bilgisayarınızda bir klasör.

### <a name="to-select-which-custom-start-page-to-display"></a>Görüntülenecek hangi özel başlangıç sayfası seçin

1. Menü çubuğunda, **Araçları** > **seçenekleri**.

1. Genişletin **ortam**ve ardından **başlangıç**.

1. İçinde **başlangıç sayfasını Özelleştir** listesinde, istediğiniz sayfayı seçin.

> [!TIP]
> Özel başlangıç sayfasındaki bir hata Visual Studio'nun çökmesine neden olursa, Visual Studio'yu güvenli modda başlatabilir ve varsayılan başlangıç sayfasını kullanacak şekilde ayarlayabilirsiniz. Bkz: [safemode (devenv.exe)](../ide/reference/safemode-devenv-exe.md).

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio IDE'yi kişiselleştirme](../ide/personalizing-the-visual-studio-ide.md)

::: moniker-end