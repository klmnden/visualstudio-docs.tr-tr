---
title: Üretkenlik ipuçları
ms.date: 2/21/2019
ms.topic: conceptual
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: e4f238046e671371a1fe83a3f5b9552b3956be8f
ms.sourcegitcommit: 5b34052a1c7d86179d7898ed532babb2d9dad4a3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2019
ms.locfileid: "69490663"
---
# <a name="productivity-tips-for-visual-studio"></a>Visual Studio için üretkenlik ipuçları

Bu makalelerde, kodunuzu daha hızlı ve verimli bir şekilde yazmanıza, gezinmenize ve hata ayıklamanıza yardımcı olan Visual Studio özelliklerine yönelik ipuçları ele alınmaktadır.

Faydalı klavye kısayolları hakkında daha fazla bilgi için bkz. [üretkenlik kısayolları](../ide/productivity-shortcuts.md). Komut kısayollarının tüm listesi için bkz. [varsayılan klavye kısayolları](../ide/default-keyboard-shortcuts-in-visual-studio.md).

## <a name="write-code"></a>Kod yazma

Aşağıdaki özellikleri kullanarak kod daha hızlı bir şekilde yazın.

- **Kolaylık komutları**. Visual Studio, daha hızlı düzenleme genel görevleri gerçekleştirmenize yardımcı olmak için çeşitli komutlara içerir. Örneğin, bir kod satırını kopyalamak zorunda kalmadan kolayca çoğaltmak için bir komut seçebilirsiniz, imleci yeniden konumlandırabilirsiniz ve yapıştırın. Seçin **Düzenle** > **yinelenen** veya basın **Ctrl**+**E**,**V**. Ayrıca > ,**Gelişmiş** **Genişlet seçimini** **Düzenle**' yi veya**Gelişmiş** > sözleşmeyiDüzenle'yiseçerekbirmetinseçiminihızlıcagenişletebilirveyasözleşmeniz > gerekir >  **Seçim**yapın veya **SHIFT**+**alt** + veyaSHIFT+alt**tuşlarına-** basın. **=** +

- **IntelliSense kullanın**. Düzenleyiciye kod girerken, gibi üyeleri listeleme, parametre bilgisi, hızlı bilgi, imza Yardım ve tam sözcük IntelliSense bilgisi görüntülenir. Bu özellikler, metnin benzer öğe eşleştirmesi destekler; Örneğin, listesi üyeleri için sonuçları listelerini sadece girdiğiniz karakterlerle başlayan girdileri olmakla kalmayıp herhangi bir yerde karakter bileşimini içeren girdileri içerir. Daha fazla bilgi için [kullanım IntelliSense](../ide/using-intellisense.md).

- **Kod girerken IntelliSense seçeneklerini otomatik ekleme değiştirme**. IntelliSense Öneri moduna çevirirseniz, IntelliSense seçeneklerini sadece açıkça bunları seçerseniz eklenmiş olduğunu belirtebilirsiniz.

     Öneri modunu etkinleştirmek için seçin **Ctrl**+**Alt**+**boşluk** anahtarları veya menü çubuğunda, **Düzenle**  >  **IntelliSense** > **tamamlama modunu Değiştir**.

- **Kod parçacıkları kullanma**. Yerleşik parçacıkları kullanabilir veya kendi parçacıklarınızı oluşturabilirsiniz.

     Menü çubuğunda bir parçacık eklemek için seçin **Düzenle** > **IntelliSense** > **parçacık Ekle** veya **Surround With**, veya bir dosyada kısayol menüsünü açın ve seçin **kod parçacığı** > **parçacık Ekle** veya **Surround With**. Daha fazla bilgi için [kod parçacıkları](../ide/code-snippets.md).

- **Kod hatalarını satır içi düzeltme**. Hızlı Eylemler, kolayca yeniden düzenleme sağlar, oluşturmak veya aksi halde kodu tek eylemle değiştirin. Tornavida kullanarak bu eylemleri uygulanabilir ![tornavida simgesi](media/screwdriver-icon.png) ya da ampul ![ampul](media/light-bulb-icon.png) simgeleri veya basarak **Alt** +  **Girin** veya **Ctrl**+ **.** imlecinizi, üzerinde uygun kod satırının olduğunda. Bkz: [hızlı Eylemler](quick-actions.md) daha fazla bilgi için.

- **Gösterme ve bir kod öğesinin tanımını Düzenle**. Hızlı bir şekilde gösterebilir ve bir üyesi, bir değişken veya yerel olarak gibi bir kod öğe tanımlandığı modülü Düzenle.

    Açılır pencerede bir tanımı açmak için öğeyi vurgulayın ve ardından **Alt**+**F12** anahtarları veya öğe için kısayol menüsünü açın ve ardından **göz at Tanım**. Ayrı bir kod penceresinde bir tanımı açmak için öğe için kısayol menüsünü açın ve ardından **Tanıma Git**.

- **Örnek uygulamaları kullanın**. Örnek uygulamalardan yükleyip tarafından uygulama geliştirmenizi hızlandıracak [Microsoft Developer Network](https://code.msdn.microsoft.com/). İndirerek ve örnek paketi o alan için keşfetmek, belirli bir teknoloji veya programlama konsepti öğrenebilirsiniz.

## <a name="navigate-within-your-code"></a>Kodunuzun içinde gezinme

Kodunuzda belirli konumları daha hızlı hareket ettirin ve bulmak için çeşitli teknikler kullanabilirsiniz.

- **Kod satırlarını yer işareti**. Belirli bir dosyaya kod satırlarını hızla gitmek için yer işaretlerini kullanabilirsiniz.

    Menü çubuğunda bir yer işareti koymak için **Düzenle** > **yer işaretleri** > **yer işaretini Değiştir**. Tüm yer işaretlerini bir çözüm için görüntüleyebileceğiniz **yer işaretleri** penceresi. Daha fazla bilgi için [kodda yer işaretleri ayarlama](../ide/setting-bookmarks-in-code.md).

- **Bir dosyada sembol tanımlarını arama**. Bir çözüm içinde Sembol tanımlarını ve dosya adlarını konumlandırmak için arama yapabilirsiniz ancak arama sonuçları ad veya yerel değişkenleri içermez.

   Menü çubuğunda, bu özelliğe erişmek için seçin **Düzenle** > **gitmek için**.

- **Kodunuzun genel yapısına gözatın**. İçinde **Çözüm Gezgini**, arama ve sınıfları ve türleri ve üyeleri, projelerinizde göz atın. Ayrıca arama, bir yöntemin çağrı hiyerarşisini görüntülemek simge başvurularını bulmak ve diğer görevleri gerçekleştirebilirsiniz. İçinde bir kod elemanını seçerseniz **Çözüm Gezgini**, ilişkili dosya açılır bir **Önizleme** sekmesi ve dosyanın içindeki öğeye işaretçi taşır. Daha fazla bilgi için [kod yapısını görüntüleme](../ide/viewing-the-structure-of-code.md).

## <a name="find-items-faster"></a>Öğeleri daha hızlı bulun

Komutlar, dosyalar ve Seçenekler, yalnızca geçerli görevinize ilgili bilgileri göstermek için araç pencerelerinin içeriğini filtre ek olarak IDE içinde arama yapabilirsiniz.

- **Araç pencerelerinin içeriğini filtre**. Aşağıdakiler gibi birçok araç pencerelerinin içeriğini içinde arama yapabilirsiniz **araç kutusu**, **özellikleri** penceresinde ve **Çözüm Gezgini**, ancak görüntü yalnızca, adları öğeler Belirttiğiniz karakterler içeriyor.

- **Yalnızca istediğiniz hataları görüntülemek adresine**. Seçerseniz **filtre** düğmesini **hata listesi** araç çubuğu içinde görünen hata sayısını azaltabilirsiniz **hata listesi** penceresi. Yalnızca hataları, düzenleyicide açık olan dosyalardaki yalnızca geçerli dosyadaki hataları veya yalnızca geçerli projedeki hataları görüntüleyebilirsiniz. İçinde arama yapabilirsiniz **hata listesi** belirli hataları bulmak için penceresi.

- **İletişim kutularını, menü komutlarını, seçenekleri ve daha fazlasını bulun**. Arama kutusuna bulmaya çalıştığınız öğeler için anahtar sözcükler veya ifadeler girin. Örneğin, **Yeni proje**girdiğinizde aşağıdaki seçenekler görüntülenir:

   ::: moniker range="vs-2017"

   !['Yeni project' hızlı başlatma sonuçları](../ide/media/productivity_quicklaunch.png)

   **Hızlı başlatma** , yeni bir proje oluşturmak, projeye yeni bir öğe eklemek ve **Seçenekler** Iletişim kutusundaki **Projeler ve çözümler** sayfasına diğerleri arasında bağlantılar görüntüler. Arama sonuçları, proje dosyalarını ve araç pencerelerini de içerebilir.

   ::: moniker-end

   ::: moniker range=">=vs-2019"

   ![' Yeni proje ' için arama sonuçları](../ide/media/vs-2019/productivity-quick-launch-new-project.png)

   ::: moniker-end

   Doğrudan arama kutusuna gitmek için **CTRL**+**Q** tuşlarına basın.

## <a name="debug-code"></a>Kodda hata ayıklama

Hata ayıklama çok zaman kullanabilir, ancak aşağıdaki ipuçları yardımcı olabilir sürecinize hız.

- **Sayfa, uygulama veya siteyi farklı tarayıcılarda test etme**. Kodunuzdaki hataları ayıklamanıza gibi dahil olmak üzere yüklü web tarayıcıları arasında kolayca geçiş yapabilirsiniz [sayfa denetçisi (Visual Studio)](https://msdn.microsoft.com/Library/65880969-1ad2-47be-85b9-bb12c81bf209), açmak zorunda kalmadan **şununla Gözat** iletişim kutusu. Kullanabileceğiniz **hata ayıklama hedefi** üzerinde olan liste **standart** yanındaki araç **hata ayıklamayı Başlat** düğme, hızlı bir şekilde hata ayıklama gibi kullanarak kullandığınız tarayıcıyı doğrulamak için veya sayfaları görüntüleyin.

    ![Web tarayıcı hata ayıklama seçenekleri seçin](../ide/media/webbrowserdropdowntoolbar.png)

- **Geçici kesme noktalarını ayarlayın**. Geçerli kod satırında geçici bir kesme noktası oluşturabilir ve aynı anda hata ayıklayıcıyı başlatın. Kodun o satırına isabet ettiğinde, hata ayıklayıcı kesme moduna girer. Daha fazla bilgi için [hata ayıklayıcısı ile kodlarda gezinme](../debugger/navigating-through-code-with-the-debugger.md).

    Bu özelliği kullanmayı tercih **Ctrl**+**F10** anahtarları veya Kes ve ardından istediğiniz kod satırı için kısayol menüsünü açın **imlece** .

- **Hata ayıklama sırasında yürütme noktasını taşımak**. Geçerli yürütme noktasını farklı bir bölüme taşımak ve hata ayıklamaya bu noktadan yeniden başlatın. Bu teknik, bu bölüme erişmek için gerekli tüm adımları yeniden oluşturmak zorunda kalmadan kodun bir bölümünü hata ayıklamak istiyorsanız kullanışlıdır. Daha fazla bilgi için [hata ayıklayıcısı ile kodlarda gezinme](../debugger/navigating-through-code-with-the-debugger.md).

     Yürütme noktasını taşımak için sarı ok başını, aynı dosya içinde sonraki deyimi ayarlayın ve ardından istediğiniz konuma sürükleyin **F5** hata ayıklamaya devam etmek için anahtarı.

- **Değişkenler için değer bilgilerini yakalama**. Kodunuzda bir değişkene bir DataTip eklemek ve hata ayıklama işlemini tamamladıktan sonra değişkenin son bilinen değerini erişebilmesi için sabitleyin. Daha fazla bilgi için [veri İpuçlarında veri değerlerini görüntüleme](../debugger/view-data-values-in-data-tips-in-the-code-editor.md).

     Bir DataTip eklemek için hata ayıklayıcının kesme modunda olması gerekir. Değişkenin üzerine imleci yerleştirin ve ardından görünen DataTip üzerinde görünen pin düğmesini seçin. Hata ayıklama durdurulduğunda, değişkeni içeren kod satırının yanındaki kaynak dosyada bir mavi iğne simgesi görüntülenir. Mavi işaret ederseniz, en son hata ayıklama oturumu değişkenin değeri görüntülenir.

- **Anlık pencereyi temizleme**. İçeriklerini silebilirsiniz [komut penceresi](../ide/reference/immediate-window.md) girerek tasarım zamanında `>cls` veya `>Edit.ClearAll`

     Ek komutlar hakkında daha fazla bilgi için bkz. [Visual Studio komut diğer adları](../ide/reference/visual-studio-command-aliases.md).

## <a name="access-visual-studio-tools"></a>Erişim Visual Studio Araçları

Başlat menüsünü ya da görev için sabitlerseniz Geliştirici komut istemi veya başka bir Visual Studio araç hızlı şekilde erişebilirsiniz.

::: moniker range="vs-2017"

1. Windows Gezgini 'nde *%ProgramData%\Microsoft\Windows\Start Menu\Programs\Visual Studio 2017 \ Visual Studio Araçları*konumuna gidin.

::: moniker-end

::: moniker range=">=vs-2019"

1. Windows Gezgini 'nde *%ProgramData%\Microsoft\Windows\Start Menu\Programs\Visual Studio 2019 \ Visual Studio Araçları*konumuna gidin.

::: moniker-end

2. Sağ tıklayın veya bağlam menüsünü **Geliştirici komut istemi**ve ardından **Başlangıç ekranına Sabitle** veya **görev çubuğuna Sabitle**.

## <a name="manage-files-toolbars-and-windows"></a>Dosyaları araç çubuklarını ve windows yönetme

Herhangi bir anda, birden fazla kod dosyasında çalışma ve uygulama geliştirme gibi birçok araç pencereleri arasında taşınması. Aşağıdaki ipuçlarını kullanarak düzeninizi izleyebilirsiniz:

- **Sık kullandığınız dosyaları düzenleyicide görünür tutma**. İyi kaç dosya düzenleyicide açık olduğundan bağımsız olarak görünür kalır dosyaları sekmenin sol tarafına sabitleyebilirsiniz.

   Bir dosyayı sabitlemek için dosyanın sekmesini seçin ve ardından **Pin durumunu değiştir** düğmesi.

- **Belgeleri ve dokümanları diğer monitörlere taşıma**. Uygulama geliştirirken birden fazla monitör kullanıyorsanız, başka bir monitöre düzenleyicide açık olan dosyaları taşıyarak uygulamanızın bölümleri üzerinde daha kolay çalışabilirsiniz. Başka bir izleme ve sekme için hata ayıklayıcı windows gibi araç pencereleri birlikte "rafts" oluşturmak için belge ve araç pencerelerini sabitlemek taşıyabilirsiniz Daha fazla bilgi için [Visual Studio'da pencere düzenlerini özelleştirme](../ide/customizing-window-layouts-in-visual-studio.md).

   Ayrıca dosyaları daha kolay başka bir örneğini oluşturarak yönetebilirsiniz **Çözüm Gezgini** ve başka bir monitöre taşıyarak. Başka bir örneğini oluşturmak için **Çözüm Gezgini**, bir kısayol menüsünü açıp **Çözüm Gezgini**ve ardından **Yeni Çözüm Gezgini görünümü**.

- **Visual Studio'da görünen yazı tiplerini özelleştirme**. Yazı tipi, boyutu ve IDE içindeki metin için kullanılan rengi değiştirebilirsiniz. Örneğin, düzenleyici ve araç pencerelerini veya IDE boyunca yazı tipini belirli kod öğelerinin rengini özelleştirebilirsiniz. Daha fazla bilgi için [nasıl yapılır: Yazı tiplerini ve renkleri](../ide/how-to-change-fonts-and-colors-in-visual-studio.md) değiştirin [ve şunları yapın: Düzenleyicideki](../ide/reference/how-to-change-fonts-and-colors-in-the-editor.md)yazı tiplerini ve renkleri değiştirin.

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio ipuçları ve püf noktaları blog gönderisi](https://devblogs.microsoft.com/visualstudio/visual-studio-tips-and-tricks/)
- [Sık kullanılan komutlar için varsayılan klavye kısayolları](../ide/default-keyboard-shortcuts-for-frequently-used-commands-in-visual-studio.md)
- [Nasıl yapılır: Menüleri ve araç çubuklarını özelleştirme](../ide/how-to-customize-menus-and-toolbars-in-visual-studio.md)
- [İzlenecek yol: Basit bir uygulama oluşturma](../get-started/csharp/tutorial-wpf.md)
- [Erişilebilirlik ipuçları ve püf noktaları](../ide/reference/accessibility-tips-and-tricks.md)
