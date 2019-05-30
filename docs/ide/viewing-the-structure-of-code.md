---
title: Sınıf Görünümü, çağrı hiyerarşisini, nesne tarayıcısı, kod tanımı penceresi
ms.date: 05/18/2018
ms.topic: conceptual
f1_keywords:
- vs.documentoutline.window
- vs.objectbrowser
- vs.classview
- VS.CodeDefinitionView
- VS.CodeDefinitionWindow
- vs.componentpicker
- vs.callbrowser
helpviewer_keywords:
- document outline window
- Visual Studio, object browser
- call hierarchy
- Visual Studio, document outline window
- code definition window [Visual Studio]
- Visual Studio, class view
- Visual Studio, call hierarchy window
- class view
- object browser
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 9e2ec8e3e51036749030036eee6ff1d268a44f69
ms.sourcegitcommit: 117ece52507e86c957a5fd4f28d48a0057e1f581
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/28/2019
ms.locfileid: "66263077"
---
# <a name="view-the-structure-of-code-using-different-tool-windows"></a>Farklı araç pencerelerini kullanarak kod yapısını görüntüleme

Sınıfları ve üyeleri dahil olmak üzere çeşitli araç pencerelerine kullanarak Visual Studio'da inceleyebilirsiniz **sınıf görünümü**, **çağrı hiyerarşisi**, **Nesne Tarayıcısı**ve **Kod tanımı** (yalnızca C++ için). Bu araç pencereleri, kod projeleri Visual Studio, .NET Framework bileşenlerini, COM bileşenlerini, dinamik bağlantı kitaplıklarını (DLL) inceleyebilirsiniz ve tür kitaplıkları (TLB).

Ayrıca **Çözüm Gezgini** türler ve üyeler sembolleri, arama projelerinizde göz atmak için bir yöntemin çağrı hiyerarşisini, Bul sembol başvuruları ve daha fazla birden çok araç pencereleri arasında geçiş yapmak zorunda kalmadan görüntüleyin.

Visual Studio Enterprise edition kullanıyorsanız, kullanabileceğiniz *kod haritaları* yapısını kodunuzu ve bağımlılıkları arasında çözümün tamamını görselleştirmek için. Daha fazla bilgi için [kod haritaları ile bağımlılıkları eşleme](../modeling/map-dependencies-across-your-solutions.md).

## <a name="class-view-visual-basic-c-c"></a>Sınıf Görünümü (Visual Basic, C#, C++)

**Sınıf Görünümü** parçası olarak gösterilen **Çözüm Gezgini** ve ayrı bir pencerede olarak. **Sınıf Görünümü** bir uygulamanın öğelerini görüntüler. Üst bölme ad alanlarını, türleri, arabirimleri, numaralandırmalar ve sınıflar ve alt bölmesinde üst bölmede seçilen türe ait üyelerini görüntüler. Bu pencere öğesini kullanarak, kaynak kodu üye tanımlarında taşıyabilirsiniz (veya **Nesne Tarayıcısı** öğe çözümünüzü dışında tanımlı ise).

Alt öğeleri görüntülemek için bir proje derlemek zorunda değilsiniz **sınıf görünümü**. Kod projenizde değiştirirken penceresi yenilenir.

Kod proje düğümünü ve seçerek projenize ekleyebilirsiniz **Ekle** açmak için düğmeyi **Yeni Öğe Ekle** iletişim kutusu. Kodu ayrı bir dosyada eklenir.

Projeniz için kaynak kodu denetimi, iade edildiğinde, her **sınıf görünümü** öğesi dosyanın kaynak kodu durumunu belirten bir simge görüntüler. Ortak kaynak kodu denetimi komutları gibi **kullanıma**, **iade**, ve **en son sürümü Al** öğesi için kısayol menüsünde de mevcuttur.

### <a name="class-view-toolbar"></a>Sınıf Görünümü araç çubuğu

**Sınıf görünümü** araç çubuğu aşağıdakileri içerir:

|||
|-|-|
|**Yeni klasör**|Sanal klasör veya sık kullanılan öğeleri düzenlemek alt klasör oluşturur. Etkin çözüm kaydedilmeden (*.suo*) dosyası. Yeniden adlandırma ya da kodunuzda bir öğeyi sil sonra sanal bir klasörde bir hata düğümü olarak görünebilir. Bu sorunu düzeltmek için hata düğümü silin. Bir öğeyi yeniden adlandırdıysanız, bu proje hiyerarşisindeki klasörüne yeniden taşıyabilirsiniz.|
|**Geri**|Daha önce seçilen öğe için gider.|
|**İleriye doğru**|Seçili öğeye ileri gider.|
|**Sınıf diyagramı görüntüle** (kod projeleri yalnızca yönetilen)|Bir ad alanı seçin veya yazın, kullanılabilir **sınıf görünümü**. Bir ad alanı seçili olduğunda, sınıf diyagramı içinde tüm türleri gösterir. Bir tür seçili olduğunda, sınıf diyagramına yalnızca bu türünü gösterir.|

### <a name="class-view-settings"></a>Sınıf Görünümü ayarlar

**Sınıf görünümü ayarlar** araç çubuğunda, aşağıdaki ayarlara sahiptir:

|||
|-|-|
|**Temel türleri Göster**|Temel türleri görüntülenir.|
|**Türetilmiş türleri Göster**|Türetilmiş türler görüntülenir.|
|**Gizli türleri ve üyeleri Göster**|Gizli türleri ve üyeleri (istemcileri tarafından kullanılmak üzere tasarlanmamıştır) açık gri metin görüntülenir.|
|**Ortak üyeleri Göster**|Genel üye görüntüleniyor.|
|**Korunan üyeleri Göster**|Korumalı üye görüntüleniyor.|
|**Özel üyeleri Göster**|Özel üyeler görüntülenir.|
|**Diğer üyeleri Göster**|Diğer türde üye görüntülenir, iç dahil olmak üzere (veya Visual Basic'te Friend) üyeler.|
|**Devralınan üyeleri Göster**|Devralınan üye görüntüleniyor.|
|**Uzantı yöntemleri Göster**|Genişletme yöntemleri görüntülenir.|

### <a name="class-view-shortcut-menu"></a>Sınıf Görünümü kısayol menüsü

Kısayol menüsünde **sınıf görünümü** seçilen proje türünü bağlı olarak aşağıdakileri içerebilir:

|||
|-|-|
|**Tanıma Git**|Kaynak kodu ya da öğenin açıklamasını bulur **Nesne Tarayıcısı**, öğeyi projede tanımlı değil.|
|**Tanım göz atın**|Seçili öğeyi görüntüler **Nesne Tarayıcısı**.|
|**Tüm başvuruları Bul**|Şu anda seçili nesne öğesi bulur ve sonuçları görüntüler bir **sonuçları Bul** penceresi.|
|**Filtre türü** (kod yalnızca yönetilen)|Yalnızca seçilen tür veya ad alanı görüntüler. Seçerek filtreyi kaldırabilirsiniz **Temizle Bul** (**X**) düğmesinin yanındaki **Bul** kutusu.|
|**Kopyala**|Öğenin tam adını kopyalar.|
|**Alfabetik olarak Sırala**|Türleri ve üyeleri alfabetik olarak ada göre listeler.|
|**Üye türe göre sırala**|Türleri ve üyeleri türe göre sırayla unutmayın (sınıflar arabirimleri koyun, arabirimler, temsilciler koyun ve yöntemler, Özellikler önünde gibi) listeler.|
|**Üye erişimine göre sırala**|Liste türleri ve üyeleri erişimlerine göre sırayla, genel veya özel gibi yazın.|
|**Üye türüne göre grupla**|Türler ve üyeler gruplara nesne türüne göre sıralar.|
|**Git için bildirimi** (yalnızca C++ kodu)|Türe veya üyeye bildirimi varsa kaynak kodunu görüntüler.|
|**Tanıma Git**|Türün veya üyenin tanımı varsa kaynak kodunu görüntüler.|
|**Başvuruya Git**|Türe veya üyeye başvuru varsa kaynak kodunu görüntüler.|
|**Çağrı hiyerarşisini görüntüle**|Seçili yöntemi görüntüler **çağrı hiyerarşisi** penceresi.|

## <a name="call-hierarchy-window-visual-basic-c-c"></a>Çağrı hiyerarşisi penceresi (Visual Basic C#, C++)

**Çağrı hiyerarşisi** penceresi gösterir burada verilen yöntemi veya özelliği olarak adlandırılır. Ayrıca, bu yönteminden çağrılan yöntemler listelenmiştir. Belirtilen kapsamda olan yöntemleri çağıran-çağrılan ilişkileri gösteren çağrı grafı birden fazla düzeyde görüntüleyebilirsiniz.

Görüntüleyebileceğiniz **çağrı hiyerarşisi** Düzenleyicisi'nde yöntem (veya özellik veya Oluşturucu) seçip ardından penceresi **çağrı hiyerarşisini** kısayol menüsünde. Ekran aşağıdaki görüntüye benzer olacaktır:

![Visual Studio çağrı hiyerarşisi penceresi](../ide/media/multiplenodes.png)

Araç çubuğunda yanıdaki açılan listeyi kullanarak, hiyerarşinin bir kapsam belirtebilirsiniz: çözüm, geçerli proje ya da geçerli belge.

Ana bölmede yöntemi gelen ve giden çağrıları görüntüler ve **çağrı siteleri** bölmesi, seçilen çağrı konumunu görüntüler. Sanal veya soyut üyeler için bir **geçersiz kılmaları yöntem adı** düğümü görüntülenir. Arabirim üyeleri için bir **uygulayan yöntem adı** düğümü görüntülenir.

**Çağrı hiyerarşisi** penceresi yöntemi burada bir yöntem bir olay işleyicisi eklenir veya bir temsilciye atanmış basamak içeren grubu başvuruları bulamazsa. Bu başvurular bulmak için kullanın **tüm başvuruları Bul** komutu.

Kısayol menüsünde **çağrı hiyerarşisi** penceresi aşağıdakileri içerir:

|||
|-|-|
|**Yeni kök olarak Ekle**|Seçili düğümü yeni bir kök düğümü ekler.|
|**Kökü Kaldır**|Ağaç görünümü bölmesinde seçilen kök düğümü kaldırır.|
|**Tanıma Git**|Bir yöntemin orijinal tanımına gider.|
|**Tüm başvuruları Bul**|Projede seçilen yöntemi tüm başvurularını bulur.|
|**Kopyala**|Seçili düğümü (ancak alt düğümlerini) kopyalar.|
|**Yenileme**|Bilgileri yeniler.|

## <a name="BKMK_ObjectBrowser"></a> Nesne Tarayıcısı

**Nesne Tarayıcısı** penceresi projelerinizde kod açıklamaları görüntüler.

Pencerenin en üstündeki açılan listesini kullanarak görüntülemek istediğiniz bileşenleri filtreleyebilirsiniz. Yönetilen kod yürütülebilir dosyaları, Kütüphane derlemelerini, tür kitaplıkları, özel bileşenler içerebilir ve *.ocx* dosyaları. C++ özel bileşenler eklemek mümkün değildir.

::: moniker range="vs-2017"

Özel ayarlar, Visual Studio kullanıcı uygulama dizinine kaydedilir *%APPDATA%\Microsoft\VisualStudio\15.0\ObjBrowEX.dat*.

::: moniker-end

::: moniker range=">=vs-2019"

Özel ayarlar, Visual Studio kullanıcı uygulama dizinine kaydedilir *%APPDATA%\Microsoft\VisualStudio\16.0\ObjBrowEX.dat*.

::: moniker-end

Sol bölmesinde **Nesne Tarayıcısı** derlemeleri gösterir. Derlemeleri içerdikleri ad alanlarını görüntülemek için genişletin ve ardından içerdikleri türleri görüntülenecek ad alanları'ı genişletin. Üyeleri (örneğin, özellikleri ve yöntemleri), bir türünü seçtiğinizde, sağ bölmede listelenir. Alt sağ bölmesinde seçtiğiniz öğe hakkındaki ayrıntılı bilgileri görüntüler.

Kullanarak belirli bir öğe için arama yapabilirsiniz **arama** pencerenin üst kısmındaki kutusu. Aramalar büyük/küçük harfe duyarsızdır. Arama sonuçları, sol bölmede görüntülenir. Aramayı temizlemek için seçin **Aramayı Temizle** (**X**) düğmesinin yanındaki **arama** kutusu.

**Nesne Tarayıcısı** yaptığınız seçimleri izini ve gidebilirsiniz seçimlerinizi arasında kullanarak **İleri** ve **geri** araç çubuğundaki düğmeler.

Kullanabileceğiniz **Nesne Tarayıcısı** (derleme, ad alanı, tür veya üye) bir öğe ve seçerek bir açık çözüme bir bütünleştirilmiş kod başvurusu eklemek için **Başvuru Ekle** araç çubuğunda.

### <a name="object-browser-settings"></a>Nesne Tarayıcısı ayarları

Kullanarak **nesne tarayıcısı ayarları** düğme araç çubuğunda, aşağıdaki görünümlerden birini belirtebilirsiniz:

|||
|-|-|
|**Görünüm ad alanları**|Sol bölmede, fiziksel kapsayıcılar yerine ad alanları görüntüler. Ad alanlarında birden çok fiziksel kapsayıcılarda depolanan birleştirilir.|
|**Görünüm kapsayıcıları**|Fiziksel kapsayıcılar yerine ad alanları, sol bölmede görüntülenir. **Ad alanlarını görüntülemek** ve **görünümü kapsayıcıları** birbirini dışlayan ayarlarıdır.|
|**Temel türleri Göster**|Temel türleri görüntüler.|
|**Türetilmiş türleri Göster**|Türetilmiş türleri görüntüler.|
|**Gizli türleri ve üyeleri Göster**|Görüntüler gizli türleri ve üyeleri (istemcileri tarafından kullanılmak üzere tasarlanmamıştır)'açık gri metin.|
|**Ortak üyeleri Göster**|Genel üyeler görüntüler.|
|**Korunan üyeleri Göster**|Korumalı üyeler görüntüler.|
|**Özel üyeleri Göster**|Özel üyeler görüntüler.|
|**Diğer üyeleri Göster**|Diğer iç üyelerini (veya Visual Basic'te Friend) türler üyelerini görüntüler.|
|**Devralınan üyeleri Göster**|Devralınan üyeleri görüntüler.|
|**Uzantı yöntemleri Göster**|Genişletme yöntemleri görüntüler.|

### <a name="object-browser-shortcut-menu-commands"></a>Nesne tarayıcı kısayol menü komutları

Kısayol menüsünde **Nesne Tarayıcısı** öğe türüne bağlı olarak aşağıdaki komutları içerebilir seçili:

|||
|-|-|
|**Tanım göz atın**|Seçili öğe için birincil düğüm gösterir.|
|**Tüm başvuruları Bul**|Şu anda seçili nesne öğesi bulur ve sonuçları görüntüler bir **sonuçları Bul** penceresi.|
|**Türe göre filtrele**|Yalnızca seçilen tür veya ad alanı görüntüler. Seçerek filtreyi kaldırabilirsiniz **Aramayı Temizle** düğmesi.|
|**Kopyala**|Öğenin tam adını kopyalar.|
|**Kaldır**|Özel bileşen kümesi kapsamı ise seçilen bileşen kapsamından kaldırır.|
|**Alfabetik olarak Sırala**|Türleri ve üyeleri alfabetik olarak ada göre listeler.|
|**Nesne türüne göre sırala**|Türleri ve üyeleri türe göre sırayla unutmayın (sınıflar arabirimleri koyun, arabirimler, temsilciler koyun ve yöntemler, Özellikler önünde gibi) listeler.|
|**Nesne erişime göre sırala**|Liste türleri ve üyeleri erişimlerine göre sırayla, genel veya özel gibi yazın.|
|**Nesne türüne göre grupla**|Türler ve üyeler gruplara nesne türüne göre sıralar.|
|**Git için bildirimi** (yalnızca C++ projeleri)|Türe veya üyeye bildirimi varsa kaynak kodunu görüntüler.|
|**Tanıma Git**|Türün veya üyenin tanımı varsa kaynak kodunu görüntüler.|
|**Başvuruya Git**|Türe veya üyeye başvuru varsa kaynak kodunu görüntüler.|
|**Çağrı hiyerarşisini görüntüle**|Seçili yöntemi görüntüler **çağrı hiyerarşisi** penceresi.|

## <a name="code-definition-window-c"></a>Kod tanımı penceresi (C++)

**Kod tanımı** penceresinde etkin projedeki seçili C++ tür veya üyenin tanımı gösterilir. Türe veya üyeye bir kod Görünümü penceresi veya Kod düzenleyicisinde seçilebilir.

Bu pencereyi salt okunur olsa da, yer imlerinde veya kesme noktaları ayarlayabilirsiniz. Görüntülenen tanımı değiştirmek için seçin **tanımını Düzenle** kısayol menüsünde. Bu kaynak dosyasını Kod düzenleyicisinde açar ve tanımı başladığı noktasını satıra taşır.

> [!NOTE]
> Visual Studio 2015'ten başlayarak **kod tanımı** penceresi yalnızca C++ kodu ile kullanılabilir.

### <a name="code-definition-shortcut-menu"></a>Kod tanımı kısayol menüsü

Kısayol menüsünde **kod tanımı** penceresinde aşağıdakileri içerebilir:

|||
|-|-|
|**Hızlı Eylemler ve yeniden düzenlemeler**||
|**Yeniden Adlandır**||
|**Ekleme dosyalarının Grafını oluştur**||
|**Tanıma göz at**||
|**Tanıma Git**|Tanımı (veya tanımları, parçalı sınıflar) bulur ve bunları görüntüler bir **sonuçları Bul** penceresi.|
|**Bildirimine gidin**||
|**Tüm başvuruları Bul**|Türe veya üyeye yapılan başvurular çözümde bulur.|
|**Çağrı hiyerarşisini görüntüle**|Yönteminde görüntüler **çağrı hiyerarşisi** penceresi.|
|**Başlık / kod dosyası**||
|**Testleri çalıştırın**|Projede birim testleri varsa, seçilen kod için testleri çalıştırır.|
|**Testlerde Hata Ayıkla**||
|**Kesme noktası**|Bir kesme noktası (veya izleme noktası) ekler.|
|**İmlece kadar Çalıştır**|Programın hata ayıklama modunda İmleç konumuna çalıştırır.|
|**Kod parçacığı**||
|**Kes**, **kopyalama**, **Yapıştır**||
|**Ek Açıklama**||
|**Anahat Oluşturma**|Standart komutlar anahat oluşturma.|
|**Yeniden tara**||
|**Tanımı Düzenle**|Ekleme noktasını kod penceresinde tanım taşır.|
|**Kodlama Seç**|Açılır **kodlama** penceresi bir dosya için kodlama ayarlayabilirsiniz.|

## <a name="document-outline-window"></a>Belge Anahattı penceresi

Kullanabileceğiniz **belge anahattı** veya HTML sayfaları için XAML sayfa tasarımcıyı veya bir Windows Form Tasarımcısı gibi tasarımcı görünümleri ile birlikte penceresi. Böylece form veya sayfadaki mantıksal yapısını görüntülemek ve derin gömülü veya gizli denetimler Bu pencere öğeleri bir ağaç görünümünde görüntüler.

## <a name="see-also"></a>Ayrıca bkz.

- [Sınıf Görünümü ve Nesne Tarayıcısı simgeleri](../ide/class-view-and-object-browser-icons.md)
