---
title: '2. Adım: İlk ASP.NET Core Web uygulamanızı oluşturma'
description: Bu video öğreticide ve adım adım yönergeleri ile ilk ASP.NET Core Web uygulamanızı oluşturun.
ms.custom: get-started
ms.date: 03/31/2019
ms.technology: vs-ide-general
ms.prod: visual-studio-windows
monikerRange: vs-2019
ms.topic: tutorial
ms.devlang: CSharp
author: ardalis
ms.author: tglee
manager: jillfra
dev_langs:
- CSharp
ms.workload:
- aspnet
- dotnetcore
ms.openlocfilehash: 5e9cc4f579b5913d5be3030828cad1a799efcd72
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58859150"
---
# <a name="step-2-create-your-first-aspnet-core-web-app"></a>2. Adım: İlk ASP.NET Core web uygulamanızı oluşturma

Bu video öğreticide ve adım adım yönergeleri ile ilk ASP.NET Core Web uygulamanızı oluşturun.

_Bu video ve bunların ilk ASP.NET Core uygulamanızı oluşturmak için izleme izleyin._

> [!VIDEO https://www.youtube.com/embed/-79RkpyFB6E]

## <a name="start-visual-studio-2019-and-create-a-new-project"></a>Visual Studio 2019'ı başlatın ve yeni bir proje oluşturun

Visual Studio 2019 başlatır ve **yeni proje oluştur**. Seçin **ASP.NET Core Web uygulaması**. Seçin **Web uygulaması** şablonu ve canlı varsayılan proje adı ve konumu. **Oluştur**'u tıklatın. Daha ayrıntılı yönergeler için bkz [Bu öğretici serisinin önceki videoda](tutorial-aspnet-core-ef-step-01.md).

![Visual Studio 2019 ASP.NET Core proje seçenekleri seçin](media/vs-2019/vs2019-choose-aspnetcore-project.png)

## <a name="explore-the-new-project"></a>Yeni Proje keşfedin

Çözüm Gezgini penceresinde, sağ taraftaki yeni projenin içeriğini görüntüleyebilirsiniz. Bunlar burada açıklanan.

![Visual Studio 2019 ASP.NET Core projesi](media/vs-2019/vs2019-solution-explorer.png)

### <a name="wwwroot"></a>wwwroot

*Wwwroot* klasör web uygulamasından genel olarak erişilebilir olan statik dosyalar tutar. Genellikle, stil sayfaları, istemci tarafı komut dosyası ve görüntü de içerir.

### <a name="pages"></a>Sayfalar

*Sayfaları* klasör sitenin Razor sayfaları içerir. Varsayılan şablon dahil olmak üzere çeşitli sayfalar sağlar *Index.cshtml* uygulama giriş sayfası, de olarak hakkında her şey sayfası, kişi ve benzeri.

### <a name="appsettingsjson"></a>appsettings.json

Bu dosya JSON biçiminde bir site için yapılandırma ayarlarını içerir.

### <a name="programcs"></a>Program.cs

Bu dosya, uygulama için giriş noktası olarak görev yapar. Uygulama çalıştırıldığında, kendi ana yöntemi çalıştırılır ve uygulamayı içerecek Web ana bilgisayarı oluşturmaktan sorumlu olan ilk yöntemidir.

### <a name="startupcs"></a>Startup.cs

Web ana bilgisayarı oluşturulan *Program.cs* başlangıç sınıfı atıfta bulunan ve uygulamayı yapılandırmak için onun yöntemlerini çağırır. Createservicereplicalisteners() yöntemi, hizmetlerin uygulama kullanır ayarlamaktan sorumludur. `Configure` Yöntemi, uygulamanın HTTP istek işlem hattı ayarlar. Her parça ile etkileşim kurma, bu işlem hattı aracılığıyla her isteğin gittiğini *ara yazılım* olarak bunu yapar.

### <a name="indexcshtml"></a>Index.cshtml

Site için giriş sayfası, bazı HTML İşaretleme ve bazı sunucu tarafı Razor kodu içerir. Razor sayfa modeli belirtmek için kullandığı `IndexModel`, bulunduğu ilişkili *Index.cshtml.cs* dosya. Ayrıca, ViewData içinde bir değer ayarlayarak sayfa başlığının da ayarlar. Bu ViewData değeri okunan  *\_Layout.cshtml* dosyası, paylaşılan klasörün içinden sayfalar klasöründe bulunan. Düzen dosyası, birçok Razor sayfaları tarafından paylaşılan ve uygulama için genel görünümü sağlar. Her sayfanın içeriğinin düzenini dosyanın HTML içinde işlenir.

## <a name="run-the-application"></a>Uygulamayı çalıştırma

Şimdi uygulamayı çalıştırın ve tarayıcıda görüntüleyebilirsiniz. Kullanarak uygulamayı çalıştırabilirsiniz **Ctrl**+**F5** seçerek veya **hata ayıklama** > **hata ayıklama olmadan Başlat**Visual Studio menüsünde.

## <a name="customize-the-application"></a>Uygulamayı özelleştirme

Bir özellik ekleyin *Index.cshtml.cs* dosyasını açıp değeri geçerli zamana Ayarla `OnGet` işleyicisi:

```csharp
public string Time { get; set; }
public void OnGet()
{
    Time = DateTime.Today.ToShortTimeString();
}
```

Değiştirin `<div>` içeriği *Index.cshtml* bu işaretleme ile:

```cshtml
<h2>It's @Model.Time right now on the server!</h2>
```

Uygulamayı yeniden çalıştırın. Sayfa artık geçerli zamanı görüntüler, ancak her zaman gece yarısıdır görmeniz gerekir! Bu doğru değil.

![Visual Studio 2019 ASP.NET Core projesi tarayıcıda](media/vs-2019/vs2019-app-in-browser.png)

## <a name="debug-the-application"></a>Uygulamada hata ayıklama

Bir kesme noktasına ekleme `OnGet` yöntemi burada biz atamak için bir değer `Time` ve uygulamada hata ayıklama bu zaman başlangıcı.

Çizgi ve yürütme duruyor, görebilirsiniz `DateTime.Today` tarihi içerir ancak zaman zaman veri içermediği için her zaman gece yarısıdır. 

![Visual Studio 2019 ASP.NET Core projesi tarayıcıda](media/vs-2019/vs2019-breakpoint.png)

Bunu kullanmak için değiştirmeniz `DateTime.Now` ve yürütme devam edin. Yeni kod için `OnGet` olmalıdır:

```csharp
public void OnGet()
{
    Time = DateTime.Now.ToShortTimeString();
}
```

Uygulamada gezindiğinizde artık gerçek sunucu zaman tarayıcıda görmeniz gerekir.

![Visual Studio 2019 ASP.NET Core projesi tarayıcıda](media/vs-2019/vs2019-app-fixed-in-browser.png)

## <a name="next-steps"></a>Sonraki adımlar

Sonraki videoda, veri desteğini uygulamanıza nasıl ekleyeceğinizi öğreneceksiniz.

[Öğretici: ASP.NET Core uygulamanızı verilerle çalışma](tutorial-aspnet-core-ef-step-03.md)

## <a name="see-also"></a>Ayrıca bkz.

- [Öğretici: ASP.NET Core Razor sayfaları web uygulaması oluşturma](/aspnet/core/tutorials/razor-pages/?view=aspnetcore-2.1)
