---
title: Python geliştiricileri için Visual Studio'nun genel bakış
titleSuffix: ''
ms.date: 03/13/2019
ms.topic: conceptual
author: JoshuaPartlow
ms.author: joshuapa
manager: jillfra
dev_langs:
- Python
ms.workload:
- python
- data-science
ms.openlocfilehash: d9c84e72551911135550c43da2b99ecb1357f9b6
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59365736"
---
# <a name="welcome-to-the-visual-studio-ide--python"></a>Visual Studio IDE Hoş Geldiniz | Python

Visual Studio *tümleşik geliştirme ortamı* bir yaratıcı launching düzenleme, hata ayıklama ve kod test etme ve ardından bir uygulama yayımlama için kullanabileceğiniz Python (ve diğer diller) için bir ortamdır. Bir tümleşik geliştirme ortamı (IDE) birçok yönüyle yazılım geliştirme için kullanılabilen zengin bir programdır. Standart Düzenleyici ve hata ayıklayıcı sağladığımız çoğu IDE'ler sağlamanızı, Visual Studio kod tamamlama içerir, etkileşimli REPL ortamları, araçları ve diğer özellikleri yazılım geliştirme işlemini kolaylaştırmak için.

[![Visual Studio ile Python projesi](media/tour-ide-overview.png)](media/tour-ide-overview.png#lightbox)

Bu görüntü, büyük olasılıkla kullanacağınız birkaç anahtar araç pencereleri ve Python Proje Aç ile Visual Studio gösterir:

- [**Çözüm Gezgini** ](../ide/solutions-and-projects-in-visual-studio.md) (sağ üstte) görüntüleyin, gidin ve kodu dosyalarınızdaki dosyalardan yönetmenize olanak tanır. **Çözüm Gezgini** dosyalarına gruplandırarak kodunuzu düzenleme şeklinizdir yardımcı olabilecek [çözümler ve projeler](/visualstudio/get-started/tutorial-projects-solutions).
    - Yanı sıra **Çözüm Gezgini** olduğu [ **Python ortamları**](managing-python-environments-in-visual-studio.md), bilgisayarınızda yüklü olan farklı Python yorumlayıcılarını yönettiği yerdir.

    ::: moniker range=">=vs-2019"
    - Visual Studio'nun proje ve çözüm dosyaları oluşturmadan bir klasör de açık ve çalışma Python kodu kullanabilirsiniz. Daha fazla bilgi için [hızlı başlangıç: Açın ve bir klasörde Python kodunu çalıştırma](quickstart-05-python-visual-studio-open-folder.md).
    ::: moniker-end

- [Düzenleyicisi penceresi](../ide/writing-code-in-the-code-and-text-editor.md) (Merkezi), büyük olasılıkla, zamanınızın çoğunu geçireceksiniz burada dosya içeriğini görüntüler. Burada, [Python kodunu Düzenle](editing-python-code-in-visual-studio.md)içinde kod yapınızı gidin ve hata ayıklama oturumları sırasında kesme noktaları ayarlayın. Python ile ayrıca kodu seçin ve bu kodu çalıştırmak için Ctrl + Enter tuşlarına basın bir [etkileşimli REPL penceresini](python-interactive-repl-in-visual-studio.md).

- [Çıkış penceresine](../ide/reference/output-window.md) (alt Merkezi), burada Visual Studio hata ayıklama ve hata iletileri, uyarılar, yayımlama durum iletilerini ve diğer bildirimleri gönderir. Her ileti kaynağı kendi sekmesi vardır.
    - A [Python etkileşimli REPL penceresini](python-interactive-repl-in-visual-studio.md) çıkış penceresi olarak aynı alanda görüntülenir.

- [Takım Gezgini](/azure/devops/user-guide/work-team-explorer?view=vsts) (sağ alt) sağlar, iş öğelerini izlemek ve kod başkalarıyla paylaşmak gibi sürüm denetimi teknolojileri kullanarak [Git](https://git-scm.com/) ve [Team Foundation sürüm denetimi (TFVC)](/azure/devops/repos/tfvc/overview?view=vsts).

## <a name="editions"></a>Sürümler

Windows ve Mac için Visual Studio kullanılabilir; Ancak, yalnızca Visual Studio için Windows üzerinde Python desteği sunulmaktadır.

Windows üzerinde Visual Studio'nun üç sürüm bulunur: Community, Professional ve Enterprise. Bkz: [karşılaştırma Visual Studio Ide'leri](https://visualstudio.microsoft.com/vs/compare/) her iki sürümünde desteklenen hangi özellikler hakkında bilgi edinmek için.

## <a name="popular-productivity-features"></a>Popüler üretkenlik özellikleri

Visual Studio yazılım geliştirme sırasında daha üretken olmanıza yardımcı olan popüler özelliklerinden bazıları şunlardır:

- [IntelliSense](editing-python-code-in-visual-studio.md#intellisense)

   IntelliSense, doğrudan düzenleyicide kod hakkında bilgi görüntüler ve bazı durumlarda, küçük kod parçalarını sizin için yazma özellikleri kümesi için kullanılan bir terimdir. Bu temel belgeleri satır içi başka bir yerde türü bilgi aramak zorunda kalmaktan kurtarır düzenleyicisinde gibidir. IntelliSense özellikleri, dile göre değişiklik gösterir ve [düzenleme Python kodu](editing-python-code-in-visual-studio.md#intellisense) makalede, Python için ayrıntılar bulunur. Aşağıdaki çizimde, IntelliSense üye listesi bir türü için nasıl görüntülediğini gösterir:

   ![Visual Studio IntelliSense üye tamamlama](media/code-editing-completions-simple.png)

- [Yeniden Düzenleme](refactoring-python-code.md)

   Kod ve seçerek bir parçasına sağ tıklanarak **hızlı Eylemler ve yeniden düzenlemeler**, Visual Studio sağlar akıllı değişkenleri, yeniden adlandırma gibi işlemler ile değiştirerek yeni bir yönteme bir veya daha fazla kod satırlarını ayıklanıyor Yöntem parametreleri ve daha fazlasını sırası.

   ![Visual Studio'da yeniden düzenleme](media/tour-ide-refactor-extract-method.png)

- [Lint uygulama](refactoring-python-code.md)

   Hatalar ve yaygın sorunlar, kodlama desenleri iyi Python ile teşvik Python kodunuzu linting denetler.

   ![Python projeleri için bağlam menüsünde PyLint komutu](media/code-pylint-command.png)

- Arama kutusu

   Visual Studio zamanlarda sürü menüleri, seçenekleri ve özellikleri ile zor görünebilir. Arama kutusuna, Visual Studio'da aradığınızı hızla bulmak için harika bir yoludur. Aradığınız bir şey adını yazmaya başladığınızda, Visual Studio tam olarak gitmek gerek duyduğunuz aldığınız sonuçları listeler. Örneğin, ek bir programlama dili için destek eklemek Visual Studio işlevselliği eklemek gerekiyorsa arama kutusuna bir iş yükü veya ayrı ayrı bileşen yüklemek için Visual Studio yükleyicisini açın sonuçları sağlar.

   ![Visual Studio'da arama kutusu](media/tour-ide-quick-launch.png)

- Dalgalı çizgiler ve [hızlı Eylemler](../ide/quick-actions.md)

   Siz yazarken, hatalar veya kodunuzdaki olası sorunlar için uyarı dalgalı alt çizgiler dalgalı çizgiler var. Bu görsel ipuçları hata derleme sırasında veya programı çalıştırdığınızda bulunmak beklenmeden hemen sorunları düzeltmek etkinleştirin. Bir dalgalı çizgi gelin, hatayla ilgili ek bilgileri görürsünüz. Hatayı düzeltmek için hızlı Eylemler bilinen eylemlerle sol kenar boşluğunda bir ampul de görünebilir.

   ![Visual Studio'da dalgalı çizgiler](media/tour-ide-squiggles.png)

- [Git ve Özet tanımı](../ide/go-to-and-peek-definition.md)

   **Tanıma** özelliği doğrudan bir işlev veya tür tanımlandığı konumuna götürür. **Özet tanımları** komut görüntüler tanımı bir pencere içinde ayrı bir dosyayı açmaya gerek kalmadan. **Tüm başvuruları Bul** komut da burada verilen herhangi bir tanımlayıcı hem tanımlandığını ve kullanıldığını keşfetmek için kullanışlı bir yol sağlar.

   ![Kod Gezinti komutları](media/tour-ide-navigation-commands.png)

## <a name="powerful-features-for-python"></a>Python için güçlü özellikler

::: moniker range=">=vs-2019"
- [Kod proje olmadan çalıştırın](quickstart-05-python-visual-studio-open-folder.md)

    Visual Studio 2019 ' başlayarak, IntelliSense ve kod için Visual Studio projesi oluşturmak zorunda kalmadan hata ayıklama gibi özelliklerden faydalanmak için Python kodu içeren bir klasörün açabilirsiniz.
::: moniker-end

- [Python etkileşimli REPL](python-interactive-repl-in-visual-studio.md)

    Visual Studio, her biri ile alma REPL üzerine artırır, Python ortamları için bir etkileşimli okuma değerlendirmek yazdırma döngü (REPL) penceresi sağlar *python.exe* komut satırında. İçinde **etkileşimli** penceresi rastgele Python kodu girin ve sonuçları hemen görün.

    ![Python etkileşimli penceresi](media/interactive-window.png)

- [Hata Ayıklama](debugging-python-in-visual-studio.md)

    Visual Studio, Python, çalışan işlemlere, ekleme dahil olmak üzere, ifadeleri değerlendirme için kapsamlı bir hata ayıklama deneyimi sunar **Watch** ve **hemen** windows, yerel inceleniyor değişkenleri, kesme noktaları, / out/üzerinden deyimleri adım **sonraki deyimi Ayarla**ve daha fazlası. Linux bilgisayarlar üzerinde çalışan uzaktan Python kod hata ayıklaması yapabilirsiniz.

    ![Visual Studio'da Python hata ayıklama](media/remote-debugging-breakpoint-hit.png)

- [C++ ile etkileşim kurma](working-with-c-cpp-python-in-visual-studio.md)

    Python için oluşturulan birçok kitaplıklarının en iyi performans için C++ dilinde yazılır. Visual Studio gibi C++ uzantıları geliştirmeye yönelik zengin olanakları sağlar [karışık mod hata ayıklama](debugging-mixed-mode-c-cpp-python-in-visual-studio.md).

    ![Python ile birlikte C++ karışık mod hata ayıklama](media/mixed-mode-debugging.png)

- [Profil Oluşturma](profiling-python-code-in-visual-studio.md)

    CPython tabanlı bir yorumlayıcı kullanırken, Visual Studio'da Python kodunuzun performansını değerlendirebilirsiniz.

    ![Profil oluşturma performans raporu](media/profiling-results.png)

- [Birim Testi](unit-testing-python-in-visual-studio.md)

    Tüm IDE bağlamında hata ayıklama birim testleri ve Visual Studio tümleşik destek bulmak, sağlar çalışır.

    ![Birim testi başarısız test durumu gösteriliyor](media/unit-test-A-fail.png)

## <a name="next-steps"></a>Sonraki adımlar

Aşağıdaki hızlı başlangıçlarını veya öğreticilerini birini izleyerek daha fazla Visual Studio'da Python'ı keşfedin:

> [!div class="nextstepaction"]
> [Hızlı Başlangıç: Flask ile web uygulaması oluşturma](../ide/quickstart-python.md?toc=/visualstudio/python/toc.json&bc=/visualstudio/python/_breadcrumb/toc.json)

> [!div class="nextstepaction"]
> [Visual Studio'da Python ile çalışma](tutorial-working-with-python-in-visual-studio-step-01-create-project.md)

> [!div class="nextstepaction"]
> [Visual Studio'da Django web çerçevesi ile çalışmaya başlama](learn-django-in-visual-studio-step-01-project-and-solution.md)

> [!div class="nextstepaction"]
> [Visual Studio'da Flask web çerçevesi ile çalışmaya başlama](learn-flask-visual-studio-step-01-project-solution.md)

## <a name="see-also"></a>Ayrıca bkz.

- Bulma [daha fazla Visual Studio özellikleri](../ide/advanced-feature-overview.md)
- Ziyaret [visualstudio.microsoft.com](https://visualstudio.microsoft.com/vs/)
- Okuma [Visual Studio blogu](https://devblogs.microsoft.com/visualstudio/)
