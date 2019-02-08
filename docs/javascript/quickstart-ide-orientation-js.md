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
ms.openlocfilehash: c1bac4ba3e929da9ad6f22666c6a6b3f71b288c0
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55920055"
---
# <a name="first-look-at-the-visual-studio-ide"></a>Visual Studio IDE’ye ilk bakış

Bu 5-10 dakikalık bir giriş Visual Studio tümleşik geliştirme ortamı (IDE), biz windows, menüler ve diğer kullanıcı Arabirimi özellikleri bazıları ilişkin tura katılın.

Visual Studio henüz yüklemediyseniz, Git [Visual Studio indirmeleri](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2017) ücretsiz yüklemek için sayfa.

## <a name="start-page"></a>Başlangıç Sayfası

Visual Studio'yu başlattıktan sonra göreceksiniz ilk şey bir olasılıktır **başlangıç sayfası**. **Başlangıç sayfası** "hub" komut bulmanıza ve proje dosyalarını daha hızlı ihtiyacınız yardımcı olmak için tasarlanmıştır. **Son** projeleri ve klasörleri, çalıştığınız üzerinde son bölümünde görüntülenir. Altında **yeni proje**, ortaya çıkarmak için bir bağlantıya tıklayabilirsiniz **yeni proje** iletişim kutusu veya altında **açın**, bir var olan kod proje veya klasör açabilirsiniz. Sağ tarafta en güncel Geliştirici haberlerini oluşan akışını ' dir.

![Visual Studio'da başlangıç sayfası](media/start-page.png)

Kapatırsanız **başlangıç sayfası** ve tekrar görmek istiyorsanız, buradan yeniden **dosya** menüsü.

![Visual Studio'da Dosya menüsü](media/quickstart-IDE-file-menu-large.png)

## <a name="create-a-project"></a>Proje oluşturma

Visual Studio'nun özellikleri keşfetmeye devam etmek için yeni bir proje oluşturalım.

1. Üzerinde **başlangıç sayfası**, arama kutusuna altında **yeni proje**, yazın **javascript** adında "javascript" içeren bu proje türleri listesini filtrelemek için veya Dil türü.

   ![Visual Studio Başlangıç sayfasında Proje şablonlarında Ara](media/start-page-search-templates.png)

   Visual Studio, çeşitli yardımcı olacak proje şablonları, hızlı bir şekilde kodlama başlama sağlar. Seçin bir **boş Node.js Web uygulaması** proje şablonu. (TypeScript geliştiricisiyseniz, alternatif olarak, o dilde bir proje oluşturmak çekinmeyin. Biz göz atan kullanıcı Arabirimi için tüm programlama dillerinde benzer.)

1. İçinde **yeni proje** görüntülenen iletişim kutusunda varsayılan proje adını kabul edin ve **Tamam**.

   Proje oluşturulur ve bir dosya adlı *server.cs* açılır **Düzenleyicisi** penceresi. **Düzenleyicisi** dosyaların içeriğini gösterir ve Visual Studio kodlama iş çoğunu burada gerçekleştirirsiniz.

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

## <a name="quick-launch"></a>Hızlı Başlat

**Hızlı başlatma** kutusu, kadar her şeyi Visual Studio'da düzgün hızlı ve kolay bir yöntemdir. Yapmak istediğiniz ilgili metin girebilir ve onu metne ait seçenekler listesini göstereceğiz. Örneğin, tam olarak ne yapı yapıyor ek bilgileri görüntülemek için derleme çıkışın ayrıntı düzeyini artırmak istediğiniz düşünün. İşte, nasıl yapabilir:

1. Tür **ayrıntı** içine **hızlı başlatma** kutusu. Görüntülenen sonuçlardan seçin **projeler ve çözümler--> derleme ve çalıştırma** altında **seçenekleri** kategorisi.

   ![Visual Studio'da hızlı başlatma kutusu](media/quickstart-IDE-quick-launch.png)

   **Seçenekleri** iletişim kutusu açılır **derleme ve çalıştırma** seçenekler sayfası.

1. Altında **MSBuild proje oluşturması çıkış ayrıntısı**, seçin **Normal**ve ardından **Tamam**.

1. Sağ tıklayarak projeyi yeniden derleyin **NodejsWebApp1** projesi **Çözüm Gezgini** seçip **yeniden** bağlam menüsünden.

   Bu süre **çıkış** penceresi, hangi dosyalar dahil olmak üzere nerede kopyalanan yapı işleminden daha ayrıntılı günlük kaydı gösterir.

   ![Visual Studio'da ayrıntılı yapı çıktısı](media/build-output-verbose.png)

## <a name="send-feedback-menu"></a>Menü geri bildirim gönder

Visual Studio kullanıyorsanız ya da ürünün iyileştirilmesine ilişkin önerileriniz varsa, kullanabileceğiniz herhangi bir sorunu karşılaşmamalıdırlar **geri bildirim gönder** Visual Studio penceresinin üst kısmındaki menü yanındaki **hızlı Başlatma** kutusu.

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
