---
title: Visual Studio SDK sözlüğü | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- glossary [Visual Studio SDK]
ms.assetid: b64d432b-c39b-4904-ad18-3c3218b6e3aa
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 6157b4bc3537a4f88feb91d512241451b8324ba7
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62838912"
---
# <a name="visual-studio-sdk-glossary"></a>Visual Studio SDK sözlüğü
Bu sözlük kullanılan terimlerin tanımları sağlar, [!INCLUDE[vsipsdk](../extensibility/includes/vsipsdk_md.md)] belgeleri.

## <a name="terms"></a>Koşulları
 yardımcı program uygulaması, sürücü veya bir birincil uygulamaya eklenen diğer yazılım eklentisi. Visual Studio tümleşik geliştirme ortamında (IDE) bir eklenti IDE özelliklerini genişleten bir Otomasyon tabanlı uygulamadır.

 genişletilebilirlik modeli olarak Visual Studio'nun önceki sürümlerinde bilinen Otomasyon modelinin otomasyon modeli, size bir programlama arabirimi erişmek için temel alınan yordamları o sürücüye IDE ' dir. Eklentiler, sihirbazlar ve makroları denetimi otomasyon modeli nesnelerini kullanın veya IDE genişletmek.

 UI bağlamı UI komut veya gibi bir araç çubuğu öğelerinin görünürlüğü GUID ilişkilendirmesini komutu. Bir pencereye bağlı değildir komut UI bağlamı seçim bağlamını olmamasıdır.

 Komut UI bağlamı için kullanılabilir:

- Belirli bir pencere etkin olduğunda görüntülenen bir araç çubuğuna bir GUID atayın.

- Bir GUID yüklemek veya bir VSPackage'ı çalıştırmak zorunda kalmadan bir komut kullanılabilirliğini atayın.

- Etkin tuş bağlama etkilemek için bir GUID atayın.

- Makro kayıt işlemini etkinleştirmek için bir GUID atayın.

- Hata ayıklama modunu etkinleştirin veya tasarım ve bir düzenleyicide çalışma modu arasında geçiş yapmak için bir GUID atayın.

  Bileşen bir uygulamanın işlevselliğini parçası yazılımın uygulaması hakkında önceden mevcut olan tüm bilgilere sahip uygulama olmadan yapılan bir yazılım parçasıdır. Bir bileşen ve uygulama arasındaki iletişimi yalnızca OLE stili arabirimleri ' dir.

  Bileşen Yöneticisi bir hizmeti, `SOleComponentManager`, üst düzey bileşenleri için olmayan kullanıcı arabirimi işbirliği hizmetleri sağlayan. `SOleComponentManager` Hizmet uygular `IOleComponentManager` arabirimi.

  Bileşen UI A manager hizmeti, `SOleComponentUIManager`, kullanıcı arabirimi koordinasyon hizmeti sunar. `SOleComponentUIManager` Hizmet uygular `IOleComponentUIManager` ve `IOleInPlaceComponentUIManager` arabirimleri.

  İçerik Paketi bir `IVsUserContext` bağlı bir ortam bileşenine nesnesi (COM nesnesi). Arama anahtar sözcükleri, bu nesne tutan **F1** anahtar sözcükleri ve bileşen ilişkili öznitelikleri. İçerik paketleri ayrıca onlara bağlı tüm üzere paketleri gelin.

  içerik sağlayıcısı bir bileşeni IDE'de kendisiyle ilişkilendirilmiş bir içerik paketi vardır. Araç penceresi, düzenleyici veya proje hiyerarşisi böyle bileşenleri içerir.

  Tasarımcı (forms, düğmeleri ve diğer denetimleri) kullanıcı arabirimi öğelerini düzenleme olanağı sağlayan bir programlama arabirimi.

  Temel alınan verileri bir belgenin bir dünyada Kapsüllenen DocData bir COM nesnesi belge/görünüm ayrımı olduğu (örneğin, metin düzenleyici durumunda bu tüm metin düzenleyicisi görünümleri alttaki metin arabelleğini olacaktır). Bu nesne EditorFactory vermiyorsa, kendi adına bir IDE üretir. Bu nesnenin veri kalıcılığı yönetmek için sorumluluğundadır ve Paylaşım semantiği çoklu seçim yapmak için bu görünümlerini aynı `DocData`. Varsa `DocData` nesnesi `IOleCommandTarget` arabirimi dahil komut yönlendirme UIShell içinde.

  DocObject teknolojisi, ana bilgisayar tarafından sağlanan bir çerçevesinde UI barındırmak için kullanılır. Daha açık belirtmek gerekirse bu terim herhangi destekleyen eklemeye kadar başvuruyor `IOleDocument` ve ilgili arabirimleri. Bu teknoloji, bir uygulama ayrıntısı COM belgelerin, araç pencerelerinde ve Visual Basic 5.0, Visual Basic 6.0 ve benzeri ActiveX tasarımcılarda gibi birçok olası uygulama vardır.

  Belgenin bir bütün olarak genel olarak başvurmak için kullanılan belge — hem `DocData` ve `DocView`. Örneğin, bir DocumentFrame içeren bir `DocView`, ancak aynı zamanda bir başvuru tutar `DocData` Kalıcılık işlemek için.

  DocView DocObject/ekleme/görüntüleme ve arka plandaki işlemek için kullanıcı ile etkileşim WindowPane `DocData`. Kullanıcılar yoksa avantajından parçası olan belge/görünüm ayrımı `DocObject` arabirimi tasarım. Kullanıcılar daha soyut (ve daha az resmileştirilmiş) bir kavram olarak bilinen temel alınan verilerin kullanmak yerine bir görünüm olarak görev yapacak bir tüm DocObject kullanın `DocData`. `DocView` nesneler her zaman belge çerçeve nesneleriyle IDE (MDI alt pencereleri) gömülüdür.

  DTE `DTE` (geliştirme araçları genişletilebilirliği) nesne, program aracılığıyla otomatikleştirmek ve IDE'yi genişletme olanak tanıyan Visual Studio Otomasyon modelinde en üst erişim noktasıdır.

  IDE tarafından uygulanan ve arama anahtar sözcüğü bir listesini görüntüleyen dinamik Yardım penceresi araç penceresi veya **F1** Yardım konuları.

  Düzenleyici uygulayan kodu (sınıf, CLSID) `DocView`. Ayrıca uygulayan `DocData` görüntüle ve veri ayırma destekleniyorsa.

  değiştiren bir uzantı özelliği özelleştirir ve bir IDE'ye ekler. VSPackages ve Otomasyon modelini kullanarak uzantıları oluşturduğunuz.

  dış düzenleyici için Microsoft Word gibi IDE'nin belirli olmayan bir düzenleyici. Bu, kendi mekanizmalar aracılığıyla kaydedilen ve IDE dışında kullanılabilir. Bu düzenleyici eklenebilir, bir pencere IDE içinde görünür. Katıştırılmış olamaz, ayrı bir üst düzey pencere oluşturulur.

  Hiyerarşi ağacı özellikler kümesi ile ilişkili her düğüm düğüm.

  Engelleyici olmayan bir üst düzey pencere kullanır ve etkili bir şekilde bir tek başına uygulama penceresi çalışabilir, ancak bir işlem içi nesnesi olarak uygulanan bağımsız en üst düzey bir bileşeni. Bu nedenle, bağımsız bir üst düzey bileşen oluşur ve ileti döngüsü Hizmetleri IDE ile koordine etmek gerekir. İşlem içi nesneleri kendi ileti döngüsü yoktur.

  bilgi sağlayıcısı bilgi sağlayıcısı olan anahtar sözcük arayın ve konuları biçiminde dönmesini sağlayan bir modülü `IVsUserContextItem` nesneleri. Sağlamak üzere **F1** ve öğeleri bilgi sağlayıcısı için arama anahtar sözcüğü, derlenmiş Yardım dosyanızı kaydedin (*. HxS*) sistemi. Dinamik Yardım penceresi görüntülenir ve kullanıcı olup olmadığını gösterilen konuların listesini Yardım konularda bu dosyalardaki **F1**.

  Bileşen bir VSPackage'ı uygulayan bir nesne yerinde `IOleInPlaceComponent` görsel olarak IDE tarafından sahip olunan bir belge penceresi içinde bulunan bir pencereyi yönetmek için arabirim. Yerinde bileşenler standart OLE menü-birleştirme içinde yer yok; Bunun yerine, kendi kullanıcı arabirimi öğeleri IDE'ye tümleştirin.

  Yerinde bileşenler iki tür vardır: sabit yerinde bileşenler ve bileşen denetimleri.

  Menüleri, araç çubukları ve doğrudan IDE'ye oluşturuldukları varsa olarak görünen IDE'nin, kullanıcı arabirimine sıkı bir şekilde tümleştirilmiş komutları sabit yerinde bileşenler vardır.

  Bileşen denetimleri herhangi bir IDE'ye tümleşik kendi kullanıcı arabirimi öğeleri gerekmez; Bunun yerine, IDE'nin menüleri, komutları ve araç çubuklarını kullanın. Örneğin, bir formda katıştırılmış zengin metin denetim içinde seçilen bir sözcük kalın kalın komutu kullanılabilir. Ancak, dinamik olarak yüklenen bileşenin özel kullanıcı Arabirimi öğeleri gösterilecek bileşeni denetimleri isteyebilir.

  Metni İşaretleme ve renklendirme gibi kod düzenleyicilerinden bilgisayar dil özellikleri uygulamak için VSPackage geliştiricilerin veren dil hizmeti bir dizi nesne.

  Çeşitli dosyalar projesi herhangi bir projede olmayan açık dosyaları barındırmak için kullanılan proje. Bu projede öğelerin listesini kalıcı değil.

  COM nesneleri uygulayan veya proje projeleri oluşan hiyerarşi nesnelerin `IVsHierarchy` arabirimi.

  Projeye özgü Tasarımcı veya düzenleyici bir Tasarımcısı, bağımsız olarak proje türü kullanılamaz. Tüm projeye özgü tasarımcılar, kayıt defterinde Düzenleyici fabrikası bilgilerini girmeniz gerekir. Belirli bir dosya türü belirli bir projeyi açtığınızda IDE Tasarımcı örneği oluşturabilir.

  Proje türü penceresi bir pencere öğesi ve şu anda etkin proje hiyerarşisi, sürekli genel seçimi bağlamdan izler. Proje türü pencerelerini kullanma `SVsTrackSelectionEx` hizmet IDE değişiklikleri uyarı ve geri bildirim kullanıcıya göstermek için. Çözüm Gezgini, bir proje türü penceresi örneğidir.

  Özellikler penceresinde eski özellik tarayıcısı.

  başvuru tabanlı projeler için projeyi aynı dizinde dosyaları gerektirmeyen bir proje. Bunun yerine, dosyalara başvuruları ilişkisiz diğer dizinlerden depolanan ve proje tarafından korunur.

  IDE tüm açık belgelerin listesini tutar çalıştırılan Belge tablosu iç yapısı. Listenin bellek olup olmadığını belgeler şu anda düzenlenmekte olan bağımsız olarak tüm açık belgeleri içerir. Kaydedilen, düzenleyici, proje dosyalarında veya ana proje dosyası (örneğin, *.vcproj) açılan saklı yordamları da dahil olmak üzere herhangi bir öğeyi bir belgedir.

  Seçim bağlamını her pencere IDE içindeki ayrıntılarını bir parçasıdır ve etkin seçimleri izlemek için kullanılan verileri. Seçim bağlamını oluşur:

- İşaretçi `IVsHierarchy` proje hiyerarşisi arabirimi

- Proje öğesi öğe tanımlayıcısı.

- İşaretçi `ISelectionContainer` arabirimi etkin nesneler için erişim özellikleri sağlar.

- Öğe değerleri dizisi.

  Bir sözleşme tek bir COM nesnesi içinde bulunduğu bir COM arabirimleri kümesi için hizmet. GUID ile tanımlanır, bir hizmet oluşturduğunuzda, hizmetin ölçeğini taşıyan COM arabirimleri kümesi tanımlar. COM nesneleri, birbirleriyle iletişim kurması için hizmetlerini kullanın.

  Çözüm grup ilgili projeleri ile bir kullanıcı çalışıyor.

  Standart Tasarımcısı proje türünü bağımsız olarak kullanılabilecek bir tasarımcı. Tüm standart tasarımcılar, kayıt defterinde Düzenleyici fabrikası bilgilerini girmeniz gerekir. Belirli bir uzantıya sahip bir dosyayı açtığınızda IDE Tasarımcı örneği oluşturabilir. Verileri bir dosyaya kalıcı gerekir.

  Standart Düzenleyici herhangi belirli bir proje türünde bağımsız olarak kullanılabilir bir düzenleyici. Bu tür düzenleyicileri kayıt defterinde kayıtlı EditorFactories vardır. Bu, bulun ve düzenleyici çağırmak IDE sağlar.

  Bir ekleme standart işletim sistemi Düzenleyicisi Visual Studio özgü değildir. İyi bilinen Win32 anahtarlar kullanılarak kaydedilmiştir (örneğin, Win32 Gezgini çağırmak nasıl bilir). Böyle bir düzenleyici eklenebilir, düzenleyici hala kullanışlılığını IDE'de gösterilir. Aksi takdirde, ayrı bir üst düzey pencere gibi düzenleyiciler için oluşturulur.

  üzere paketi bir `IVsUserContext` nesne bağlı bir içerik paketi için. Arama anahtar sözcükleri, nesne tutan **F1** anahtar sözcükleri ve IDE bileşeni içinde bir seçim için öznitelikler. Üzere bir komut araç penceresi ya da bir anahtar sözcüğü bir düzenleyicide örneklerindendir.

  IDE tarafından uygulanan ve Etkin Görevler listesini görüntüleyen görev listesi araç penceresi.

  metin arabelleği ortak ad nesne için `VSTextBuffer`.

  Nesne için metin görünümü ortak ad `VSTextView`.

  IDE kullanıcı arabirimi ile sıkı bir şekilde koordine bir geçici açılır pencere olarak çalışır aracı en üst düzey bileşenini bileşeni. Üst düzey bağımsız bileşenler gibi aracı en üst düzey bileşenleri de oluşur ve ileti döngüsü Hizmetleri IDE ile koordine etmeleri gerekir.

  Engelleyici olmayan bir üst düzey pencere IDE bir pencerenin istemci alanını yerine yönetir en üst düzey bileşen bir VSPackage nesnesi. Üst düzey bileşenleri uygulamak `IOleComponent` boşta kalma süresi için ileti döngüsü Hizmetleri erişim gibi yararlanmak için arabirim.

  Görünür ve odağa sahip kullanıcı Arabirimi etkin bir VSPackage nesne.

  Uygulayan UI hiyerarşi bir COM Nesne `IVsUIHierarchy` bir hiyerarşinin görüntü izin vermek için arabirim. UI hiyerarşi penceresinde uygulayan `ISelectionContainer` Özellikler penceresinde güncelleştirmek için arabirim; diğer proje türü windows isterseniz bu uygulama kullanabilirsiniz.

  VSCT Visual Studio komut tablosu. .Vsct dosyası yerleştirme ve menüler, araç çubukları ve XML biçiminde komutları davranışları hakkında bilgi içerir.

  VSPackage'ı bir veya daha fazla aşağıdaki öğe katılarak Visual Studio IDE genişleten yazılım yüklenebilir bir parçasıdır: kullanıcı arabirimi, hizmetleri, proje türleri veya Düzenleyicisi/Tasarımcısı. VSPackage'ı uygulayan bir COM nesnesi oluşur `IVsPackage` arabirimi ve seçim ve diğer özellikleri desteklemek için diğer arabirimleri uygulayan bir veya daha fazla diğer COM nesneleri. Ayrıca, bir VSPackage belirli kayıt gereksinimleri vardır.