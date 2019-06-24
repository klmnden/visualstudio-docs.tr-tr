---
title: .NET geliştirme üretkenliğinizi artırın
description: Gezinti, Kod Analizi genel bir bakış, daha hızlı .NET kod yazmanıza yardımcı olmak için birim testi ve diğer özellikleri daha iyi.
author: kuhlenh
ms.author: gewarren
manager: jillfra
ms.date: 04/25/2019
ms.topic: conceptual
helpviewer_keywords:
- editor
ms.workload:
- dotnet
ms.openlocfilehash: bd36b75f3df640df0e1910fb3a7a52d17c37d30f
ms.sourcegitcommit: 7eb2fb21805d92f085126f3a820ac274f2216b4e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/22/2019
ms.locfileid: "67328773"
---
# <a name="visual-studio-productivity-guide-for-c-developers"></a>Visual Studio üretkenliği Kılavuzu C# geliştiriciler

Nasıl Visual Studio geliştiricileri her zamankinden daha üretken hale getirdiğini öğrenin. Yazdığınız sırada bir hiyerarşi görünümüne bizim performans ve üretkenlik geliştirmeleri gezinme gibi kaynak koda dönüştürülmüş derlemeler için değişken adı önerileri yararlanmak **Test Gezgini**, tümüne Git (**Ctrl** + **T**) için dosya/türü/üyeye/sembole bildirimleri, akıllı gitmek için **özel durum Yardımcısı**, kod stili yapılandırması ve zorlaması ve birçok yeniden düzenlemeler ve kod düzeltir.

## <a name="im-used-to-keyboard-shortcuts-from-a-different-editor"></a>Klavye kısayolları farklı düzenleyicisinden kullandım yaşıyorum

::: moniker range="vs-2017"

**Yeni Visual Studio 2017 sürüm 15,8**

::: moniker-end

Başka bir IDE'den kullanıma sunulacak ya da ortam kodlaması, klavye düzenine değiştirebilirsiniz *Visual Studio Code* veya *ReSharper (Visual Studio)* :

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
| **Ctrl**+ **.** (Ayrıca **Alt**+**girin** profilindeki C#) | Hızlı Eylemler ve Yeniden Düzenlemeler | Hangi kod düzeltmeleri görmek için İmleç konumuna veya kod seçim sırasında kod oluşturma işlemleri, yeniden düzenlemeler veya diğer hızlı Eylemler kullanılabilir |
| **Ctrl**+**D** | Satırı Yinele | İmlecin bulunduğu kod satırının çoğaltır (kullanılabilir **Visual Studio 2017 sürüm 15.6** ve üzeri) |
| **Shift**+**Alt**+ **+** / **-** | Seçimi Genişlet/Sözleşmesi | Genişletir ya da geçerli seçimi Düzenleyicisi'nde sözleşmeler (kullanılabilir **Visual Studio 2017 sürüm 15.5** ve üzeri) |
| **Shift** + **Alt** +  **.** | Eşleşen bir sonraki giriş işareti Ekle | Seçim ve giriş işaretini geçerli seçimi ile eşleşen bir sonraki konumda ekler (kullanılabilir **Visual Studio 2017 sürüm 15,8** ve üzeri) |
| **CTRL**+**Q** | Ara | Tüm Visual Studio ayarları arama |
| **F5** | Hata Ayıklamayı Başlat | Uygulamanızı hata ayıklamayı Başlat |
| **CTRL**+**F5** | Hata ayıklama Çalıştır | Uygulamanızı yerel olarak hata ayıklama olmadan çalıştırma |
| **CTRL**+**K**,**D** (varsayılan profili) veya **Ctrl**+**E**,**D**  (C# profili) | Belgeyi Biçimlendir | Yeni satır, aralık ve girintileme ayarlarını göre dosyanızdaki ihlalleri biçimlendirme temizler |
| **CTRL**+ **\\** ,**Ctrl**+**E** (varsayılan profili) veya **Ctrl** + **W**,**E** (C# profili) | Hata Listesi görünümü | Belge, proje veya çözüm tüm hataları görmek |
| **Alt** + **PgUp/PgDn** | Sonraki/önceki soruna gidin | Bağlantı Uyarısı, öneri, belgedeki önceki/sonraki hata için (kullanılabilir **Visual Studio 2017 sürüm 15,8** ve üzeri) |
| **CTRL**+**K**, **/** | İki durumlu tek satır açıklama açıklamasını kaldırın | Bu komut, ekler veya seçiminizi zaten açıklamalı bağlı olarak bir tek satır açıklama kaldırır |
| **CTRL**+**kaydırma**+ **/** | İki durumlu blok açıklama açıklamasını kaldırın | Bu komut ekler veya kaldırır seçmiş olduğunuz bağlı olarak açıklama engelle |

> [!NOTE]
> Bazı uzantılar, varsayılan Visual Studio tuş bağlamalarını bağlamayı Kaldır. Yukarıdaki komutları kullanmak için tuş bağlamaları Visual Studio'nun ayarlarına giderek geri yüklemek **Araçları** > **içeri ve dışarı aktarma ayarları** > **tüm ayarları sıfırla**  veya **Araçları** > **seçenekleri** > **klavye** > **sıfırlama**.

Klavye kısayolları ve komutlar hakkında daha fazla bilgi için bkz. [üretkenlik kısayolları](../ide/productivity-shortcuts.md) ve [popüler klavye kısayolları](default-keyboard-shortcuts-for-frequently-used-commands-in-visual-studio.md).

## <a name="navigate-quickly-to-files-or-types"></a>Hızlı bir şekilde dosyaları veya türleri gidin

Visual Studio denilen bir özelliği olan **tümüne Git** (**Ctrl**+**T**). **Tümüne Git** herhangi dosya, tür, üye veya sembol bildirimi hızla atlamak sağlar.

- Bu Arama çubuğuna konumunu değiştirmek veya canlı Gezinti önizlemeyi kullanarak Kapat **dişli** simgesi.
- Filtre söz dizimini kullanarak sonuçları `t mytype`.
- Yalnızca geçerli belgede aramanızın kapsamını.
- Camel case eşleşen desteklenir.

![Visual Studio tüm Git](../ide/media/VS2017Guide-go-to-all.png)

## <a name="enforce-code-style-rules"></a>Kod stili kurallarını zorla

Kodlama kurallarını kod oluşturma ve bunları kaynağınızla seyahat EditorConfig dosyası kullanabilirsiniz.

![Visual Studio'da kod stil uygulama](../ide/media/VSGuide_CodeStyle.png)

- Varsayılan ekleyin veya. NET stil EditorConfig dosyasını seçerek projenize **Ekle** > **yeni öğe**. İçinde **Yeni Öğe Ekle** iletişim kutusu, "editorconfig" arayın. Birini **editorconfig dosya** öğe şablonları ve ardından **Ekle**.

   ![EditorConfig Visual Studio öğe şablonları](media/editorconfig-item-templates.png)

::: moniker range=">=vs-2019"

- Otomatik olarak bir *.editorconfig* kod stili ayarlarınızı temel dosya **Araçları** > **seçenekleri** > **metin Düzenleyici** > **C#** > **kod stili**.

   ![VS 2019 ayarlarından .editorconfig dosyası oluştur](media/vs-2019/generate-editorconfig-file.png)

::: moniker-end

- [Kod çıkarımı özelliği](/visualstudio/intellicode/code-style-inference) Visual Studio Intellicode, mevcut koddan, kod stilleri algılar. Ardından, kod stili tercihleri zaten tanımlanmış bir boş olmayan EditorConfig dosyası oluşturur.

Kullanıma [.NET kodlama kuralı seçeneklerini](editorconfig-code-style-settings-reference.md) belgeleri, ayrıca eksiksiz bir EditorConfig dosyası örneği içerir.

::: moniker range=">=vs-2019"

## <a name="code-cleanup"></a>Kodu temizleme

Visual Studio sağlar kod stili tercihleri dahil olmak üzere kod dosyanızın üzerine biçimlendirme **kod Temizleme** özelliği. Kod temizleme çalıştırılacak broom tuşuna basın ve düzenleyici altındaki simgesini **Ctrl**+**K**, **Ctrl**+**E**.

![Visual Studio 2019 kod temizleme düğmesi](media/execute-code-cleanup.png)

Tüm proje veya çözümünüzdeki arasında kod temizleme de çalıştırabilirsiniz. İçinde proje veya çözüm adına sağ tıklayın **Çözüm Gezgini**seçin **analiz ve kod Temizleme**ve ardından **çalıştırma kod Temizleme**.

![Tüm proje veya çözüm arasında kod temizleme işlemi çalıştırın](media/run-code-cleanup-project-solution.png)

Dosyanızı alanları, girintileri yapmalıyız, biçimlendirme yanı sıra **kod Temizleme** seçili kod stilleri için de geçerlidir. Her kod stili tercihlerinizi okuyabilir [EditorConfig dosya](code-styles-and-code-cleanup.md#code-styles-in-editorconfig-files), bir proje için ya da yoksa [kod stili ayarları](code-styles-and-code-cleanup.md#code-styles-in-the-options-dialog-box) içinde **seçenekleri** iletişim kutusu.

::: moniker-end

## <a name="refactorings-and-code-fixes"></a>Yeniden düzenleme ve kod düzeltmeleri

Visual Studio ile çok sayıda yeniden düzenlemeler, kod oluşturma eylemleri ve kod düzeltmeleri gelir. Kırmızı dalgalı çizgiler hataları temsil eden yeşil dalgalı çizgiler uyarıları temsil eder ve gri üç noktaya kod önerileri temsil eder. Ampul veya tornavida simgesine tıklayarak veya basarak erişim kod düzeltmeleri yapabilirsiniz **Ctrl**+ **.** veya **Alt**+**girin**. Her düzeltme, düzeltme nasıl çalıştığına ilişkin bir Canlı kod fark gösteren bir önizleme penceresi ile birlikte gelir.

Popüler hızlı düzeltmeler ve yeniden düzenlemeler içerir:

- Rename
- Ayıklama Yöntemi
- Metot imzasını değiştirme
- Oluşturucu Oluşturma
- Metodunu üret
- Türü dosyaya Taşı
- Null denetimi Ekle
- Parametre Ekle
- Gereksiz kullanımları Kaldır
- Foreach döngüsü LINQ sorgusu veya LINQ yöntemi
- Üyeleri çekme

Daha fazla bilgi için [oluşturma özellikleri kod](code-generation-in-visual-studio.md).

Yapabilecekleriniz [FxCop Çözümleyicileri yükleme](../code-quality/install-fxcop-analyzers.md) bayrağı kod sorunları. Veya, kendi yeniden düzenleme ve kod düzeltme ile yazma [Roslyn Çözümleyicileri](https://github.com/dotnet/roslyn/wiki/Getting-Started-Writing-a-Custom-Analyzer-&-Code-Fix).

Çeşitli topluluk üyeleri, ek kod incelemeleri ekleme ücretsiz uzantıya yazmış:

- [Roslynator](https://marketplace.visualstudio.com/items?itemName=josefpihrt.Roslynator2017)
- [Visual Studio için SonarLint](https://marketplace.visualstudio.com/items?itemName=SonarSource.SonarLintforVisualStudio2017)
- [StyleCopAnalyzers](https://www.nuget.org/packages/stylecop.analyzers/)
- [CodeCracker](https://www.nuget.org/packages/codecracker.CSharp/)

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

Visual Studio Intellicode gidebilir [bağlama duyarlı kod tamamlama](/visualstudio/intellicode/intellicode-visual-studio) alfabetik bir listesi yerine. Ayrıca eğitebilirsiniz bir [özel IntelliSense model](/visualstudio/intellicode/custom-model-faq) kendi etki alanına özgü kitaplıklarını temel alan.

## <a name="unit-testing"></a>Birim testi

Visual Studio 2017'den itibaren çok sayıda test deneyimi geliştirmeleri vardır. Test çerçeveleri, MSTest v1, MSTest v2, NUnit veya XUnit test edebilirsiniz.

- **Test Gezgini** test bulma işleminin hızlı.

- Testlerinizde düzenlemek **Test Gezgini** ile *hiyerarşik sıralama*.

   ![Visual Studio'da metin Gezgini hiyerarşi görünümü](../ide/media/VSGuide_Testing.png)

- [Live unit Testing](../test/live-unit-testing.md) sürekli olarak kod değişikliklerinizden etkilenen testleri çalıştırır ve testlerinizi durumunu bildirmek için satır içi Düzenleyicisi simgeleri güncelleştirir. Dahil belirli testleri hariç veya test projelerinden, Canlı test kümesi. (Yalnızca visual Studio Enterprise sürümü.)

## <a name="debugging"></a>Hata Ayıklama

Visual Studio'nun hata ayıklama özelliklerini bazıları şunlardır:

::: moniker range=">=vs-2019"

- Bir dize içinde arama yapma **Watch**, **Otolar**, ve **Yereller** windows.
- *Çalıştır'ı tıklatın*, olanak sağlayan bir kod satırının yanındaki üzerine gelme görüntülenen yeşil 'Yürüt' simge ulaşmak ve bu satırı ulaşana kadar programınızı çalıştırın.
- **Özel durum Yardımcısı**, hangi değişken en üst düzeyinde iletişim kutusunda, örneğin, en önemli bilgileri yerleştiren `null` içinde bir `NullReferenceException`.
- [Hata ayıklamasına geri adım](../debugger/view-historical-application-state.md), olanak tanıyan, önceki kesme noktaları veya adımlara geri dönün ve daha önce olduğu gibi uygulama durumunu görüntüleyin.
- [Anlık görüntü hata ayıklama](/azure/application-insights/app-insights-snapshot-debugger), olanak sağlayan bir canlı web uygulaması bir özel durum oluşturuldu anda durumunu araştırmak (Azure'da olmalıdır).

::: moniker-end

::: moniker range="vs-2017"

- *Çalıştır'ı tıklatın*, olanak sağlayan bir kod satırının yanındaki üzerine gelme görüntülenen yeşil 'Yürüt' simge ulaşmak ve bu satırı ulaşana kadar programınızı çalıştırın.
- **Özel durum Yardımcısı**, hangi değişken en üst düzeyinde iletişim kutusunda, örneğin, en önemli bilgileri yerleştiren `null` içinde bir `NullReferenceException`.
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
| Başvuru bütünleştirilmiş kodları ve NuGet paketleri içinde türler için using ekleme | Bir hata ampul başvurulmayan bir türü için bir NuGet paketini yüklemek için bir kod düzeltme gösterir | **Araçlar** > **seçenekleri** > **metin düzenleyici** > **C#**  > **Gelişmiş**   >  **Reference bütünleştirilmiş kodlarında türler için using Öner** ve **NuGet paketlerinde türler için using Öner** |
| Tam çözüm analizini etkinleştirme | Çözümünüzdeki tüm hataları görmek **hata listesi** | **Araçlar** > **seçenekleri** > **metin düzenleyici** > **C#**  > **Gelişmiş**   >  **Tam çözüm analizini etkinleştirme** |
| Kaynak koda dönüştürülmüş kaynaklara gezintiyi etkinleştir | Tür/üye dış kaynaklardan tanıma ver ve metot gövdeleri gösterilecek yetenek kaynak koda dönüştürücü kullanma | **Araçlar** > **seçenekleri** > **metin düzenleyici** > **C#**  > **Gelişmiş**   >  **Kaynak koda dönüştürülmüş kaynaklara gezintiyi etkinleştir** |
| Tamamlanma/öneri modu | IntelliSense tamamlanma davranışı değiştirir. Intellij arka planlar geliştiricilere, varsayılan olmayan bir ayarı burada kullanma eğilimindedir. | **Menü** > **Düzenle** > **IntelliSense** > **tamamlama modunu Değiştir** |
| [CodeLens](../ide/find-code-changes-and-other-history-with-codelens.md) | Başvuru bilgileri kod ve değişiklik geçmişi Düzenleyicisi'nde görüntüler. (Kaynak denetimi CodeLens göstergeleri içinde Visual Studio Community sürümü kullanıma sunulmaz.) | **Araçlar** > **seçenekleri** > **metin düzenleyici** > **tüm diller**  >   **CodeLens** |
| [Kod parçacıkları](../ide/visual-csharp-code-snippets.md) | Ortak Demirbaş kodu saplama Yardım | Bir kod parçacığı adı yazıp basın **sekmesini** iki kez. |
