---
title: Visual Studio IDE turu
titleSuffix: ''
ms.date: 02/05/2019
ms.topic: quickstart
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 677dddbde5e90117dc19acfaf54a941c304ae7f1
ms.sourcegitcommit: 44e9b1d9230fcbbd081ee81be9d4be8a485d8502
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/30/2019
ms.locfileid: "70180062"
---
# <a name="first-look-at-the-visual-studio-ide"></a>Visual Studio IDE’ye ilk bakış

Bu 5-10 dakikalık bir giriş Visual Studio tümleşik geliştirme ortamı (IDE), biz windows, menüler ve diğer kullanıcı Arabirimi özellikleri bazıları ilişkin tura katılın.

::: moniker range="vs-2017"

Visual Studio henüz yüklemediyseniz, Git [Visual Studio indirmeleri](https://visualstudio.microsoft.com/vs/older-downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=vs+2017+download) ücretsiz yüklemek için sayfa.

::: moniker-end

::: moniker range="vs-2019"

Visual Studio henüz yüklemediyseniz, Git [Visual Studio indirmeleri](https://visualstudio.microsoft.com/downloads) ücretsiz yüklemek için sayfa.

::: moniker-end

::: moniker range=">=vs-2019"

## <a name="start-window"></a>Başlangıç penceresi

Visual Studio 'Yu başlattıktan sonra ilk olarak göreceğiniz şey başlangıç penceresidir. Başlangıç penceresi, "koda ulaşmak" için daha hızlı yardımcı olacak şekilde tasarlanmıştır. Kodu kapatma veya kullanıma alma, var olan bir projeyi veya çözümü açma, yeni bir proje oluşturma veya yalnızca bazı kod dosyalarını içeren bir klasörü açma seçeneklerine sahiptir.

[![Visual Studio 2019 ' de başlangıç penceresi](media/vs-2019/start-window.png)](media/vs-2019/start-window.png)

Visual Studio 'Yu ilk kez kullanıyorsanız, son projeler listeniz boş olur.

MSBuild tabanlı olmayan kod tabanlarında çalışıyorsanız, Visual Studio 'da kodunuzu açmak için **yerel klasör aç** seçeneğini kullanacaksınız. Daha fazla bilgi için [kod Visual Studio'da projeler veya çözümler olmadan geliştirme](develop-javascript-code-without-solutions-projects.md). Aksi takdirde, yeni bir proje oluşturabilir veya GitHub ya da Azure DevOps gibi bir kaynak sağlayıcıdan proje kopyalayabilirsiniz.

**Kod olmadan devam et** seçeneği, Visual Studio geliştirme ortamını belirli bir proje veya kod yüklenmeden yalnızca açar. Bir [live share](/visualstudio/liveshare/) oturumuna katmak veya hata ayıklama için bir işleme iliştirmek üzere bu seçeneği belirleyebilirsiniz. Başlangıç penceresini kapatmak ve IDE 'yi açmak için **ESC** tuşuna da basabilirsiniz.

::: moniker-end

::: moniker range="vs-2017"

## <a name="start-page"></a>Başlangıç Sayfası

Visual Studio'yu başlattıktan sonra göreceksiniz ilk şey bir olasılıktır **başlangıç sayfası**. **Başlangıç sayfası** "hub" komut bulmanıza ve proje dosyalarını daha hızlı ihtiyacınız yardımcı olmak için tasarlanmıştır. **Son** projeleri ve klasörleri, çalıştığınız üzerinde son bölümünde görüntülenir. Altında **yeni proje**, ortaya çıkarmak için bir bağlantıya tıklayabilirsiniz **yeni proje** iletişim kutusu veya altında **açın**, bir var olan kod proje veya klasör açabilirsiniz. Sağ tarafta en güncel Geliştirici haberlerini oluşan akışını ' dir.

![Visual Studio'da başlangıç sayfası](media/start-page.png)

Kapatırsanız **başlangıç sayfası** ve tekrar görmek istiyorsanız, buradan yeniden **dosya** menüsü.

![Visual Studio'da Dosya menüsü](media/quickstart-IDE-file-menu-large.png)

::: moniker-end

## <a name="create-a-project"></a>Proje oluşturma

Visual Studio'nun özellikleri keşfetmeye devam etmek için yeni bir proje oluşturalım.

::: moniker range=">=vs-2019"

1. Başlangıç penceresinde, **Yeni proje oluştur**' u seçin ve ardından Proje türleri listesini ad veya dil türünde "JavaScript" içeren olanlarla filtrelemek için **JavaScript** 'teki arama kutusuna yazın.

   Visual Studio, çeşitli yardımcı olacak proje şablonları, hızlı bir şekilde kodlama başlama sağlar. (Alternatif olarak, bir TypeScript geliştiricisiyseniz bu dilde bir proje oluşturmayı ücretsiz olarak kullanabilirsiniz. Biz göz atan kullanıcı Arabirimi için tüm programlama dillerinde benzer.)

   ![Visual Studio başlangıç penceresinde proje şablonları ara](media/vs-2019/create-new-project.png)

1. Boş bir **Node. js web uygulaması** projesi şablonu seçin ve **İleri**' ye tıklayın.

1. Görüntülenen **yeni projeyi Yapılandır** iletişim kutusunda, varsayılan proje adını kabul edin ve **Oluştur**' u seçin.

::: moniker-end

::: moniker range="vs-2017"

1. **Başlangıç sayfasında**, **Yeni proje**altındaki arama kutusuna, proje türleri listesini ad veya dil türlerine "JavaScript" içeren olanlarla filtrelemek için **JavaScript** yazın.

   ![Visual Studio Başlangıç sayfasında Proje şablonlarında Ara](media/start-page-search-templates.png)

   Visual Studio, çeşitli yardımcı olacak proje şablonları, hızlı bir şekilde kodlama başlama sağlar. Boş bir **Node. js web uygulaması** proje şablonu seçin. (Alternatif olarak, bir TypeScript geliştiricisiyseniz bu dilde bir proje oluşturmayı ücretsiz olarak kullanabilirsiniz. Biz göz atan kullanıcı Arabirimi için tüm programlama dillerinde benzer.)

1. İçinde **yeni proje** görüntülenen iletişim kutusunda varsayılan proje adını kabul edin ve **Tamam**.
::: moniker-end

   Proje oluşturulur ve **Düzenleyici** penceresinde *Server.cs* adlı bir dosya açılır. **Düzenleyicisi** dosyaların içeriğini gösterir ve Visual Studio kodlama iş çoğunu burada gerçekleştirirsiniz.

   ![Visual Studio Düzenleyicisi](media/editor.png)

## <a name="solution-explorer"></a>Çözüm Gezgini

**Çözüm Gezgini**, genellikle Visual Studio'nun sağ tarafta olduğu gösterir, dosya ve klasörlerin hiyerarşi grafik gösterimi proje, çözüm veya kod klasörü. Hiyerarşi göz atabilir ve bir dosyaya gidin **Çözüm Gezgini**.

![Visual Studio'daki Çözüm Gezgini'nde](media/quickstart-IDE-solution-explorer.png)

## <a name="menus"></a>Menüler

Visual Studio'nun üst menü çubuğu komutlarını kategoriler halinde gruplandırır. Örneğin, **proje** menüsü, içinde çalışmakta olduğunuz projeye ilgili komutları içerir. Üzerinde **Araçları** menüsünde seçerek Visual Studio nasıl davranacağını özelleştirebileceğiniz **seçenekleri**, veya özelliklerini seçerek yüklemenize ekleyin **araçları ve özellikleri Al**.

![Visual Studio'da menü çubuğu](media/quickstart-IDE-menu-bar.png)

Açalım **hata listesi** penceresini seçerek **görünümü** menüsü, ardından **hata listesi**.

## <a name="error-list"></a>Hata Listesi

**Hata listesi** hata, uyarı ve kodunuzu geçerli durumuna ilişkin ileti gösterir. Hataları (örneğin, bir eksik küme ayracı veya noktalı virgül) dosyanızı veya herhangi bir projeniz varsa, bunlar burada listelenen.

![Visual Studio hata listesi](media/quickstart-IDE-error-list.png)

## <a name="output-window"></a>Çıktı penceresi

**Çıkış** çıkış penceresi şunu gösterir, iletileri projenizi oluşturma ve kaynak denetimi sağlayıcınız.

Şimdi projeyi görmek için bazı derleme çıkışı. Gelen **derleme** menüsünde seçin **Çözümü Derle**. **Çıkış** penceresi otomatik olarak odağa gelir ve derleme başarılı iletisini görüntüler.

![Visual Studio çıktı penceresinde](media/build-output-minimal.png)

## <a name="search-box"></a>Arama kutusu

Arama kutusu, Visual Studio 'da oldukça çok şey yapmanın hızlı ve kolay bir yoludur. Yapmak istediğiniz ilgili metin girebilir ve onu metne ait seçenekler listesini göstereceğiz. Örneğin, tam olarak ne yapı yapıyor ek bilgileri görüntülemek için derleme çıkışın ayrıntı düzeyini artırmak istediğiniz düşünün. İşte, nasıl yapabilir:

1. Arama kutusuna **ayrıntı düzeyi** yazın. Görüntülenen sonuçlardan seçin **projeler ve çözümler--> derleme ve çalıştırma** altında **seçenekleri** kategorisi.

   ![Visual Studio 'da arama kutusu](media/quickstart-IDE-quick-launch.png)

   **Seçenekleri** iletişim kutusu açılır **derleme ve çalıştırma** seçenekler sayfası.

1. Altında **MSBuild proje oluşturması çıkış ayrıntısı**, seçin **Normal**ve ardından **Tamam**.

1. **Çözüm Gezgini** ' de **NodejsWebApp1** projesine sağ tıklayıp bağlam menüsünden **yeniden oluştur** ' u seçerek projeyi yeniden derleyin.

   Bu süre **çıkış** penceresi, hangi dosyalar dahil olmak üzere nerede kopyalanan yapı işleminden daha ayrıntılı günlük kaydı gösterir.

   ![Visual Studio'da ayrıntılı yapı çıktısı](media/build-output-verbose.png)

## <a name="send-feedback-menu"></a>Menü geri bildirim gönder

Visual Studio kullanırken herhangi bir sorunla karşılaşmanız gerekir ya da ürünü geliştirme hakkında önerileriniz varsa, Visual Studio penceresinin en üstündeki **geri bildirim gönder** menüsünü kullanabilirsiniz.

![Visual Studio'da menü geri bildirim gönder](../ide/media/quickstart-ide-send-feedback.png)

## <a name="next-steps"></a>Sonraki adımlar

Visual Studio kullanıcı arabirimi ile tanışın özelliklerinin birkaçı adresindeki inceledik. Daha iyi keşfedilebilmesi için:

> [!div class="nextstepaction"]
> [Kod Düzenleyicisi hakkında bilgi edinin](write-and-edit-code.md)

> [!div class="nextstepaction"]
> [Projeler ve çözümler hakkında bilgi edinin](../get-started/tutorial-projects-solutions.md)

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio IDE genel bakış](../get-started/visual-studio-ide.md)
- [Visual Studio 2017'in daha fazla özellik](../ide/advanced-feature-overview.md)
- [Tema ve yazı tipi renkleri değiştirme](../ide/quickstart-personalize-the-ide.md)
