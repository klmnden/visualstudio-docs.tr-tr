---
title: ASP.NET Core kullanmaya başlama
description: Bu makalede, yeni proje oluşturma ve yükleme dahil olmak üzere Mac için Visual Studio'da ASP.NET ile başlamak açıklar.
author: conceptdev
ms.author: crdun
ms.date: 04/02/2019
ms.assetid: 6E8B0C90-33D6-4546-8207-CE0787584565
ms.custom: video
ms.openlocfilehash: 183431a160245fd8fc0ec2193c00c32659230459
ms.sourcegitcommit: 509fc3a324b7748f96a072d0023572f8a645bffc
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58856800"
---
# <a name="getting-started-with-aspnet-core"></a>ASP.NET Core kullanmaya başlama

 Mac için Visual Studio için en yeni ASP.NET Core Web geliştirme platformu desteği ile uygulamanızın hizmeti geliştirmek kolaylaştırır. ASP.NET Core, .NET Core çalışma zamanı ve .NET Framework son gelişimi çalıştırır. Hızlı performans için ayarlanmış, küçük yükleme boyutları factored ve Linux ve macOS, hem de Windows çalıştırmak için yeniden oluşturuldu.

## <a name="installing-net-core"></a>.NET Core'u yükleme

.NET core 2.1 Mac için Visual Studio'yu yüklediğinizde otomatik olarak yüklenir

## <a name="creating-an-aspnet-core-app-in-visual-studio-for-mac"></a>Mac için Visual Studio'da ASP.NET Core uygulaması oluşturma

Mac için Visual Studio'yu Aç Başlat ekranında seçin **yeni proje...**

![Yeni Proje iletişim kutusu](media/asp-net-core-2019-new-asp-core.png)

Bu, uygulamanızı oluşturmak üzere şablonu seçmenize olanak sağlar yeni proje iletişim kutusu görüntülenir.

ASP.NET Core uygulamanızı oluşturmaya başlamak için önceden oluşturulmuş bir şablonla sağlayacak projeleri vardır. Bunlar:

- **.NET core > boş**
- **.NET core > API**
- **.NET core > Web uygulaması**
- **.NET core > Web uygulaması (Model-View-Controller)**

![ASP.NET proje seçenekleri](media/asp-net-core-2019-new-asp-core.png)

Seçin **ASP.NET Core boş Web uygulaması** basın **sonraki**. Projeye bir ad ve ENTER tuşuna vermek **Oluştur**. Bu, aşağıdaki görüntüye benzer olmalıdır, yeni bir ASP.NET Core uygulaması oluşturur:

![Yeni ASP.NET Core boş proje görünümü](media/asp-net-core-2019-empty-project.png)

ASP.NET Core boş şablonu bir web uygulaması ile iki varsayılan dosyaları oluşturur: **Program.cs** ve **Startup.cs**, hangi aşağıda açıklanmıştır. Ayrıca, ASP.NET Core ve .NET Core framework Proje yapı MSBuild hedefleri gibi projenizin NuGet Paket bağımlılıklarını içeren bir bağımlılıklar klasörünü oluşturur:

![Çözüm bölmesi bağımlılıklarını görüntüleme](media/asp-net-core-2019-solution-dependencies.png)

### <a name="programcs"></a>Program.cs

Açın ve İnceleme **Program.cs** projenizdeki dosya. Çeşitli nda şeyler bildirimi `Main` yöntemi – uygulamanıza girişi:

```csharp
    public class Program
    {
        public static void Main(string[] args)
        {
            CreateWebHostBuilder(args).Build().Run();
        }

        public static IWebHostBuilder CreateWebHostBuilder(string[] args) =>
            WebHost.CreateDefaultBuilder(args)
                .UseStartup<Startup>();
    }
```
ASP.NET Core uygulaması bir web sunucusunu yapılandırarak ve bir ana bilgisayar örneği aracılığıyla başlatma kendi ana yönteminde oluşturur [ `WebHostBuilder` ](/aspnet/core/fundamentals/hosting). Bu oluşturucu yapılandırılması konağın izin vermek için yöntemler sağlar. Şablon uygulaması, aşağıdaki yapılandırmaları kullanılır:

* `.UseStartup<Startup>()`: Başlangıç sınıfı belirtir.

Ancak, da ek yapılandırmalar gibi ekleyebilirsiniz:

* `UseKestrel`: Kestrel'i sunucusu uygulama tarafından kullanılacak belirtir
* `UseContentRoot(Directory.GetCurrentDirectory())`: Uygulama bu klasörden başlattığınızda web projesinin kök klasörüne uygulamanın içerik kök olarak kullanır.
* `.UseIISIntegration()`: Uygulamanın IIS ile çalışmalıdır belirtir. IIS, ASP.NET Core ile iki kullanılacak `UseKestrel` ve `UseIISIntegration` belirtilmesi gerekir.

### <a name="startupcs"></a>Startup.cs

Uygulamanız için başlangıç sınıfı belirtilen `UseStartup()` metodunda `CreateWebHostBuilder`. İstek ardışık düzeninde işleme belirteceği bu sınıfta olan ve hizmetlerin yapılandırdığınız.

Açın ve İnceleme **Startup.cs** proje dosyasında:

```csharp
    public class Startup
    {
        // This method gets called by the runtime. Use this method to add services to the container.
        // For more information on how to configure your application, visit https://go.microsoft.com/fwlink/?LinkID=398940
        public void ConfigureServices(IServiceCollection services)
        {
        }

        // This method gets called by the runtime. Use this method to configure the HTTP request pipeline.
        public void Configure(IApplicationBuilder app, IHostingEnvironment env)
        {
            if (env.IsDevelopment())
            {
                app.UseDeveloperExceptionPage();
            }

            app.Run(async (context) =>
            {
                await context.Response.WriteAsync("Hello World!");
            });
        }
    }
```

Bu başlangıç sınıfı, her zaman şu kurallara uymalıdır:

 - Her zaman genel olmalıdır
 - İki genel yöntemini içermelidir: `ConfigureServices` ve `Configure`

`ConfigureServices` Uygulamanız tarafından kullanılan hizmetler yöntemi tanımlar.

`Configure` İstek kullanarak işlem hattı oluşturmak sağlar [ara yazılım](/aspnet/core/fundamentals/middleware). Bunlar içinde bir ASP.NET uygulaması ardışık düzenini isteklerini ve yanıtlarını işlemek için kullanılan bileşenlerdir. HTTP ardışık düzen isteği Temsilciler, sıralı olarak adlandırılan bir dizi oluşur. Her temsilci isteği işlemek veya sonraki bir temsilciye geçirmek seçebilirsiniz.

Temsilcileri kullanarak yapılandırabilirsiniz `Run`,`Map`, ve `Use` yöntemlerde `IApplicationBuilder`, ancak `Run` yöntemi hiçbir zaman bir sonraki temsilci çağırır ve işlem hattınızı sonunda her zaman kullanılmalıdır.

`Configure` Bazı şeyleri önceden oluşturulmuş şablon yöntemi oluşturulur. İlk olarak, bir özel durum geliştirme sırasında kullanmak için sayfa işleme yapılandırır. Ardından, bir basit "Hello World" isteyen web sayfasıyla yanıt gönderir.

Bu basit bir Hello World proje artık eklenen ek kod çalıştırabilirsiniz. Uygulamayı çalıştırın ve tarayıcınızda görüntülemek için araç çubuğunda yürütme (üç taraflı) düğmesine basın:

![Uygulamayı çalıştırma](media/asp-net-core-2019-run-debug.png)

Mac için Visual Studio, web projenizin başlatmak için rastgele bir bağlantı noktası kullanır. Bu bağlantı kullanıma bulmak için ise açın altında listelenen uygulama çıktısı **Görüntüle > doldurmalar**. Çıkış aşağıdakine benzer bulmanız gerekir:

![Uygulama çıktısı dinleme bağlantı noktasını görüntüleme](media/asp-net-core-image6.png)

Proje çalışır duruma geçtikten sonra varsayılan web tarayıcınızı başlatın ve uygulama çıktıda listelenen URL'ye bağlanın. Alternatif olarak, tercih ettiğiniz herhangi bir tarayıcıda açabilir ve girin `http://localhost:5000/`, değiştirmeyi `5000` uygulama çıktıda Visual Studio çıkış bağlantı noktasına sahip. Metin görmelisiniz `Hello World!`:

![Tarayıcı gösteren metin](media/asp-net-core-image7.png)

## <a name="adding-a-controller"></a>Denetleyici Ekleme

ASP.NET Core uygulamaları için uygulamanın her bir parçasının sorumluluklarını mantıksal bir ayrım sağlamak için Model-View-Controller (MVC) tasarım deseni kullanın. MVC aşağıdakilerden oluşur:

- **Model**: Uygulama verilerini temsil eden sınıf.
- **Görünüm**: (Bu genellikle model verileri), uygulamanın kullanıcı arabirimini görüntüler.
- **Denetleyici**: Tarayıcı isteklerini yürüten bir sınıf kullanıcı girişini ve etkileşimini yanıt verir.

MVC kullanma hakkında daha fazla bilgi için bkz [ASP.NET Core MVC genel bakış](/aspnet/core/mvc/overview) Kılavuzu.

Bir denetleyici eklemek için aşağıdakileri yapın:

1. Proje adına sağ tıklayıp **Ekle > Yeni dosyaları**. Seçin **genel > boş sınıf**, denetleyici adı girin:

    ![Yeni dosya iletişim kutusu](media/asp-net-core-image8.png)

2. Yeni denetleyici için aşağıdaki kodu ekleyin:

    ```csharp
    using System;
    using Microsoft.AspNetCore.Mvc;
    using System.Text.Encodings.Web;

    namespace Hello_ASP
    {
        public class HelloWorldController : Controller
        {
            //
            // GET: /HelloWorld/

            public string Index()
            {
                return "This is my default action...";
            }

        }
    }
    ```

3. Ekle `Microsoft.AspNetCore.Mvc` projeye sağ tıklayarak bağımlılık **bağımlılık** klasörü ve seçerek **' paket Ekle...** .

4. NuGet kütüphaneye göz atmak için arama kutusunu kullanın `Microsoft.AspNetCore.Mvc`seçip **Paketi Ekle**. Bu yükleme birkaç dakika sürebilir ve gerekli bağımlılıkları için çeşitli lisans kabul istenebilir:

    ![Nuget ekleme](media/asp-net-core-image9.png)

5. Başlangıç sınıfında kaldırma `app.Run` lambda ve kümesi MVC tarafından hangi kod belirlemek için kullanılan URL yönlendirme mantığı aşağıdaki çağırma:

    ```csharp
    app.UseMvc(routes =>
    {
        routes.MapRoute(
        name: "default",
        template: "{controller=HelloWorld}/{action=Index}/{id?}");
    });
    ```

    Kaldırdığınızdan emin olun `app.Run` olarak bir lambda, yönlendirme mantığı kılar.

    MVC çalıştırmak için hangi kodun belirlemek için aşağıdaki biçimi kullanır:

    `/[Controller]/[ActionName]/[Parameters]`

    Yukarıdaki kod parçacığında eklediğinizde, varsayılan olarak uygulamaya söylüyoruz `HelloWorld` denetleyicisi ve `Index` eylem yöntemi.

6. Ekleme `services.AddMvc();` çağrısı `ConfigureServices` aşağıda gösterildiği gibi yöntemi:

    ```csharp
    public void ConfigureServices(IServiceCollection services)
    {
        services.AddMvc();
    }
    ```

    Denetleyiciye URL'den parametre bilgileri de geçirebilirsiniz.

7. Başka bir yöntem, HelloWorldController için aşağıda gösterildiği gibi ekleyin:

    ```csharp
    public string Xamarin(string name)
    {
        return HtmlEncoder.Default.Encode($"Hello {name}, welcome to Visual Studio for Mac");
    }
    ```

8. Uygulamayı şimdi çalıştırırsanız, otomatik olarak tarayıcınızı açın:

    ![Tarayıcıda çalışan uygulama](media/asp-net-core-image13.png)

9. İçin göz atmayı deneyin `http://localhost:xxxx/HelloWorld/Xamarin?name=Amy` (değiştirerek `xxxx` doğru bağlantı noktası ile), aşağıdaki görmeniz gerekir:

    ![Bağımsız değişkenlerle tarayıcıda çalışan uygulama](media/asp-net-core-image10.png)


## <a name="troubleshooting"></a>Sorun giderme

.NET Core el ile Mac OS 10.12 (Sierra) ve üzeri yüklemeniz gerekiyorsa, aşağıdakileri yapın:

1. .NET Core yüklemeye başlamadan önce en son kararlı bir sürüm için güncelleştirilen tüm işletim sistemi güncelleştirmelerini emin olun. Bu App Store uygulamaya gidip Güncelleştirmeler sekmesini seçerek kontrol edebilirsiniz.

2. Listelenen adımları [.NET Core site](https://www.microsoft.com/net/core#macos).

Başarıyla .NET Core başarıyla yüklendiğinden emin olmak için tüm adımları tamamladığınızdan emin olun.

## <a name="summary"></a>Özet

Bu kılavuz, bir ASP.NET Core'a giriş getirdi. Ne, ne zaman, kullanacağınız ise ve Mac için Visual Studio'da sistemlerindeki bilgileri sağlanan açıklar
Sonraki adımlar buradan hakkında daha fazla bilgi için aşağıdaki kılavuzlara bakın:
- [ASP.NET Core](/aspnet/core/?view=aspnetcore-2.1#build-web-ui-and-web-apis-using-aspnet-core-mvc) belgeleri.
- [Yerel mobil uygulamalar için arka uç hizmetleri oluşturma](/aspnet/core/mobile/native-mobile-backend), bir Xamarin.Forms uygulaması için ASP.NET Core kullanarak REST hizmeti oluşturmak nasıl gösterir.
- [ASP.NET Core uygulamalı laboratuvarı](https://github.com/Microsoft/vs4mac-labs/tree/master/Web/Getting-Started).

## <a name="related-video"></a>İlgili Video

> [!Video https://channel9.msdn.com/Shows/Visual-Studio-Toolbox/Visual-Studio-for-Mac-Build-Your-First-App/player]