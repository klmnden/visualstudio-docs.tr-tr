---
title: Razor
description: Mac için Visual Studio'da asp.net core uygulamaları razor desteği hakkında bilgi
author: conceptdev
ms.author: crdun
ms.date: 05/03/2018
ms.topic: article
ms.technology: vs-ide-general
ms.assetid: F898CB6E-05ED-44CD-8DB6-427B2592CCC6
ms.openlocfilehash: 181059ae2985f570ad1dc0749045e39ed4ec1e7e
ms.sourcegitcommit: 3cc73e74921a9ceb622542e0e263abeebc455c00
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/08/2019
ms.locfileid: "67624511"
---
# <a name="razor"></a>Razor

Mac için Visual Studio destek sağlar, Razor düzenleme için IntelliSense hem de söz dizimi de dahil olmak üzere *.cshtml* dosyaları.

![Razor Mac için Visual Studio'da düzenleme](media/razor-editor.png)

Bu kılavuz, ilk Razor web uygulamanızı oluşturmak için bir giriş sağlar. Daha ayrıntılı bir kılavuz için bkz [Razor sayfaları .NET Core belgelerindeki](/aspnet/core/razor-pages/index).

## <a name="creating-a-new-razor-project"></a>Yeni bir Razor projesi oluşturma

* Karşılama ekranında seçin **yeni** yeni bir proje oluşturmak için:

![Yeni Proje Mac için Visual Studio](media/razor-new.png)

* Yeni Proje iletişim kutusunda gidin **.NET Core** > **uygulama** > **Web uygulaması** seçip **sonraki**düğmesi:

![Razor proje şablonu](media/razor-new-project1.png)

* Gerekli, .NET Core hedef çerçeve seçin (önerilen 2.2 veya üzeri) seçip **sonraki**.  Projeniz için bir ad seçin ve gerekiyorsa git desteği ekleyin. Seçin **Oluştur** projeyi oluşturmak için.

![Razor proje adı](media/razor-new-project2.png)

Mac için Visual Studio projeniz kod düzende açılır.

* Projeyi kullanarak hata ayıklama olmadan çalıştırmak **Cmd iyileştirilmiş F5**

Visual Studio başlayacak [Kestral](https://docs.microsoft.com/aspnet/core/fundamentals/servers/kestrel) ve için bir tarayıcıyı başlatacak `https://localhost:5001` ve ilk Razor web uygulamanızı görüntüleyin:

![Safari'de Razor web uygulaması](media/razor-webapp.png)

## <a name="project-anatomy"></a>Proje anatomisi

Razor web uygulamaları aşağıdaki bileşenlerden oluşur:

### <a name="pages-folder"></a>Sayfaları klasörü

Proje içinde sayfalar klasöründe, web sayfaları, arka plan kod her birlikte bulunabileceği şöyledir:
*    A * *.cshtml* HTML İşaretleme ve Razor sözdizimi için dosya.
*    A * *. cshtml.cs* dosya, C# sayfa olaylarını işlemek için arka plan kod.

Destekleyici dosyaları bir alt çizgi ile başlayan adları vardır. Örneğin, kullanıcı Arabirimi öğeleri tüm sayfalar için ortak _Layout.cshtml dosyasını yapılandırır. Bu dosya sayfanın üst gezinti menüsünde ve sayfanın alt kısmındaki telif hakkı bildirimi ayarlar. Daha fazla bilgi için [ASP.NET Core düzende](https://docs.microsoft.com/aspnet/core/mvc/views/layout).

### <a name="launch-settings"></a>Başlatma ayarları

*LaunchSettings.json* dosya IIS ayarlarını içeriyorsa, uygulama URL'si ve diğer ilgili ayarları.

### <a name="app-settings"></a>Uygulama ayarları

*AppSettings, json* dosya bağlantı dizeleri gibi yapılandırma verilerini içerir.

Yapılandırma hakkında daha fazla bilgi için bkz. [ASP.NET Kılavuzu'nda yapılandırma](https://docs.microsoft.com/aspnet/core/fundamentals/configuration/index).

### <a name="wwwroot-folder"></a>wwwroot klasörü

HTML dosyaları, JavaScript dosyaları ve CSS dosyaları gibi statik dosyalar içerir. Daha fazla bilgi için [ASP.NET core'da statik dosyalar](https://docs.microsoft.com/aspnet/core/fundamentals/static-files).

### <a name="programcs"></a>Program.cs

Programın giriş noktası içerir. Daha fazla bilgi için [ASP.NET Core Web ana bilgisayarı](https://docs.microsoft.com/aspnet/core/fundamentals/host/web-host).

### <a name="startupcs"></a>Startup.cs

Olup olmadığı için tanımlama bilgileri onayı gerektirir gibi uygulama davranışını yapılandıran kodunu içerir. Daha fazla bilgi için [ASP.NET Core uygulaması başlangıç](https://docs.microsoft.com/aspnet/core/fundamentals/startup).

## <a name="see-aso"></a>ASO bakın

Razor web uygulamaları oluşturma hakkında daha kapsamlı bir kılavuz için bkz. [ASP.NET Core Razor sayfalar giriş](https://docs.microsoft.com/aspnet/core/razor-pages/index).
