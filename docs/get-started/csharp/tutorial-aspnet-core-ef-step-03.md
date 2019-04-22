---
title: '3. Adım: ASP.NET Core uygulamanızı verilerle çalışma'
description: Entity Framework Core, ASP.NET Core Web uygulaması bu videosu ve adım adım yönergeler kullanarak verilerle çalışmaya başlayın.
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
ms.openlocfilehash: c1d95d7621a97a36fdf737e7d3dd4f8baf713645
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59018187"
---
# <a name="step-3-work-with-data-using-entity-framework"></a>3. Adım: Entity Framework kullanarak verileri ile çalışma

Entity Framework Core, ASP.NET Core Web uygulamanızı kullanarak verilerle çalışmaya başlamak için aşağıdaki adımları izleyin.

_Bu videoyu izleyin ve ilk ASP.NET Core uygulamanızı veri eklemek için ilerleyebilmek._

> [!VIDEO https://www.youtube.com/embed/dulJCwNrqhM]

## <a name="open-your-project"></a>Projenizi açın

Yanı sıra bu videolardan, takip ediyorsanız önceki bölümde oluşturduğunuz Web uygulaması projesini açın. Burada başlıyor ister yeni bir proje oluşturun ve gerekirse **ASP.NET Web uygulaması** ardından **Web uygulaması**. Diğer seçenekleri varsayılan olarak bırakın.

## <a name="add-your-model"></a>Model ekleme

Veriler aşağıdaki gibi görünmelidir tanımlamak için ASP.NET Core uygulamanızı verilerle çalışmak için yapmanız gereken ilk şey var. Bu oluşturarak çağırmak bir *modeli* şeylerle ilgili sorunu çözmeye çalıştığınız ediyoruz. Belirli şekilde davranır ve bizim için görevleri otomatikleştirmek için gerçek dünyadaki uygulamalarda, özel iş mantığı Bu modeller için ekleyeceğiz. Bu örnek için masa üstü oyunları izlemek için basit bir sistem oluşturmak için bunu dağıtacağız. Oyun temsil eder ve desteklemek kaç oyuncunun gibi oyunun hakkında kaydetmek için isteyebileceğiniz bazı özellikleri içeren bir sınıf ihtiyacımız var. Bu sınıf adlı web projesi kökündeki oluşturacağımız yeni bir klasöre gider *modelleri*.

```csharp
public class Game
{
    public int Id { get; set; }
    public string Title { get; set; }
    public int PublicationYear { get; set; }
    public int MinimumPlayers { get; set; }
    public int MaximumPlayers { get; set; }
}
```

## <a name="create-the-pages-to-manage-your-game-library"></a>Oyun kitaplığınızı yönetmek için sayfa oluşturma

Şimdi biz kitaplığımızı oyun yönetmek için kullanacağız sayfaları oluşturmaya hazırsınız demektir. Bunun için ürkütücü, ancak gerçekte şaşırtıcı derecede kolaydır. İlk olarak biz burada uygulamamızı bu işlevselliği Canlı karar vermeniz gerekir. Web projesinde sayfalar klasöründe açın ve orada yeni bir klasör ekleyin. Bu çağrı *oyunlar*.

Artık, oyun sağ tıklatın ve seçin **Ekle** > **yeni iskele kurulmuş öğe**. Razor sayfaları kullanan seçin **Entity Framework (CRUD)** seçeneği. "Oluşturma, okuma, güncelleştirme ve silme" ve bu şablonu CRUD anlamına gelir ("tüm liste" bir sayfa ve bir "bir öğenin ayrıntılarını görüntüle" sayfası dahil) bu işlemlerin her biri için sayfa oluşturacaksınız.

![Visual Studio 2019 ASP.NET Core iskele kurulmuş sayfaları ekleme](media/vs-2019/vs2019-add-scaffold.png)

Oyun model sınıfınızın seçin ve yeni veri bağlamı sınıfı eklemek için '+' simgesini kullanın. Adlandırın `AppDbContext`. Geri kalan varsayılan olarak bırakın ve tıklayın **Ekle**.

Aşağıdaki Razor sayfaları, oyun klasöre eklenen görürsünüz:

- Create.cshtml
- DELETE.cshtml
- Details.cshtml
- Edit.cshtml
- Index.cshtml

![Visual Studio 2019 ASP.NET Core iskele kurulmuş sayfaları](media/vs-2019/vs2019-scaffolded-pages.png)

Sayfalar ekleme yanı sıra *oyunlar* klasörü, iskele kurma işlemi eklenen kod benim *Startup.cs* sınıfı. Arayan `ConfigureServices` yöntemi bu sınıftaki bu kodu eklendiğini görürsünüz:

```csharp
services.AddDbContext<AppDbContext>(options =>
    options.UseSqlServer(Configuration.GetConnectionString("AppDbContext")));
```

Ayrıca bulacaksınız `AppDbContext` bağlantı dizesi projenin eklendiğini *appsettings.json* dosya.

Uygulamayı şimdi çalıştırırsanız, veritabanı, henüz oluşturulmadığından başarısız olabilir. Gerekirse, veritabanı otomatik olarak oluşturmak için uygulama yapılandırabileceğiniz [Program.cs için bazı kod ekleme](/aspnet/core/data/ef-rp/intro?view=aspnetcore-2.1&tabs=visual-studio#update-main):

```csharp
public static void Main(string[] args)
{
    var host = CreateWebHostBuilder(args).Build();

    using (var scope = host.Services.CreateScope())
    {
        var services = scope.ServiceProvider;

        try
        {
            var context = services.GetRequiredService<SchoolContext>();
            context.Database.EnsureCreated();
        }
        catch (Exception ex)
        {
            var logger = services.GetRequiredService<ILogger<Program>>();
            logger.LogError(ex, "An error occurred creating the DB.");
        }
    }

    host.Run();
}
```

Çoğu kod olduğu için hata işleme ve EF Core için erişim sağlamak için `AppDbContext` uygulama çalıştırılmadan önce. Önemli bir bildiren çizgidir `context.Database.EnsureCreated()`, oluşturulmasını veritabanı zaten mevcut değilse. Artık uygulamayı çalıştırmak hazırdır.

## <a name="test-it-out"></a>Test etmek

Uygulamayı çalıştırmak ve gidin `/Games` adres çubuğundaki. Boş liste sayfası görürsünüz. Tıklayın **Yeni Oluştur** yeni bir `Game` koleksiyonuna. Formu doldurun ve tıklayın **Oluştur**. Bu liste görünümünde görmeniz gerekir. Tıklayarak **ayrıntıları** tek bir kaydın ayrıntılarını görmek için.

Başka bir kayıt ekleyin. Tıklayabilirsiniz *Düzenle* bir kaydın ayrıntılarını değiştirmek için veya **Sil** kaldırmak, aslında bir kaydı siler önce onaylamanız istenir.

![Visual Studio 2019 ASP.NET Core tarayıcı sayfalarında iskele kurulmuş.](media/vs-2019/vs2019-game-list.png)

EF Core ve Visual Studio 2019'ı kullanarak bir ASP.NET Core uygulaması verilerle çalışmaya başlamak için geçen tüm budur.

## <a name="next-steps"></a>Sonraki adımlar

Sonraki videoda, web API desteğini uygulamanıza nasıl ekleyeceğinizi öğreneceksiniz.

[4. Adım: Bir web API öğesinden ASP.NET Core uygulamanızı gösterme](tutorial-aspnet-core-ef-step-04.md)

## <a name="see-also"></a>Ayrıca bkz.

- [ASP.NET Core, Entity Framework Core ile Razor sayfaları](/aspnet/core/data/ef-rp/intro?view=aspnetcore-2.1&tabs=visual-studio)
- [EF çekirdekli ASP.NET Core Razor sayfalar](/aspnet/core/data/?view=aspnetcore-2.1)
