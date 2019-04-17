---
title: Visual Studio IDE turu
titleSuffix: ''
ms.date: 02/21/2019
ms.topic: quickstart
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: da6c19341a1e1ab37b38ae4f5379ee5aaace5b87
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/17/2019
ms.locfileid: "59651064"
---
# <a name="quickstart-first-look-at-the-visual-studio-ide"></a>Hızlı Başlangıç: Visual Studio IDE’ye ilk bakış

Bu 5-10 dakikalık bir giriş Visual Studio tümleşik geliştirme ortamı (IDE), biz windows, menüler ve diğer kullanıcı Arabirimi özellikleri bazıları ilişkin tura katılın.

::: moniker range="vs-2017"

Visual Studio henüz yüklemediyseniz, Git [Visual Studio indirmeleri](https://visualstudio.microsoft.com/vs/older-downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=vs+2017+download) ücretsiz yüklemek için sayfa.

::: moniker-end

::: moniker range=">=vs-2019"

Visual Studio henüz yüklemediyseniz, Git [Visual Studio indirmeleri](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2019) ücretsiz yüklemek için sayfa.

::: moniker-end

::: moniker range="vs-2017"

## <a name="start-page"></a>Başlangıç Sayfası

Visual Studio'yu açtıktan sonra göreceksiniz ilk şey bir olasılıktır **başlangıç sayfası**. **Başlangıç sayfası** "hub" komut bulmanıza ve proje dosyalarını daha hızlı ihtiyacınız yardımcı olmak için tasarlanmıştır. **Son** projeleri ve klasörleri, çalıştığınız üzerinde son bölümünde görüntülenir. Altında **yeni proje**, ortaya çıkarmak için bir bağlantıya tıklayabilirsiniz **yeni proje** iletişim kutusu veya altında **açın**, bir var olan kod proje veya klasör açabilirsiniz. Sağ tarafta en güncel Geliştirici haberlerini oluşan akışını ' dir.

![Visual Studio'da başlangıç sayfası](media/start-page.png)

Kapatırsanız **başlangıç sayfası** ve tekrar görmek istiyorsanız, buradan yeniden **dosya** menüsü.

![Visual Studio'da Dosya menüsü](media/quickstart-IDE-file-menu-large.png)

::: moniker-end

::: moniker range=">=vs-2019"

## <a name="start-window"></a>Başlangıç penceresi

Visual Studio'yu açtıktan sonra gördüğünüz ilk şey bir başlangıç penceredir. Başlangıç penceresi "kodu daha hızlı" yardımcı olmak için tasarlanmıştır. Bu, kopyalama veya kullanıma alma kodu, varolan bir projeyi veya çözümü açın, yeni bir proje oluşturun veya yalnızca bazı kod dosyaları içeren klasör Aç için seçenek vardır.

[![](media/vs-2019/start-window-labeled.png "Visual Studio 2019 başlangıç penceresi")](media/vs-2019/start-window-labeled.png#lightbox)

Visual Studio kullanıyorsanız ilk kez varsa, son kullanılan projeler listesi boş olur.

İle çalışıyorsanız dayalı MSBuild dışındaki kod tabanlarında, kullanacağınız **yerel bir klasöre açın** kodunuzu Visual Studio'da açmak için seçeneği. Daha fazla bilgi için [kod Visual Studio'da projeler veya çözümler olmadan geliştirme](develop-code-in-visual-studio-without-projects-or-solutions.md). Aksi takdirde, yeni bir proje oluşturun veya GitHub ya da Azure DevOps gibi bir kaynak sağlayıcısı bir projeden kopyalayın.

**Kod olmadan devam** seçeneği yalnızca belirli bir proje veya yüklenen kod olmadan Visual Studio geliştirme ortamını açar. Katılmak için bu seçeneği belirleyebilirsiniz bir [Live Share](/visualstudio/liveshare/) oturuma veya hata ayıklama için bir işleme iliştirin. Ayrıca basabilirsiniz **Esc** başlangıç pencereyi kapatın ve IDE açın.

::: moniker-end

## <a name="create-a-project"></a>Proje oluşturma

Visual Studio'nun özellikleri keşfetmeye devam etmek için yeni bir proje oluşturalım.

::: moniker range="vs-2017"

1. Üzerinde **başlangıç sayfası**, arama kutusuna altında **yeni proje**, yazın **konsol** adında içeren "konsol" Bu proje türleri listesini filtrelemek için.

   ![Visual Studio Başlangıç sayfasında Proje şablonlarında Ara](media/start-page-search-templates.png)

   Visual Studio, çeşitli yardımcı olacak proje şablonları, hızlı bir şekilde kodlama başlama sağlar. C# seçin **konsol uygulaması (.NET Framework)** proje şablonu. (Visual Basic, C++, Javascript veya diğer dil Geliştirici kullanıyorsanız alternatif olarak, bir projeyi bu dillerden birinde oluşturun çekinmeyin. Biz göz atan kullanıcı Arabirimi için tüm programlama dillerinde benzer.)

1. İçinde **yeni proje** görüntülenen iletişim kutusunda varsayılan proje adını kabul edin ve **Tamam**.

::: moniker-end

::: moniker range=">=vs-2019"

1. Pencerenin başlangıç seçin **yeni bir proje oluşturma**.

   Bildiren bir iletişim kutusu açılır **yeni bir proje oluşturma**. Burada, arayabilirsiniz, filtreleme ve bir proje şablonu seçin. Ayrıca, son kullanılan proje şablonları listesini gösterir.

1. Üstteki arama kutusuna yazın **konsol** adında içeren "konsol" Bu proje türleri listesini filtrelemek için. Daha fazla çekme tarafından arama sonuçlarını iyileştirmek **C#** (veya tercih ettiğiniz başka bir dil) öğesinden **dil** Seçici.

   ![Visual Studio 2019'teki yeni proje iletişim kutusu](media/vs-2019/create-a-new-project.png)

1. Seçtiyseniz C#, Visual Basic veya F# diliniz olarak seçin **konsol uygulaması (.NET Framework)** şablonu seçip **sonraki**. (Farklı bir dil seçtiyseniz yalnızca herhangi bir şablon seçin. Biz göz atan kullanıcı Arabirimi için tüm programlama dillerinde benzer.)

1. Üzerinde **yeni projenizi yapılandırın** sayfasında, varsayılan proje adını ve konumunu kabul edin ve ardından **Oluştur**.

::: moniker-end

   Proje oluşturulur ve bir dosya adlı *Program.cs* açılır **Düzenleyicisi** penceresi. **Düzenleyicisi** dosyaların içeriğini gösterir ve Visual Studio kodlama iş çoğunu burada gerçekleştirirsiniz.

   ![Visual Studio Düzenleyicisi](media/editor.png)

## <a name="solution-explorer"></a>Çözüm Gezgini

**Çözüm Gezgini**, genellikle Visual Studio'nun sağ tarafta olduğu gösterir, dosya ve klasörlerin hiyerarşi grafik gösterimi proje, çözüm veya kod klasörü. Hiyerarşi göz atabilir ve bir dosyaya gidin **Çözüm Gezgini**.

![Visual Studio'daki Çözüm Gezgini'nde](media/quickstart-IDE-solution-explorer.png)

## <a name="menus"></a>Menüler

Visual Studio'nun üst menü çubuğu komutlarını kategoriler halinde gruplandırır. Örneğin, **proje** menüsü, içinde çalışmakta olduğunuz projeye ilgili komutları içerir. Üzerinde **Araçları** menüsünde seçerek Visual Studio nasıl davranacağını özelleştirebileceğiniz **seçenekleri**, veya özelliklerini seçerek yüklemenize ekleyin **araçları ve özellikleri Al**.

::: moniker range="vs-2017"

![Visual Studio 2017 menü çubuğu](media/quickstart-IDE-menu-bar.png)

::: moniker-end

::: moniker range=">=vs-2019"

![Visual Studio 2019 menü çubuğundaki](media/vs-2019/menu-bar.png)

::: moniker-end

## <a name="error-list"></a>Hata Listesi

Açık **hata listesi** penceresini seçerek **görünümü** menüsü, ardından **hata listesi**.

**Hata listesi** hata, uyarı ve kodunuzu geçerli durumuna ilişkin ileti gösterir. Hataları (örneğin, bir eksik küme ayracı veya noktalı virgül) dosyanızı veya herhangi bir projeniz varsa, bunlar burada listelenen.

![Visual Studio hata listesi](media/quickstart-IDE-error-list.png)

## <a name="output-window"></a>Çıktı penceresi

**Çıkış** çıkış penceresi şunu gösterir, iletileri projenizi oluşturma ve kaynak denetimi sağlayıcınız.

Şimdi projeyi görmek için bazı derleme çıkışı. Gelen **derleme** menüsünde seçin **Çözümü Derle**. **Çıkış** penceresi otomatik olarak odağa gelir ve derleme başarılı iletisini görüntüler.

![Visual Studio çıktı penceresinde](media/build-output-minimal.png)

## <a name="search-box"></a>Arama kutusu

Arama kutusuna, neredeyse her şey Visual Studio'da gitmek için hızlı ve kolay bir yoludur. Yapmak istediğiniz ilgili metin girebilir ve onu metne ait seçenekler listesini göstereceğiz. Örneğin, tam olarak ne yapı yapıyor ek bilgileri görüntülemek için derleme çıkışın ayrıntı düzeyini artırmak istediğiniz düşünün. İşte, nasıl yapabilir:

::: moniker range="vs-2017"

1. Bulun **hızlı başlatma** IDE, sağ üst kısımdaki arama kutusuna. (Alternatif olarak, basın **Ctrl**+**Q** erişmek için.)

2. Tür **ayrıntı** kartındaki arama kutusuna. Görüntülenen sonuçlardan seçin **projeler ve çözümler--> derleme ve çalıştırma** altında **seçenekleri** kategorisi.

   ![Visual Studio 2017'de arama kutusuna hızlı başlatma](media/quickstart-IDE-quick-launch.png)

   **Seçenekleri** iletişim kutusu açılır **derleme ve çalıştırma** seçenekler sayfası.

::: moniker-end

::: moniker range=">=vs-2019"

1. Tuşuna **Ctrl**+**Q** IDE üst kısmındaki arama kutusuna etkinleştirmek için.

2. Tür **ayrıntı** kartındaki arama kutusuna. Görüntülenen sonuçlardan seçin **değişiklik MSBuild ayrıntı**.

   ![Visual Studio 2019 arama kutusuna](media/vs-2019/quick-launch-verbosity.png)

   **Seçenekleri** iletişim kutusu açılır **derleme ve çalıştırma** seçenekler sayfası.

::: moniker-end

3. Altında **MSBuild proje oluşturması çıkış ayrıntısı**, seçin **Normal**ve ardından **Tamam**.

4. Sağ tıklayarak projeyi yeniden derleyin **ConsoleApp1** projesi **Çözüm Gezgini** seçip **yeniden** bağlam menüsünden.

   Bu süre **çıkış** penceresi, hangi dosyalar dahil olmak üzere nerede kopyalanan yapı işleminden daha ayrıntılı günlük kaydı gösterir.

   ![Visual Studio'da ayrıntılı yapı çıktısı](media/build-output-verbose.png)

## <a name="send-feedback-menu"></a>Menü geri bildirim gönder

Visual Studio kullanıyorsanız ya da ürünün iyileştirilmesine ilişkin önerileriniz varsa, kullanabileceğiniz herhangi bir sorunu karşılaşmamalıdırlar **geri bildirim gönder** Visual Studio penceresinin üst kısmındaki menü.

::: moniker range="vs-2017"

![Visual Studio 2017'de menüsünde geri bildirim gönder](media/quickstart-IDE-send-feedback.png)

::: moniker-end

::: moniker range=">=vs-2019"

![İçinde Visual Studio 2019 menüsünde geri bildirim gönder](media/vs-2019/send-feedback-menu.png)

::: moniker-end

## <a name="next-steps"></a>Sonraki adımlar

Visual Studio kullanıcı arabirimi ile tanışın özelliklerinin birkaçı adresindeki inceledik. Daha iyi keşfedilebilmesi için:

> [!div class="nextstepaction"]
> [Kod Düzenleyicisi hakkında bilgi edinin](../get-started/tutorial-editor.md)

> [!div class="nextstepaction"]
> [Projeler ve çözümler hakkında bilgi edinin](../get-started/tutorial-projects-solutions.md)

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio IDE genel bakış](../get-started/visual-studio-ide.md)
- [Visual Studio'nun daha fazla özellik](../ide/advanced-feature-overview.md)
- [Tema ve yazı tipi renkleri değiştirme](../ide/quickstart-personalize-the-ide.md)
