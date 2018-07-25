---
title: Visual Studio IDE turu
ms.date: 07/12/2018
ms.prod: visual-studio-dev15
ms.technology: vs-ide-general
ms.topic: quickstart
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: aeb7156998b7c6ea91205bd2c05de690b597490a
ms.sourcegitcommit: 8ee7efb70a1bfebcb6dd9855b926a4ff043ecf35
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/17/2018
ms.locfileid: "39081543"
---
# <a name="quickstart-first-look-at-the-visual-studio-ide"></a>Hızlı Başlangıç: Visual Studio IDE ilk bakış

Bu 5-10 dakikalık bir giriş Visual Studio tümleşik geliştirme ortamı (IDE), biz windows, menüler ve diğer kullanıcı Arabirimi özellikleri bazıları ilişkin tura katılın.

Visual Studio henüz yüklemediyseniz, Git [Visual Studio indirmeleri](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017) ücretsiz yüklemek için sayfa.

## <a name="start-page"></a>Başlangıç Sayfası

Visual Studio'yu başlattıktan sonra göreceksiniz ilk şey bir olasılıktır **başlangıç sayfası**. **Başlangıç sayfası** "hub" komut bulmanıza ve proje dosyalarını daha hızlı ihtiyacınız yardımcı olmak için tasarlanmıştır. **Son** projeleri ve klasörleri, çalıştığınız üzerinde son bölümünde görüntülenir. Altında **yeni proje**, ortaya çıkarmak için bir bağlantıya tıklayabilirsiniz **yeni proje** iletişim kutusu veya altında **açın**, bir var olan kod proje veya klasör açabilirsiniz. Sağ tarafta en güncel Geliştirici haberlerini oluşan akışını ' dir.

![Visual Studio'da başlangıç sayfası](media/start-page-dark.png)

Kapatırsanız **başlangıç sayfası** ve tekrar görmek istiyorsanız, buradan yeniden **dosya** menüsü.

![Visual Studio'da Dosya menüsü](media/file-menu-start-page-dark.png)

## <a name="create-a-project"></a>Proje oluşturma

Visual Studio'nun özellikleri keşfetmeye devam etmek için yeni bir proje oluşturalım.

1. Üzerinde **başlangıç sayfası**, arama kutusuna altında **yeni proje**, yazın **konsol** adında içeren "konsol" Bu proje türleri listesini filtrelemek için.

   ![Visual Studio Başlangıç sayfasında Proje şablonlarında Ara](media/start-page-search-templates-dark.png)

   Visual Studio, çeşitli yardımcı olacak proje şablonları, hızlı bir şekilde kodlama başlama sağlar. C# seçin **konsol uygulaması (.NET Framework)** proje şablonu. (Visual Basic, C++, Javascript veya diğer dil Geliştirici kullanıyorsanız alternatif olarak, bir projeyi bu dillerden birinde oluşturun çekinmeyin. Biz göz atan kullanıcı Arabirimi için tüm programlama dillerinde benzer.)

1. İçinde **yeni proje** görüntülenen iletişim kutusunda varsayılan proje adını kabul edin ve **Tamam**.

   Proje oluşturulur ve bir dosya adlı *Program.cs* açılır **Düzenleyicisi** penceresi. **Düzenleyicisi** dosyaların içeriğini gösterir ve Visual Studio kodlama iş çoğunu burada gerçekleştirirsiniz.

   ![Visual Studio Düzenleyicisi](media/editor-dark.png)

## <a name="solution-explorer"></a>Çözüm Gezgini

**Çözüm Gezgini**, genellikle Visual Studio'nun sağ tarafta olduğu gösterir, dosya ve klasörlerin hiyerarşi grafik gösterimi proje, çözüm veya kod klasörü. Hiyerarşi göz atabilir ve bir dosyaya gidin **Çözüm Gezgini**.

![Visual Studio'daki Çözüm Gezgini'nde](media/solution-explorer-console-app-dark.png)

## <a name="menus"></a>Menüler

Visual Studio'nun üst menü çubuğu komutlarını kategoriler halinde gruplandırır. Örneğin, **proje** menüsü, içinde çalışmakta olduğunuz projeye ilgili komutları içerir. Üzerinde **Araçları** menüsünde seçerek Visual Studio nasıl davranacağını özelleştirebileceğiniz **seçenekleri**, veya özelliklerini seçerek yüklemenize ekleyin **araçları ve özellikleri Al**.

![Visual Studio'da menü çubuğu](media/menu-bar-dark.png)

Açalım **hata listesi** penceresini seçerek **görünümü** menüsü, ardından **hata listesi**.

## <a name="error-list"></a>Hata Listesi

**Hata listesi** hata, uyarı ve kodunuzu geçerli durumuna ilişkin ileti gösterir. Hataları (örneğin, bir eksik küme ayracı veya noktalı virgül) dosyanızı veya herhangi bir projeniz varsa, bunlar burada listelenen.

![Visual Studio hata listesi](media/error-list-dark.png)

## <a name="output-window"></a>Çıktı penceresi

**Çıkış** çıkış penceresi şunu gösterir, iletileri projenizi oluşturma ve kaynak denetimi sağlayıcınız.

Şimdi projeyi görmek için bazı derleme çıkışı. Gelen **derleme** menüsünde seçin **Çözümü Derle**. **Çıkış** penceresi otomatik olarak odağa gelir ve derleme başarılı iletisini görüntüler.

![Visual Studio çıktı penceresinde](media/output-window-dark.png)

## <a name="quick-launch"></a>Hızlı Başlat

**Hızlı başlatma** kutusu, kadar her şeyi Visual Studio'da düzgün hızlı ve kolay bir yöntemdir. Yapmak istediğiniz ilgili metin girebilir ve onu metne ait seçenekler listesini göstereceğiz. Örneğin, tam olarak ne yapı yapıyor ek bilgileri görüntülemek için derleme çıkışın ayrıntı düzeyini artırmak istediğiniz düşünün. İşte, nasıl yapabilir:

1. Tür **ayrıntı** içine **hızlı başlatma** kutusu. Görüntülenen sonuçlardan seçin **projeler ve çözümler--> derleme ve çalıştırma** altında **seçenekleri** kategorisi.

   ![Visual Studio'da hızlı başlatma kutusu](media/quick-launch-verbosity-dark.png)

   **Seçenekleri** iletişim kutusu açılır **derleme ve çalıştırma** seçenekler sayfası.

1. Altında **MSBuild proje oluşturması çıkış ayrıntısı**, seçin **Normal**ve ardından **Tamam**.

1. Sağ tıklayarak projeyi yeniden derleyin **ConsoleApp1** projesi **Çözüm Gezgini** seçip **yeniden** bağlam menüsünden.

   Bu süre **çıkış** penceresi, hangi dosyalar dahil olmak üzere nerede kopyalanan yapı işleminden daha ayrıntılı günlük kaydı gösterir.

   ![Visual Studio'da ayrıntılı yapı çıktısı](media/build-output-verbose-dark.png)

## <a name="send-feedback-menu"></a>Menü geri bildirim gönder

Visual Studio kullanıyorsanız ya da ürünün iyileştirilmesine ilişkin önerileriniz varsa, kullanabileceğiniz herhangi bir sorunu karşılaşmamalıdırlar **geri bildirim gönder** Visual Studio penceresinin üst kısmındaki menü yanındaki **hızlı Başlatma** kutusu.

![Visual Studio'da menü geri bildirim gönder](media/send-feedback-dark.png)

## <a name="next-steps"></a>Sonraki adımlar

Visual Studio kullanıcı arabirimi ile tanışın özelliklerinin birkaçı adresindeki inceledik. Daha iyi keşfedilebilmesi için:

- Visual Studio'nun daha kapsamlı bir tura katılın ve hatta hata ayıklama, buna dabble [Visual Studio IDE'ye genel bakış](../ide/visual-studio-ide.md)

- Gözat **genel kullanıcı arabirimi öğeleri** pencereleri hakkında daha fazla derinlik gibi girmeyeceğini VS belgelerinin bölümü [hata listesi](../ide/reference/error-list-window.md), [çıkış penceresine](../ide/reference/output-window.md), [ Özellikler penceresi](../ide/reference/properties-window.md), ve [Seçenekler iletişim kutusu](../ide/reference/options-dialog-box-visual-studio.md)

## <a name="see-also"></a>Ayrıca bkz.

- [Hızlı Başlangıç: IDE'yi kişiselleştirme](../ide/personalizing-the-visual-studio-ide.md)
- [Hızlı Başlangıç: düzenleyicide kod yazma](../ide/quickstart-editor.md)
- [Hızlı Başlangıç: Projeler ve çözümler](../ide/quickstart-projects-solutions.md)