---
title: Başlangıç sayfasını özelleştirme | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: conceptual
f1_keywords:
- vs.startpage
- VS.StartPage.HowDoI
- vs.ToolsOptionsPages.Startup
helpviewer_keywords:
- Start Page [Visual Studio]
- customizing Start Page [Visual Studio]
- Visual Studio Start page
ms.assetid: 925d42eb-ec34-426e-ad81-19db8630e536
caps.latest.revision: 48
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 266082af039ee7f0ba2bd60e0c9a67145aaed1d3
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65701132"
---
# <a name="customizing-the-start-page-for-visual-studio"></a>Visual Studio için Başlangıç Sayfasını Özelleştirme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Gösterildiği gibi bazı varsayılan yöntemlerle Visual Studio için başlangıç sayfasını özelleştirebilirsiniz **açık proje** iletişim kutusu veya en son yüklenen çözümü açma. Araç penceresinde çalışan ve Visual Studio'ya özel dahili komutları çalıştıran bir Windows Presentation Foundation (WPF) XAML sayfası olarak, özel bir başlangıç sayfası da gösterebilirsiniz.

## <a name="customizing-the-default-start-page"></a>Varsayılan başlangıç sayfasını özelleştirme

1. Menü çubuğunda, **Araçları**, **seçenekleri**.

2. Genişletin **ortam**ve ardından **başlangıç**.

3. İçinde **başlangıçta** listesinde, kullanmak istediğiniz özelleştirme için öğeyi seçin.

## <a name="show-a-custom-start-page"></a>Özel başlangıç sayfası gösterme

1. Özel bir başlangıç sayfası yüklemek için aşağıdaki yöntemlerden birini kullanın:

    - Buradan yükleyin [Visual Studio Market](https://marketplace.visualstudio.com/), başka bir Web sitesi veya yerel intranet ağınızdaki bir sayfa.

        > [!NOTE]
        > Visual Studio'nun önceki bir sürümü için hedeflenen bir sayfayı beğeniyorsanız, Visual Studio SDK kullanarak sayfayı yükseltebilirsiniz. Bkz: [nasıl yapılır: Visual Studio özel başlangıç sayfası yükseltme](../misc/how-to-upgrade-a-visual-studio-custom-start-page.md).

         Özel başlangıç sayfası içeren .vsix dosyasını açın, kopyalayın ve başlangıç sayfası dosyalarına yapıştırın **% USERPROFILE % \My Documents\Visual Studio 2015\StartPages** bilgisayarınızda bir klasör.

    - Visual Studio SDK yüklediyseniz kendi başlangıç sayfanızı oluşturun.

         Bkz: [oluşturarak kendi başlangıç sayfanızı](../misc/creating-your-own-start-page.md).

2. Menü çubuğunda, **Araçları**, **seçenekleri**.

3. Genişletin **ortam**ve ardından **başlangıç**.

4. İçinde **başlangıç sayfasını Özelleştir** listesinde, istediğiniz sayfayı seçin.

> [!NOTE]
> Özel başlangıç sayfasındaki bir hata Visual Studio'nun çökmesine neden olursa, Visual Studio'yu güvenli modda başlatabilir ve varsayılan başlangıç sayfasını kullanacak şekilde ayarlayabilirsiniz. Bkz: [safemode (devenv.exe)](../ide/reference/safemode-devenv-exe.md).

## <a name="see-also"></a>Ayrıca Bkz.
 [Visual Studio'da geliştirme ayarlarını özelleştirme](https://msdn.microsoft.com/22c4debb-4e31-47a8-8f19-16f328d7dcd3) [başlangıç sayfasının kendi oluşturma](../misc/creating-your-own-start-page.md)
