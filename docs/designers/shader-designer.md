---
title: Gölgelendirici Tasarımcısı
ms.date: 09/21/2018
ms.topic: conceptual
f1_keywords:
- vs.graphics.designer.effectdesigner
- vs.graphics.shaderdesigner
ms.assetid: 5db09a16-b82c-4ba3-8ec9-630cdc109397
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 1377034853907ce0c3585e4672296c1c8747259f
ms.sourcegitcommit: 75807551ea14c5a37aa07dd93a170b02fc67bc8c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/11/2019
ms.locfileid: "67823863"
---
# <a name="shader-designer"></a>Gölgelendirici Tasarımcısı

Bu belge, Visual Studio ile çalışmaya açıklar **gölgelendirici Tasarımcısı** oluşturmak isterseniz değiştirme ve olarak bilinen özel görsel efektler dışarı *gölgelendiricileri*.

Kullanabileceğiniz **gölgelendirici Tasarımcısı** üst düzey gölgelendirici dili (HLSL) programlama bilmeseniz bile oyunlarda veya uygulamalarda için özel görsel efektler oluşturmak için. Gölgelendirici olarak oluşturmak için **gölgelendirici Tasarımcısı**, teslim bir grafik oluşturun. Diğer bir deyişle, tasarım yüzeyine eklediğiniz *düğümleri* verileri ve işlemleri temsil eder ve ardından verileri nasıl işlemlerini tanımlamak için bunlar arasında bağlantı kurun. Sonuç görselleştirebilir, böylece her işlem düğümünde o noktaya kadar etkili önizlemesi sağlanır. Veri düğümleri gölgelendirici çıkışı temsil eden bir son düğümü doğru akar.

## <a name="supported-formats"></a>Desteklenen biçimler

**Gölgelendirici Tasarımcısı** bu gölgelendirici biçimlerini destekler:

|Biçim Adı|Dosya Uzantısı|Desteklenen işlemler (görüntüleme, düzenleme, dışarı aktarma)|
|-----------------| - | - |
|Yönlü graf gölgelendirici dili|*.dgsl*|Görüntüle, Düzenle|
|HLSL gölgelendirici (kaynak kodu)|*.hlsl*|Dışarı Aktarma|
|HLSL gölgelendirici (bayt)|*.CSO*|Dışarı Aktarma|
|C++ üst bilgisi (HLSL bayt dizesi)|*.h*|Dışarı Aktarma|

## <a name="get-started"></a>Kullanmaya başlayın

Bu bölümde, Visual Studio C++ projenize DGSL gölgelendirici eklemeyi açıklar ve başlamanıza yardımcı olmak için temel bilgiler sağlar.

> [!NOTE]
> Gölgelendirici grafikler (.dgsl dosyaları) gibi grafik öğelerinin otomatik derleme tümleştirmesi yalnızca C++ projeleri için desteklenir.

### <a name="to-add-a-dgsl-shader-to-your-project"></a>Projenize DGSL gölgelendirici ekleme

1. Grafiklerle gerektiğini bileşeni yüklü gerekli Visual Studio olduğundan emin olun. Bileşen çağrılır **görüntü ve 3B model düzenleyicileri**.

   Yüklemek için Visual Studio yükleyicisi seçerek açın **Araçları** > **araçları ve özellikleri Al** çubuğu ve ardından menüden **tek tek bileşenler**sekmesi. Seçin **görüntü ve 3B model düzenleyicileri** altındaki bileşen **oyunlar ve grafik** kategori tıklayın ve ardından **Değiştir**.

   ![Görüntü ve 3B model düzenleyicileri bileşeni](media/image-3d-model-editors-component.png)

2. İçinde **Çözüm Gezgini**, gölgelendirici ekleyin ve ardından istediğiniz C++ projesi için kısayol menüsünü açın **Ekle** > **yeni öğe**.

3. İçinde **Yeni Öğe Ekle** iletişim kutusunun **yüklü**seçin **grafik**ve ardından **görsel gölgelendirici grafiği (.dgsl)** .

   > [!NOTE]
   > Görmüyorsanız **grafik** kategorisinde **Yeni Öğe Ekle** iletişim ve **görüntü ve 3B model düzenleyicileri** bileşeni yüklü, grafik öğeleri desteklenmez Proje türü için.

4. Belirtin **adı** gölgelendirici dosyası ve **konumu** sonra istediğiniz yere oluşturulacak.

5. Seçin **Ekle** düğmesi.

### <a name="the-default-shader"></a>Varsayılan gölgelendiriciyi

İsteğe bağlı olarak bir DGSL gölgelendirici oluşturmak her zaman sadece sahip en az bir gölgelendirici başladığı bir **nokta rengi** bağlı düğüm **son rengini** düğümü. Bu gölgelendiriciyi tam ve işlevsel olsa da, çok yapmaz. Bu nedenle, çalışma gölgelendirici oluşturmanın ilk adımı genellikle silmektir **nokta rengi** düğümü veya bağlantısını kesmeniz **son rengini** diğer düğümler için yer açmak için düğümü.

## <a name="work-with-the-shader-designer"></a>Gölgelendirici Tasarımcısı ile çalışma

Aşağıdaki bölümlerde, gölgelendirici Tasarımcısı özel gölgelendiricilerle çalışmak için nasıl kullanılacağını açıklanmaktadır.

### <a name="shader-designer-toolbars"></a>Gölgelendirici Tasarımcısı araç çubukları

Gölgelendirici Tasarımcısı araç çubukları içeren DGSL gölgelendirici grafikler ile çalışmanıza yardımcı olan komutlar.

Gölgelendirici Tasarımcısı durumunu etkileyen komutlar bulunur **gölgelendirici Tasarımcısı modu** ana Visual Studio penceresinde araç çubuğu. Tasarım araçları ve komutlar bulunur **gölgelendirici Tasarımcısı** gölgelendirici Tasarımcısı tasarım yüzeyinde araç çubuğu.

İşte **gölgelendirici Tasarımcısı modu** araç çubuğu:

![Gölgelendirici Tasarımcısı kalıcı araç çubuğu.](../designers/media/digit-dsd-modal-toolbar.png)

Bu tabloda öğeleri açıklar **gölgelendirici Tasarımcısı modu** araç çubuğu göründükleri soldan sağa doğru sırayla listelenir:

|Araç Çubuğu Öğesi|Açıklama|
|------------------|-----------------|
|**Seçin**|Düğümler ve kenarlar graftaki etkileşimine olanak tanır. Bu modda, düğümleri seçin ve taşıyabilir veya silebilirsiniz ve kenarlar oluşturmak veya bunları bölün.|
|**Pan**|Pencere çerçevesine göre bir gölgelendirici grafiği hareketini sağlar. Kaydırmak için bir tasarım yüzeyi noktasında seçin ve farklı yerlerinde taşıyın.<br /><br /> İçinde **seçin** modu basın ve basılı tutun **Ctrl** etkinleştirmek için **Pan** geçici olarak modu.|
|**Yakınlaştırma**|Gölgelendirici grafiği ayrıntısı pencere çerçevesine göre daha az veya görüntülenmesini sağlar. İçinde **yakınlaştırma** modu, bir tasarım yüzeyi noktasında seçin ve ardından Sağa Taşı veya yakınlaştırmak için aşağı veya sola veya ettirin yetersiz.<br /><br /> İçinde **seçin** modu basın ve basılı tutun **Ctrl** yakınlaştırmak veya uzaklaştırmak fare tekerleğini kullanarak için.|
|**Sığacak kadar Yakınlaştır**|Tam gölgelendirici grafiği pencere çerçevesinde görüntüler.|
|**Gerçek zamanlı işleme modu**|Hiçbir kullanıcı eylemi gerçekleştirilmediğinde bile Visual Studio gerçek zamanlı işleme etkin olduğunda, tasarım yüzeyini yeniden çizer. Bu mod, zamanla değişen gölgelendiriciler ile çalıştığınızda kullanışlıdır.|
|**Küre ile Önizleme**|Etkin olduğunda, bir model kürenin gölgelendiricinin önizlemesini görüntülemek için kullanılır. Aynı anda yalnızca bir önizleme şekli etkinleştirilebilir.|
|**Küp ile Önizleme**|Etkin olduğunda, bir küp modeli gölgelendiricinin önizlemesini görüntülemek için kullanılır. Aynı anda yalnızca bir önizleme şekli etkinleştirilebilir.|
|**Silindir ile Önizleme**|Etkin olduğunda, bir model silindir gölgelendiricinin önizlemesini görüntülemek için kullanılır. Aynı anda yalnızca bir önizleme şekli etkinleştirilebilir.|
|**Koni ile Önizleme**|Etkin olduğunda, bir model bir koni gölgelendiricinin önizlemesini görüntülemek için kullanılır. Aynı anda yalnızca bir önizleme şekli etkinleştirilebilir.|
|**Çaydanlık ile Önizleme**|Etkin olduğunda, bir çaydanlık modelinin gölgelendiricinin önizlemesini görüntülemek için kullanılır. Aynı anda yalnızca bir önizleme şekli etkinleştirilebilir.|
|**Düzlem ile Önizleme**|Etkin olduğunda, bir uçak modelinin gölgelendiricinin önizlemesini görüntülemek için kullanılır. Aynı anda yalnızca bir önizleme şekli etkinleştirilebilir.|
|**Araç Kutusu**|Alternatif olarak gösterir veya gizler **araç kutusu**.|
|**Özellikler**|Alternatif olarak gösterir veya gizler **özellikleri** penceresi.|
|**Gelişmiş**|Gelişmiş komutları ve seçenekleri içerir.<br /><br /> **Dışarı aktarma**: Gölgelendirici çeşitli biçimlerde verilmesini sağlar.<br /><br /> **Dışarı Aktar**: Gölgelendirici ya da HLSL kaynak kodu veya derlenmiş gölgelendirici bytecode'una olarak dışarı aktarır. Gölgelendiricileri dışarı aktarma hakkında daha fazla bilgi için bkz. [nasıl yapılır: Gölgelendiriciyi dışarı aktarma](../designers/how-to-export-a-shader.md).<br /><br /> **Grafik motorları**: Tasarım yüzeyinde görüntülemek için kullanılan Oluşturucu seçimini etkinleştirir.<br /><br /> **D3d11 ile işle**: Gölgelendirici Tasarımcısı tasarım yüzeyini işlemek için Direct3D 11 kullanır.<br /><br /> **D3d11warp ile işle**: Gölgelendirici Tasarımcısı tasarım yüzeyini işlemek için Direct3D 11 Windows Gelişmiş Pikselleştirme Platformu'nu (WARP) kullanır.<br /><br /> **Görünüm**: Gölgelendirici Tasarımcısı hakkında ek bilgi sağlar.<br /><br /> **Kare hızı**: Etkin olduğunda, tasarım yüzeyinin sağ üst köşesinde bulunan geçerli kare hızını görüntüler. Kare hızı, saniye başına çizilen çerçeve sayısıdır. Bu seçenek, etkinleştirdiğinizde kullanışlıdır **gerçek zamanlı işleme modu** seçeneği.|

> [!TIP]
> Seçebileceğiniz **Gelişmiş** düğmesine son komutu yeniden çalıştırın.

### <a name="work-with-nodes-and-connections"></a>Düğümler ve bağlantılar ile çalışma

Kullanım **seçin** eklemek, kaldırmak, yeniden konumlandırma, bağlanma ve düğümleri yapılandırmak için modu. Bu temel işlemleri gerçekleştirmek nasıl aşağıda verilmiştir:

#### <a name="to-perform-basic-operations-in-select-mode"></a>Seçim modunda temel işlemleri gerçekleştirmek için

- İşte nasıl:

  - Grafiğe bir düğüm eklemek, onu seçip **araç kutusu** ve ardından tasarım yüzeyine taşıyın.

  - Grafikten bir düğümü kaldırmak için onu seçin ve tuşuna **Sil**.

  - Bir düğüme yeniden konumlandırmak için onu seçin ve ardından yeni bir konuma taşıyın.

  - İki düğüm bağlanmak için bir çıkış terminal düğümün diğer düğümü için bir giriş uç taşıyın. Uyumlu türleri olan terminaller bağlanabilir. Bir satır Terminaller arasında bağlantı gösterir.

  - Kısayol menüsünde herhangi birine bağlı terminaller yönelik bir bağlantı kaldırmak için **Bağlantıları Kes**.

  - Bir düğüm özelliklerini yapılandırmak için düğümü seçin ve ardından **özellikleri** penceresinde özellikleri için yeni değerler belirtin.

### <a name="preview-shaders"></a>Önizleme gölgelendiricileri

Gölgelendirici uygulamanızda nasıl görüneceğini anlamanıza yardımcı olması için etkili nasıl önizlemesini görebilirsiniz yapılandırabilirsiniz. Uygulamanızı yaklaşık olarak belirlemenizi sağlayan, işleme, dokuları ve diğer malzeme parametreleri yapılandırmak, animasyon zaman tabanlı etkileri etkinleştirmek ve farklı açılardan Önizleme incelemek için birkaç şekil birini seçebilirsiniz.

#### <a name="shapes"></a>Şekiller

Gölgelendirici Tasarımcısı altı şekiller içerir — bir küre, küp, silindir, bir koni, bir çaydanlık ve düzlem — gölgelendiricinizi önizlemek için kullanabilirsiniz. Gölgelendirici bağlı olarak belirli şekiller daha iyi önizleme verebilir.

Bir önizleme şekli üzerinde seçmek için **gölgelendirici Tasarımcısı modu** araç, istediğiniz şekli seçin.

#### <a name="textures-and-material-parameters"></a>Dokular ve malzeme parametreleri

Dokular ve malzeme özelliklerine nesne uygulamanızdaki her tür için benzersiz bir görünüm oluşturmak için birçok gölgelendirici dayanır. Gölgelendiricinizi, uygulamanızda nasıl görüneceğini görmek için dokular ve doku ve uygulamanızda kullanabileceğiniz parametreler eşleştirmek için Önizleme işlemek için kullanılan malzeme özellikleri ayarlayabilirsiniz.

Farklı bir doku bağlamak için bir doku kaydı veya diğer malzeme parametreleri değiştirmek için:

1. İçinde **seçin** modu, tasarım yüzeyinde boş bir alanı seçin. Bu neden **özellikleri** genel gölgelendirici özelliklerini görüntülemek için penceresi.

2. İçinde **özellikleri** penceresinde değiştirmek istediğiniz doku ve parametre özellikleri için yeni değerler belirtin.

Aşağıdaki tabloda, gölgelendirici değiştirebileceğiniz parametreler gösterilmektedir:

|Parametre|Özellikler|
|---------------|----------------|
|**Doku 1** - **doku 8**|**Erişim**:                             **Genel** özelliğin Model Düzenleyicisi'nden Ayarla; tersi durumda, izin vermek için **özel**.<br /><br /> **Filename**: Bu doku kaydı ile ilişkili doku dosyasının tam yolu.|
|**Malzeme ortam**|**Erişim**:                             **Genel** özelliğin Model Düzenleyicisi'nden Ayarla; tersi durumda, izin vermek için **özel**.<br /><br /> **Değer**: Dolaylı - veya ortam - aydınlatma nedeniyle geçerli pikselin yayınık rengi.|
|**Malzeme Yayınık**|**Erişim**: **Genel** özelliğin Model Düzenleyicisi'nden Ayarla; tersi durumda, izin vermek için **özel**.<br /><br /> **Değer**:  Geçerli pikselin doğrudan aydınlatmayı nasıl pürüzlü açıklayan bir renk.|
|**Malzeme Yayımlatıcı**|**Erişim**:                              **Genel** özelliğin Model Düzenleyicisi'nden Ayarla; tersi durumda, izin vermek için **özel**.<br /><br /> **Değer**: Kendi kendine sağlanan aydınlatma nedeniyle geçerli pikselin renk katkısı.|
|**Malzeme Yansımalı**|**Erişim**:                              **Genel** özelliğin Model Düzenleyicisi'nden Ayarla; tersi durumda, izin vermek için **özel**.<br /><br /> **Değer**: Geçerli pikselin doğrudan aydınlatmayı nasıl yansıttığını açıklayan bir renk.|
|**Malzeme Yansımalı güç**|**Erişim**:                             **Genel** özelliğin Model Düzenleyicisi'nden Ayarla; tersi durumda, izin vermek için **özel**.<br /><br /> **Değer**: Geçerli pikselin Yansımalı vurgular yoğunluğunu tanımlayan üs.|

#### <a name="time-based-effects"></a>Zamana bağlı etkileri

Bazı gölgelendirici efekti canlandırır zamana bağlı bir bileşen var. Etkin uygulamada nasıl göründüğünü görmek için önizleme birkaç kez saniyede güncelleştirilmesi gerekir. Gölgelendirici değiştirildiğinde, varsayılan olarak, yalnızca önizleme güncelleştirilir; zamana bağlı etkileri görüntüleyebilmesi için bu davranışı değiştirmek için gerçek zamanlı işleme olanağı vardır.

Gölgelendirici Tasarımcısı araç çubuğunda, gerçek zamanlı işleme etkinleştirmeyi tercih **gerçek zamanlı işleme**.

#### <a name="examine-the-effect"></a>Etkisini inceleyin

Birçok gölgelendirici açısını veya tek yönlü ışık görüntüleme gibi değişkenleri etkilenir. Bu değişkenler değiştikçe etkisi nasıl yanıt vereceğini incelemek için Önizleme şekle serbestçe döndürmek ve gölgelendirici nasıl davranacağını gözlemleyin.

Şekli döndürmek için basılı tutun **Alt**ve ardından tasarım yüzeyinde herhangi bir noktasını seçin ve taşıyın.

### <a name="export-shaders"></a>Gölgelendiricileri dışarı aktarma

Uygulamanızda bir gölgelendirici kullanmadan önce DirectX anlayan bir biçimde dışarı gerekir.

Gölgelendiricileri HLSL kaynak kodu veya derlenmiş gölgelendirici bytecode'una olarak dışarı aktarabilirsiniz. HLSL kaynak kodu içeren bir metin dosyasına dışarı bir *.hlsl* dosya adı uzantısı. Gölgelendirici bytecode'una olabilir ya da olan bir ham ikili dosyası dışarı bir *.cso* dosya adı uzantısı veya C++ üst bilgisi ( *.h*) bir diziye gölgelendirici bytecode'una kodlar dosya.

Gölgelendiricileri dışarı aktarma hakkında daha fazla bilgi için bkz. [nasıl yapılır: Gölgelendiriciyi dışarı aktarma](../designers/how-to-export-a-shader.md).

## <a name="keyboard-shortcuts"></a>Klavye kısayolları

|Komut|Klavye kısayolları|
|-------------| - |
|Geçiş **seçin** modu|**Ctrl**+**G**, **Ctrl**+**Q**<br /><br /> **S**|
|Geçiş **yakınlaştırma** modu|**Ctrl**+**G**, **Ctrl**+**Z**<br /><br /> **Z**|
|Geçiş **Pan** modu|**Ctrl**+**G**, **Ctrl**+**P**<br /><br /> **K**|
|Tümünü seç|**CTRL**+**A**|
|Geçerli seçimi sil|**Delete**|
|Geçerli seçimi iptal et|**Kaçış** (**Esc**)|
|Yakınlaştır|**CTRL**+**fare tekerleği ileriye doğru**<br /><br /> Artı işareti ( **+** )|
|Uzaklaştır|**CTRL**+**fare tekerleği geriye doğru**<br /><br /> Eksi işareti ( **-** )|
|Tasarım yüzeyine yukarı kaydır|**Fare tekerleği geriye doğru**<br /><br /> **PageDown**|
|Tasarım yüzeyine aşağı kaydır|**Fare tekerleği ileriye doğru**<br /><br /> **PageUp**|
|Tasarım yüzeyine sola kaydır|**Shift**+**fare tekerleği geriye doğru**<br /><br /> **Fare tekerleği sol**<br /><br /> **Shift**+**PageDown**|
|Tasarım yüzeyine sağa kaydır|**Shift**+**fare tekerleği ileriye doğru**<br /><br /> **Fare tekerleği sağ**<br /><br /> **Shift**+**PageUp**|
|Klavye odağı başka bir düğüme taşı|**Ok** anahtarları|
|Klavye odağı (düğümü seçimi gruba ekler) olan düğümü seçin|**Shift**+**Ara çubuğu**|
|Klavye girintisine sahip düğümün Seçimi Değiştir|**CTRL**+**Ara çubuğu**|
|Geçerli seçimi Değiştir (düğüm seçilirse, klavye girintisine sahip düğümü seçin)|**Ara çubuğu**|
|Geçerli seçimi Yukarı Taşı|**Shift**+**yukarı ok**|
|Geçerli seçimi aşağı taşı|**Shift**+**aşağı ok**|
|Geçerli seçimi sola taşı|**Shift**+**sol ok**|
|Geçerli seçimi sağa taşı|**Shift**+**sağ ok**.|

## <a name="related-topics"></a>İlgili konular

|Başlık|Açıklama|
|-----------|-----------------|
|[Oyunlar ve uygulamalar için 3B varlıklarla çalışma](../designers/working-with-3-d-assets-for-games-and-apps.md)|Dokular ve resimler, 3B modeller ve gölgelendirici efektleri ile çalışmak için kullanabileceğiniz Visual Studio Araçları'nın genel bir bakış sağlar.|
|[Görüntü Düzenleyicisi](../designers/image-editor.md)|Dokularla ve görüntülerle çalışma için Visual Studio Resim Düzenleyici kullanmayı açıklar.|
|[Model Düzenleyicisi](../designers/model-editor.md)|3B modellerle çalışmak için Visual Studio Model Düzenleyicisi'ni kullanmayı açıklar.|
