---
title: 'Test Alanı 3: Onay dışarı geri alma | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- source control plug-ins, checkout
- source control plug-ins, undo checkout
- source control [Visual Studio SDK], checking out
- source control [Visual Studio SDK], undo checkout
ms.assetid: ce00c5a5-d472-4f45-8776-d77a1fbe9d37
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 93ca3f2c656c6bea81139e5e6101499a7fc8febd
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66331077"
---
# <a name="test-area-3-check-outundo-checkout"></a>Test Alanı 3: Kullanıma almayı geri al / gözden geçirin
Bu kaynak denetimi eklentisi test alanı sürüm deposu düzenleme ve geri döndürülüyor öğelerinden kapsar **kullanıma** ve **kullanıma almayı geri al** komutları.

**Kullanıma**: Sürüm deposu olarak bir öğeyi kullanıma işaretleri okuma/yazma için yerel kopyayı değiştirir.

**Kullanıma almayı geri al**: Sürüm deposu olarak bir öğe iade işaretleri (Seçenekler) bağlı olarak kullanıma almadan önce yerel kopyasına geri döner.

## <a name="command-menu-access"></a>Komut menü erişimi

Aşağıdaki [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] tümleşik geliştirme ortamı menüsü yolları test durumlarında kullanılır.

##### <a name="check-out"></a>Kontrol etme:

- **Dosya**, **kaynak denetimi**, **kullanıma**.

- **Dosya**, **kullanıma**.

- Kısayol menüsünde, **kullanıma**.

- Kullanıma almayı geri al: **Dosya**, **kaynak denetimi**, **geri alma**.

## <a name="common-expected-behavior"></a>Ortak beklenen davranışı

- İşlem teslim sonra hedef dosyaların ve/veya klasörleri sürüm deposuna kullanıma olarak işaretlenir.

- Sürüm deposu kullanıma alma için doğru kullanıcı öznitelikleri.

- Kullanıma alma tarih ve saat (kullanıcı ayarlarını) doğrudur.

## <a name="test-cases"></a>Test çalışmaları

Kullanıma alma/geri almayı test alanı için belirli test çalışmaları aşağıda verilmiştir.

### <a name="case-3a-check-out"></a>Büyük/küçük harf 3a: Kullanıma Al

Bu bölümde, kullanıma komut işlemi ele alınmaktadır.

|Eylem|Test adımları|Beklenen sonuçları doğrulamak için|
|------------|----------------|--------------------------------|
|Denetleme kullanıma özel (COE) istemci projesi|1.  Bir istemci projesi oluşturun.<br />2.  Çözüm kaynak denetimine ekleyin.<br />3.  Tüm projeyi özel kontrol (**dosya**, **kullanıma**).|Kullanıma gerçekleşir.|
|Bir dosya sisteminde veya yerel IIS Web projesi özel olarak kullanıma al (COE) denetleyin|1.  Dosya Paylaşımı için Web sunucusu bağlantısını Ayarla **Araçları**, **seçenekleri**, **projeleri**, **Web ayarları**.<br />2.  Web projesi oluşturun.<br />3.  Çözüm kaynak denetimine ekleyin.<br />4.  Tüm projeyi özel kontrol (**dosya**, **kaynak denetimi**, **kullanıma**).|Kullanıma gerçekleşir.|
|Çözüm Öğeleri bir çözümde (diğer dosyaları işlemek için yeni yöntem) göz atın|1.  Boş bir çözüm oluşturun.<br />2.  Çözüm kaynak denetimine ekleyin.<br />3.  Çözümü denetleyin.<br />4.  Birkaç çözüm öğeleri ekleyin.<br />5.  Yeni eklenen öğelerde denetleyin.<br />6.  Birden çok çözüm öğeleri seçin.<br />7.  Seçili öğeleri kullanıma (kısayol menüsünde, **kullanıma**).|Seçilen dosyalar kullanıma alındı.|
|Denetleme kullanıma yerel (test eklentisi bu özelliğin destekliyorsa) sürümü|1.  1. kullanıcı: Bir istemci projesi oluşturun.<br />2.  1. kullanıcı: Çözüm kaynak denetimine ekleyin.<br />3.  2. kullanıcı: Çözümü kaynak denetiminden başka bir konuma açın.<br />4.  2. kullanıcı: Dosyasını gözden geçirin.<br />5.  2. kullanıcı: Dosyayı değiştirin.<br />6.  2. kullanıcı: Dosyayı iade edin.<br />7.  1. kullanıcı: Dosyanın yerel sürümü kullanıma alma (denetleyin **yerel sürüm kullanıma** seçeneğinde Gelişmiş **kullanıma** iletişim kutusunda).|Dosyanın yerel sürümü kullanıma alınır.<br /><br /> Kullanıcı 1 dosyasına değişiklikler 2 kullanıcı tarafından uygulanmaz.|

### <a name="case-3b-disconnected-check-out"></a>Büyük/küçük harf 3b: Bağlantısı kesilen kullanıma alma

Bağlantı kesik moddayken çalışan kullanıcıların belirli bir düzeyde doğrudan bir sürüm deposuna bağlı olmayan sürekli kaynak denetimi desteği sağlar. Bu, kayıtlı çözüm ve projeler ilgili tüm bilgileri yerel olarak önbelleğe alarak gerçekleştirilir.

Yalnızca özel kullanıma alma işlemleri için kaynak denetim deposunda bağlıyken ortaya çıkabilir. Paylaşılan kullanıma alma işlemleri, bağlı veya bağlantısı kesilmiş herhangi bir zamanda gerçekleşebilir. Bu nedenle, sürüm Mağazası'ndan yalnızca bağlı değilken **kullanıma denetleyin paylaşılan** (komut etkin COS). Bağlı değilken **kullanıma almayı geri al** kullanıcı tarafından yapılan değişiklikleri değiştirmek için eski sürümü alınamadığından devre dışı bırakıldı.

Kullanıcı sürümüne bağlandığında depolamak, kullanıma alma durumunu tüm kayıtlı çözümler ve projeler eşitlenir. Kullanıcı yürüttü kullanıma alma için gerekli güncelleştirmeleri deposuna yapar. Eşitleme gerçekleşen sonra kullanıcı (bağlı) normal şekilde çalışmaya devam edebilir.

#### <a name="expected-behavior"></a>Beklenen davranış

- Kullanamazsınız **kullanıma özel kontrol** sürüm Mağazası'ndan bağlı değilken komutu.

- Kullanamazsınız **kullanıma almayı geri al** sürüm Mağazası'ndan bağlı değilken komutu.

- **Paylaşılan kullanıma** komut çalışır.

|Eylem|Test adımları|Beklenen sonuçları doğrulamak için|
|------------|----------------|--------------------------------|
|Bağlı değilken dosyasını gözden geçirin ve ardından eşitleme için Bağlan|1.  Kaynak denetimini Değiştir iletişim kutusunu kullanarak bir denetimli proje bağlantısını kes (**dosya**, **kaynak denetimi**, **kaynak denetimini Değiştir**).<br />2.  Bir dosyayı gözden geçirin.<br />3.  (Uyarı iletişim kutusunda bağlantısı kesildi) kullanıma tıklayın.<br />4.  Dosyayı düzenleyin.<br />5.  Kaynak denetimini Değiştir iletişim kutusunu kullanarak bağlanın.<br />6.  Düzenlenen dosyasının en son sürümünü alın.|Ortak beklenen davranışı|

### <a name="case-3c-query-editquery-save-qeqs"></a>Durum 3c: Sorgu düzenleme/sorgu kaydetme (QEQS)
 Kaynak denetimi altındaki öğeler düzenlemeler, değişiklikleri izlenir ve kullanıcıların bir kolayca yardımcı olmak için kaydeder dosyalarına yönetin. "İade" denetimli bir öğeyi düzenlendiğinde QEQS girişimi Düzenle durdurur ve düzenlemek için dosyayı kullanıma alın, istediği kullanıcıya sorar. Yapılandırmanıza bağlı olarak **Araçları**, **seçenekleri** ayarları, kullanıcı olduğunu denetlemek için zorunlu ya da dosyayı teslim düzenlemek için veya bellekte kopya Düzenle ve daha sonra kullanıma de izin verilir. Kullanıcının **Araçları**, **seçenekleri** ayar iletişim kutusu kullanıma görüntülemek ve hemen kullanıma iade için ayarlı değil ve ardından, düzenleme kullanıcının yaptığı gibi dosyayı otomatik olarak, mümkün olduğunda denetler.

#### <a name="expected-behavior"></a>Beklenen davranış

- İşlem teslim sonra hedef dosyaların ve/veya klasörleri sürüm deposuna kullanıma olarak işaretlenir.

- Sürüm deposu kullanıma için doğru kullanıcı öznitelikleri.

- (Kullanıcı ayarlarını) göz atın, tarih ve saat doğrudur.

- Hedef dosya veya klasörün yerel kopyayı yazılabilir.

|Eylem|Test adımları|Beklenen sonuçları doğrulamak için|
|------------|----------------|--------------------------------|
|İade metin dosyasını düzenleyin|1.  Bir metin dosyasını içeren yeni bir proje oluşturun.<br />2.  Çözüm kaynak denetimine ekleyin.<br />3.  Ayarlama **Araçları**, **seçenekleri**, **kaynak denetimi**, **dosyalarının salt okunur sırasında disk üzerinde düzenlenmesine izin ver** için işaretlenmemiş.<br />4.  Ayarlama **Araçları**, **seçenekleri**, **kaynak denetimi**, **kullanıma sor** içinde **dosyaları iade düzenlenenalındığında** birleşik giriş kutusu.<br />5.  Ayarlama **Araçları**, **seçenekleri**, **kaynak denetimi**, **kullanıma sor** içinde **iade, dosyalarıkaydedilir** birleşik giriş kutusu.<br />6.  Metin Dosyası Düzenleyicisi'nde açın, yeni bir metin dosyasına yazmak çalışır. Bu adım başarılı olursa, sonraki adıma geçin.<br />7.  Tıklayın **iptal** içinde **düzenleme için kullanıma** iletişim kutusu. Bu adım başarılı olursa, sonraki adıma geçin.<br />8.  Ayarlama **Araçları**, **seçenekleri**, **kaynak denetimi**, **dosyalarının salt okunur sırasında disk üzerinde düzenlenmesine izin ver** için işaretlenmiş.<br />9. Proje Dosyası Düzenleyicisi'nde açın, yeni bir metin dosyasında yazın girişimi. Bu adım başarılı olursa, sonraki adıma geçin.<br />10. Tıklayın **Düzenle** içinde **düzenleme için kullanıma** iletişim kutusu. Bu adım başarılı olursa, sonraki adıma geçin.<br />11. Metin dosyasını düzenleyin ve kaydetmeyi deneyin.|`Result of step 6:`<br /><br /> Düzenle iletişim kutusu görünür göz atın.<br /><br /> `Result of step 7:`<br /><br /> Dosya değiştirilmez.<br /><br /> `Result of step 9:`<br /><br /> Düzenle iletişim kutusu görünür göz atın.<br /><br /> `Result of step 10:`<br /><br /> Bellek proje dosyasında düzenleyebilirsiniz.<br /><br /> `Result of step 11:`<br /><br /> Kaydetme kullanıma üzerinde Kaydet iletişim kutusu görünür.|
|İade edildiğinde bir çözüm dosyası Düzenle|Altında açıklandığı gibi adımları test ancak bir metin dosyasını değiştirmek yerine, çözüm çözüm özellikleri değiştirerek değiştirme yineleyin.|Önceki test aynı|
|İade edildiğinde bir proje dosyasını Düzenle|Önceki açıklanan adımları test ancak bir metin dosyası değiştirmek yerine proje özelliklerini değiştirerek proje değiştirme yineleyin.|Önceki test ile aynıdır.|

### <a name="case-3d-silent-check-out"></a>Case 3d: Sessiz kullanıma alma
 Bu senaryolar alt alanı kapsar kullanıma burada **kullanıma** iletişim kutusu, kullanıcı görünmez **Araçları**, **seçenekleri**, **kaynak denetim ayarları** .

#### <a name="expected-behavior"></a>Beklenen davranış

- İşlem teslim sonra hedef dosyaların ve/veya klasörleri sürüm deposuna kullanıma olarak işaretlenir.

- Sürüm deposu kullanıma için doğru kullanıcı öznitelikleri.

- Göz atın, tarih ve saat (kullanıcı ayarlarını) doğru.

- Hedef dosya veya klasörün yerel kopyayı yazılabilir.

|Eylem|Test adımları|Beklenen sonuçları doğrulamak için|
|------------|----------------|--------------------------------|
|Bir dosya için sessiz kullanıma alma|1.  Ayarlama **Araçları**, **seçenekleri**, **kaynak denetimi** için **kullanıma alma dosyaları otomatik olarak düzenleme**.<br />2.  Yeni bir proje, bir dosya oluşturun.<br />3.  Çözüm kaynak denetimine ekleyin.<br />4.  Dosyasını gözden geçirin.|Dosya kullanıma sessizce (kullanıcı Arabirimi).|
|Bir proje için sessiz kullanıma alma|1.  Ayarlama **Araçları**, **seçenekleri**, **kaynak denetimi** için **kullanıma alma dosyaları otomatik olarak düzenleme**.<br />2.  Yeni bir proje oluşturun.<br />3.  Çözüm kaynak denetimine ekleyin.<br />4.  Projeyi kontrol edin.|Dosya kullanıma sessizce (kullanıcı Arabirimi).|

### <a name="case-3e-undo-check-out"></a>Büyük/küçük harf 3e: Kullanıma almayı geri al
 **Kullanıma Al** bir dosyanın durumu kontrol iptal etmek ve dosya üzerinde yaptığınız değişiklikleri iade önlemek için kullanılır.

#### <a name="expected-behavior"></a>Beklenen davranış

- Kullanıcının varsayılan alan **yerel sürümü kullanıma alma** ayarı. Yerel sürüm kullanıma denetlemek kullanıcı tarafından seçmiş, her zaman kullanıma aldığınız sürümle geri dönmek için geri alma için varsayılan değer yoktur.

- Simgeleri geri almayı kabul ettiğiniz andan **Çözüm Gezgini** etkilenen güncelleştirilen dosyaları ve öğesi kaldırılır **Bekleyen İadeler** penceresi.

|Eylem|Test adımları|Beklenen sonuçları doğrulamak için|
|------------|----------------|--------------------------------|
|Özel olarak kullanıma tek bir dosyayı kullanıma almayı geri al|1.  Bir istemci projesi oluşturun.<br />2.  Çözüm kaynak denetimine ekleyin.<br />3.  Bir dosyayı kullanıma özel kontrol edin.<br />4.  Dosyayı değiştirin.<br />5.  Kullanıma almayı geri al (**dosya**, **kaynak denetimi**, **geri alma**).|Ortak beklenen bir davranış.|
|Paylaşılan denetlenir tek bir dosyayı kullanıma almayı geri al|1.  Bir istemci projesi oluşturun.<br />2.  Çözüm kaynak denetimine ekleyin.<br />3.  Paylaşılan bir dosyasını gözden geçirin.<br />4.  Dosyayı değiştirin.<br />5.  Kullanıma almayı geri al (**dosya**, **kaynak denetimi**, **geri alma**).|Ortak beklenen bir davranış.|
|Dosyalar projeye ekledikten sonra proje kullanıma almayı geri al|1.  Yeni bir proje oluşturun ve kaynak denetimine ekleyin.<br />2.  Projeyi kontrol edin.<br />3.  Bir dosyayı projeye ekleyin.<br />4.  Projeyi kullanıma almayı geri al.|Çözüm Gezgini'nde projeye eklenen dosya kaldırılır.<br /><br /> Proje artık kullanıma alındı.|
|Projeden dosyaları sildikten sonra proje kullanıma almayı geri al|1.  Yeni bir proje oluşturun ve kaynak denetimine ekleyin.<br />2.  Projeyi kontrol edin.<br />3.  Bir dosyayı projeden silin.<br />4.  Projeyi kullanıma almayı geri al.|Silinen dosya Çözüm Gezgini'nde projeye altında görünür.<br /><br /> Proje artık kullanıma alındı.|

## <a name="see-also"></a>Ayrıca Bkz.
- [Kaynak Denetimi Eklentileri için Test Kılavuzu](../../extensibility/internals/test-guide-for-source-control-plug-ins.md)
