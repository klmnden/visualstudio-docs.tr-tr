---
title: .NET geliştirme üretkenliğinizi artırın
description: Gezinti, Kod Analizi genel bir bakış, daha hızlı .NET kod yazmanıza yardımcı olmak için birim testi ve diğer özellikleri daha iyi.
author: kuhlenh
ms.author: gewarren
manager: jillfra
ms.date: 03/26/2019
ms.topic: conceptual
helpviewer_keywords:
- editor
ms.workload:
- dotnet
ms.openlocfilehash: e7b451cf18a461f94e1d8682652e16dac9ee8ab2
ms.sourcegitcommit: d4bea2867a4f0c3b044fd334a54407c0fe87f9e8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2019
ms.locfileid: "58790465"
---
# <a name="visual-studio-productivity-guide-for-c-developers"></a>Visual Studio üretkenliği Kılavuzu C# geliştiriciler

Nasıl Visual Studio geliştiricileri her zamankinden daha üretken hale getirdiğini öğrenin. Yazdığınız sırada bir hiyerarşi görünümüne bizim performans ve üretkenlik geliştirmeleri gezinme gibi kaynak koda dönüştürülmüş derlemeler için değişken adı önerileri yararlanmak **Test Gezgini**, tümüne Git (**Ctrl** + **T**) için dosya/türü/üyeye/sembole bildirimleri, akıllı gitmek için **özel durum Yardımcısı**, kod stili yapılandırması ve zorlaması ve satır ve kod düzeltmeleri.

## <a name="im-used-to-keyboard-shortcuts-from-a-different-editor"></a>Klavye kısayolları farklı düzenleyicisinden kullandım yaşıyorum

::: moniker range="vs-2017"

**Yeni Visual Studio 2017 sürüm 15,8**

::: moniker-end

Başka bir IDE'den kullanıma sunulacak ya da ortam kodlaması, klavye düzenine değiştirebilirsiniz *Visual Studio Code* veya *ReSharper (Visual Studio)*:

![Visual Studio'da klavye düzenleri](../ide/media/VS2017Guide-Keyboard.png)

Bazı uzantılar da klavye düzenleri:

- [Visual Studio (ReSharper/Intellij) için kısayol tuşları](https://marketplace.visualstudio.com/items?itemName=JustinClareburtMSFT.HotKeys)
- [Emacs benzetimi](https://marketplace.visualstudio.com/items?itemName=JustinClareburtMSFT.EmacsEmulation)
- [VSVim](https://marketplace.visualstudio.com/items?itemName=JaredParMSFT.VsVim)

Popüler Visual Studio kısayolları şunlardır:

| Kısayol (tüm profilleri) | Komut | Açıklama |
|-|-|-|
| **CTRL**+**T** | Tümüne Git | Tüm dosya, tür, üye veya sembol bildirimi gidin |
| **F12** (Ayrıca **Ctrl**+**tıklayın**) | Tanıma Git | Bir simgenin tanımlandığı gidin |
| **CTRL**+**F12** | Uygulamaya Git | Bir temel tür veya üye, çeşitli uygulamalar için gidin |
| **Shift**+**F12** | Tüm Başvuruları Bul | Tüm sembol veya değişmez değer başvuruları bakın |
| **Ctrl**+**.** (Ayrıca **Alt**+**girin** profilindeki C#) | Hızlı Eylemler ve Yeniden Düzenlemeler | Hangi kod düzeltmeleri görmek için İmleç konumuna veya kod seçim sırasında kod oluşturma işlemleri, yeniden düzenlemeler veya diğer hızlı Eylemler kullanılabilir |
| **Ctrl**+**D** | Satırı Yinele | İmlecin bulunduğu kod satırının çoğaltır (kullanılabilir **Visual Studio 2017 sürüm 15.6** ve üzeri) |
| **Shift**+**Alt**+**+**/**-** | Seçimi Genişlet/Sözleşmesi | Genişletir ya da geçerli seçimi Düzenleyicisi'nde sözleşmeler (kullanılabilir **Visual Studio 2017 sürüm 15.5** ve üzeri) |
| **Shift** + **Alt** + **.** | Eşleşen bir sonraki giriş işareti Ekle | Seçim ve giriş işaretini geçerli seçimi ile eşleşen bir sonraki konumda ekler (kullanılabilir **Visual Studio 2017 sürüm 15,8** ve üzeri) |
| **CTRL**+**Q** | Ara | Tüm Visual Studio ayarları arama |
| **F5** | Hata Ayıklamayı Başlat | Uygulamanızı hata ayıklamayı Başlat |
| **CTRL**+**F5** | Hata ayıklama Çalıştır | Uygulamanızı yerel olarak hata ayıklama olmadan çalıştırma |
| **CTRL**+**K**,**D** (varsayılan profili) veya **Ctrl**+**E**,**D**  (C# profili) | [Belgeyi Biçimlendir](code-styles-and-quick-actions.md#format-document-command) | Yeni satır, aralık ve girintileme ayarlarını göre dosyanızdaki ihlalleri biçimlendirme temizler |
| **CTRL**+**\\**,**Ctrl**+**E** (varsayılan profili) veya **Ctrl** + **W**,**E** (C# profili) | Hata Listesi görünümü | Belge, proje veya çözüm tüm hataları görmek |
| **Alt** + **PgUp/PgDn** | Sonraki/önceki soruna gidin | Bağlantı Uyarısı, öneri, belgedeki önceki/sonraki hata için (kullanılabilir **Visual Studio 2017 sürüm 15,8** ve üzeri) |

> [!NOTE]
> Bazı uzantılar, varsayılan Visual Studio tuş bağlamalarını bağlamayı Kaldır. Yukarıdaki komutları kullanmak için tuş bağlamaları Visual Studio'nun ayarlarına giderek geri yüklemek **Araçları** > **içeri ve dışarı aktarma ayarları** > **tüm ayarları sıfırla**  veya **Araçları** > **seçenekleri** > **klavye** > **sıfırlama**.

Klavye kısayolları ve komutlar hakkında daha fazla bilgi için bkz. [klavye kısayolları](../ide/tips-and-tricks-for-visual-studio.md).

## <a name="navigate-quickly-to-files-or-types"></a>Hızlı bir şekilde dosyaları veya türleri gidin

Visual Studio 2017 adlı bir özellik olan **tümüne Git** (**Ctrl**+**T**). **Tümüne Git** herhangi dosya, tür, üye veya sembol bildirimi hızla atlamak sağlar.

- Bu Arama çubuğuna konumunu değiştirmek veya canlı Gezinti önizlemeyi kullanarak Kapat **dişli** simgesi.
- Filtre söz dizimini kullanarak sonuçları `t mytype`.
- Yalnızca geçerli belgede aramanızın kapsamını.
- CamelCase eşleşen desteklenir.

![Visual Studio tüm Git](../ide/media/VS2017Guide-go-to-all.png)

## <a name="enforce-code-style-rules-on-a-codebase"></a>Bir kod temeli üzerinde kod stili kurallarını zorla

Kullanabileceğiniz bir *.editorconfig* kodlama kurallarını kod oluşturma ve bunları kaynağınızla seyahat dosya.

::: moniker range="vs-2017"

- Yükleyebileceğiniz [EditorConfig dil Hizmetleri Uzantısı](https://aka.ms/editorconfig), kolaylaştıran ekleme ve düzenleme bir *.editorconfig* dosyasını Visual Studio'da.

::: moniker-end

::: moniker range=">=vs-2019"

- Otomatik olarak bir *.editorconfig* kod stili ayarlarınızı dosyasından **Araçları** > **seçenekleri** > **metin düzenleyicisi**  > **C#** > **Kod stili**.

   ![VS 2019 ayarlarından .editorconfig dosyası oluştur](media/vs-2019/generate-editorconfig-file.png)

::: moniker-end

- Denemenin [için Visual Studio Intellicode uzantısı](/visualstudio/intellicode/intellicode-visual-studio). Bu Deneysel uzantı mevcut koddan, kod stilleri algılar ve ardından boş olmayan oluşturur *.editorconfig* dosya ile kod stili tercihlerinizden zaten tanımlanmış.

- Kullanıma [.NET kodlama kuralı seçeneklerini](editorconfig-code-style-settings-reference.md) belgeleri.

- Bkz: [bu gist](https://gist.github.com/kuhlenh/5471666a7a2c57fea427e81cf0a41da8) örneği *.editorconfig* dosya.

![Visual Studio'da kod stil uygulama](../ide/media/VSGuide_CodeStyle.png)

## <a name="refactorings-and-code-fixes"></a>Yeniden düzenleme ve kod düzeltmeleri

Visual Studio ile çok sayıda yeniden düzenleme, kod oluşturma eylemleri ve kod düzeltmeleri gelir. Kırmızı dalgalı çizgiler hataları temsil eden yeşil dalgalı çizgiler uyarıları temsil eder ve gri üç noktaya kod önerileri temsil eder. Ampul veya tornavida simgesine tıklayarak veya basarak erişim kod düzeltmeleri yapabilirsiniz **Ctrl**+**.** veya **Alt**+**girin**. Her düzeltme, düzeltme nasıl çalıştığına ilişkin bir Canlı kod fark gösteren bir önizleme penceresi ile birlikte gelir.

Popüler hızlı düzeltmeler ve yeniden düzenlemeler içerir:

- *Yeniden Adlandır*
- *Ayıklama Yöntemi*
- *Metot İmzasını Değiştirme*
- *Oluşturucu Oluşturma*
- *Üretme Metodu*
- *Türü dosyaya Taşı*
- *Null denetimi Ekle*
- *Parametre Ekle*
- *Gereksiz kullanımları Kaldır*
- *Foreach döngüsü LINQ sorgusu veya LINQ yöntemi*
- *Üyeleri çekme*
- Daha fazla bilgi için [kod oluşturma özellikleri](code-generation-in-visual-studio.md)

Yapabilecekleriniz [FxCop Çözümleyicileri yükleme](../code-quality/install-fxcop-analyzers.md) bayrağı kod sorunları. Veya, kendi yeniden düzenleme ve kod düzeltme ile yazma [Roslyn Çözümleyicileri](https://github.com/dotnet/roslyn/wiki/Getting-Started-Writing-a-Custom-Analyzer-&-Code-Fix).

Çeşitli topluluk üyeleri, ek kod incelemeleri ekleme ücretsiz uzantıya yazmış:

- [Roslynator](https://marketplace.visualstudio.com/items?itemName=josefpihrt.Roslynator2017)
- [Visual Studio için SonarLint](https://marketplace.visualstudio.com/items?itemName=SonarSource.SonarLintforVisualStudio2017)
- [StyleCopAnalyzers](https://www.nuget.org/packages/stylecop.analyzers/)

![Visual Studio'da yeniden düzenlemeler](../ide/media/VSGuide_CodeAnalysis.png)

## <a name="find-usages-go-to-implementation-and-navigate-to-decompiled-assemblies"></a>Kullanımları uygulamasına gidin ve kaynak koda dönüştürülmüş derlemelere Git Bul

Visual Studio aramanıza yardımcı olması için birçok özelliklere sahiptir ve [kodunuzda gezinin](../ide/navigating-code.md).

| Özellik | Kısayol | Ayrıntılar/geliştirmeleri |
|- | - | -|
| Tüm Başvuruları Bul | **Shift**+**F12**| Sonuçları renklendirilmiş ve proje, tanım ve okuma veya yazma gibi bir başvuru türüne göre gruplandırılabilir. Ayrıca "sonuçları kilitleyebilir". |
| Uygulamaya Git | **CTRL**+**F12** | Tanıma Git kullanabileceğiniz `override` için geçersiz kılınan üyesiyle gitmek için anahtar sözcüğü |
| Tanıma Git | **F12** veya **Ctrl**+**tıklayın**| Tuşuna **Ctrl** tanımına gitmenizi tıklatırken |
| Tanıma göz at | **Alt**+**F12** | Satır içi görünüm tanımı |
| Yapı Görselleştirici | Gri, noktalı satırları ayraçlar arasındaki | Üzerine gelindiğinde, kod yapısını görmek için |
| Kaynak koda dönüştürülmüş derlemeleri gitme | **F12** veya **Ctrl**+**tıklayın** | Dış Kaynak (ile yetenek decompiled) özelliği etkinleştirerek gidin: **Araçlar** > **seçenekleri** > **metin düzenleyici**  >  **C#**  >   **Gelişmiş** > **kaynak koda dönüştürülmüş kaynaklara gezintiyi etkinleştir**. |

![Tümüne Git ve tüm başvuruları Bul](../ide/media/VSIDE_Productivity_Navigation.png)

## <a name="improved-intellisense"></a>Geliştirilmiş IntelliSense

İndirme [Intellicode uzantısı](https://marketplace.visualstudio.com/items?itemName=VisualStudioExptTeam.VSIntelliCode) almak için [bağlama duyarlı kod tamamlama](/visualstudio/intellicode/intellicode-visual-studio) alfabetik bir listesi yerine. Ayrıca eğitebilirsiniz bir [özel IntelliSense model](/visualstudio/intellicode/custom-model-faq) kendi etki alanına özgü kitaplıklarını temel alan.

## <a name="unit-testing"></a>Birim testi

Visual Studio 2017'den itibaren çok sayıda test deneyimi geliştirmeleri vardır. Test çerçeveleri, MSTest v1, MSTest v2, NUnit veya XUnit test edebilirsiniz.

- **Test Gezgini** test bulma işleminin hızlı.
- Testlerinizde düzenlemek **Test Gezgini** ile *hiyerarşik sıralama*.
- [Live unit Testing](../test/live-unit-testing.md) sürekli olarak kod değişikliklerinizden etkilenen testleri çalıştırır ve testlerinizi durumunu bildirmek için satır içi Düzenleyicisi simgeleri güncelleştirir. Dahil belirli testleri hariç veya test projelerinden, Canlı test kümesi.

![Visual Studio'da metin Gezgini hiyerarşi görünümü](../ide/media/VSGuide_Testing.png)

## <a name="debugging"></a>Hata Ayıklama

Visual Studio'nun hata ayıklama özelliklerini bazıları şunlardır:

::: moniker range=">=vs-2019"

- Bir dize içinde arama yapma **Watch**, **Otolar**, ve **Yereller** windows.
- *Çalıştır'ı tıklatın*, olanak sağlayan bir kod satırının yanındaki üzerine gelme görüntülenen yeşil 'Yürüt' simge ulaşmak ve bu satırı ulaşana kadar programınızı çalıştırın.
- **Özel durum Yardımcısı**, yerleştiren en önemli bilgileri üst düzey iletişim kutusunda, örneğin, hangi değişken `null` içinde bir `NullReferenceException`.
- [Hata ayıklamasına geri adım](../debugger/view-historical-application-state.md), olanak tanıyan, önceki kesme noktaları veya adımlara geri dönün ve daha önce olduğu gibi uygulama durumunu görüntüleyin.
- [Anlık görüntü hata ayıklama](/azure/application-insights/app-insights-snapshot-debugger), olanak sağlayan bir canlı web uygulaması bir özel durum oluşturuldu anda durumunu araştırmak (Azure'da olmalıdır).

::: moniker-end

::: moniker range="vs-2017"

- *Çalıştır'ı tıklatın*, olanak sağlayan bir kod satırının yanındaki üzerine gelme görüntülenen yeşil 'Yürüt' simge ulaşmak ve bu satırı ulaşana kadar programınızı çalıştırın.
- **Özel durum Yardımcısı**, yerleştiren en önemli bilgileri üst düzey iletişim kutusunda, örneğin, hangi değişken `null` içinde bir `NullReferenceException`.
- [Hata ayıklamasına geri adım](../debugger/view-historical-application-state.md), olanak tanıyan, önceki kesme noktaları veya adımlara geri dönün ve daha önce olduğu gibi uygulama durumunu görüntüleyin.
- [Anlık görüntü hata ayıklama](/azure/application-insights/app-insights-snapshot-debugger), olanak sağlayan bir canlı web uygulaması bir özel durum oluşturuldu anda durumunu araştırmak (Azure'da olmalıdır).

::: moniker-end

![Visual Studio'da özel durum Yardımcısı](../ide/media/VSGuide_Debugging.png)

## <a name="version-control"></a>Sürüm denetimi

Git veya TFVC, depolama ve Visual Studio'da kodunuzu güncelleştirmek için kullanabilirsiniz.

::: moniker range=">=vs-2019"

- Yükleme [çekme istekleri için Visual Studio](https://marketplace.visualstudio.com/items?itemName=vsideversioncontrolmsft.pr4vs) oluşturmak için gözden geçirin, kullanıma ve çekme istekleri Visual Studio'dan ayrılmanıza gerek kalmadan çalıştırın.

::: moniker-end

- Değişikliklerinizi yerel düzenleme [Takım Gezgini](reference/team-explorer-reference.md) ve durum çubuğunda işlemeler ve değişiklikleri izlemek için kullanabilirsiniz.

- Sürekli tümleştirme ve teslim ile Visual Studio içinde ASP.NET projeleri için ayarlama [Visual Studio için sürekli teslim Araçları](https://marketplace.visualstudio.com/items?itemName=VSIDEDevOpsMSFT.ContinuousDeliveryToolsforVisualStudio) uzantısı.

![Visual Studio kaynak denetimi](../ide/media/VSIDE_Productivity_SourceControl.png)

## <a name="what-other-features-should-i-know-about"></a>Hakkında başka hangi özellikler bilmeniz?

Kod yazma daha verimli hale getirmek için düzenleyici ve üretkenlik özelliklerin bir listesi aşağıda verilmiştir. Bazı özellikler devre dışı (bunlar makinenizde şeyler dizin, tartışmalı veya şu anda Deneysel) varsayılan olarak olduklarından etkinleştirilmesi gerekebilir.

| Özellik | Ayrıntılar | Etkinleştirme |
|-|-|-|
| Çözüm Gezgini'nde dosyayı bulun | Etkin dosyada vurgular **Çözüm Gezgini** | **Araçlar** > **seçenekleri** > **projeler ve çözümler** > **Çözüm Gezgini'nde etkin öğe izleme** |
| Başvuru bütünleştirilmiş kodları ve NuGet paketleri içinde türler için using ekleme | Bir hata ampul başvurulmayan bir türü için bir NuGet paketini yüklemek için bir kod düzeltme gösterir | **Araçlar** > **seçenekleri** > **metin düzenleyici** > **C#** > **Gelişmiş**   >  **Reference bütünleştirilmiş kodlarında türler için using Öner** ve **NuGet paketlerinde türler için using Öner** |
| Tam çözüm analizini etkinleştirme | Çözümünüzdeki tüm hataları görmek **hata listesi** | **Araçlar** > **seçenekleri** > **metin düzenleyici** > **C#** > **Gelişmiş**   >  **Tam çözüm analizini etkinleştirme** |
| Kaynak koda dönüştürülmüş kaynaklara gezintiyi etkinleştir | Tür/üye dış kaynaklardan tanıma ver ve metot gövdeleri gösterilecek yetenek kaynak koda dönüştürücü kullanma | **Araçlar** > **seçenekleri** > **metin düzenleyici** > **C#** > **Gelişmiş**   >  **Kaynak koda dönüştürülmüş kaynaklara gezintiyi etkinleştir** |
| Tamamlanma/öneri modu | IntelliSense tamamlanma davranışı değiştirir. Intellij arka planlar geliştiricilere, varsayılan olmayan bir ayarı burada kullanma eğilimindedir. | **Menü** > **Düzenle** > **IntelliSense** > **tamamlama modunu Değiştir** |
| [CodeLens](../ide/find-code-changes-and-other-history-with-codelens.md) | Başvuru bilgileri kod ve değişiklik geçmişi Düzenleyicisi'nde görüntüler | **Araçlar** > **seçenekleri** > **metin düzenleyici** > **tüm diller**  >   **CodeLens** |
| [Kod parçacıkları](../ide/visual-csharp-code-snippets.md) | Ortak Demirbaş kodu saplama Yardım | Bir kod parçacığı adı yazıp basın **sekmesini** iki kez. |