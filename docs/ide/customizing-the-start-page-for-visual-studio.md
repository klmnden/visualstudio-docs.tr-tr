---
title: Özel başlangıç sayfası yüklemek veya başlangıç öğesini değiştirin
ms.date: 02/01/2017
ms.prod: visual-studio-dev15
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
ms.openlocfilehash: 8fca98116a6d810a97abbf4e1f850b2312f42c60
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/26/2019
ms.locfileid: "55070988"
---
# <a name="customize-the-start-page-for-visual-studio"></a>Visual Studio için başlangıç sayfasını özelleştirme

Visual Studio için başlangıç deneyimi gösterildiği gibi birkaç farklı yolla özelleştirebileceğiniz **açık proje** iletişim kutusu veya en son yüklenen çözümü açma. Araç penceresinde çalışan ve Visual Studio'ya özel dahili komutları çalıştıran bir Windows Presentation Foundation (WPF) XAML sayfası olarak, özel bir başlangıç sayfası da gösterebilirsiniz.

## <a name="to-change-the-startup-item"></a>Başlangıç öğesini değiştirmek için

1. Menü çubuğunda, **Araçları** > **seçenekleri**.

1. Genişletin **ortam**ve ardından **başlangıç**.

1. İçinde **başlangıçta** listesinde, Visual Studio'yu başlattıktan sonra görüntülenecek öğeyi seçin.

## <a name="to-show-a-custom-start-page"></a>Özel başlangıç sayfası göstermek için

Yapabilecekleriniz [kendi özel başlangıç sayfası oluşturma](../extensibility/creating-a-custom-start-page.md) Visual Studio SDK'sını kullanarak veya bir başkası zaten oluşturduğu kullanın. Örneğin, özel başlangıç sayfalarda bulabilirsiniz [Visual Studio Market](https://marketplace.visualstudio.com/search?target=VS&category=Tools&vsVersion=&subCategory=Start%20Pages&sortBy=Downloads).

Özel başlangıç sayfası yüklemek için açın *.vsix* dosyası veya kopyalayın ve başlangıç sayfası dosyalarına yapıştırın *%USERPROFILE%\Documents\Visual Studio 2017\StartPages* bilgisayarınızda bir klasör.

### <a name="to-select-which-custom-start-page-to-display"></a>Görüntülenecek hangi özel başlangıç sayfası seçin

1. Menü çubuğunda, **Araçları** > **seçenekleri**.

1. Genişletin **ortam**ve ardından **başlangıç**.

1. İçinde **başlangıç sayfasını Özelleştir** listesinde, istediğiniz sayfayı seçin.

> [!NOTE]
> Özel başlangıç sayfasındaki bir hata Visual Studio'nun çökmesine neden olursa, Visual Studio'yu güvenli modda başlatabilir ve varsayılan başlangıç sayfasını kullanacak şekilde ayarlayabilirsiniz. Bkz: [safemode (devenv.exe)](../ide/reference/safemode-devenv-exe.md).

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio IDE'yi kişiselleştirme](../ide/personalizing-the-visual-studio-ide.md)