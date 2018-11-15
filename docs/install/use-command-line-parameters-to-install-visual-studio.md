---
title: Komut satırı parametrelerini kullanarak Visual Studio'yu yükleme
description: Komut satırı parametreleri denetlemek veya Visual Studio yüklemenizi özelleştirmek için kullanmayı öğrenin.
ms.custom: ''
ms.date: 05/07/2018
ms.technology: vs-acquisition
ms.prod: visual-studio-dev15
ms.topic: conceptual
f1_keywords:
- command-line parameters
- switches
- command prompt
ms.assetid: 480f3cb4-d873-434e-a8bf-82cff7401cf2
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 55cf6eb2a46f707e5c0c20633ab92ac2304214ec
ms.sourcegitcommit: 20d1b9a5bf041bb28453501eb63bc0537a8e4f54
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/14/2018
ms.locfileid: "51645204"
---
# <a name="use-command-line-parameters-to-install-visual-studio-2017"></a>Visual Studio 2017'yi yüklemek için komut satırı parametrelerini kullanma

Visual Studio 2017'yi bir komut isteminden yüklediğinizde, denetim ya da yüklemeyi özelleştirmek için çeşitli komut satırı parametreleri kullanabilirsiniz. Komut satırından aşağıdaki eylemleri gerçekleştirebilirsiniz:

- Yükleme önceden belirli seçenekleri ile başlayın.
- Yükleme işlemini otomatik hale getirin.
- Daha sonra kullanmak için yükleme dosyalarından oluşan bir önbellek (Düzen) oluşturun.

Komut satırı seçenekleri, indirme işlemini başlatan küçük (yaklaşık 1 MB) dosya kurulum önyükleyici ile birlikte kullanılır. Önyükleyici Visual Studio sitesinden indirdiğinizde başlatıldığında ilk yürütülebilir ' dir. Doğrudan bir bağlantı için en son sürüm önyükleyici için yüklemekte olduğunuz ürün sürümünü almak için aşağıdaki bağlantıları kullanın:

- [Visual Studio 2017 Enterprise](https://visualstudio.microsoft.com/thank-you-downloading-visual-studio/?sku=enterprise&rel=15?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=link+cta&utm_content=download+commandline+parameters+vs2017)
- [Visual Studio 2017 Professional](https://visualstudio.microsoft.com/thank-you-downloading-visual-studio/?sku=professional&rel=15?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=link+cta&utm_content=download+commandline+parameters+vs2017)
- [Visual Studio 2017 Community](https://visualstudio.microsoft.com/thank-you-downloading-visual-studio/?sku=community&rel=15?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=link+cta&utm_content=download+commandline+parameters+vs2017)

## <a name="list-of-command-line-parameters"></a>Komut satırı parametrelerinin listesi

 Visual Studio komut satırı parametreleri büyük/küçük harfe duyarsızdır.

> Sözdizimi: `vs_enterprise.exe [command] <options>...`

(Değiştir `vs_enterprise.exe` ürün sürümü için uygun şekilde yüklemekte.)

>[!TIP]
> Visual Studio 2017'yi yüklemek için komut satırını kullanmayı daha fazla örnek için bkz. [komut satırı parametresi örnekleri](command-line-parameter-examples.md) sayfası.)

| **Komutu** | **Açıklama** |
| ----------------------- | --------------- |
| (boş) | Ürün yükler. |
| `modify` | Yüklü bir ürün değiştirir. |
| `update` | Yüklü bir ürün güncelleştirir. |
| `repair` | Yüklü bir ürün onarır. |
| `uninstall` | Yüklü bir ürün kaldırır. |
| `export` | **Yeni 15.9**: yükleme seçimi bir yükleme yapılandırma dosyasına dışarı aktarır. |

| **Yükleme seçeneği** | **Açıklama** |
| ----------------------- | --------------- |
| `--installPath <dir>` | Yükleme dizini örneği üzerinde işlem yapmak için. Yükleme komutu için budur **isteğe bağlı** ve örneğin yüklü olduğu. Diğer komutlar için budur **gerekli** ve önceden yüklenmiş örnek yüklendiği. |
| `--addProductLang <language-locale>` | **İsteğe bağlı**: bir yükleme sırasında veya değiştirme işlemi, bu ürünü yüklü UI dil paketlerini belirler. Bu, birden çok dil paketlerini eklemek için komut satırında birden çok kez görünebilir. Yoksa, yükleme makine yerel ayarı kullanır. Daha fazla bilgi için [dil yerel ayarlar listesini](#list-of-language-locales) bu sayfadaki bölümü.|
| `--removeProductLang <language-locale>` | **İsteğe bağlı**: bir yükleme sırasında veya değiştirme işlemi, bu ürün kaldırılacak kullanıcı Arabirimi dil paketlerini belirler. Bu, birden çok dil paketlerini eklemek için komut satırında birden çok kez görünebilir. Daha fazla bilgi için [dil yerel ayarlar listesini](#list-of-language-locales) bu sayfadaki bölümü.|
| `--add <one or more workload or component IDs>` | **İsteğe bağlı**: bir veya daha fazla iş yükü veya Bileşen kimlikleri eklemek için. Yapıtın gerekli bileşenleri, değil önerilen veya isteğe bağlı bileşenler yüklenir. Genel olarak aracılığıyla ek bileşenler denetleyebilirsiniz `--includeRecommended` ve/veya `--includeOptional`. Birden çok iş yükleri veya bileşenleri eklemek için yineleyin `--add` komutu (örneğin, `--add Workload1 --add Workload2`). Daha ayrıntılı denetim için eklediğiniz `;includeRecommended` veya `;includeOptional` kimliği (örneğin, `--add Workload1;includeRecommended` veya `--add Workload2;includeRecommended;includeOptional`). Daha fazla bilgi için [iş yükü ve Bileşen kimlikleri](workload-and-component-ids.md) sayfası. Bu seçenek gerekli olarak yineleyebilir.|
| `--remove <one or more workload or component IDs>` | **İsteğe bağlı**: bir veya daha fazla iş yükü veya Bileşen kimlikleri kaldırmak için. Daha fazla bilgi için müşterilerimize [iş yükü ve Bileşen kimlikleri](workload-and-component-ids.md) sayfası. Bu seçenek gerekli olarak yineleyebilir.|
| `--in <path>` | **İsteğe bağlı**: URI veya bir yanıt dosyasının yolu.  |
| `--all` | **İsteğe bağlı**: tüm iş yüklerinin ve bileşenlerin bir ürünün yükleneceğini. |
| `--allWorkloads` | **İsteğe bağlı**: tüm iş yüklerinin ve bileşenlerin, hiçbir önerilen veya isteğe bağlı bileşenleri yükler. |
| `--includeRecommended` | **İsteğe bağlı**: yüklü olan tüm iş yükleri için önerilen bileşenleri, ancak isteğe bağlı bileşenler içerir. Belirtilen iş yükleri ile birlikte `--allWorkloads` veya `--add`. |
| `--includeOptional` | **İsteğe bağlı**: isteğe bağlı bileşenler yüklü olan tüm iş yükleri için ancak önerilen bileşenleri içerir. Belirtilen iş yükleri ile birlikte `--allWorkloads` veya `--add`.  |
| `--quiet, -q` | **İsteğe bağlı**: yükleme gerçekleştirirken herhangi bir kullanıcı arabirimi gösterme. |
| `--passive, -p` | **İsteğe bağlı**: kullanıcı arabirimini görüntüler, ancak kullanıcı etkileşimi isteme. |
| `--norestart` | **İsteğe bağlı**: ile varsa, komutları `--passive` veya `--quiet` otomatik olarak makine (gerekirse) yeniden başlatmaz.  Bu ne sayılır `--passive` ya da `--quiet` belirtilir.  |
| `--nickname <name>` | **İsteğe bağlı**: Bu takma ad atamak için yüklü bir ürün için tanımlar. Takma ad 10 karakterden uzun olamaz.  |
| `--productKey` | **İsteğe bağlı**: Bu ürün anahtarı yüklü bir ürün için tanımlar. Şunlardan oluşur 25 alfasayısal karakter ya da biçimi `xxxxx-xxxxx-xxxxx-xxxxx-xxxxx` veya `xxxxxxxxxxxxxxxxxxxxxxxxx`. |
| `--help, --?, -h, -?` | Bu sayfanın çevrimdışı bir sürümünü görüntüler. |
| `--config <path>` | **15.9, isteğe bağlı olarak yeni**: bir yükleme sırasında veya değiştirme işlemi, bu iş yükleri belirler ve bileşenleri eklemek için temel bir önceden kaydedilmiş yükleme yapılandırma dosyası. . Bu işlem eklenebilir ve bunlar dosyasında mevcut değilse herhangi bir iş yükü veya bileşen kaldırmaz. Ayrıca, ürün için geçerli olmayan öğeler eklenmeyecek. Dışa aktarma işlemi sırasında bu yükleme yapılandırma dosyasını kaydetmek istediğiniz konumu belirler. |

> Not: birden çok iş yüklerinin ve bileşenlerin belirtirken, tekrarlamalısınız `--add` veya `--remove` her öğe için komut satırı anahtarı.

| **Düzen Seçenekleri** | **Açıklama** |
| ----------------------- | --------------- |
| `--layout <dir>` | Yükleme önbelleği çevrimdışı oluşturmak için bir dizini belirtir. Daha fazla bilgi için [Visual Studio'nun ağ tabanlı yüklemesini oluşturma](create-a-network-installation-of-visual-studio.md).|
| `--lang <one or more language-locales>` | **İsteğe bağlı**: ile kullanılan `--layout` hazırlamak için çevrimdışı önbellek ile yükleme kaynak paketleri ile belirtilen diller. Daha fazla bilgi için [dil yerel ayarlar listesini](#list-of-language-locales) bu sayfadaki bölümü.|
| `--add <one or more workload or component IDs>` | **İsteğe bağlı**: bir veya daha fazla iş yükü veya Bileşen kimlikleri eklemek için. Yapıtın gerekli bileşenleri, değil önerilen veya isteğe bağlı bileşenler yüklenir. Genel olarak aracılığıyla ek bileşenler denetleyebilirsiniz `--includeRecommended` ve/veya `--includeOptional`. Daha ayrıntılı denetim için eklediğiniz `;includeRecommended` veya `;includeOptional` kimliği (örneğin, `--add Workload1;includeRecommended` veya `--add Workload2;includeOptional`). Daha fazla bilgi için [iş yükü ve Bileşen kimlikleri](workload-and-component-ids.md) sayfası. <br/>**Not**: varsa `--add` olan kullanıldığında, yalnızca belirtilen iş yükleri ve bileşenleri ve bunların bağımlılıklarını karşıdan yüklenir. Varsa `--add` belirtilmezse, tüm iş yüklerinin ve bileşenlerin düzene indirilir.|
| `--includeRecommended` | **İsteğe bağlı**: yüklü olan tüm iş yükleri için önerilen bileşenleri, ancak isteğe bağlı bileşenler içerir. Belirtilen iş yükleri ile birlikte `--allWorkloads` veya `--add`. |
| `--includeOptional` | **İsteğe bağlı**: önerilen içerir *ve* düzende tüm iş yükleri için isteğe bağlı bileşenler. İş yükleri ile belirtilen `--add`.  |
| `--keepLayoutVersion` | **15.3, isteğe bağlı olarak yeni**: Düzen sürümüne güncelleştirmeden düzene değişiklikleri uygulayın. |
| `--verify` | **15.3, isteğe bağlı olarak yeni**: bir düzen içeriğini doğrulayın. Herhangi bir bozuk veya eksik dosyalar listelenir. |
| `--fix` | **15.3, isteğe bağlı olarak yeni**: bir düzen içeriğini doğrulayın.  Bozuk veya eksik olması için herhangi bir dosya bulunamazsa, bunlar yeniden indirilecek. Bir düzen düzeltmek için Internet erişimi gerekir. |
| `--clean <one or more paths to catalogs>` | **15.3, isteğe bağlı olarak yeni**: yeni bir sürüme güncelleştiren bir düzenden eski sürümlerini bileşenleri kaldırır. |

| **Gelişmiş yükleme seçenekleri** | **Açıklama** |
| ----------------------- | --------------- |
| `--channelId <id>` | **İsteğe bağlı**: kanal örneği için yüklenecek kimliği. Diğer komutlar için gözardı yükleme komutu için gerekli olana `--installPath` belirtilir. |
| `--channelUri <uri>` | **İsteğe bağlı**: kanal bildirimi, URI. Güncelleştirme gerekli değil, `--channelUri` varolmayan bir dosyaya işaret edebilir. (örneğin,--channelUri C:\doesntExist.chman) Bu yükleme komutu için kullanılabilir; diğer komutlar için göz ardı edilir. |
| `--installChannelUri <uri>` | **İsteğe bağlı**: kanal bildiriminin yüklenmesi için kullanılacak URI. URI tarafından belirtilen `--channelUri` (olması gereken belirtilen `--installChannelUri` belirtilir) güncelleştirmeleri algılamak için kullanılır. Bu yükleme komutu için kullanılabilir; diğer komutlar için göz ardı edilir. |
| `--installCatalogUri <uri>` | **İsteğe bağlı**: Katalog bildiriminin yüklenmesi için kullanılacak URI. Belirtilmişse, kanal Yöneticisi, yükleme kanal bildiriminde URI'yi kullanmadan önce bu URI'den Kataloğu bildirimi indirmeyi dener. Bu parametre, daha önce indirilip ürün kataloğu ile Düzen önbelleği oluşturulacağı çevrimdışı yükleme desteği için kullanılır. Bu yükleme komutu için kullanılabilir; diğer komutlar için göz ardı edilir. |
| `--productId <id>` | **İsteğe bağlı** yüklenecek örneği için ürün kimliği. Bu, normal yükleme koşullarında doldurulur. |
| `--wait` | **İsteğe bağlı**: İşlem çıkış kodu döndürmeden önce yükleme tamamlanana kadar bekler. Bir yükleme dönüş kodu, işlemek için tamamlanması için beklemesi gereken yere otomatikleştirerek yüklemelerine istediğinizde yararlıdır. |
| `--locale <language-locale>` | **İsteğe bağlı**: yükleyici için kullanıcı arabirimi görüntüleme dilini değiştirin. Ayarı kalıcıdır. Daha fazla bilgi için [dil yerel ayarlar listesini](#list-of-language-locales) bu sayfadaki bölümü.|
| `--cache` | **15.2, isteğe bağlı olarak yeni**: varsa, paketler için sonraki onarım yüklendikten sonra tutulacak. Bu, sonraki yükler, onarır veya değişiklikler için kullanılacak için genel ilke ayarını geçersiz kılar. Önbellek paketleri olan varsayılan ilkedir. Bu kaldırma komutu için göz ardı edilir. Nasıl olduğunu okuyun için [devre dışı bırakın veya paket önbelleğini taşıma](disable-or-move-the-package-cache.md) daha fazla bilgi için. |
| `--nocache` | **15.2, isteğe bağlı olarak yeni**: varsa, paketler kaldıktan sonra ya da onarılması işlemlerinin hangisinin yapılacağını silinecek. Bunlar, yalnızca gerekli ve yeniden kullanımdan sonra silinmesi yeniden indirilir. Bu, sonraki yükler, onarır veya değişiklikler için kullanılacak için genel ilke ayarını geçersiz kılar. Önbellek paketleri olan varsayılan ilkedir. Bu kaldırma komutu için göz ardı edilir. Nasıl olduğunu okuyun için [devre dışı bırakın veya paket önbelleğini taşıma](disable-or-move-the-package-cache.md) daha fazla bilgi için. |
| `--noUpdateInstaller` | **15.2, isteğe bağlı olarak yeni**: varsa, sessiz belirtildiğinde kendini güncelleştirmesini yükleyici engeller. Yükleyici komutu başarısız ve yükleyici güncelleştirme gerekli olduğunda noUpdateInstaller sessiz ile belirtilmişse sıfır olmayan çıkış kodu döndürür. |
| `--noWeb` | **15.3, isteğe bağlı olarak yeni**: Kurulum artık Internet'ten yüklüyor herhangi bir içeriği indirir.  Yüklenmekte olan tüm içeriği çevrimdışı bir düzen içinde kullanılabilir olmalıdır.  Düzen içeriği eksik kurulum başarısız olur.  Daha fazla bilgi için [ağ yüklemesinden dağıtma](create-a-network-installation-of-visual-studio.md). |
| `--path <name>=<path>` | **15.7, isteğe bağlı olarak yeni**: yükleme için özel yükleme yollarını belirtmek için kullanılır. Adları paylaşılan desteklenen bir yolu, önbellek ve yükleyin. |
| `--path cache=<path>` | **15.7, isteğe bağlı olarak yeni**: belirttiğiniz yükleme dosyalarının indirileceği konumu kullanır. Bu konum yalnızca Visual Studio'nun yüklü olduğu ilk kez ayarlanabilir. Örnek: `--path cache="C:\VS\cache"` |
| `--path shared=<path>` | **15.7, isteğe bağlı olarak yeni**: yan yana Visual Studio yüklemeleri için paylaşılan dosyaları içerir. Bazıları bu ayarı geçersiz ve başka bir sürücüye yükleme sırasında bazı araçları ve SDK'lar bu sürücüdeki bir konuma yükleyin. Örnek: `--path shared="C:\VS\shared"` <br><br>Önemli: Bu yalnızca bir kez ve Visual Studio'nun yüklü olduğu ilk kez ayarlanabilir. |
| `--path install=<path>` | **15.7, isteğe bağlı olarak yeni**: eşdeğer `–-installPath`. Özellikle, `--installPath "C:\VS"` ve `--path install="C:\VS"` eşdeğerdir. Aynı anda bunlardan yalnızca biri kullanılabilir. |

## <a name="list-of-workload-ids-and-component-ids"></a>İş yükü kimlikleri ve bileşen listesi

İş yükü ve Bileşen kimlikleri Visual Studio ürüne göre sıralı bir listesi için bkz. [Visual Studio 2017 iş yükü ve Bileşen kimlikleri](workload-and-component-ids.md) sayfası.

## <a name="list-of-language-locales"></a>Dil yerel ayarlar listesi

| **Dil yerel ayar** | **Dil** |
| ----------------------- | --------------- |
| Cs-cz | Çekçe |
| De-de | Almanca |
| En-us | İngilizce |
| ES-es | İspanyolca |
| FR-fr | Fransızca |
| İt-IT | İtalyanca |
| Ja-jp | Japonca |
| Ko-kr | Korece |
| PL-pl | Lehçe |
| PT-br | Portekizce - Brezilya |
| RU-ru | Rusça |
| Tr-tr | Türkçe |
| Zh-cn | Çince - Basitleştirilmiş |
| Zh-tw | Çince - Geleneksel |

## <a name="error-codes"></a>Hata kodları

İşlemin sonucu bağlı olarak `%ERRORLEVEL%` ortam değişkeni aşağıdaki değerlerden birine ayarlanır:

| **Değer** | **Sonuç** |
| --------- | ---------- |
| 0 | İşlem başarıyla tamamlandı |
| 1602 | İşlem iptal edildi |
| 3010 | İşlem başarıyla tamamlandı ancak kullanmadan önce yükleme, yeniden başlatma gerekiyor. |
| 5004 | İşlem iptal edildi |
| 5007 | İşlem engellendi - bilgisayar gereksinimleri karşılamıyor |
| Diğer | Hata durumu oluştu - daha fazla bilgi için günlüklere bakın |

Her işlemin birkaç günlük dosyalarında oluşturur `%TEMP%` yüklemenin ilerleme durumunu belirten bir dizin. Klasör tarihe göre sıralayın ve ile başlayan dosyaları arayın `dd_bootstrapper`, `dd_client`, ve `dd_setup` önyükleyici için yükleyici uygulama ve Kurulum altyapısı, sırasıyla.

[!INCLUDE[install_get_support_md](includes/install_get_support_md.md)]

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio 2017 yüklemesi için komut satırı parametresi örnekleri](command-line-parameter-examples.md)
- [Visual Studio 2017'in çevrimdışı yüklemesini oluşturma](create-an-offline-installation-of-visual-studio.md)
- [Yanıt dosyası ile Visual Studio yüklemesini otomatikleştirme](automated-installation-with-response-file.md)
- [Visual Studio 2017 iş yükü ve Bileşen kimlikleri](workload-and-component-ids.md)