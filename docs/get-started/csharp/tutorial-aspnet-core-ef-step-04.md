---
title: '4. Adım: Bir web API öğesinden ASP.NET Core uygulamanızı gösterme'
description: ASP.NET Core Web uygulamanızı bu videosu ve adım adım yönergeleri içeren bir web API'sini ekleyin.
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
ms.openlocfilehash: 93e3b0af04060c3a3805b29e5d1da71c4f60ec31
ms.sourcegitcommit: b6177ce198c7c5a00030604c9d4faa735405d5df
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/04/2019
ms.locfileid: "59018096"
---
# <a name="step-4-expose-a-web-api-from-your-aspnet-core-app"></a>4. Adım: ASP.NET Core uygulamanızı bir web API'SİNİN kullanıma sunma

Mevcut ASP.NET Core uygulamanızı bir web API eklemek için aşağıdaki adımları izleyin.

_Bu videoyu izleyin ve ilk ASP.NET Core uygulamanızı web API desteği eklemek için ilerleyebilmek._

> [!VIDEO https://www.youtube.com/embed/o_fYPOsAXts]

## <a name="open-your-project"></a>Projenizi açın

ASP.NET Core uygulamanızı Visual Studio 2019 ' açın. Uygulama zaten EF Core, model türlerini yönetmek için yapılandırılan kullanılmalı [Bu öğretici serisinin 3. adım](tutorial-aspnet-core-ef-step-03.md).

## <a name="add-an-api-controller"></a>Bir API denetleyicisi Ekle

Projeye sağ tıklayın ve adlı yeni bir klasör ekleyin *API*. Ardından, bu klasörü sağ tıklatın ve seçin **Ekle** > **yeni iskele kurulmuş öğe**. Seçin **API denetleyici Entity Framework kullanarak Eylemler ile.** Artık mevcut bir model sınıfı seçin ve tıklayın **Ekle**.

![Visual Studio 2019 ASP.NET Core API denetleyicisi iskele kurulmuş.](media/vs-2019/vs2019-add-scaffold-api.png)

## <a name="reviewing-the-generated-controller"></a>Oluşturulan denetleyici gözden geçirme

Oluşturulan kodun yeni bir denetleyici sınıfı içerir. Sınıf tanımının en üstünde iki öznitelikleridir.

```csharp
[Route("api/[controller]")]
[ApiController]
public class GamesController : ControllerBase
```

İlk olarak bu denetleyicideki eylemler için rota belirtir `api/[controller]` yani denetleyici adlandırılır `GamesController` yol olacak `api/Games`.

İkinci öznitelik `[ApiController]`, bazı yararlı doğrulamaları ekler sınıfa, her eylem sağlama gibi kendi includes yöntemi `[Route]` özniteliği.

```csharp
public class GamesController : ControllerBase
{
    private readonly AppDbContext _context;

    public GamesController(AppDbContext context)
    {
        _context = context;
    }
```

Mevcut denetleyici kullanan `AppDbContext`, içine oluşturucusuna geçirilen. Her eylem, uygulamanın verilerle çalışmak için bu alanı kullanır.

```csharp
// GET: api/Games
[HttpGet]
public IEnumerable<Game> GetGame()
{
    return _context.Game;
}
```

İlk yöntem olarak belirtilen kullanarak bir basit GET isteği, olup `[HttpGet]` özniteliği. Bu parametre almayan ve veritabanındaki tüm oyunların listesini döndürür.

```csharp
// GET: api/Games/5
[HttpGet("{id}")]
public async Task<IActionResult> GetGame([FromRoute] int id)
{
    if (!ModelState.IsValid)
    {
        return BadRequest(ModelState);
    }

    var game = await _context.Game.FindAsync(id);

    if (game == null)
    {
        return NotFound();
    }

    return Ok(game);
}
```

Sonraki yöntem belirtir `{id}` yolda ekleneceği yol şu şekilde bir `/` tam yol şöyle olur `api/Games/5` üst açıklamasında gösterildiği gibi. `id` Giriş eşlenmiş durumda `id` yöntem parametresi. Model geçersizse, yöntemin içindeki bir `BadRequest` sonuç döndürülür. Aksi takdirde EF sağlanan eşleşen kayıt bulmayı dener `id`. Erişilemiyorsa bir `NotFound` sonuç döndürülür, aksi takdirde uygun `Game` kayıt döndürülür.

```csharp
// PUT: api/Games/5
[HttpPut("{id}")]
public async Task<IActionResult> PutGame([FromRoute] int id, [FromBody] Game game)
{
    if (!ModelState.IsValid)
    {
        return BadRequest(ModelState);
    }

    if (id != game.Id)
    {
        return BadRequest();
    }

    _context.Entry(game).State = EntityState.Modified;

    try
    {
        await _context.SaveChangesAsync();
    }
    catch (DbUpdateConcurrencyException)
    {
        if (!GameExists(id))
        {
            return NotFound();
        }
        else
        {
            throw;
        }
    }

    return NoContent();
}
```

Ardından, bir `[HttpPut]` API'sine yapılan istek güncelleştirmeleri gerçekleştirmek için kullanılır. Yeni `Game` kaydı, istek gövdesinde sağlanır. Bazı doğrulama ve hata denetimi gerçekleştirilir ve her şeyi başarılı olursa, veritabanı kaydı istek gövdesinde sağlanan değerlerle güncelleştirilir. Aksi takdirde bir uygun hata yanıtı döndürülür.

```csharp
// POST: api/Games
[HttpPost]
public async Task<IActionResult> PostGame([FromBody] Game game)
{
    if (!ModelState.IsValid)
    {
        return BadRequest(ModelState);
    }

    _context.Game.Add(game);
    await _context.SaveChangesAsync();

    return CreatedAtAction("GetGame", new { id = game.Id }, game);
}
```

Bir `[HttpPost]` istek sisteme yeni kayıtları eklemek için kullanılır. Olduğu gibi `[HttpPut]`, istek gövdesinde kaydı eklenir. Geçerliyse, EF Core kaydı veritabanına ekler ve eylem güncelleştirilen kaydı (ile oluşturulan veritabanı Kimliğini) ve bağlantı API kaydı döndürür.

```csharp
// DELETE: api/Games/5
[HttpDelete("{id}")]
public async Task<IActionResult> DeleteGame([FromRoute] int id)
{
    if (!ModelState.IsValid)
    {
        return BadRequest(ModelState);
    }

    var game = await _context.Game.FindAsync(id);
    if (game == null)
    {
        return NotFound();
    }

    _context.Game.Remove(game);
    await _context.SaveChangesAsync();

    return Ok(game);
}
```

Son olarak, bir `[HttpDelete]` rota bir Kimliğine sahip bir kaydı silmek için kullanılır. İstek geçerliyse ve belirtilen Kimliğe sahip bir kayıt varsa EF Core silin veritabanından.

## <a name="adding-swagger"></a>Swagger'ı ekleme

Swagger bir API belgeleri ve ASP.NET Core uygulaması için bir dizi Hizmetleri ve ara yazılımı eklenebilir sınama Aracı ' dir. Bunu yapmak için proje üzerinde sağ tıklatın ve seçin **NuGet paketlerini Yönet**. Tıklayarak **Gözat** araması `Swashbuckle.AspNetCore` ve ilgili paket yükleyin.

![Visual Studio 2019 Swashbuckle Nuget tarafından Ekle](media/vs-2019/vs2019-nuget-swashbuckle.png)

Yüklendikten sonra açmak `Startup.cs` ve sonuna aşağıdakini ekleyin `ConfigureServices` yöntemi:

```csharp
services.AddSwaggerGen(c =>
{
    c.SwaggerDoc("v1", new Info { Title = "My API", Version = "v1" });
});
```

Eklemeniz gerekecektir `using Swashbuckle.AspNetCore.Swagger;` dosyanın üst.

Ardından, aşağıdaki ekleyin `Configure` yöntemi hemen önce `UseMvc`:

```csharp
// Enable middleware to serve generated Swagger as a JSON endpoint.
app.UseSwagger();

// Enable middleware to serve swagger-ui (HTML, JS, CSS, etc.), 
// specifying the Swagger JSON endpoint.
app.UseSwaggerUI(c =>
{
    c.SwaggerEndpoint("/swagger/v1/swagger.json", "My API V1");
});
```

Artık uygulamanızı derleme ve mümkün olması gerekir. Tarayıcıda gidin `/swagger` adres çubuğundaki. Uygulamanızın API uç noktaları ve modelleri listesini görmeniz gerekir. 

![Visual Studio 2019 Swagger sayfasını tarayıcıda](media/vs-2019/vs2019-swagger-browser.png)

Bir uç nokta altında oyunlar, ardından `Try it out` ve `Execute` farklı uç noktalar nasıl davrandığını görmek için.

## <a name="next-steps"></a>Sonraki adımlar

Sonraki videoda, uygulamanızı Azure'a dağıtmayı öğreneceksiniz.

[5. Adım: ASP.NET Core uygulamanızı Azure'a dağıtma](tutorial-aspnet-core-ef-step-05.md)

## <a name="see-also"></a>Ayrıca bkz.

- [Swashbuckle'ı ve ASP.NET Core ile çalışmaya başlama](/aspnet/core/tutorials/getting-started-with-swashbuckle?view=aspnetcore-2.2&tabs=visual-studio)
- [ASP.NET Core web API Yardım sayfaları ile Swagger / Openapı](/aspnet/core/tutorials/web-api-help-pages-using-swagger?view=aspnetcore-2.2)