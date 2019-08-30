---
title: "Hızlı Başlangıç: Python web uygulaması oluşturmak için Visual Studio'yu kullanın."
description: Bu hızlı başlangıçta, Visual Studio ve Flask framework python'da basit web uygulaması oluşturmak için kullanın.
ms.date: 03/07/2019
ms.technology: vs-python
ms.topic: quickstart
author: JoshuaPartlow
ms.author: joshuapa
manager: jillfra
ms.workload:
- python
- data-science
ms.openlocfilehash: cbb06ac800fd21e2354b04fb2e7e46306da7ed72
ms.sourcegitcommit: 44e9b1d9230fcbbd081ee81be9d4be8a485d8502
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/30/2019
ms.locfileid: "70180349"
---
# <a name="quickstart-create-your-first-python-web-app-using-visual-studio"></a>Hızlı Başlangıç: Visual Studio kullanarak ilk Python web uygulamanızı oluşturma

Bu 5-10 dakikalık bir giriş Visual Studio'ya bir Python IDE olarak, Flask framework tabanlı basit bir Python web uygulaması oluşturun. Ayrık'aracılığıyla projenin oluşturduğunuz yardımcı adımlar Visual Studio temel özellikleri hakkında bilgi edinin.

::: moniker range="vs-2017"

Visual Studio henüz yüklemediyseniz, Git [Visual Studio indirmeleri](https://visualstudio.microsoft.com/vs/older-downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=vs+2017+download) ücretsiz yüklemek için sayfa. Yükleyicide seçtiğinizden emin olun **Python geliştirme** iş yükü.

::: moniker-end

::: moniker range=">=vs-2019"

Visual Studio henüz yüklemediyseniz, Git [Visual Studio indirmeleri](https://visualstudio.microsoft.com/downloads) ücretsiz yüklemek için sayfa. Yükleyicide seçtiğinizden emin olun **Python geliştirme** iş yükü.

::: moniker-end

## <a name="create-the-project"></a>Projeyi oluşturma

Aşağıdaki adımlar, uygulama için bir kapsayıcı görevi gören boş bir proje oluşturur:

::: moniker range="vs-2017"
1. Visual Studio 2017'yi açın.

2. Üstteki menü çubuğundan seçin **Dosya > Yeni > Proje**.

3. İçinde **yeni proje** iletişim kutusunda, sağ üst köşedeki arama alanına "Python Web projesi" girin, **Web projesi** ortadaki listeyi proje "HelloPython" gibi bir ad verin ve ardından seçin**Tamam**.

    ![Python Web Seçili proje ile yeni proje iletişim kutusu](media/quickstart-python-00-web-project.png)

    Python proje şablonlarını görmüyorsanız, **Visual Studio yükleyicisi**çalıştırın, **daha fazla** > **Değiştir**' i seçin, **Python geliştirme** iş yükünü seçin ve ardından **Değiştir**' i seçin.

    ![Python geliştirme iş yüküyle Visual Studio](../python/media/installation-python-workload.png)

4. Yeni Proje açılır **Çözüm Gezgini** sağ bölmede. Proje, bu noktada, başka hiçbir dosya içerdiği için boştur.

    ![Yeni oluşturulan boş projeyi gösteren Çözüm Gezgini](media/quickstart-python-01-empty-project.png)
::: moniker-end

::: moniker range=">=vs-2019"
1. Visual Studio 2019 ' i açın.
2. Başlangıç ekranında **Yeni proje oluştur**' u seçin.
3. **Yeni proje oluştur** iletişim kutusunda, üstteki arama alanına "Python web" yazın, ortadaki listede **Web projesi** ' ni seçin ve ardından **İleri**' yi seçin:

    ![Python web projesi seçiliyken yeni bir proje ekranı oluştur](media/quickstart-python-00-web-project-2019a.png)

    Python proje şablonlarını görmüyorsanız, **Visual Studio yükleyicisi**çalıştırın, **daha fazla** > **Değiştir**' i seçin, **Python geliştirme** iş yükünü seçin ve ardından **Değiştir**' i seçin.

    ![Python geliştirme iş yüküyle Visual Studio](../python/media/installation-python-workload.png)

4. Aşağıdaki **yeni projeyi Yapılandır** iletişim kutusunda, **Proje adı**için "Merhaba Python" yazın, bir konum belirtin ve **Oluştur**' u seçin. ( **Çözüm adı** , **Proje adı**ile eşleşecek şekilde otomatik olarak ayarlanır.)

    ![Yeni proje iletişim kutusunu yapılandırın](media/quickstart-python-00-web-project-2019b.png)

5. Yeni Proje açılır **Çözüm Gezgini** sağ bölmede. Proje, bu noktada, başka hiçbir dosya içerdiği için boştur.

    ![Yeni oluşturulan boş projeyi gösteren Çözüm Gezgini](media/quickstart-python-01-empty-project-2019.png)
::: moniker-end

**Unuza Visual Studio 'da bir Python uygulaması için proje oluşturmanın avantajı nedir?**

**Cevap**: Python uygulamaları genellikle yalnızca klasörler ve dosyalar kullanılarak tanımlanır, ancak bu basit yapı, uygulamalar daha büyük hale geldiğinde ve belki de otomatik olarak oluşturulan dosyalar, Web uygulamaları için JavaScript vb. dahil olmak üzere çok sayıda bulunabilir. Visual Studio projesi Bu karmaşıklığı yönetmenize yardımcı olur. Proje (bir *.pyproj* dosyası) kaynak ve projenizle ilişkili içerik dosyalarını tanımlar, her dosya için yapı bilgisi içerir, kaynak denetimi sistemleriyle tümleştirmeyi bilgilerini korur ve yardımcı olur mantıksal bileşenler uygulamanıza düzenleyin.

**Unuza Çözüm Gezgini ' de gösterilen "Çözüm" nedir?**

**Cevap**: Visual Studio çözümü bir veya daha fazla ilgili projeyi grup olarak yönetmenize yardımcı olan bir kapsayıcıdır ve bir projeye özgü olmayan yapılandırma ayarlarını depolar. Bir çözümde proje ayrıca birbirlerine başvurabilir, (bir Python uygulaması) sağlayacak şekilde çalışan tek bir proje, otomatik olarak (örneğin, Python uygulaması içinde kullanılan C++ uzantısı) ikinci bir proje oluşturur.

## <a name="install-the-flask-library"></a>Flask kitaplığını yükle

Python Web uygulamalarında hemen her zaman birçok kullanılabilir Python kitaplıkları yönlendirme web isteklerini ve yanıtlarını şekillendirme gibi alt düzey ayrıntıları işlemek için kullanın. Bu amaç için Visual Studio, çeşitli web apps, biri bu hızlı başlangıçta kullanmak için şablonları sağlar.

Burada, "Bu proje için Visual Studio kullanan varsayılan genel ortama" Flask kitaplığını yüklemek için aşağıdaki adımları kullanın.

::: moniker range="vs-2017"
1. Genişletin **Python ortamları** proje için varsayılan ortam görmek için proje düğümü.

    ![Varsayılan ortamı gösteren Çözüm Gezgini](media/quickstart-python-02-default-environment.png)

2. Ortam sağ tıklayıp **Python paketini Yükle**. Bu komut açılır **Python ortamları** penceresinde **paketleri** sekmesi.

3. Arama alanına "flask" girin ve seçin **pip, Pypı flask yükleme**. Sizden yönetici ayrıcalıkları kabul edin ve gözlemleyin **çıkış** ilerleme için Visual Studio penceresinde. (Bir komut istemi packages klasörünü genel ortam için bir korumalı alanı içinde bulunduğu yükseltme olur için ister *C:\Program Files*.)

    ![Pip kullanılarak Flask kitaplık yükleme](media/quickstart-python-03-install-package.png)
::: moniker-end
::: moniker range=">=vs-2019"
1. Genişletin **Python ortamları** proje için varsayılan ortam görmek için proje düğümü.

    ![Varsayılan ortamı gösteren Çözüm Gezgini](media/quickstart-python-02-default-environment-2019.png)

2. Ortama sağ tıklayın ve **Python paketlerini Yönet...** seçeneğini belirleyin. Bu komut, **Packages (PyPI)** sekmesindeki **Python ortamları** penceresini açar.

3. Arama alanına "Flask" yazın. Arama kutusunun altında **Flask** görünürse, bu adımı atlayabilirsiniz. Aksi takdirde, **Çalıştır komutunu seçin: PIP Install Flask**. Sizden yönetici ayrıcalıkları kabul edin ve gözlemleyin **çıkış** ilerleme için Visual Studio penceresinde. (Bir komut istemi packages klasörünü genel ortam için bir korumalı alanı içinde bulunduğu yükseltme olur için ister *C:\Program Files*.)

    ![Pip kullanılarak Flask kitaplık yükleme](media/quickstart-python-03-install-package-2019.png)
::: moniker-end

4. Yüklendikten sonra kitaplık ortamda görünür **Çözüm Gezgini**, yapabileceğiniz anlamına gelir bunu Python kodu kullanın.

    ::: moniker range="vs-2017"
    ![Flask kitaplığının yüklü ve Çözüm Gezgini'nde gösteriliyor](media/quickstart-python-04-package-installed.png)
    ::: moniker-end
    ::: moniker range=">=vs-2019"
    ![Flask kitaplığının yüklü ve Çözüm Gezgini'nde gösteriliyor](media/quickstart-python-04-package-installed-2019.png)
    ::: moniker-end

> [!Note]
> Genel bir ortamda kitaplıklarını yüklemek yerine, geliştiricilerin, belirli bir projenin kitaplıklarını yüklemek "sanal ortam" genellikle oluşturun. Visual Studio şablonları bölümünde açıklandığı gibi bu seçenek genellikle teklif [hızlı başlangıç - şablon kullanarak bir Python projesi oluşturma](../python/quickstart-02-python-in-visual-studio-project-from-template.md).

**Unuza Diğer kullanılabilir Python paketleri hakkında nereden daha fazla bilgi edinebilirim?**

**Cevap**: [Python paket dizinini](https://pypi.org/)ziyaret edin.

## <a name="add-a-code-file"></a>Bir kod dosyası Ekle

Python kodu en az bir web uygulamasını uygulamak için biraz eklemek artık hazırsınız.

1. Projeye sağ **Çözüm Gezgini** seçip **Ekle > Yeni öğe**.

1. Görüntülenen iletişim kutusunda, seçmek **boş Python dosyası**, adlandırın *app.py*seçip **Ekle**. Visual Studio, düzenleyici penceresinde dosya otomatik olarak açılır.

1. Aşağıdaki kodu kopyalayın ve yapıştırın *app.py*:

    ```python
    from flask import Flask

    # Create an instance of the Flask class that is the WSGI application.
    # The first argument is the name of the application module or package,
    # typically __name__ when using a single module.
    app = Flask(__name__)

    # Flask route decorators map / and /hello to the hello function.
    # To add other resources, create functions that generate the page contents
    # and add decorators to define the appropriate resource locators for them.

    @app.route('/')
    @app.route('/hello')
    def hello():
        # Render the page
        return "Hello Python!"

    if __name__ == '__main__':
        # Run the app server on localhost:4449
        app.run('localhost', 4449)
    ```

1. Fark etmiş **Ekle > Yeni öğe** diğer türlerde dosyaları Python sınıfı, bir Python paketi, bir Python birim testi dahil olmak üzere bir Python projeye Ekle iletişim kutusu görüntüler *web.config* dosyaları ve daha fazlası. Genel olarak, adlı gibi bu öğe şablonları dosyaları yararlı Demirbaş kod ile hızlı bir şekilde oluşturmak için harika bir yol sağlar.

**Unuza Flask hakkında nereden daha fazla bilgi edinebilirim?**

**Cevap**: [Flask hızlı](https://flask.palletsprojects.com/en/1.1.x/quickstart/#quickstart)başlangıç Ile başlayarak Flask belgelerine bakın.

## <a name="run-the-application"></a>Uygulamayı çalıştırma

1. Sağ *app.py* içinde **Çözüm Gezgini** seçip **başlangıç dosyası olarak ayarla**. Bu komut, uygulamayı çalıştırırken Python'da başlatmak için kod dosyası tanımlar.

    ::: moniker range="vs-2017"
    ![Çözüm Gezgini'nde bir proje için başlangıç dosyası ayarı](media/quickstart-python-05-set-as-startup-file.png)
    ::: moniker-end
    ::: moniker range=">=vs-2019"
    ![Çözüm Gezgini'nde bir proje için başlangıç dosyası ayarı](media/quickstart-python-05-set-as-startup-file-2019.png)
    ::: moniker-end

2. Projeye sağ **Çözüm Gezgini** seçip **özellikleri**. Ardından **hata ayıklama** ayarlayın ve sekme **bağlantı noktası numarası** özelliğini `4449`. Visual Studio ile bir tarayıcı başlatır, bu adım sağlar `localhost:4449` eşleştirilecek `app.run` koddaki bağımsız değişkenler.

3. Seçin **hata ayıklama > hata ayıklama olmadan Başlat** (**Ctrl**+**F5**), dosyaları değişiklikleri kaydeder ve uygulamayı çalıştırır.

4. İletinin bir komut penceresi görünür "* çalışan <https://localhost:4449/>", ve bir tarayıcı penceresi açılmalıdır `localhost:4449` iletisini gördüğünüz yerde "Hello, Python!" GET isteği, durumu 200 olan komut penceresinde de görünür.

    Bir tarayıcı otomatik olarak açılmazsa, tercih ettiğiniz tarayıcıyı başlatın ve gidin `localhost:4449`.

    Yalnızca Python etkileşimli Kabuk komut penceresinde görürseniz veya o pencereyi kısaca ekranda yanıp, ayarladığınız olun *app.py* yukarıdaki 1. adımda başlangıç dosyası olarak.

5. Gidin `localhost:4449/hello` , test etmek için dekoratör `/hello` kaynak de çalışır. Komut penceresinde durumu 200 olan yeniden GET isteği görüntülenir. 404 durum kodu komut penceresinde Göster görmek için bazı diğer URL'sini de deneyin çekinmeyin.

6. Uygulamayı durdurmak için komut penceresini kapatın, ardından tarayıcı penceresini kapatın.

**Unuza Hata ayıklama komutu olmadan Başlat ve hata ayıklamayı Başlat arasındaki fark nedir?**

**Cevap**: Uygulamayı [Visual Studio hata ayıklayıcısı](../python/debugging-python-in-visual-studio.md)bağlamında çalıştırmak Için **hata ayıklamayı Başlat** ' ı kullanarak, kesme noktalarını ayarlamanıza, değişkenleri incelemenize ve kod satırınızın sonuna kadar ilerlemenize izin vermiş olursunuz. Uygulamalar, hata ayıklama mümkün kılan çeşitli kancaları nedeniyle hata ayıklayıcıda yavaş çalışabilir. **Hata ayıklama olmadan Başlat**, buna karşılık, komut satırından, hiçbir hata ayıklama içeriğini çalıştırdıysanız gibi doğrudan uygulama çalışır ve da otomatik olarak bir tarayıcı başlatır ve belirtilen proje özelliklerinde URL'sine gider  **Hata ayıklama** sekmesi.

## <a name="next-steps"></a>Sonraki adımlar

Visual Studio'yu bir Python IDE kullanma hakkında biraz öğrendiğinize göre ilk Python uygulamanızı Visual Studio'dan içinde çalıştırma Tebrikler!

> [!div class="nextstepaction"]
> [Uygulamayı Azure App Service'e dağıtma](../python/publishing-python-web-applications-to-azure-from-visual-studio.md)

Bu hızlı başlangıçta uyguladığınız adımları oldukça geneldir çünkü olabilir ve otomatik hale getirilmelidir büyük olasılıkla tahmin. Bu otomasyon, Visual Studio Proje şablonları rolüdür. Git aracılığıyla [hızlı başlangıç - şablon kullanarak bir Python projesi oluşturma](../python/quickstart-02-python-in-visual-studio-project-from-template.md) benzeyen bir web uygulaması oluşturan bir örnek için bu makalede, ancak daha az adım ile oluşturulmuş.

Etkileşimli pencere, hata ayıklama, veri görselleştirme ve git ile çalışma dahil olmak üzere Visual Studio 'da Python hakkında daha kapsamlı bir öğreticiye devam etmek için [öğreticiye geçin: Visual Studio](../python/tutorial-working-with-python-in-visual-studio-step-01-create-project.md)'da Python ile çalışmaya başlayın.

Daha fazla sunmak Visual Studio sahip olduğunu keşfetmek için aşağıdaki bağlantıları seçin.

- Hakkında bilgi edinin [Python web uygulaması şablonları Visual Studio'da](../python/python-web-application-project-templates.md).
- Hakkında bilgi edinin [Python hata ayıklama](../python/debugging-python-in-visual-studio.md)
- Daha fazla bilgi edinin [Visual Studio IDE](../get-started/visual-studio-ide.md) genel.
