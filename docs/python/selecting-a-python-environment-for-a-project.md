---
title: Python yorumlayıcısı ve ortamınız için bir proje seçin
description: Anaconda ve sanal ortamlar, belirli bir projeye uygulamak da dahil olmak üzere bir Python ortamı özel olarak seçebilirsiniz.
ms.date: 03/18/2019
ms.topic: conceptual
author: JoshuaPartlow
ms.author: joshuapa
manager: jillfra
ms.custom: seodec18
ms.workload:
- python
- data-science
ms.openlocfilehash: 9d7736365e8e2bb371a71580492401bb2660fcc3
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62429723"
---
# <a name="how-to-select-a-python-environment-for-a-project"></a>Nasıl bir proje için bir Python ortamı seçin

Bir global Python ortamı, Anaconda ortamı, bir sanal ortam ya da conda ortamı gibi belirli bir ortama bağlamında bir Python projesindeki tüm kod çalıştırır. Visual Studio bu ortamda hata ayıklama, içeri aktarma ve üye tamamlama, sözdizimi denetimi ve Python sürümü ve yüklü paketleri birtakım özel dil hizmetleri gerektiren herhangi bir görev için de kullanır.

Tüm yeni Python projeleri Visual Studio'da ilk altında görüntülenen varsayılan genel ortam kullanmak üzere yapılandırılmış **Python ortamları** düğümünde **Çözüm Gezgini**:

![Çözüm Gezgini'nde gösterilen genel varsayılan Python ortamı](media/environments/environments-project.png)

::: moniker range="vs-2017"
Bir proje için ortamı değiştirmek için sağ **Python ortamları** düğümünü seçip alt **Ekle/Kaldır Python ortamları**. Conda ortamları altında görüntülenmesini istediğiniz tüm sürücüler seçin ve görüntülenen listeden hangi içerir genel, sanal **Python ortamları** düğüm:

![Python ortamları Ekle/Kaldır iletişim kutusu](media/environments/environments-add-remove.png)

Seçtiğinizde **Tamam**, seçilen tüm ortamlara altında görünür **Python ortamları** düğümü. Şu anda etkin ortam kalın yazı tipinde görünür:

![Çözüm Gezgini'nde birden çok Python ortamları](media/environments/environments-project-multiple.png)

Hızlı bir şekilde farklı bir ortama etkinleştirmek için bu ortam adını sağ tıklatın ve seçin **etkinleştirme ortam**. Seçtiğiniz proje ile kaydedilir ve proje gelecekte açtığınızda bu ortamda etkinleştirilir. Tüm seçenekleri işaretini kaldırırsanız **Ekle/Kaldır Python ortamları** iletişim kutusunda, Visual Studio genel varsayılan ortam etkinleştirir.

Bağlam menüsünde **Python ortamları** düğüm ayrıca ek komutlar sağlar:

| Komut | Açıklama |
| --- | --- |
| **Sanal ortam Ekle** | Projede yeni bir sanal ortam oluşturma işlemi başlar. Bkz: [sanal ortam Oluştur](#create-a-virtual-environment). |
| **Var olan sanal ortama Ekle** | Bir sanal ortam içeren bir klasör seçmenizi ister ve altındaki listeye ekler **Python ortamları**, ancak etkinleştirmez. Bkz: [var olan bir sanal ortam etkinleştirme](#activate-an-existing-virtual-environment). |
| **Conda ortamı oluşturma** | Ağınızdan **Python ortamları** *penceresi* , ortam için bir ad girin ve kendi temel yorumlayıcı belirtin. Bkz: [Conda ortamları](managing-python-environments-in-visual-studio.md#conda-environments). |
::: moniker-end

::: moniker range=">=vs-2019"
Ortam bir proje için değiştirmek için sağ tıklayın **Python ortamları** düğümünü seçip alt **ortam Ekle**, ya da seçin **ortam Ekle** ortamından Python araç çubuğu açılır.

İçinde bir kez **ortam Ekle** iletişim kutusunda **varolan ortam** sekmesine ve ardından yeni bir ortamdan **ortam** açılan liste:

![Proje ortam seçerek ortamları Ekle iletişim kutusunda](media/environments/environments-project-2019.png)

Bir proje için genel varsayılan dışında bir ortam zaten eklediyseniz, yeni eklenen bir ortam etkinleştirmeniz gerekebilir. Bu ortamda sağ **Python ortamları** düğüm ve seçin **etkinleştirme ortam**. Bir ortam projeden kaldırmak için seçin **Kaldır**.

![Etkinleştirme ve proje ortam kaldırma](media/environments/environments-project-add-remove-2019.png)
::: moniker-end

## <a name="use-virtual-environments"></a>Sanal ortamları kullanma

Bir sanal ortam belirli bir Python yorumlayıcısı eşsiz bir bileşimiyle ve diğer genel ve conda ortamları farklı olan belirli bir kümesini kitaplıkları ' dir. Bir sanal ortam, projeye özgü ve proje klasöründe saklanır. Ortamının yüklü kitaplıkları ile birlikte bu klasörde bir *pyvenv.cfg* ortamın yolunu belirtir dosya *temel yorumlayıcı* dosya sistemindeki başka bir yerde. (Diğer bir deyişle, bir sanal ortamın bir kopyasını Yorumlayıcı, yalnızca bir bağlantı içermiyor.)

Bir sanal ortam kullanmanın bir avantajı, zaman içinde proje geliştirirken, sanal ortamı her zaman tam proje bağımlılıkları yansıtır ' dir. (Bunları projenizde veya olmanızdan bağımsız bir paylaşılan genel ortam, diğer taraftan, herhangi bir sayıda kitaplıkları içerir.) Daha sonra kolayca oluşturabilirsiniz bir *requirements.txt* dosyadan sonra bu bağımlılıkları başka bir geliştirme veya üretim bilgisayarına yeniden yüklemek için kullanılan sanal ortamı. Daha fazla bilgi için [requirements.txt ile gerekli paketleri yönetme](managing-required-packages-with-requirements-txt.md).

Visual Studio'da içeren bir proje açtığınızda, bir *requirements.txt* dosya, Visual Studio otomatik olarak sanal ortam yeniden oluşturmak için seçeneği size sunar. Visual Studio'nun yüklü olmayan bilgisayarlarda kullanabilirsiniz `pip install -r requirements.txt` paketlerini geri yüklemek için.

Bir sanal ortam için temel yorumlayıcı sabit kodlanmış bir yol içerdiğinden ve ortam kullanarak yeniden oluşturabilirsiniz *requirements.txt*, genellikle kaynak denetiminden tüm sanal ortamın klasöre çıkarın.

Aşağıdaki bölümlerde, bir proje var olan bir sanal ortamda etkinleştirme ve yeni bir sanal ortamının nasıl oluşturulacağı açıklanmaktadır.

Visual Studio'da gibi başka bir proje için bir sanal ortam etkinleştirilebilmesi için **Python ortamları** düğümünde **Çözüm Gezgini**.

Bir sanal ortam projenize eklendikten sonra görünür **Python ortamları** penceresi. Ardından, herhangi bir ortam gibi etkinleştirebilir ve kendi paketleri yönetebilirsiniz.

::: moniker range="vs-2017"
### <a name="create-a-virtual-environment"></a>Sanal ortam oluştur

Doğrudan Visual Studio'da yeni bir sanal ortam şu şekilde oluşturabilirsiniz:

1. Sağ **Python ortamları** içinde **Çözüm Gezgini** seçip **sanal ortama ekleme**, aşağıdaki iletişim kutusunu getirir:

    ![Bir sanal ortam oluşturma](media/environments/environments-add-virtual-1.png)

1. İçinde **sanal ortam konumunu** alanında, sanal ortam için bir yol belirtin. Yalnızca bir ad belirtirseniz, sanal ortamın içinde bu ada sahip bir alt klasör geçerli projeye oluşturulur.

1. Temel yorumlayıcı bir ortam seçin ve seçin **Oluştur**. Visual Studio ortamı yapılandırır ve gerekli tüm paketleri indirir bir ilerleme çubuğu görüntülenir. Sanal ortam tamamlandıktan sonra görünür **Python ortamları** içeren proje penceresi.

1. Sanal ortam varsayılan olarak etkin değildir. Proje için etkinleştirmek için sağ tıklatın ve seçin **etkinleştirme ortam**.

> [!Note]
> Konumu yolu mevcut bir sanal ortam tanımlıyorsa, Visual Studio temel yorumlayıcı otomatik olarak algılar (kullanarak *ORIG prefix.txt* ortamın dosyasında *LIB* dizini) ve değişiklikleri **Oluştur** düğmesi **Ekle**.
>
> Varsa bir *requirements.txt* dosyası mevcut bir sanal ortamda eklerken **sanal ortama ekleme** iletişim kutusunu görüntüler paketleri otomatik olarak yüklemek için bir seçenek yeniden oluşturmayı kolaylaştıran bir ortam başka bir bilgisayarda:
>
> ![Requirements.txt ile sanal ortam oluştur](media/environments/environments-requirements-txt.png)
>
> Senaryosuyla her iki durumda da aynı sonucudur **var olan sanal ortama ekleme** komutu.

### <a name="activate-an-existing-virtual-environment"></a>Mevcut bir sanal ortam etkinleştir

Bir sanal ortam başka bir yerde zaten oluşturduysanız, proje için şu şekilde etkinleştirebilirsiniz:

1. Sağ **Python ortamları** içinde **Çözüm Gezgini** seçip **var olan sanal ortama ekleme**.

1. İçinde **Gözat** görüntülenen iletişim gidin ve sanal ortam içeren klasörü seçin ve **Tamam**. Visual Studio algılarsa bir *requirements.txt* dosya o ortamda, bu paketleri yüklenip yüklenmeyeceğini ister.

1. Birkaç dakika sonra sanal ortamı altında görünür. **Python ortamları** düğümünde **Çözüm Gezgini**. Sanal ortam varsayılan olarak etkin değildir, bu nedenle sağ tıklayın ve seçin **etkinleştirme ortam**.
::: moniker-end

::: moniker range=">=vs-2019"
### <a name="create-a-virtual-environment"></a>Sanal ortam oluştur

Doğrudan Visual Studio'da yeni bir sanal ortam şu şekilde oluşturabilirsiniz:

1. Sağ **Python ortamları** içinde **Çözüm Gezgini** seçip **ortam Ekle**, ya da seçin **ortam Ekle** gelen ortamlar açılan listesinde bir Python araç çubuğundaki aşağı açılır. İçinde **ortam Ekle** görüntülenirse, seçin iletişim **sanal ortam** sekmesinde:

    ![Sanal ortam sekmesinde ortam Ekle iletişim kutusu](media/environments/environments-add-virtual-1-2019.png)

1. Sanal ortam için bir ad belirtin, temel yorumlayıcıyı seçin ve konumunu doğrulayın. Altında **dosyasından paketleri yükleme**, yolunu sağlamanız bir *requirements.txt* isterseniz dosya.

1. İletişim kutusundaki diğer seçenekleri gözden geçirin:

    | Seçenek | Açıklama |
    | --- | --- |
    | Geçerli ortam ayarlayın | Ortam oluşturulduktan sonra seçili projeye yeni ortamda etkinleştirir. |
    | Yeni projeler için varsayılan ortam olarak ayarlayın | Otomatik olarak ayarlar ve tüm yeni projeler Visual Studio'da oluşturulan sanal ortamda etkinleştirir. Bu seçenek kullanıldığında, sanal ortamın belirli bir proje dışında bir konumda yerleştirilmelidir.  |
    | Python ortamları penceresinde görüntüleme | Açmak belirtir **Python ortamları** ortamı oluşturduktan sonra penceresi. |
    | Bu ortamın genel olarak kullanılabilir yap | Sanal ortamın genel bir ortamı olarak davranıp davranmadığını belirtir. Bu seçenek kullanıldığında, sanal ortamın belirli bir proje dışında bir konumda yerleştirilmelidir. |

1. Seçin **Oluştur** sanal ortam sonlandırmak için. Visual Studio ortamı yapılandırır ve gerekli tüm paketleri indirir bir ilerleme çubuğu görüntülenir. Tamamlandıktan sonra sanal ortamın etkinleştirilir ve görünür **Python ortamları** düğümünde **Çözüm Gezgini** ve **Python ortamları** penceresi projeyi içeren.

### <a name="activate-an-existing-virtual-environment"></a>Mevcut bir sanal ortam etkinleştir

Bir sanal ortam başka bir yerde zaten oluşturduysanız, proje için şu şekilde etkinleştirebilirsiniz:

1. Sağ **Python ortamları** içinde **Çözüm Gezgini** seçip **ortam Ekle**.

1. İçinde **Gözat** görüntülenen iletişim gidin ve sanal ortam içeren klasörü seçin ve **Tamam**. Visual Studio algılarsa bir *requirements.txt* dosya o ortamda, bu paketleri yüklenip yüklenmeyeceğini ister.

1. Birkaç dakika sonra sanal ortamı altında görünür. **Python ortamları** düğümünde **Çözüm Gezgini**. Sanal ortam varsayılan olarak etkin değildir, bu nedenle sağ tıklayın ve seçin **etkinleştirme ortam**.
::: moniker-end

### <a name="remove-a-virtual-environment"></a>Bir sanal ortam Kaldır

1. İçinde **Çözüm Gezgini**, sanal ortama sağ tıklayıp **Kaldır**.

1. Visual Studio kaldırın veya sanal ortamın silinmesini ister. Seçme **Kaldır** projeye kullanılamaz duruma getirir, ancak dosya sisteminde bırakır. Seçme **Sil** hem ortamı projeden kaldırır ve dosya sisteminden siler. Temel yorumlayıcı etkilenmez.

## <a name="view-installed-packages"></a>Paketleri yüklü görüntüle

Çözüm Gezgini'nde hızlı bir şekilde (içeri aktarıp ortamı etkin olduğunda bu paketleri kodunuzu kullanmak anlamına gelir) bu ortamda yüklü paketleri görüntülemek için belirli bir ortamın düğümünü genişletin:

![Çözüm Gezgini'nde bir ortam için Python paketleri](media/environments/environments-installed-packages.png)

::: moniker range="vs-2017"
Yeni paketler yüklemek için ortamı sağ tıklayıp **Python paketini Yükle** uygun geçiş yapmak için **paketleri** sekmesinde **Python ortamları** pencere. Bir arama girin (genellikle paket adı) terim ve Visual Studio eşleşen paketleri görüntüler.
::: moniker-end
::: moniker range=">=vs-2019"
Yeni paketler yüklemek için ortamı sağ tıklayıp **Python paketlerini Yönet** (veya Python araç paketi düğmesini kullanın) uygun geçiş yapmak için **paketleri** sekmede**Python ortamları** penceresi. İçinde bir kez **paketleri** sekmesinde, bir arama girin terim (genellikle paket adı) ve Visual Studio eşleşen paketleri görüntüler.
::: moniker-end

Visual Studio içinden gelen yüklenen paketler (ve bağımlılıkları) çoğu ortam için [Python paket dizinini (Pypı)](https://pypi.org), nerede kullanılabilir paketler için arama da yapabilirsiniz. Visual Studio'nun durum çubuğu ve çıkış penceresine yükleme hakkında bilgi gösterir. Bir paketi kaldırmak için sağ tıklayın ve seçin **Kaldır**.

Genellikle conda paket yöneticisini kullanan `https://repo.continuum.io/pkgs/` varsayılan olarak kanal, ancak diğer kanallar kullanılabilir. Daha fazla bilgi için [Yönet kanalları](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-channels.html) (docs.conda.io).

Görüntülenen girişler her zaman doğru olmayabilir ve yüklenmesi veya kaldırılması güvenilir veya kullanılabilir olmayabilir unutmayın. Visual Studio indirmeleri varsa, pip Paket Yöneticisi'ni kullanır ve gerektiğinde yükler. Visual Studio easy_install Paket Yöneticisi'ni de kullanabilirsiniz. Kullanarak yüklü paketleri `pip` veya `easy_install` komut satırından da görüntülenir.

Ayrıca Visual Studio kullanarak şu anda desteklemiyor Not `conda` conda ortamına paketlerini yükleyin. Kullanım `conda` komut satır yerine.

> [!Tip]
> Paket, kaynak kodu yerel bileşenlerin içerir. burada pip başarısız bir paketi yüklemek için ortak bir durum olduğunda  *\*.pyd* dosyaları. Yüklü Visual Studio gerekli sürümü, bu bileşenlerin pip derlenemiyor. Bu durumda görüntülenen hata iletisi **hata: Vcvarsall.bat bulunamıyor**. `easy_install` önceden derlenmiş ikili dosyaları, genellikle indirebildiğini Python'dan eski sürümlerine yönelik bir uygun derleyici indirebilirsiniz [ https://aka.ms/VCPython27 ](https://aka.ms/VCPython27). Daha fazla ayrıntı için ["vcvarsallbat bulmak alınamıyor", sorunlu ile nasıl](https://devblogs.microsoft.com/python/unable-to-find-vcvarsall-bat/) üzerinde Python araçları ekip blogu.

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio'da Python ortamlarını yönetme](managing-python-environments-in-visual-studio.md)
- [Bağımlılıklar için Requirements.txt dosyasını kullanma](managing-required-packages-with-requirements-txt.md)
- [Arama yolları](search-paths.md)
- [Python ortamları penceresi başvurusu](python-environments-window-tab-reference.md)
