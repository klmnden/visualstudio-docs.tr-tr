---
title: ASP.NET Core Mac için Visual Studio'da uygulama oluşturma
description: Bu makalede, yeni proje oluşturma ve yükleme dahil olmak üzere Mac için Visual Studio'da ASP.NET ile başlamak açıklar.
author: sayedihashimi
ms.author: sayedha
ms.date: 05/30/2019
ms.assetid: 771C2F8E-46BC-4280-AFE8-ED9D5C7790CE
ms.openlocfilehash: f0a2e8433877b3eb61228a886280707f3b4a37fe
ms.sourcegitcommit: 7fbfb2a1d43ce72545096c635df2b04496b0be71
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/09/2019
ms.locfileid: "67693135"
---
# <a name="building-aspnet-core-applications-in-visual-studio-for-mac"></a>ASP.NET Core Mac için Visual Studio'da uygulama oluşturma 

ASP.NET Core modern bulut tabanlı İnternet'e bağlı uygulamalar, web uygulamaları ve Hizmetleri, IOT uygulamaları ve mobil arka uçları gibi oluşturmaya yönelik açık kaynaklı ve platformlar arası bir çerçevedir. ASP.NET Core uygulamaları çalışabileceği [.NET Core](https://www.microsoft.com/net/core/platform) veya .NET Framework çalışma zamanları. Bu buluta dağıtılan uygulamalar için en iyi duruma getirilmiş geliştirme framework sağlamak üzere tasarlanmış veya şirket içinde çalıştırın. Çözümlerinizi oluşturulurken esneklik korumak için çok az ek yük, modüler bileşenlerden oluşur. Geliştirin ve Windows, Mac ve Linux'ta ASP.NET Core uygulamaları platformlar arası çalıştırın. ASP.NET Core, açık kaynak konumunda [GitHub](https://github.com/aspnet/home).

Bu laboratuvarda oluşturacak ve Mac için Visual Studio ile bir ASP.NET Core uygulaması keşfedin

## <a name="objectives"></a>Amaçlar

> [!div class="checklist"]
> * Bir ASP.NET Core web uygulaması oluşturma
> * ASP.NET Core barındırma, yapılandırma ve ara yazılım modeli keşfedin
> * Bir ASP.NET Core web uygulamasında hata ayıklama

## <a name="prerequisites"></a>Önkoşullar

- [Mac için Visual Studio](https://www.visualstudio.com/vs/visual-studio-mac)

## <a name="intended-audience"></a>Hedef kitle

Bu Laboratuvar, alışkın olan geliştiricilerin yönelik C#, ancak deneyime gerekli değildir.

## <a name="task-1-creating-a-new-aspnet-core-application"></a>Görev 1: Yeni bir ASP.NET Core uygulaması oluşturma

1. Başlatma **Mac için Visual Studio**.

2. Seçin **Dosya > Yeni Çözüm**.

3. Seçin **.NET Core > Uygulama** kategorisi ve **ASP.NET Core Web uygulaması (C#)** şablonu. **İleri**'ye tıklayın.

    ![](media/netcore-image1.png)

4. Bir ad girin **"CoreLab"** tıklatıp **Oluştur** projeyi oluşturmak için. Bu, tamamlanması biraz zaman alır.

    ![](media/netcore-image2.png)

## <a name="task-2-touring-the-solution"></a>Görev 2: Çözüm hiç yapmadığı bir şey

1. Varsayılan şablonu adlı tek bir ASP.NET Core projesi ile bir çözüm oluşturacak **CoreLab**. İçeriğini göstermek için proje düğümünü genişletin.

    ![](media/netcore-image3.png)

2. Bu proje, sorumluluk veri (modeller), sunu (görünümleri) ve işlev (denetleyiciler) arasında NET bir bölme sağlamak için model-view-controller (MVC) paradigma izler. Açık **HomeController.cs** dosya **denetleyicileri** klasör.

    ![](media/netcore-image4.png)

3. **HomeController** sınıfı tarafından kuralı tutamaçları ile başlayan tüm gelen istekleri **/Home**. **Dizin** yöntemi istekleri kök dizin işler (gibi `http://site.com/Home`) ve diğer yöntemleri, adlandırılmış yol kuralı üzerinde gibi tabanlı istekleri işleyen **About()** istekleri işleme `http://site.com/Home/About`. Elbette, bu tüm yapılandırılabilir. Bir dikkat çeken bir şey olduğunu **HomeController** yeni bir proje varsayılan denetleyicisidir, böylece sitenin kök dizinine istekleri (`http://site.com`) çıkacak **İNDİS()** ,  **HomeController** olduğu, istekleri gibi `http://site.com/Home` veya `http://site.com/Home/Index`.

    ![](media/netcore-image5.png)

4. Proje de sahip bir **görünümleri** her denetleyici için harita diğer klasörler içeren klasörü (biri yanı sıra **paylaşılan** görünümleri. Örneğin, görünüm CSHTML dosyası (HTML uzantı) için **/Home/About** yolu konumunda olacak **Views/Home/About.cshtml**. Bu dosyayı açın.

    ![](media/netcore-image6.png)

5. Bu CSHTML dosyasını birleşimi standart etiketleri ve satır içi C# dayalı HTML oluşturmak için Razor sözdizimini kullanır. Bu konuda daha fazla bilgi [çevrimiçi belgeleri](https://docs.microsoft.com/aspnet/web-pages/overview/getting-started/introducing-razor-syntax-c).

    ![](media/netcore-image7.png)

6. Çözüm ayrıca içeren bir **wwwroot** , web siteniz için kök klasör. Statik içerik, CSS, görüntü ve JavaScript kitaplıkları gibi doğrudan site dağıtıldığında olması istersiniz yollarında koyabilirsiniz.

    ![](media/netcore-image8.png)

7. Proje, paketleri ve uygulama çalışma zamanında yönetmek için hizmet yapılandırma dosyalarının birçok vardır. Örneğin, varsayılan uygulama [yapılandırma](https://docs.microsoft.com/aspnet/core/fundamentals/configuration) depolanan **appsettings.json**. Ancak, tüm/bazı ortam başına temelinde, bu ayarları gibi sağlayarak kılabilirsiniz bir **appsettings. Development.JSON** dosya **geliştirme** ortam.

    ![](media/netcore-image9.png)

## <a name="task-3-understanding-how-the-application-is-hosted"></a>Görev 3: Uygulamayı nasıl barındırılıyor anlama

1. Gelen **Çözüm Gezgini**açın **Program.cs**. Uygulamanızın çalışacağı önyükleyici budur.

    ![](media/netcore-image10.png)

2. Yalnızca iki satırlık bir kod burada olsa da, önemli. Şimdi bunları parçalara ayırın. İlk olarak, yeni bir **WebHostBuilder** oluşturulur. ASP.NET Core uygulamaları, yürütülecek bir konak gerektirir. Bir konak uygulamalıdır **IWebHost** koleksiyonları özellikler ve hizmetler sunan, arabirimi ve **Başlat** yöntemi. Ana bilgisayar genellikle örneği kullanılarak oluşturulan bir **WebHostBuilder**, oluşturur ve döndürür bir **WebHost** örneği. **WebHost** isteklerini işleyecek sunucunun başvuruyor.

    ![](media/netcore-image11.png)

3. Sırada **WebHostBuilder** sorumlu oluşturduğunuz ana sunucu uygulaması için önyükleme için uygulayan bir sunucuda verdiğiniz gerektirir **IServer**. Varsayılan olarak,  **[Kestrel](https://docs.microsoft.com/aspnet/core/fundamentals/servers/kestrel)** , ASP.NET Core platformlar arası web sunucusuna bağlı **libuv**, platformlar arası bir zaman uyumsuz g/ç kitaplığı olduğu.

    ![](media/netcore-image12.png)

4. Ardından, sunucunun içerik kök ayarlanır. Bu, burada MVC görünümü dosyaları gibi içerik dosyaları için Aranan belirler. Varsayılan içerik kök uygulama çalıştırıldığı klasördür.

    ![](media/netcore-image13.png)

5. Internet Information Services (IIS) web sunucusu ile uygulama çalışmanız gerekiyorsa **UseIISIntegration** yöntemi konak oluşturmanın bir parçası olarak çağrılabilir. Bu bir sunucu gibi yapılandırmaz **UseKestrel** yapar. IIS, ASP.NET Core ile kullanmak için her ikisini de belirtmelisiniz **UseKestrel** ve **UseIISIntegration**. **Kestrel'i** bir proxy'nin arkasındayken çalıştırılmak üzere tasarlanmıştır ve doğrudan internet'e yönelik dağıtılmamalıdır. **UseIISIntegration** IIS olan makineler üzerinde çalışan IIS'ye yalnızca ilgili ters proxy sunucusu, ancak onun olarak belirtir. Windows uygulamanızı dağıtmak, onu bırakın. Aksi takdirde zararı olmaz.

    ![](media/netcore-image14.png)

6. Önyükleme uygulama ayarlarının yüklenmesini ayırmak için temiz bir uygulamadır. Kolayca Bunu yapmak için **UseStartup** belirtmek için çağırılır **başlangıç** sınıfı, yükleme ayarlarını ve ara yazılım ardışık düzende HTTP ekleme gibi diğer başlangıç görevleri için çağrılabilir. Birden çok olabilir **UseStartup** gerektiğinde her bir önceki ayarların üzerine yazılacağını beklentisiyle çağırır.

    ![](media/netcore-image15.png)

7. Oluşturmanın son adımı **IWebHost** çağırmaktır **yapı**.

    ![](media/netcore-image16.png)

8. Sırada **IWebHost** engelleyici olmayan uygulamak için gerekli sınıfların **Başlat**, ASP.NET Core projeleri sahip olarak adlandırılan bir genişletme yöntemi **çalıştırmak** sonuna geldik  **Başlangıç** kod engelleme ile el ile yöntemi hemen çıkmasını önlemek zorunda kalmazsınız.

    ![](media/netcore-image17.png)

## <a name="task-4-running-and-debugging-the-application"></a>Görev 4: Çalıştıran ve uygulamada hata ayıklama

1. İçinde **Çözüm Gezgini**, sağ **CoreLab** proje düğümünü seçip alt **seçenekleri**.

    ![](media/netcore-image18.png)

2. **Proje seçenekleri** iletişim nasıl uygulama yerleşik çalıştırın ve ayarlamak için ihtiyacınız olan her şeyi içerir. Seçin **Çalıştır > yapılandırmaları > Varsayılan** sol panelde düğümünden.

3. Denetleme **harici konsol üzerinde Çalıştır** kaldırın **konsol çıkışını duraklatmak**. Normalde şirket içinde barındırılan bir uygulamanın konsol görünür olmaması, ancak bunun yerine sonuçlarını günlüğe kaydedersiniz **çıkış** paneli. Normal geliştirme sırasında yapmanız gerekmez, ancak bu Laboratuvarın amacı doğrultusunda, bu da ayrı bir pencerede göstereceğiz.

4. **Tamam**'ı tıklatın.

    ![](media/netcore-image19.png)

5. Tuşuna **F5** oluşturun ve uygulamayı çalıştırın. Alternatif olarak, seçebileceğiniz **çalıştırın > hata ayıklamayı Başlat**.

6. İki windows, Mac için Visual Studio başlatılır. Şirket içinde barındırılan bir sunucu uygulaması bir görünüm sağlar bir konsol penceresi davranıştır.

    ![](media/netcore-image20.png)

7. Siteyi sınamak için tipik tarayıcı penceresini saniyedir. Tarayıcı bilir kadar bu uygulama herhangi bir yerde barındırılabilir. Tıklayın **hakkında** söz konusu sayfaya gidin.

    ![](media/netcore-image21.png)

8. Başka şeylerin yanında sayfası hakkında denetleyicisi ayarlamak metin işler.

    ![](media/netcore-image22.png)

9. Tutun hem windows açın ve Mac için Visual Studio'ya geri dönün Açık **Controllers/HomeController.cs** zaten açık değilse.

    ![](media/netcore-image23.png)

10. İlk satırında bir kesme noktası ayarlamak **hakkında** yöntemi. Kenar boşluğunu tıklayarak veya imleci satır ve tuşlarına basarak ayarlamaya bunu yapabilirsiniz **F9**. Bu satırı bazı veri kümelerine **ViewData** CSHTML sayfa işlenir koleksiyonu **Views/Home/About.cshtml**.

    ![](media/netcore-image24.png)

11. Tarayıcı ve yenileme için iade hakkında sayfası. Bu Mac için Visual Studio'da kesme noktası tetikler

12. Fare üzerindeyken **ViewData** üye onun verilerini görüntüleyebilirsiniz. İç içe geçmiş verileri görmek için alt üyeleri daha da genişletebilirsiniz.

    ![](media/netcore-image25.png)

13. Uygulama kesme noktası eklemek için kullanılan yöntemin aynısını kullanarak kaldırın.

14. Açık **Views/Home/About.cshtml**.

15. Metni Değiştir **"ek"** için **"değiştirildi"** ve dosyayı kaydedin.

    ![](media/netcore-image26.png)

16. Tuşuna **devam** yürütmeye devam etmek için düğmeyi.

    ![](media/netcore-image27.png)

17. Güncelleştirilen metin görmek için tarayıcı penceresine dönün. Bu değişiklik, herhangi bir zamanda yapılabilir ve hata ayıklayıcı bir kesme noktası mutlaka gerektiren kaydetmedi. Hemen yansıtılmasını değişiklik görmüyorsanız, tarayıcıyı yenileyin.

    ![](media/netcore-image28.png)

18. Test tarayıcı penceresi ve uygulama konsolunu kapatın. Bu işlem de hata ayıklamayı durdurur.

## <a name="task-5-application-startup-configuration"></a>Görev 5: Uygulama başlangıç yapılandırması

1. Gelen **Çözüm Gezgini**açın **Startup.cs**. Roslyn derleyici, proje bağımlılıkları eksiksiz bir görünümünü oluşturmak ve arka planda NuGet paketleri geri gibi bazı kırmızı dalgalı çizgiler başlangıçta görebilirsiniz.

    ![](media/netcore-image29.png)

2. Bulun **başlangıç** yöntemi. Bu bölümde, uygulama için başlangıç yapılandırmasını tanımlar ve kümelenmesini. Bu konuyu biraz açalım.

    ![](media/netcore-image30.png)

3. Yöntem başlatarak başlangıcıdır bir **ConfigurationBuilder** ve kendi temel yolu ayarlama.

    ![](media/netcore-image31.png)

4. Ardından, gerekli bir yükler **appsettings.json** dosya.

    ![](media/netcore-image32.png)

5. Bundan sonra bir ortama özgü yük çalışır **appsettings.json** dosyasını mevcut ayarları geçersiz kılarsınız. Örneğin, bir sağlanan budur **appsettings. Development.JSON** belirli bu ortam için kullanılan dosya. Daha fazla bilgi için ASP.NET Core hakkında yapılandırması, kullanıma [docs](https://docs.microsoft.com/aspnet/core/fundamentals/configuration).

    ![](media/netcore-image34.png)

6. Son olarak, ortam değişkenlerini yapılandırma oluşturucuya eklenir ve yapılandırma oluşturulur ve kullanım için ayarlayın.

    ![](media/netcore-image35.png)

## <a name="task-6-inserting-application-middleware"></a>6\. Görev: Uygulama ara yazılım ekleme

1. Bulun **yapılandırma** yönteminde **başlangıç** sınıfı. HTTP ardışık düzende eklenen ve sunucuya her isteği işlemek için kullanılan tüm ara yazılım yapılandırıldığı budur. Bu yöntem yalnızca bir kez yöntemleri içeriğini çağırıldıktan (gibi **UseStaticFiles**) her bir istek üzerinde çalıştırılabilir.

    ![](media/netcore-image36.png)

2. Ayrıca, işlem hattının bir parçası yürütülecek ek ara yazılım ekleyebilirsiniz. Sonra aşağıdaki kodu ekleyin **uygulama. UseStaticFiles** otomatik olarak eklemek için bir **X Test** her giden yanıt üst bilgisi. IntelliSense, kod yazdığınız sırada tamamlama yardımcı olur.

    ```csharp
    app.Use(async (context, next) =>
    {
        context.Response.Headers.Add("X-Test", new[] { "Test value" });
        await next();
    });
    ```

3. Tuşuna **F5** oluşturup projeyi çalıştırın.

4. Eklenen doğrulamak için üstbilgileri incelemek için tarayıcı kullanabiliriz. Safari için aşağıdaki yönergeleri verilmiştir, ancak aynı yapabilirsiniz [Chrome](https://stackoverflow.com/questions/4423061/view-http-headers-in-google-chrome) veya [Firefox](https://stackoverflow.com/questions/33974595/in-firefox-how-do-i-see-http-request-headers-where-in-web-console).

5. Tarayıcı site yüklendikten sonra Seç **Safari > Tercihler**.

6. Üzerinde **Gelişmiş** sekmesinde, onay **Göster geliştirme menüsünü menü çubuğunda** ve iletişim kutusunu kapatın.

    ![](media/netcore-image37.png)

7. Seçin **geliştirme > Göster sayfası kaynakları**.

8. Yeni açılan geliştirici araçları, izlemek ve içeriği ve trafiği çözümleyin tarayıcı penceresini yenileyin.

9. Sunucu tarafından işlenen localhost HTML sayfası, varsayılan olarak seçili öğe olacaktır.

    ![](media/netcore-image38.png)

10. Genişletin **ayrıntıları kenar**.

    ![](media/netcore-image39.png)

11. Kodda daha önce eklediğiniz yanıt üst bilgisini görmek için kenar alt kısmına kaydırın.

    ![](media/netcore-image40.png)

12. Tarayıcı penceresi ve koşullar karşılanırsa konsolunu kapatın.

## <a name="summary"></a>Özet

Bu laboratuvarda, Mac için Visual Studio ile ASP.NET Core uygulamaları geliştirmeye başlamak nasıl öğrendiniz. İsterseniz daha eksiksiz bir film veritabanı uygulaması geliştirmeye keşfetmek için bkz: [ASP.NET Core MVC ile çalışmaya başlama](https://docs.microsoft.com/aspnet/core/tutorials/first-mvc-app/start-mvc) öğretici.
