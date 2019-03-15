---
title: Bulma ve uzantıları kullanma
ms.date: 01/30/2019
ms.topic: conceptual
f1_keywords:
- vs.ExtensionManager
helpviewer_keywords:
- install extensions
- install packages
- managing extensions visual studio
ms.assetid: 4ca92d93-31b9-47ef-8109-4a429d9e2ca3
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 8815e4cf58703efa0ab092f6030f6eeb22a813cd
ms.sourcegitcommit: 4ffb7be5384ad566ce46538032bf8561754c61a4
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2019
ms.locfileid: "57983396"
---
# <a name="find-and-use-visual-studio-extensions"></a>Visual Studio uzantıları bulma ve kullanma

Visual Studio uzantıları Visual Studio içinde çalıştırın ve yeni veya geliştirilmiş Visual Studio özellikleri sağlayan kod paketlerdir. Visual Studio uzantıları hakkında daha fazla bilgi bulabilirsiniz: [Visual Studio SDK](../extensibility/visual-studio-sdk.md).

::: moniker range="vs-2017"

Kullanım **Uzantılar ve güncelleştirmeler** yüklemek ve Visual Studio uzantıları yönetmek için iletişim kutusu. Açmak için **Uzantılar ve güncelleştirmeler** iletişim kutusunda seçin **Araçları** > **Uzantılar ve güncelleştirmeler**, veya tür **uzantıları** içinde **hızlı başlatma** arama kutusu.

::: moniker-end

::: moniker range=">=vs-2019"

Kullanım **uzantıları yönetme** yüklemek ve Visual Studio uzantıları yönetmek için iletişim kutusu. Açmak için **uzantıları yönetme** iletişim kutusunda seçin **uzantıları** > **uzantıları yönetme**. Veya, tür **uzantıları** içinde **hızlı başlatma** seçin ve arama kutusuna **uzantıları yönetme**.

::: moniker-end

![Visual Studio'daki uzantıları](media/finding-using-visual-studio-extensions/extensions-and-updates.png)

Sol bölmede o yüklendiğinden, Visual Studio Market'te mevcut kodlar tarafından uzantıları kategorilere ayıran (**çevrimiçi**) ve mevcut güncelleştirmeleri olanlar. **Dolaşım uzantısı Yöneticisi** herhangi bir makine veya Visual Studio örneğinde yükledim tüm Visual Studio uzantılarının bir listesini tutar. Sık kullandığınız uzantıların daha kolay bulmanızı sağlamak için tasarlanmıştır.

## <a name="find-visual-studio-extensions"></a>Visual Studio uzantıları bulma

Uzantılardan yükleyebileceğiniz [Visual Studio Market](https://marketplace.visualstudio.com/vs). Uzantılar; denetimler, örnekler, şablonlar, araçlar veya Visual Studio'ya işlevsellik katan diğer bileşenler olabilir. Visual Studio, VSIX paketi biçimindeki uzantıları destekler; bu proje şablonları içerir, öğe şablonları, **araç kutusu** öğeleri, yönetilen uzantı çerçevesi (MEF) bileşenleri ve VSPackages.

::: moniker range="vs-2017"

Ayrıca indirin ve MSI tabanlı uzantılar yükleyin ancak **Uzantılar ve güncelleştirmeler** iletişim kutusunu etkinleştirin veya devre dışı. Visual Studio Market VSIX hem de MSI uzantıları içerir.

::: moniker-end

::: moniker range=">=vs-2019"

Ayrıca indirin ve MSI tabanlı uzantılar yükleyin ancak **uzantıları yönetme** iletişim kutusunu etkinleştirin veya devre dışı. Visual Studio Market VSIX hem de MSI uzantıları içerir.

::: moniker-end

## <a name="install-or-uninstall-visual-studio-extensions"></a>Yükleme veya Visual Studio uzantıları kaldırma

::: moniker range="vs-2017"

İçinde **Uzantılar ve güncelleştirmeler**, yüklemek istediğiniz uzantıyı bulun. (Adı veya uzantı adının bir kısmını biliyorsanız, içinde arama yapabilirsiniz **arama** penceresi.) **İndir**'e tıklayın. Bu uzantı yüklenmek üzere zamanlandı. Visual Studio'nun tüm örneklerini kapatıldıktan sonra uzantınızı yüklenir.

Bağımlılıkları olan bir uzantıyı yüklemeye çalışırsanız, yükleyici bunların yüklenmiş olup olmadığını denetler. Bunlar yüklü değilse **Uzantılar ve güncelleştirmeler** iletişim kutusunda uzantıyı yükleyebilmeniz için önce yüklenmesi gereken bağımlılıklar listelenmiştir.

::: moniker-end

::: moniker range=">=vs-2019"

İçinde **uzantıları yönetme**, yüklemek istediğiniz uzantıyı bulun. (Adı veya uzantı adının bir kısmını biliyorsanız, içinde arama yapabilirsiniz **arama** penceresi.) **İndir**'e tıklayın. Bu uzantı yüklenmek üzere zamanlandı. Visual Studio'nun tüm örneklerini kapatıldıktan sonra uzantınızı yüklenir.

Bağımlılıkları olan bir uzantıyı yüklemeye çalışırsanız, yükleyici bunların yüklenmiş olup olmadığını denetler. Bunlar yüklü değilse **uzantıları yönetme** iletişim kutusunda uzantıyı yükleyebilmeniz için önce yüklenmesi gereken bağımlılıklar listelenmiştir.

::: moniker-end

Bir uzantıyı kullanmayı bırakmak isterseniz devre dışı bırakabilir veya kaldırabilirsiniz. Bir uzantı devre dışı bırakıldığında yüklü kalır, ancak etkin değildir. Yalnızca VSIX uzantılarını devre dışı bırakabilirsiniz; MSI kullanarak yüklenmiş uzantıları sadece kaldırılabilir. Uzantı bulun ve tıklatın **kaldırma** veya **devre dışı**. Devre dışı bırakılmış bir uzantıyı kaldırmak için Visual Studio'yu yeniden başlatın.

## <a name="per-user-and-administrative-extensions"></a>Kullanıcı başına ve yönetim uzantıları

Uzantıların çoğu kullanıcı başına uzantılar ve yüklenmiş *%LocalAppData%\Microsoft\VisualStudio\\< Visual Studio sürümü\>\Extensions\\*  klasör. Bazı uzantılar yönetimsel uzantıları ve yüklenmiş *\<Visual Studio yükleme klasörü > \Common7\IDE\Extensions\\* klasör.

Hata veya kötü amaçlı kod içerebilecek uzantıları karşı sisteminizi korumak için yalnızca Visual Studio normal kullanıcı izinleriyle çalıştırıldığında yüklemek için kullanıcı başına uzantılar kısıtlayabilirsiniz. Başka bir deyişle, Visual Studio Yönetici kullanıcı izinleriyle çalıştırdığınızda kullanıcı başına uzantılar devre dışı bırakılır. Bunu yapmak için uzantıları seçenekleri sayfasına gidin (**Araçları** > **seçenekleri** > **ortam**  >   **Uzantıları**). NET **bağımsız kullanıcı uzantılarının yönetici olarak çalışırken yük** onay kutusunu işaretleyin ve ardından Visual Studio'yu yeniden başlatın.

## <a name="automatic-extension-updates"></a>Otomatik uzantı güncelleştirmeleri

Uzantılar, Visual Studio Market'te yeni bir sürümü kullanılabilir olduğunda otomatik olarak güncelleştirilir. Uzantının yeni sürümünü algılanır ve arka planda yüklü. Visual Studio'nun bir sonraki açışınızda, uzantıyı yeni sürümünü çalıştırırsınız.

Otomatik Güncelleştirmeler devre dışı bırakmak istiyorsanız, tüm uzantıları veya yalnızca belirli uzantılara özelliği devre dışı bırakabilirsiniz.

::: moniker range="vs-2017"

- Tüm uzantılar için Otomatik Güncelleştirmeler devre dışı bırakmayı tercih **Uzantılar ve güncelleştirmeler ayarlarınızı değiştirin** bağlantısını **Uzantılar ve güncelleştirmeler** iletişim. İçinde **seçenekleri** iletişim kutusunun işaretini kaldırın **uzantıları otomatik olarak güncelleştir**.

- Belirli bir uzantı için Otomatik Güncelleştirmeler devre dışı bırakmak için işareti kaldırın **bu uzantıyı otomatik olarak güncelleştir** seçeneği uzantının ayrıntıları bölmesinde sağ alt tarafında **Uzantılar ve güncelleştirmeler** iletişim.

::: moniker-end

::: moniker range=">=vs-2019"

- Tüm uzantılar için Otomatik Güncelleştirmeler devre dışı bırakmayı tercih **uzantıları için ayarlarınızı değiştirmeniz** bağlantısını **uzantıları yönetme** iletişim. İçinde **seçenekleri** iletişim kutusunun işaretini kaldırın **uzantıları otomatik olarak güncelleştir**.

- Belirli bir uzantı için Otomatik Güncelleştirmeler devre dışı bırakmak için işareti kaldırın **bu uzantıyı otomatik olarak güncelleştir** seçeneği uzantının ayrıntıları bölmesinde sağ alt tarafında **uzantıları yönetme** iletişim.

::: moniker-end

## <a name="extension-crash-and-unresponsiveness-notifications"></a>Uzantı kilitlenme ve yanıt vermeyi durdurma sorununa bildirimleri

Visual Studio, uzantı bir önceki oturumu sırasında içindeki bir kilitlenme konusuydu gerçeğe aykırı size bildirir. Visual Studio kilitleniyor, özel durum yığını depolar. Visual Studio başlatılır, sonraki açışınızda yaprak ile başlayan ve temel çalışma yığını inceler. Visual Studio çerçeve uzantı yüklü ve etkin bir parçası olan bir modüle ait olduğunu belirlerse, bir bildirim gösterilir.

Uzantı yanıt vermediği UI neden olan gerçeğe aykırı visual Studio ayrıca size bildirir.

Bu bildirimleri gösterilirken, bildirim Yoksay veya aşağıdaki eylemlerden birini gerçekleştirin:

::: moniker range="vs-2017"

- Seçin **bu uzantıyı devre dışı**. Visual Studio, uzantıyı devre dışı bırakır ve devre dışı bırakma etkinleşmesi için sisteminizi yeniden başlatması gerek olup olmadığını bildirir. Uzantı yeniden etkinleştirebilirsiniz **Uzantılar ve güncelleştirmeler** istiyorsanız iletişim kutusu.

::: moniker-end

::: moniker range=">=vs-2019"

- Seçin **bu uzantıyı devre dışı**. Visual Studio, uzantıyı devre dışı bırakır ve devre dışı bırakma etkinleşmesi için sisteminizi yeniden başlatması gerek olup olmadığını bildirir. Uzantı yeniden etkinleştirebilirsiniz **uzantıları yönetme** istiyorsanız iletişim kutusu.

::: moniker-end

- Seçin **bu iletiyi bir daha gösterme**.

  - Bildirim önceki bir oturumda bir kilitlenme ilgiliyse, Visual Studio artık bu uzantıyla ilişkili bir kilitlenme olduğunda bir uyarı gerçekleşir gösterir. Bu uzantı veya kilitlenme veya diğer uzantıları ile ilişkilendirilebilen yanıt vermeyi durdurma sorununa yanıt vermeyi durdurma sorununa ilişkilendirilebilir zaman visual Studio hala bildirimleri göster.
  - Bildirim yanıt vermeyi durdurma sorununa ilgiliyse, bu uzantının yanıt vermeyi durdurma sorununa ile ilişkili olduğunda, IDE artık bir bildirimi gösterir. Visual Studio hala bu uzantı için kilitlenme ile ilgili bildirimleri ve diğer uzantılar için kilitlenme ve yanıt vermeyi durdurma sorununa ilgili bildirimleri de gösterilir.

- Seçin **daha fazla bilgi edinin** bu sayfaya geliyor.

- Seçin **X** bildirimi kapatmak için bildirim sonunda düğmesi. Gelecekteki bir kilitlenme veya kullanıcı Arabirimi yanıt vermeyi durdurma sorununa ile ilişkilendiriliyor uzantısı örneklerinin yeni bir bildirim görüntülenir.

> [!NOTE]
> Bir kullanıcı Arabirimi yanıt vermeyi durdurma sorununa veya kilitlenme bildirimi yalnızca bir uzantının modüllerinin yığında UI yanıt vermiyor veya kilitlenme ortaya çıktığında anlamına gelir. Bu mutlaka uzantısı sorunlu olduğunu gelmez. Bu uzantı, yanıt vermeyen kullanıcı Arabirimi veya kilitlenme sırayla sonuçlandı Visual Studio'nun bir parçası olan kod adlı mümkündür. Ancak, bildirim yine de kullanıcı Arabirimi yanıt vermeyi durdurma sorununa veya kilitlenme sonuçlanan uzantı sizin için önemli değilse yararlı olabilir. Bu durumda, uzantıyı devre dışı kullanıcı Arabirimi yanıt vermeyi durdurma sorununa veya kilitlenme gelecekte üretkenliğinizi etkilemeden önler.

## <a name="sample-master-copies-and-working-copies"></a>Örnek ana kopyalar ve çalışma kopyaları

Çevrimiçi bir örneği yüklediğinizde, çözüm iki konumda depolanır:

- Belirtilen konumda bir çalışma kopyası depolanır **yeni proje** iletişim kutusu.

- Ayrı bir ana kopya bilgisayarınızda depolanır.

::: moniker range="vs-2017"

Kullanabileceğiniz **Uzantılar ve güncelleştirmeler** penceresi örneklerle ilgili şu görevleri gerçekleştirebilirsiniz:

::: moniker-end

::: moniker range=">=vs-2019"

Kullanabileceğiniz **uzantıları yönetme** penceresi örneklerle ilgili şu görevleri gerçekleştirebilirsiniz:

::: moniker-end

- Yüklediğiniz örneklerin ana kopyalarını listeleyin.

- Bir örneğin ana kopyasını devre dışı bırakın veya kaldırın.

- Örnek Paketleri (bir teknoloji veya özellik ile ilgili örnek koleksiyonları) yükleyin.

- Tek tek çevrimiçi örnekleri yükleyin. (Ayrıca bunu yapabilirsiniz **yeni proje** iletişim kutusu.)

- Yüklü örnekler için kaynak kodu değişiklikleri yayımlandığında güncelleştirme bildirimlerini görüntüleyin.

- Bir güncelleştirme bildirimi olduğunda yüklü bir örneğin ana kopyasını güncelleştirin.

::: moniker range="vs-2017"

## <a name="installing-without-using-the-extensions-and-updates-dialog-box"></a>Uzantılar ve güncelleştirmeler iletişim kutusunu kullanmadan yükleme

İçinde paketlenmiş Uzantılar *.vsix* dosyaları kullanılabilir Visual Studio Market dışındaki konumlarda. **Uzantılar ve güncelleştirmeler** iletişim kutusunda, bu dosyaları silemese ancak yükleyebileceğiniz bir *.vsix* dosyasına çift veya bir dosya seçip tuşuna basarak dosya **Enter**anahtarı. Bundan sonra yalnızca yönergeleri izleyin. Uzantı yüklendiğinde, kullanabileceğiniz **Uzantılar ve güncelleştirmeler** etkinleştirmek, devre dışı bırakmak veya kaldırmak için iletişim kutusu.

## <a name="extension-types-not-supported-by-the-extensions-and-updates-dialog-box"></a>Uzantı türleri Uzantılar ve güncelleştirmeler iletişim kutusu tarafından desteklenmiyor

Visual Studio Microsoft Installer (MSI) tarafından yüklenen Uzantıları desteği devam eder ancak ile **Uzantılar ve güncelleştirmeler** yapmadan iletişim kutusu.

> [!TIP]
> MSI tabanlı bir uzantı içeriyorsa bir *extension.vsixmanifest* dosya, uzantısı görünür **Uzantılar ve güncelleştirmeler** iletişim kutusu.

::: moniker-end

::: moniker range=">=vs-2019"

## <a name="installing-without-using-the-manage-extensions-dialog-box"></a>Uzantıları Yönet iletişim kutusunu kullanmadan yükleme

İçinde paketlenmiş Uzantılar *.vsix* dosyaları kullanılabilir Visual Studio Market dışındaki konumlarda. **Uzantıları yönetme** iletişim kutusunda, bu dosyaları silemese ancak yükleyebileceğiniz bir *.vsix* dosyasına çift veya bir dosya seçip tuşuna basarak dosya **Enter** anahtarı. Bundan sonra yalnızca yönergeleri izleyin. Uzantı yüklendiğinde, kullanabileceğiniz **uzantıları yönetme** etkinleştirmek, devre dışı bırakmak veya kaldırmak için iletişim kutusu.

## <a name="extension-types-not-supported-by-the-manage-extensions-dialog-box"></a>Uzantıları Yönet iletişim kutusu tarafından desteklenmeyen uzantı türleri

Visual Studio Microsoft Installer (MSI) tarafından yüklenen Uzantıları desteği devam eder ancak ile **uzantıları yönetme** yapmadan iletişim kutusu.

> [!TIP]
> MSI tabanlı bir uzantı içeriyorsa bir *extension.vsixmanifest* dosya, uzantısı görünür **uzantıları yönetme** iletişim kutusu.

::: moniker-end