---
title: F#Araçları
description: Visual Studio'nun hangi özellikler desteklenir öğrenin F#.
ms.date: 07/11/2018
ms.topic: reference
helpviewer_keywords:
- F# features [Visual Studio]
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- dotnet
ms.openlocfilehash: dc3a49c586b7a8f5a67d6c1a3a77d00772698389
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62793423"
---
# <a name="develop-with-visual-f-in-visual-studio"></a>Görselle geliştirme F# Visual Studio'da

Bu makale, Visual Studio özellikleri hakkında bilgi içerir. F# geliştirme.

## <a name="install-f-support"></a>Yükleme F# desteği

Geliştirme için F# Visual Studio'da ilk yükleme **.NET masaüstü geliştirme** yapmadıysanız, iş yükü. Visual Studio iş yükleri seçerek açabilirsiniz. Visual Studio yükleyicisi aracılığıyla yükleyin **Araçları** > **araçları ve özellikleri Al**.

![Visual Studio'da .NET masaüstü geliştirme iş yükü](media/dotnet-desktop-development-workload.png)

## <a name="f-project-features"></a>F#Proje Özellikleri

Çeşitli proje ve öğe şablonları kullanılabilir F# Visual Studio'da. Aşağıdaki resimde bazıları gösterilmektedir F# .NET Core ve .NET Standard için proje şablonları:

![F#Visual Studio Proje şablonları](media/fsharp-project-templates.png)

Aşağıdaki resimde bazıları gösterilmektedir F# öğe şablonları:

![F#Visual Studio öğe şablonları](media/fsharp-item-templates.png)

Veri erişimi için öğe şablonları hakkında daha fazla bilgi için bkz: [ F# tür sağlayıcıları](/dotnet/fsharp/tutorials/type-providers/index).

Proje özelliklerinde özellikler aşağıdaki tabloda özetlenmiştir F#:

|Proje ayarı|Desteklenen F#?|Notlar|
|---------------|----------------|-----|
|Kaynak dosyaları|Evet||
|Derleme ve hata ayıklama ayarları başvurusu|Evet||
|Çoklu Sürüm Desteği|Evet||
|Simge ve bildirim|Hayır|Derleyici komut satırı seçenekleri aracılığıyla kullanılabilir.|
|ASP.NET İstemci Hizmetleri|Hayır||
|ClickOnce|Hayır|Bir istemci projesi varsa başka bir .NET Framework dil kullanın.|
|Kesin adlandırma|Hayır|Derleyici komut satırı seçenekleri aracılığıyla kullanılabilir.|
|Yayımlama derleme ve sürüm oluşturma|Hayır||
|Kod Analizi|Hayır|Kod çözümleme araçları, el ile veya bir derleme sonrası komutunun bir parçası olarak çalıştırılabilir.|
|Güvenlik (güven düzeylerini değiştirme)|Hayır||

## <a name="project-designer"></a>Proje Tasarımcısı

**Proje Tasarımcısı** ilgili işlevselliğe göre gruplandırılan çeşitli proje özellik sayfaları oluşur. Sayfaları için kullanılabilir F# projeler çoğunlukla diğer diller için mevcut kodlar alt kümesidir ve aşağıdaki tabloda açıklanmıştır. Bağlantılar sağlanır karşılık gelen C# için **Proje Tasarımcısı** sayfası.

|Proje Tasarımcısı sayfası|İlgili bağlantılar|Açıklama|
| - |-------------|-----------|
|Uygulama|[Uygulama sayfası, Proje Tasarımcısı](reference/application-page-project-designer-csharp.md)|Uygulama düzeyi ayarları ve özellikleri, bir kitaplık veya yürütülebilir bir dosya, uygulama hangi .NET Framework sürümünü hedefliyor ve burada kaynak dosyaları hakkında bilgi oluşturmakta olduğunuz gibi belirtmenize olanak tanıyan uygulama kullanan depolanır.|
|Yapı|[Derleme sayfası, Proje Tasarımcısı](reference/build-page-project-designer-csharp.md)|Kodun nasıl derlendiğini denetlemenize olanak verir.|
|Derleme olayları|[Derleme olayları sayfası, Proje Tasarımcısı](reference/build-events-page-project-designer-csharp.md)|Önce veya sonra bir derleme için komutları belirtmenizi sağlar.|
|Hata ayıklama|[Hata Ayıklama Sayfası, Proje Tasarımcısı](reference/debug-page-project-designer.md)|Hata ayıklama sırasında uygulamanın nasıl çalışacağını denetlemesine olanak sağlar. Yerel kod ve SQL gibi etkinleştirmek istediğiniz herhangi bir özel hata ayıklama modlarını ve bu dizin ne kullanın ve uygulamanızın başlangıç komutları içerir.|
|Paket (yalnızca .NET SDK)|Yok|NuGet paketi meta verileri bir NuGet paketi olarak yayımlarken tanımlamanızı sağlar.|
|Başvuru yolları|[Bir projedeki başvuruları yönetme](managing-references-in-a-project.md)|Kodu bağımlı derlemelerin aranacağı yeri belirtmek sağlar.|
|Kaynaklar (yalnızca .NET SDK)|Yok|Oluştur ve varsayılan kaynak dosyası yönetmenize olanak sağlar.|

### <a name="f-specific-settings"></a>F#-belirli ayarları

Özgü ayarları aşağıdaki tabloda özetlenmiştir F#:

|Proje Tasarımcısı sayfası|Ayar|Açıklama|
| - |-------|-----------|
|Yapı|Kuyruk çağrıları oluştur|Seçili olduğunda, Microsoft Ara dil (MSIL) yönerge kuyruğunu kullanımını etkinleştirir. Bu yığın çerçevesinin tail özyinelemeli işlevler için yeniden neden olur. Eşdeğer `--tailcalls` derleyici seçeneği.|
|Yapı|Diğer bayrakları|Ek derleyici komut satırı seçenekleri belirtmenizi sağlar.|

## <a name="code-and-text-editor-features"></a>Kod ve metin düzenleyici özellikleri

Visual Studio kodu ve metin düzenleyiciler, aşağıdaki özellikleri desteklenir F#:

|Özellik|Açıklama|Desteklenen F#?|
|-------|-----------|----------------|
|Otomatik olarak açıklaması|Açıklama satırı yapın veya kodun bölümlerine sağlar.|Evet|
|Otomatik olarak Biçimlendir|Standart girinti ve stil kod yeniden biçimlendirir.|Hayır|
|Yer İşaretleri|Düzenleyicide yerler kaydetmenizi sağlar.|Evet|
|Girinti değiştirme|Girintileri veya seçili satırları girintilemez.|Evet|
|Akıllı girintileme|Otomatik olarak Girintiler ve imleci göre XML'deki girintiler F# kapsama kuralları.|Evet|
|[Metin bulma ve değiştirme](finding-and-replacing-text.md)|Bir dosya, proje veya çözüm arayın ve potansiyel olarak metin değiştirmek etkinleştirir.|Evet|
|.NET Framework API tanımına Git|İmleç bir .NET Framework API üzerinde konumlandırıldığında, .NET Framework meta verileri kullanarak oluşturulan kodu gösterir.|Hayır|
|Kullanıcı tanımlı API tanımına Git|İmleç imleç kodunuzda varlık tanımlandığı yere taşır, tanımlı bir program varlık üzerinde olduğunda.|Evet|
|Satıra Gitme|Bir dosyadaki satır numarası tarafından belirli bir satıra gitmenizi sağlar.|Evet|
|Dosyasının üst gezinti çubukları|Kodda, konumları, örneğin, işlev adı atlamak sağlar.|Evet|
|Blok yapısı kılavuzları|Gösteren gösterir yönergeleri F# kapsamlar, üzerine bir önizleme gelindiğinde.|Evet|
|[Anahat Oluşturma](outlining.md)|Daha kısa bir görünüm oluşturmak için kod bölümlerini daraltmak olanak tanır.|Evet|
|Sekmeye Dönüştür|Boşlukları sekmelere dönüştürür.|Evet|
|Tür renklendirme|Özel bir renk ile tanımlanmış tür adları gösterir.|Evet|
|Hızlı bulun. Hızlı Bul Bul ve Değiştir penceresi görürsünüz.|Bir dosya ya da proje aramanızı sağlar.|Evet|
|**CTRL**+**tıklayın** için Tanıma Git|Tutacak sağlar **Ctrl** tıklayın bir F# Tanıma Git çağırmak için Sembol.|Evet|
|Hızlıbilgi Tanıma Git|Çağırma araç ipuçları içinde tıklanabilir sembolleri Tanıma Git.|Evet|
|Tümüne Git|Tüm genel, benzer öğe eşleştirmesi gezinme sağlar F# aracılığıyla yapıları **Ctrl**+**T**.|Evet|
|Satır içi yeniden adlandırma|Sembol satır içi tüm örneklerini yeniden adlandırır.|Evet|
|Tüm başvuruları Bul|Tüm sembol oluşumlarını bir kod temelinde bulur.|Evet|
|Adı kod düzeltme basitleştirin|Gereksiz niteleyicilerinin kaldırır F# semboller.|Evet|
|Kullanılmayan Kaldır `open` deyimi kod düzeltmesi|Tüm gereksiz kaldırır `open` belgede deyimleri.|Evet|
|Kullanılmayan değere kod düzeltmesi|Alt çizgi için kullanılmayan bir tanımlayıcı yeniden adlandırma önerir.|Evet|

Visual Studio ve özellikleri metin düzenleyicisi kod düzenleme hakkında daha fazla genel bilgi için bkz. [düzenleyicide kod yazma](writing-code-in-the-code-and-text-editor.md).

## <a name="intellisense-features"></a>IntelliSense özellikleri

Aşağıdaki tablo desteklenen ve içinde desteklenmeyen IntelliSense özelliklerini özetler F#:

|Özellik|Açıklama|Desteklenen F#?|
|-------|-----------|----------------|
|Otomatik olarak uygulanan arabirimler|Arabirim yöntemleri için kod saplamalar oluşturur.|Evet|
|Kod parçacıkları|Kod yaygın kodlama yapıları içeren konulara ekler.|Hayır|
|Tam Sözcük|Siz yazarken sözcükler ve adları tamamlayarak yazarak kaydeder.|Evet|
|Otomatik Tamamlama|Etkin olduğunda, ilk eşleşmeyi seçin veya beklemek yerine tür olarak seçmek Sözcük tamamlama neden **Ctrl**+**alanı**.|Evet|
|Teklif tamamlama sembolleri açılmamış ad alanları|Otomatik Tamamlama özelliğiyle açılmamış bir ad alanında bulunan eşleşen bir sembol, karşılık gelen ile tamamlamak teklif önerilen `open` seçildiğinde deyimi.|Evet|
|Kod öğeleri oluşturma|Çeşitli yapılar saplama kodunun oluşturulacağı sağlar.|Hayır|
|Üyeleri Listeleme|Üye erişimi işleci (.) yazın, türün üyeleri gösterir.|Evet|
|Using deyimlerini/açık düzenleme|Tarafından başvurulan ad alanlarını düzenler **kullanarak** deyimlerinde C# veya **açın** yönergelerinde F#.|Hayır|
|Parametre Bilgisi|Bir işlev çağrısı türü olarak parametreler hakkında yararlı bilgiler gösterir.|Evet|
|Hızlı Bilgi|Kodunuzdaki herhangi bir tanımlayıcı için bütün bildirimi görüntüler.|Evet|
|Otomatik küme ayracı tamamlama|Otomatik olarak tamamlar F# küme ayracı benzeri sözdizimi işlemsel bir şekilde oluşturur.|Evet|

IntelliSense hakkında genel bilgi için bkz: [kullanım IntelliSense](using-intellisense.md).

## <a name="debugging-features"></a>Hata ayıklama özellikleri

Aşağıdaki tabloda, hata ayıklarken kullanılabilen özellikler özetlenmiştir F# kod:

|Özellik|Açıklama|Desteklenen F#?|
|-------|-----------|----------------|
|Otomatik değişkenler penceresi|Otomatik veya geçici değişkenleri gösterir.|Hayır|
|Kesme noktaları|Hata ayıklama sırasında kod yürütme belirli noktalarda duraklatmanıza da olanak sağlar.|Evet|
|Koşullu kesme noktaları|Test yürütme duraklaması gerekip gerekmediğini belirleyen bir koşulu kesme noktaları sağlar.|Evet|
|Düzenle ve Devam Et|Değiştirilebilir ve çalışan bir programı durdurup yeniden başlatmadan hata ayıklayıcı hata ayıklama gibi derlenmiş kodun sağlar.|Hayır|
|İfade değerlendirici|Değerlendirir ve çalışma zamanında kodu yürütür.|Hayır, ancak C# ifade değerlendiricisi kullanılabilir, ancak C# sözdizimini kullanmanız gerekir.|
|Geçmiş hata ayıklama|Daha önce yürütülen kodda ilerleyebilmeniz olanak tanır.|Evet|
|Yerel öğeler penceresi|Değerleri ve değişkenleri tanımlanmış yerel olarak gösterir.|Evet|
|İmlece kadar Çalıştır|İmlecin bulunduğu satıra ulaşılıncaya kadar kod yürütmesine olanak tanır.|Evet|
|Adımla|Yürütme ilerleyin ve herhangi bir işlev çağrısına taşıma sağlar.|Evet|
|Üzerinden adımla|Geçerli yığın çerçevesi yürütme ilerleyin ve herhangi bir işlev çağrısına taşıma sağlar.|Evet|

Visual Studio hata ayıklayıcısı hakkında genel bilgi için bkz. [Visual Studio'da hata ayıklama](../debugger/index.md).

## <a name="additional-tools"></a>Ek araçlar

Aşağıdaki tabloda özetlenmiştir desteğini F# Visual Studio Araçları.

|Aracı|Açıklama|Desteklenen F#?|
|----|-----------|----------------|
|Çağrı Hiyerarşisi|Görüntüler, kodunuzda iç içe geçmiş yapısı işlevi çağırır.|Hayır|
|Kod Ölçümleri|Satır sayısı gibi kodunuz hakkında bilgiler toplar.|Hayır|
|Sınıf Görünümü|Bir projedeki kod türüne göre bir görünümünü sağlar.|Hayır|
|[Hata Listesi penceresi](reference/error-list-window.md)|Kod hatalarının bir listesini gösterir.|Evet|
|[F# Interactive](/dotnet/fsharp/tutorials/fsharp-interactive/)|Yazın (veya kopyalayıp yapıştırın) sayesinde F# kod ve projenizin yapı bağımsız olarak hemen çalıştırın. F# Etkileşimli penceresi, okuma, Evaluate, yazdırma Loop (REPL).|Evet|
|Nesne Tarayıcısı|Bir derlemede bulunan türleri görüntülemenizi sağlar.|F#derlenmiş bütünleştirilmiş kod içinde göründükleri gibi tam olarak yazar gibi türleri görünmez. Derlenmiş temsili göz atabilirsiniz F# türleri, ancak görüntülenemez türleri gelen göründükleri gibi F#.|
|[Çıkış penceresi](reference/output-window.md)|Derleme çıkışı görüntüler.|Evet|
|Performans Analizi|Kodunuzun performansını ölçmek için araçlar sağlar.|Evet|
|Özellik penceresi|Görüntüler ve odaklı geliştirme ortamında nesnenin özelliklerini düzenlemesini sağlar.|Evet|
|Server Explorer|Sunucu kaynaklarını çeşitli ile etkileşim için yöntemler sağlar.|Evet|
|Çözüm Gezgini|Projeleri ve dosyaları görüntülemek ve yönetmek etkinleştirir.|Evet|
|Görev Listesi|İş öğelerini kodunuza yönetmenizi sağlar.|Hayır|
|Test projeleri|Yardımcı kodunuzu test etmek sağlar.|Hayır|
|Araç Kutusu|Denetimlerini ve metin veya kod bölümlerini gibi sürüklenebilir nesneleri içeren bir sekme görüntüler.|Evet|

## <a name="see-also"></a>Ayrıca bkz.

- [F#Kılavuzu (.NET Framework)](/dotnet/fsharp/)
- [Kullanmaya başlama F# Visual Studio'da](/dotnet/fsharp/get-started/get-started-visual-studio)