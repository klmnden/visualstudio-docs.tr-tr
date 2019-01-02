---
title: Program hataları düzeltin ve kod geliştirin
description: Bu makalede, Visual Studio hata ayıklama araçları ve birim testleri, derleme hataları dahil olmak üzere, kodunuzda, Kod Analizi sorunlarını düzeltilmesine yardımcı olabilir bazı temel yolu anlatılmaktadır.
ms.date: 05/02/2018
ms.prod: visual-studio-dev15
ms.topic: conceptual
ms.assetid: c3a14d28-d811-4ff3-bd09-21dce14025ca
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: e61c5917ee3d77161c31213d4851472e714d1679
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53940183"
---
# <a name="make-code-work-in-visual-studio"></a>Kodu Visual Studio'da çalışma

Visual Studio projeyi derleme ve hata ayıklama araçları, güçlü tümleşik sunmaktadır. Bu makalede, Visual Studio nasıl artıracağını hata ayıklama araçları kullanarak yapı çıktı, kodunuzda Kod Analizi sorunlarını bulmak ve birim testlerini bulun.

Düzenleyicisini verdi ve bazı kod oluşturulan. Artık, kod düzgün çalıştığından emin olmanız gerekir. Visual Studio'da çoğu ıde'lerle gibi kod çalışması için iki aşama vardır: catch ve proje ve derleme hatalarını gidermek için kodu derleme ve çalışma zamanı ve dinamik hatalarını bulmak için kodu çalıştıran.

## <a name="build-your-code"></a>Kodunuzu oluşturma

İki temel tür yapı yapılandırması vardır: **Hata ayıklama** ve **yayın**. **Hata ayıklama** yapılandırma daha zengin bir etkileşimli çalışma zamanı hata ayıklama deneyimi için izin veren bir yavaş, daha büyük yürütülebilir üretir. **Hata ayıklama** yürütülebilir hiçbir zaman gönderilmemelidir. **Yayın** yapılandırmayı oluşturmak uygun olan daha hızlı ve en iyi duruma getirilmiş bir yürütülebilir oluşturur (en az derleyici perspektifinden). Varsayılan yapı yapılandırma **hata ayıklama**.

Projenizi yapılandırmak için en kolay yolu basmaktır **F7**, ancak yapı seçerek de başlatabilirsiniz **derleme** > **Çözümü Derle** ana menüden.

![Visual Studio derleme Proje menüsünde Seçimi](../ide/media/vs_ide_gs_debug_build_menu_item.png)

Derleme işleminde inceleyebileceğiniz **çıkış** penceresinin altındaki Visual Studio kullanıcı arabirimi. Hataları, uyarıları ve yapı işlemleri burada görüntülenir. Hata (veya yapılandırılan bir düzey uyarılar olup olmadığını) varsa, yapı başarısız olur. Hataları ve Uyarıları nerede oluştuğunu satıra gitmek için tıklayabilirsiniz. Projenizi yeniden derleyin ya basarak **F7** yeniden (yalnızca dosyalar hatalarla yeniden derlemek için) veya **Ctrl**+**Alt**+**F7**  (için bir temiz ve tam yeniden derleme).

Düzenleyici aşağıdaki sonuçları penceresinde iki sekmeli pencere vardır: **çıkış** içeriyor (hata iletileri de dahil olmak üzere) çıktı; ham derleyici penceresinde ve **hata listesi** sağlayan penceresini bir sıralanabilir ve filtrelenebilir listesi tüm hataları ve Uyarıları.

Derleme başarılı olduğunda bu sonuçları görmek **çıkış** penceresi:

![Visual Studio başarılı derleme çıkış](../ide/media/vs_ide_gs_debug_success_build.png)

## <a name="review-the-error-list"></a>Hata listesini gözden geçirin

Daha önce ve başarıyla derlenen kod için herhangi bir değişiklik yapmış olduğunuz sürece, muhtemelen bir hata vardır. Kodlamaya yeniyseniz, muhtemelen bunlardan çok fazla vardır. Hataları bazen basit söz dizimi hatası veya yanlış bir değişken adı gibi belirgin olan ve bazen, size yol göstermesi için yalnızca bir şifreli koduyla anlaşılması zor olan. Sorunların daha net bir görünüm için derleme alt kısmına gidin **çıkış** pencere seçeneğine tıklayıp **hata listesi** sekmesi. Projeniz için uyarıları ve hataları daha düzenli bir görünümünü götürür ve bazı ek seçenekler de sunar.

![Visual Studio çıktı ve hata listesi](../ide/media/vs_ide_gs_debug_bad_build_error_list.png)

Hata satırında tıklayın **hata listesi** penceresi hata satırına gitmek oluşuyor. (Veya tıklayarak satır numaralarını Aç **hızlı başlatma** "satır numaralarını" içine yazarak ve basarak dokunun, çubuğunda **Enter**. Bu ulaşmak için en hızlı yoludur **seçenekleri** Burada, kapatabilir satır numaralarını iletişim. Kullanmayı öğrenme **hızlı başlatma** çubuk ve kendiniz çok sayıda UI tıklama Kaydet!)

![Satır numaraları ile Visual Studio Düzenleyicisi](../ide/media/vs_ide_gs_debug_line_numbers.png)

![Visual Studio satır numaralarını seçeneği](../ide/media/vs_ide_gs_debug_options_line_numbers.png)

Tuşuna **Ctrl**+**G** hızla hatanın gerçekleştiği satır numarası atlamak için.

Hata, kırmızı bir "dalgalı çizgi" alt çizgi ile tanımlanır. Üzerinde ek detaylar için üzerine gelin. Düzeltme yapmak ve yeni bir hata düzeltmesi yükleyebilecek olsa da çalıştırmayı, geçer. (Bu bir "regresyon" olarak adlandırılır.)

![Visual Studio hata üzerine gelme](../ide/media/vs_ide_gs_debug_error_hover1.png)

Hata listesi izlemek ve kodunuzda tüm hatalarla ilgilenin.

![Visual Studio hata ayıklama hataları penceresi](../ide/media/vs_ide_gs_debug_error_list.png)

### <a name="review-errors-in-detail"></a>Ayrıntılı hataları gözden geçirin

Birçok hatayı yok, derleyicinin koşullarını oldukları gibi tümcecik oluşturulmuş mantıklı olabilir. Bu gibi durumlarda, ek bilgi gerekir. Gelen **hata listesi** penceresi, hata veya uyarı hakkında daha fazla bilgi için otomatik bir Bing arama yapabilirsiniz. Karşılık gelen giriş satırına sağ tıklayıp **hata yardımını göster** bağlam menüsünden veya köprülü hata kodu değeri tıklatın **kod** sütununun **hatalistesi**.

![Visual Studio hata listesi Bing arama](../ide/media/vs_ide_gs_debug_error_list_error_help.png)

Ayarlarınıza bağlı olarak, web tarayıcınızın hata kodu ve metin için arama sonuçlarını görüntüler veya bir sekme Visual Studio içinde açılır ve Bing arama sonuçları gösterilmektedir. Internet'teki birçok farklı kaynaklardan sonuçları olan ve tüm yararlı olabilir.

## <a name="use-code-analysis"></a>Kod Analizi kullanma

Kod Çözümleyicileri çalışma zamanı hatalarına yol açabilir ortak kod sorunları veya sorunları kod Yönetimi'nde arayın.

### <a name="c-and-visual-basic-code-analysis"></a>C#ve Visual Basic kod analizi

Visual Studio 2017'yi içeren yerleşik bir dizi [.NET derleyici platformu Çözümleyicileri](../code-quality/roslyn-analyzers-overview.md) , inceleyin C# ve yazarken Visual Basic kod yazın. Visual Studio uzantısı olarak veya bir NuGet paketi olarak ek Çözümleyicileri yükleyebilirsiniz. Kural ihlallerinin bulunamazsa, hem bir dalgalı ve sorunlu kod altında olarak kod düzenleyicisinde bildirilirken **hata listesi**.

### <a name="c-code-analysis"></a>C++ Kod Analizi

C++ kodunu analiz etmek için çalıştırma [statik kod analizi](../code-quality/quick-start-code-analysis-for-c-cpp.md). Başarılı bir derleme önlemek ve onu üretebilir uyarıları gidermek için biraz zaman alabilir belirgin hataları temizledikten sonra çalışan alýþkanlýk alın. Kendiniz yol aşağı bazı zorlukların kurtulmuş olursunuz ve birkaç kod stili teknikleri öğrenin.

Tuşuna **Alt**+**F11** (veya **Çözümle** > **çözüm üzerinde kod analizini Çalıştır** üstteki menüden) için statik kod analizi başlatın.

![Visual Studio Kod Analizi menü öğesi](../ide/media/vs_ide_gs_debug_run_code_analysis.png)

Tüm yeni veya güncelleştirilmiş uyarı görünür **hata listesi** IDE alt kısmındaki sekme. Uyarılar için kodda atlamak için tıklayın.

![Visual Studio hata listesinde uyarılar ile](../ide/media/cpp-code-analysis-warning.png)

## <a name="use-light-bulbs-to-fix-or-refactor-code"></a>Kodu yeniden düzenleyin veya ampuller kullanın

[Hızlı Eylemler](../ide/quick-actions.md)tornavida simgesine ya da ampul erişilebilir let satır içi kodu yeniden düzenleyin. Genel uyarıları gidermek için kolay bir yol oldukları hızla ve etkili bir şekilde de C#, C++ ve Visual Basic kodu. Bunlara erişmek için bir uyarı dalgalı oku üzerinde sağ tıklayıp **hızlı Eylemler ve yeniden düzenlemeler**. Veya imlecinizi renkli dalgalı çizgi içeren satırda olduğunda basın **Ctrl**+**.** veya kenar boşluğunda ampul veya tornavida simgesini seçin. Olası düzeltmeleri veya yeniden düzenlemeler, bu kod satırı için uygulayabileceğiniz bir listesini görürsünüz.

![Visual Studio ampul Önizleme](../ide/media/quick-actions-options.png)

Hızlı Eylemler, kod Çözümleyicileri, yeniden düzenleme, düzeltin veya kodunuzu geliştirmek için bir fırsat olup belirlemek her yerde kullanılabilir. Herhangi bir kod satırında, bağlam menüsünü açmak için sağ tıklayın ve seçin **hızlı Eylemler ve yeniden düzenlemeler**. Yeniden düzenleme ve geliştirme seçenekleri kullanılabilir ise bunlar görüntülenir. Aksi takdirde, iletinin **hiçbir hızlı Eylemler kullanılabilir burada** IDE'nin sol alt köşesinde görüntülenir.

![Hızlı Eylemler kullanılabilir metni yok](../ide/media/vs_ide_gs_debug_light_bulb_no_options.png)

Deneyimiyle hızlı bir şekilde ok tuşlarını kullanabilirsiniz ve **Ctrl**+**.** Denetlenecek kodunuzu kolay fırsatları yeniden düzenleme ve temiz yukarı!

## <a name="debug-your-running-code"></a>Çalışan kodda hata ayıklama

Sizin başarıyla kodunuzu derleyip biraz temizleme gerçekleştirilen göre çalıştırın tuşlarına basarak **F5** veya seçerek **hata ayıklama** > **hata ayıklamayı Başlat**. Ayrıntılı davranışını görebilirsiniz. Bu nedenle bu bir hata ayıklama ortamında uygulamanızı başlatır. Visual Studio IDE değişiklikleri uygulamanız çalışırken: **çıkış** penceresi (varsayılan yapılandırmasında pencere), iki yeni etiketler ile değiştirilir **Yereller/değişkenler/Watch** sekmeli pencere ve **Çağrı yığını/kesme noktaları/özel durum ayarları/çıkış** sekmeli pencere. Bu windows inceleyin ve çalıştırdığı gibi uygulamanızın değişkenleri, iş parçacıkları, çağrı yığınları ve diğer çeşitli davranışların değerlendirme olanak tanıyan birden fazla sekme vardır.

![Visual Studio Otolar ve çağrı yığını Windows](../ide/media/vs_ide_gs_debug_autos_and_call_stack.png)

Tuşuna basarak uygulamanızı durdurmak **Shift**+**F5** veya tıklayarak **Durdur** düğmesi. Veya yalnızca uygulamanın ana penceresi (veya komut satırı iletişim) kapatabilirsiniz.

Kodunuzu mükemmel çalıştırdıysanız ve tam olarak bekleniyordu, Tebrikler! Ancak, askıda kalma, veya kilitlenmiş veya bazı ilginç sonuçlar verdiğiniz, bu sorunların kaynağını bulun ve hataları düzeltmek gerekir.

### <a name="set-simple-breakpoints"></a>Basit kesme noktaları belirleyin

[Kesme noktaları](../debugger/using-breakpoints.md) güvenilir hata ayıklama en temel ve gerekli bir özelliktir. Bir kesme noktası değişkenlerin değerleri veya bellek davranışını göz olabilmesi için Visual Studio çalışan kodunuzu nereye askıya almanız ya da bir dal kod getting run olup olmadığını gösterir. Bir projeyi ayarlama ve kesme noktaları kaldırma sonrasında yeniden gerek yoktur.

Kesme oluşur veya istediğiniz kadar kenar boşluğunu satırının tıklayarak bir kesme noktası ayarlamak **F9** geçerli kod satırında bir kesme noktası ayarlamak için. Kodunuzu çalıştırmak, Duraklat (veya *sonu*) yönergeleri için bu kod satırı yürütülmeden önce.

![Visual Studio kesme noktası](../ide/media/vs_ide_gs_debug_breakpoint1.png)

Kesme noktaları için yaygın kullanımları şunlardır:

- Bir kilitlenme veya kapanma kaynağını daraltmak için kesme noktaları boyunca ve hataya neden olduğunu düşündüğünüz yöntem çağrısının kod etrafında dağılım. Siz hata ayıklayıcıda kod çalıştırma, kaldırmak ve kod geçemediğinde bulana kadar yakın kesme noktaları birlikte sıfırlayın. Hata ayıklayıcıda kod çalıştırma hakkında bilgi edinmek için sonraki bölüme bakın.

- Yeni kod yapılırsa, başında, bir kesme noktası ayarlayın ve beklendiği gibi davrandığından emin olmak için kodu çalıştırın.

- Karmaşık bir davranış uyguladık, program böldüğünde veri ve değişken değerlerini inceleyebilirsiniz. Bu nedenle algoritmik kodu için kesme noktaları ayarlayın.

- Bunu C veya C++ koduna kodunu durdurmak için kullanım kesme noktaları yazıyorsanız, bellekle ilgili hataları için hata ayıklama sırasında adres değerlerini (NULL arayın) ve başvuru sayısı inceleyebilirsiniz.

Kesme noktaları kullanma hakkında daha fazla bilgi için okuma [kesme noktalarını kullanma](../debugger/using-breakpoints.md).

### <a name="inspect-your-code-at-run-time"></a>Çalışma zamanında kodunuzu inceleyin

Çalışan kodunuz bir kesme noktası ve duraklatmalarının ulaştığında, sarı (geçerli deyim) ile işaretlenmiş bir kod satırının henüz yürütüldü değil. Bu noktada, geçerli deyimi yürütün ve sonra değiştirilmiş değerleri incelemek isteyebilirsiniz. Birkaç kullanabileceğiniz *adım* hata ayıklayıcıda kod yürütmek için komutları. Bir yöntem çağrısının işaretlenmiş kod ise, içine tuşlarına basarak adım **F11**. Ayrıca *atla* tuşuna basarak kod satırının **F10**. Ek komutlar ve kodunuz içinde adım adım hakkında ayrıntılı bilgi için okuma [hata ayıklayıcısı koda gitmek](../debugger/navigating-through-code-with-the-debugger.md).

![Visual Studio çalışma zamanı değerlerini İnceleme](../ide/media/vs_ide_gs_debug_hit_breakpoint.png)

Önceki çizimde, hata ayıklayıcı bir deyim ya da tuşlarına basarak ilerletebilirsiniz **F10** veya **F11** (hiçbir metot çağrısı olduğundan, her iki komut aynı sonucu sahip).

Hata Ayıklayıcı duraklatılmış durumdayken, değişkenlerinizi inceleyin ve neler olduğunu belirlemek için yığınları çağırın. Görmeyi beklediğiniz aralıklara değerler? Aramalar doğru sırada yapılır?

![Visual Studio çalışma zamanı değerlerini İnceleme](../ide/media/vs_ide_gs_debug_inspect_value.png)

Geçerli değerini ve başvuruları görmek için bir değişken üzerinde gezdirin. Beklemediğiniz bir değer görürseniz, muhtemelen önceki veya çağıran koddaki bir hata vardır. Daha fazla ayrıntılı hata ayıklama bilgi [daha fazla bilgi edinin](../debugger/debugger-feature-tour.md) hata ayıklayıcıyı kullanma hakkında.

Ayrıca, Visual Studio görüntüler **tanılama araçları** penceresi, burada, gözlemleyin uygulamanızın CPU ve bellek kullanımının zaman içinde. Daha sonra uygulama geliştirme, beklenmeyen yoğun CPU kullanımı veya bellek ayırma için aramak için bu araçları kullanabilirsiniz. İle birlikte kullanmak **Watch** penceresi ve hangi beklenmeyen, yoğun kullanım veya yayımlanmamış kaynak neden olduğunu belirlemek için kesme noktaları. Daha fazla bilgi için [profil oluşturma özelliği Turu](../profiling/profiling-feature-tour.md).

## <a name="run-unit-tests"></a>Birim testleri çalıştırma

Doğru yapıldığında, bunlar tek bir kod, genellikle tek bir işlev, "Birim" test ve hata ayıklama tam programınızı kolaydır, birim testlerini kod hataları karşı savunması kodunuzun ilk satırını olduğu. Visual Studio, hem yönetilen hem de yerel kod için Microsoft birim testi çerçevelerini yükler. Birim testleri oluşturun, bunları çalıştırmak ve bu testlerin sonuçları rapor için bir birim testi Çerçevesi'ni kullanın. Kodunuzun düzgün çalışıp çalışmadığını test etmek için değişiklik yaptığınızda yeniden birim testleri. Visual Studio Enterprise edition ile testleri otomatik olarak her yapıdan sonra çalıştırabilirsiniz.

Başlamak için okuma [Intellitest ile kodunuz için birim testleri oluşturmak](../test/generate-unit-tests-for-your-code-with-intellitest.md).

Visual Studio ve bunların nasıl daha kaliteli kod oluşturmanıza yardımcı olabileceğini birim testleri hakkında daha fazla bilgi edinmek için [birim testi temel bilgileri](../test/unit-test-basics.md).

## <a name="see-also"></a>Ayrıca bkz.

- [Hata ayıklayıcısı özellik turu](../debugger/debugger-feature-tour.md)
- [Hata ayıklayıcıyı kullanma hakkında daha fazla bilgi edinin](../debugger/debugger-feature-tour.md)
- [Kod oluşturma ve düzeltme](../ide/code-generation-in-visual-studio.md)