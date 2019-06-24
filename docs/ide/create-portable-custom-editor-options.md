---
title: EditorConfig ayarları
ms.date: 08/01/2018
ms.topic: conceptual
helpviewer_keywords:
- editorconfig [Visual Studio]
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: f48a690513c80b02683df61a0abf68a3cad58293
ms.sourcegitcommit: 7eb2fb21805d92f085126f3a820ac274f2216b4e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/22/2019
ms.locfileid: "67328800"
---
# <a name="create-portable-custom-editor-settings-with-editorconfig"></a>EditorConfig ile taşınabilir, özel düzenleyici ayarları oluşturma

Ekleyebileceğiniz bir [EditorConfig](http://editorconfig.org/) dosya projeye ya da tutarlı kodlama zorlamak için kod temeli stiller herkes kod temelinde çalışır. EditorConfig ayarları Düzenleyicisi ayarları genel Visual Studio metin üzerinde önceliklidir. Bu, her kod temelini o projeye özel metin düzenleyici ayarlarını kullanmak üzere uyarlayabileceğiniz anlamına gelir. Visual Studio'da kendi kişisel Düzenleyici tercihleri yine de ayarlayabilirsiniz **seçenekleri** iletişim kutusu. Bir kod temelinde çalışırken sürekli bu ayarlar geçerli bir *.editorconfig* dosyası veya *.editorconfig* dosya belirli bir ayarı geçersiz kılma değil. Böyle bir tercih, girinti stili örneğidir&mdash;sekme veya boşluk.

EditorConfig ayarlar, çok sayıda kod düzenleyici ve IDE'ler, Visual Studio da dahil olmak üzere tarafından desteklenir. Bu kodunuzla dolaşır ve Visual Studio dışında bile kodlama stillerini zorunlu kılabilir taşınabilir bir bileşendir.

Visual Studio projenize bir EditorConfig dosya eklediğinizde, belgeyi Biçimlendir sürece var olan kod biçimlendirme değişmez (**Düzenle** > **Gelişmiş**  >  **Belgeyi Biçimlendir** veya **Ctrl**+**K**, **Ctrl**+**D**varsayılan profilde). Ancak, yeni bir kod satırlarını EditorConfig ayarlarına göre biçimlendirilir.

::: moniker range="vs-2017"

İstediğiniz hangi EditorConfig ayarlar tanımlayabilirsiniz **belgeyi Biçimlendir** uygulamak için [ **biçimlendirme** seçenekleri sayfasında](reference/options-text-editor-csharp-formatting.md#format-document-settings).

::: moniker-end

> [!NOTE]
> Bu konu, Windows üzerinde Visual Studio için geçerlidir. Mac için Visual Studio için bkz: [Mac için Visual Studio'da EditorConfig](/visualstudio/mac/editorconfig).

## <a name="code-consistency"></a>Kod tutarlılık

Tutarlı kodlama stili ve girinti stili, sekme genişliği, satır sonu karakterleri, gibi kod tabanında kodlama, ayarları korumak EditorConfig dosyaları ayarlarında etkinleştirmeniz ve daha fazlasını düzenleyicimizi veya IDE'mizi bağımsız olarak kullanırsınız. Örneğin, kod temelinizde girintileri her zaman beş boşluk karakterlerinden oluşamaz tercih edilmesi bir kuralı varsa, C# kodlama, UTF-8 kodlamasını, belgeleri kullanın ve her satırı bir CR/LF ile her zaman sona erer, yapılandırabileceğiniz bir *.editorconfig* Bunu yapmak için dosya.

Kodlama kuralları kişisel projelerinizi kullandığınız takımınızın projelerde kullanılanlardan farklı olabilir. Örneğin, kodlamaya, girintilendirme bir sekme karakteri ekler tercih edebilirsiniz. Ancak, takımınızın girintileme bir sekme karakteri yerine dört boşluk karakterleri ekler tercih edebilirsiniz. EditorConfig dosyaları, her senaryo için bir yapılandırmaya sahip olanak sağlayarak bu sorunu giderin.

Ayarları bir kod temeli dosyasında bulunduğundan, bu kod temeli ile birlikte seyahat. Kod dosyası EditorConfig uyumlu bir düzenleyicide açık olduğu sürece, metin düzenleyici ayarları uygulanır. EditorConfig dosyaları hakkında daha fazla bilgi için bkz. [EditorConfig.org](http://editorconfig.org/) Web sitesi.

> [!NOTE]
> Bir EditorConfig dosyasında ayarlanan kuralları, şu anda hata veya uyarı oluştururken bir CI/CD işlem hattında zorlanamaz. Yalnızca Visual Studio düzenleyicisinde herhangi bir stil sapmaları görünür ve **hata listesi**.

## <a name="supported-settings"></a>Desteklenen ayarlar

Visual Studio düzenleyicisinde çekirdek kümesini destekleyen [EditorConfig özellikleri](http://editorconfig.org/#supported-properties):

- indent_style
- indent_size
- tab_width
- Son\_of_line
- karakter kümesi
- Trim\_trailing_whitespace
- INSERT\_final_newline
- kök

EditorConfig Düzenleyici ayarları XML dışında tüm Visual Studio tarafından desteklenen dillerde desteklenir. Ayrıca, EditorConfig destekler [kod stili](../ide/editorconfig-code-style-settings-reference.md) kuralları da dahil olmak üzere [dil](../ide/editorconfig-language-conventions.md), [biçimlendirme](../ide/editorconfig-formatting-conventions.md), ve [adlandırma](../ide/editorconfig-naming-conventions.md) için kuralları C# ve Visual Basic.

## <a name="add-and-remove-editorconfig-files"></a>EditorConfig dosyaları ekleyip

EditorConfig dosyayı projenize ekleyin veya kod tabanı, yeni satırları, yazdığınız kodun EditorConfig dosyanın göre biçimlendirilir. Belgeyi Biçimlendir kadar ancak EditorConfig dosya ekleme mevcut stilleri yenilerini dönüştürmez. Örneğin, sekmeler olarak biçimlendirilen girintileri dosyanızdaki varsa ve boşluklarla girinti bir EditorConfig dosyası eklerseniz, girinti karakterleri otomatik olarak boşluklara dönüştürülmez. Belgeyi Biçimlendir ne zaman (**Düzenle** > **Gelişmiş** > **belgeyi Biçimlendir** veya **Ctrl** + **K**, **Ctrl**+**D**), mevcut kod satırlarına EditorConfig dosyasındaki ayarları uygulanır.

EditorConfig dosya projenizden kaldırmak veya kod temeli ve yeni satır göre genel Düzenleyici ayarları Biçimlendirilecek kod istiyorsanız kapatın ve herhangi bir açık kod dosyaları yeniden açın.

### <a name="add-an-editorconfig-file-to-a-project"></a>EditorConfig dosyası bir projeye ekleyin.

1. Bir proje veya çözüm Visual Studio'da açın. Bağlı olarak proje veya çözüm düğümü seçin, *.editorconfig* ayarları, Çözümdeki tüm projeleri veya tek uygulamalıdır. Ayrıca, proje veya çözümü eklemek için bir klasör seçebilirsiniz *.editorconfig* dosya.

1. Menü çubuğundan seçin **proje** > **Yeni Öğe Ekle**, veya basın **Ctrl**+**Shift** + **A**.

   **Yeni Öğe Ekle** iletişim kutusu açılır.

1. Arama kutusuna arama **editorconfig**.

   İki **editorconfig dosya** öğe şablonları, arama sonuçlarında gösterilir.

   ![Visual Studio'da EditorConfig dosya öğesi şablonları](media/editorconfig-item-templates.png)

1. Seçin **editorconfig dosyası (varsayılan)** EditorConfig dosyası eklemek için şablon önceden doldurulmuş iki çekirdek girinti stili ve boyutu için EditorConfig seçeneği. Ya da seçin **editorconfig dosyası (.NET)** varsayılan ile önceden doldurulmuş bir EditorConfig dosyası eklemek için şablon [.NET kod stili, biçimlendirme ve adlandırma kuralları](../ide/editorconfig-code-style-settings-reference.md).

   Bir *.editorconfig* dosyası Çözüm Gezgini'nde görünür ve düzenleyicide açılır.

   ![Çözüm Gezgini ve düzenleyici .editorconfig dosyasında](media/editorconfig-dotnet.png)

1. Dosyayı istediğiniz gibi düzenleyin.

### <a name="other-ways-to-add-an-editorconfig-file"></a>EditorConfig dosya eklemenin başka yolları

EditorConfig dosyayı projenize ekleyebilirsiniz birkaç yolu vardır:

- [Kod çıkarımı özelliği](/visualstudio/intellicode/code-style-inference) Visual Studio Intellicode, mevcut koddan, kod stilleri algılar. Ardından, kod stili tercihleri zaten tanımlanmış bir boş olmayan EditorConfig dosyası oluşturur.

- Visual Studio 2019 ' başlayarak, şunları yapabilirsiniz [kod stili ayarlarınızı temel alan bir EditorConfig dosyası oluştur](/visualstudio/ide/code-styles-and-code-cleanup#code-styles-in-editorconfig-files) içinde **Araçları** > **seçenekleri**.

## <a name="file-hierarchy-and-precedence"></a>Dosya hiyerarşisi ve önceliği

Eklediğinizde bir *.editorconfig* dosya dosya hiyerarşinizdeki bir klasöre tüm ilgili dosyalar aynı düzeyde ve altı ayarlarını uygulayın. Diğer bölümlerini kod tabanının daha farklı kurallar kullanır, ayrıca belirli proje, codebase veya bir kod temeli bir parçası için EditorConfig ayarları geçersiz kılabilirsiniz. Başka bir yerde koddan birleştirmek ve kendi kuralları değiştirmek istemiyorsanız, bu yararlı olabilir.

Bazı veya tüm EditorConfig ayarlarını geçersiz kılmak için ekleme bir *.editorconfig* dosya düzeyinde geçersiz kılınan bu ayarların uygulanmasını istediğiniz dosya hiyerarşisi. Aynı düzeyde ve alt dizinlerde dosyaları yeni EditorConfig dosya ayarlar uygulanır.

![EditorConfig hiyerarşisi](../ide/media/vside_editorconfig_hierarchy.png)

Bazı geçersiz kılmak istiyorsanız, ancak tüm ayarları yalnızca ayarlarında *.editorconfig* dosya. Yalnızca alt düzey dosyasında açıkça listesinde özellikler geçersiz kılınır. Üst düzey'nden diğer ayarlar *.editorconfig* dosyaları devam uygulamak. Emin olmak istiyorsanız _hiçbir_ ayarlarından _herhangi_ üst düzey *.editorconfig* dosyaları kod tabanının kısmına uygulanır, ekleme ```root=true``` özelliği alt düzey *.editorconfig* dosyası:

```ini
# top-most EditorConfig file
root = true
```

EditorConfig dosyaları yukarıdan okunur. Aynı ada sahip birden çok özellik varsa, en yakın zamanda bu ada sahip özelliği önceliklidir bulundu.

## <a name="edit-editorconfig-files"></a>EditorConfig dosyaları düzenleme

Visual Studio düzenlemenize yardımcı olur *.editorconfig* IntelliSense tamamlanma listelerinde sağlayarak dosyaları.

![.Editorconfig dosyasında IntelliSense](media/editorconfig-intellisense-no-extension.png)

EditorConfig dosyanızı düzenlediğiniz sonra yeni ayarların etkili olması kod dosyalarınızı yeniden yüklemeniz gerekir.

Çok sayıda düzenlerseniz *.editorconfig* dosyaları, ilginizi çekebilecek [EditorConfig dil hizmeti uzantısı](https://marketplace.visualstudio.com/items?itemName=MadsKristensen.EditorConfig) yararlıdır. Bu uzantı özelliklerinden bazılarını söz dizimi vurgulama, geliştirilmiş IntelliSense, doğrulama ve biçimlendirme kodu içerir.

![IntelliSense ile EditorConfig dil hizmeti uzantısı](media/editorconfig-intellisense.png)

## <a name="example"></a>Örnek

Aşağıdaki örnek bir C# kod parçacığı girinti durumunu, önce ve ekledikten sonra gösterir. bir *.editorconfig* projeye dosya. **Sekmeleri** ayarı **seçenekleri** bastığınızda boşluk karakterleri oluşturmak için Visual Studio Metin Düzenleyicisi iletişim kutusu ayarlanmış **sekmesini** anahtarı.

![Metin Düzenleyici sekmesinde ayarı](../ide/media/vside_editorconfig_tabsetting.png)

Beklendiği gibi tuşuna basarak **sekmesini** anahtar sonraki satıra dört ek boşluk karakterleri ekleyerek satırı girintiler.

![EditorConfig kullanmadan önce kod](../ide/media/vside_editorconfig_before.png)

Adlı yeni bir dosya ekleme *.editorconfig* projeye aşağıdaki içeriğe sahip. `[*.cs]` Ayarı, bu değişiklik yalnızca C# kod dosyaları proje uygulandığı anlamına gelir.

```ini
# Top-most EditorConfig file
root = true

# Tab indentation
[*.cs]
indent_style = tab
```

Bastığınızda artık **sekmesini** anahtar, sekme karakterlerini yerine boşluk sahip olursunuz.

![Sekme tuşunu sekme karakteri ekler.](../ide/media/vside_editorconfig_tab.png)

## <a name="troubleshoot-editorconfig-settings"></a>EditorConfig ayarlarında sorun giderme

Varsa bir EditorConfig dosyası herhangi bir dizin yapısına veya projenizin konumunu üzerindeki Visual Studio Düzenleyicisi ayarları, dosya düzenleyiciniz için geçerlidir. Bu durumda, durum çubuğundaki şu iletiyi görebilirsiniz:

   **"Bu dosya türü için kullanıcı tercihleri bu projenin kodlama kuralları tarafından geçersiz kılınır."**

Bu durumlarda, herhangi bir düzenleyici ayarları anlamına gelir **Araçları** > **seçenekleri** > **metin düzenleyici** (örneğin, girinti boyutu ve stilini, sekme boyutunu veya kodlama kuralları), bir EditorConfig dosyasında veya proje dizin yapısına üzerindeki belirtilirse, kuralları EditorConfig dosyasındaki ayarları geçersiz kılan **seçenekleri**. Değiştirerek bu davranışı denetleyebilirsiniz **proje kodlaması kurallarını** seçeneğini **Araçları** > **seçenekleri**  >  **Metin düzenleyici**. Bu seçeneğin işaretini Visual Studio için EditorConfig desteğiyle kapatır.

![Araçlar Seçenekler - Proje kodlama kuralları](media/coding_conventions_option.png)

Tüm bulabilirsiniz *.editorconfig* üst dizininde bir komut istemi açıp aşağıdaki komutu çalıştırarak projenizi içeren disk kökünden dosyaları:

```Shell
dir .editorconfig /s
```

Ayarlayarak, EditorConfig kuralları kapsamını denetleyebilirsiniz ```root=true``` özelliğinde *.editorconfig* deponuzun veya projenizin bulunduğu dizine kök dosya. Visual Studio görünen adlı bir dosya için *.editorconfig* açılan dosya dizininde bulunan ve her bir üst dizin. Kök dosya yolunu ulaştığında veya arama biten bir *.editorconfig* ile dosya ```root=true``` bulunur.

## <a name="see-also"></a>Ayrıca bkz.

- [.NET kod stili kuralları](../ide/editorconfig-code-style-settings-reference.md)
- [Dil hizmeti için Editorconfig'i destekleme](../extensibility/supporting-editorconfig.md)
- [EditorConfig.org](http://editorconfig.org/)
- [Kod Düzenleyicisi özellikleri](writing-code-in-the-code-and-text-editor.md)
- [EditorConfig (Mac için Visual Studio)](/visualstudio/mac/editorconfig)