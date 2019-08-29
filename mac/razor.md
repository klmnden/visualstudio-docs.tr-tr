---
title: Razor
description: Mac için Visual Studio 'de asp.net Core uygulamalarındaki Razor desteğiyle ilgili bilgiler
author: sayedihashimi
ms.author: sayedha
ms.date: 05/03/2018
ms.technology: vs-ide-general
ms.assetid: F898CB6E-05ED-44CD-8DB6-427B2592CCC6
ms.openlocfilehash: a66a31d2c63fcb0e2adc4554c49a76c727f9a288
ms.sourcegitcommit: cf8c0fef2b9690595e99ce3802586cdd55fd37c2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/28/2019
ms.locfileid: "70107924"
---
# <a name="razor"></a>Razor

Mac için Visual Studio, IntelliSense ve *. cshtml* dosyalarında sözdizimi vurgulama dahil olmak üzere Razor düzenlemesi için destek sağlar.

![Mac için Visual Studio 'de Razor düzenlemesi](media/razor-editor.png)

Bu kılavuz, ilk Razor Web uygulamanızı oluşturmaya bir giriş sağlar. Daha ayrıntılı bir kılavuz için lütfen [.NET Core belgelerindeki Razor Pages](/aspnet/core/razor-pages/index)bakın.

## <a name="creating-a-new-razor-project"></a>Yeni bir Razor projesi oluşturma

* Yeni bir proje oluşturmak için hoş geldiniz ekranından **Yeni** ' yi seçin:

![Yeni Mac için Visual Studio proje](media/razor-new.png)

* Yeni proje iletişim kutusunda **.NET Core** > **uygulama** > **Web uygulaması** ' na gidin ve **İleri** düğmesini seçin:

![Razor proje şablonu](media/razor-new-project1.png)

* .NET Core hedef çatısını gerekli (önerilen 2,2 veya üzeri) seçin ve **İleri ' yi**seçin.  Projeniz için bir ad seçin ve gerekirse git desteği ekleyin. Projeyi oluşturmak için **Oluştur** ' u seçin.

![Razor proje adı](media/razor-new-project2.png)

Mac için Visual Studio, projenizi kod düzeninde açacak.

* **Cmd-opt-F5** kullanarak projeyi hata ayıklama olmadan çalıştırma

Visual Studio, [Kestral](https://docs.microsoft.com/aspnet/core/fundamentals/servers/kestrel) 'ı başlatacak ve ilk Razor Web `https://localhost:5001` uygulamanızı görüntülemesi için bir tarayıcı başlatacaktır:

![Safari 'de Razor Web uygulaması](media/razor-webapp.png)

## <a name="project-anatomy"></a>Proje anatomumu

Razor Web uygulamaları aşağıdaki bileşenlerden oluşur:

### <a name="pages-folder"></a>Sayfalar klasörü

Projenin içindeki sayfalar klasörü, Web sayfalarının her biri için arka plan kodu ile birlikte bulunabileceği yerdir:
* HTML biçimlendirme ve Razor söz dizimi için * *. cshtml* dosyası.
* Arka plan C# kodu için sayfa olaylarını işlemek için bir * *. cshtml.cs* dosyası.

Destekleyici dosyalar bir alt çizgiyle başlayan adlara sahiptir. Örneğin, _Layout. cshtml dosyası tüm sayfalarda ortak kullanıcı arabirimi öğelerini yapılandırır. Bu dosya sayfanın en üstündeki gezinti menüsünü ve sayfanın alt kısmındaki telif hakkı bildirimini ayarlar. Daha fazla bilgi için [ASP.NET Core düzen](https://docs.microsoft.com/aspnet/core/mvc/views/layout)bölümüne bakın.

### <a name="launch-settings"></a>Başlatma ayarları

*Launchsettings. JSON* dosyası IIS ayarları, uygulama URL 'si ve diğer ilgili ayarları içerir.

### <a name="app-settings"></a>Uygulama ayarları

*AppSettings, JSON* dosyası bağlantı dizeleri gibi yapılandırma verilerini içerir.

Yapılandırma hakkında daha fazla bilgi için [ASP.net Kılavuzu 'Ndaki yapılandırmaya](https://docs.microsoft.com/aspnet/core/fundamentals/configuration/index)bakın.

### <a name="wwwroot-folder"></a>Wwwroot klasörü

HTML dosyaları, JavaScript dosyaları ve CSS dosyaları gibi statik dosyaları içerir. Daha fazla bilgi için [ASP.NET Core Içindeki statik dosyalar](https://docs.microsoft.com/aspnet/core/fundamentals/static-files)bölümüne bakın.

### <a name="programcs"></a>Program.cs

Programın giriş noktasını içerir. Daha fazla bilgi için bkz. [ASP.NET Core Web Host](https://docs.microsoft.com/aspnet/core/fundamentals/host/web-host).

### <a name="startupcs"></a>Startup.cs

Tanımlama bilgilerinin onayını gerektirip gerektirmediğini belirten uygulama davranışını yapılandıran kodu içerir. Daha fazla bilgi için [ASP.NET Core uygulamasında uygulama başlatma](https://docs.microsoft.com/aspnet/core/fundamentals/startup)bölümüne bakın.

## <a name="see-aso"></a>Bkz. ASO

Razor Web uygulamaları oluşturma hakkında daha kapsamlı bir kılavuz için bkz. [ASP.NET Core Razor Pages giriş](https://docs.microsoft.com/aspnet/core/razor-pages/index).
