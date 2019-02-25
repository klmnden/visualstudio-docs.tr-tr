---
title: Visual Studio için animasyonları | Microsoft Docs
ms.date: 04/26/2017
ms.topic: conceptual
ms.assetid: 446773a9-e6f7-4c0c-8dbc-9e303bf32eb1
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 0d132c9689348fa728fc639d2aa3c8ecd8ba9e25
ms.sourcegitcommit: 1c8e07b98fc0a44b5ab90bcef77d9fac7b3eb452
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/25/2019
ms.locfileid: "56796796"
---
# <a name="animations-for-visual-studio"></a>Visual Studio için animasyonları
## <a name="animation-fundamentals"></a>Animasyonu ile ilgili temel bilgiler

### <a name="animation-best-practices-in-visual-studio"></a>Visual Studio'da animasyon en iyi uygulamalar
Visual Studio IDE arasında tutarlı ve kullanımı kolay animasyon stilleri emin olmak için bu kuralları izleyin.

-   **Seçici olun.** Belirli bir amaca hizmet eder bu animasyonları sınırlayın.

-   **Zamanlama ve hızını önemli** geçişleri hızlı ve doğal düşünüyorsanız emin olmak için:

    -   Animasyonlu geçişler yarım saniye (500 milisaniye cinsinden) içinde tamamlayın.

    -   Sık oluşacak animasyonları kullanıcının iş akışı kesintiye yoksa yeterince hızlı olması gerekir. Döngü içinde animasyon izleyin ve doğru hissettirir kadar zamanlamasını ayarlayın.

    -   Animasyonları, bu nedenle hızlı veya jarring anlaşılması zor ancak değil çok yavaş bir geçişi tamamlamak için sabırsız kolaylaştırır, olduğunu olmamalıdır.

    -   Değişken zamanlama önem vurgulamak için kullanın. Örneğin, bir sınıf diyagramında öğelerinin bir dizisini aracılığıyla gittiğinizde, öğeleri arasında geçişler hızlandırmak sonra önemli öğeye odaklanmayı yavaşlayabilir.

-   **Aşamalı doğrusal olmayan hızlandırma kullanın** diğerine bir durumdan diğerine taşıma sakin ve doğal bir fikir verir.

-   Mümkün olduğunda, **üzerine gelindiğinde zarif bir animasyon kullanın** fare altında etkileşimli öğeleri göstermek için.

-   Yoğun animasyonları özelliklerinizi, ardından kullanan, **kapatmak için bir yol sağlar** yerel olarak (için tüm özelliklerinizi) bir seçenek olarak **Araçlar > Seçenekler** iletişim.

-   **Yalnızca bir animasyon teker teker gerçekleşmesi** ve iletmek yalnızca bir bilgi parçasıdır. Taşıma veya birden çok şey aktarmaya çalışırken birden fazla nesne kafa karıştırıcı olabilir.

-   **Subtlety büyük/küçük harf önemlidir.** Çoğu durumda, animasyon için isteğe bağlı kullanıcı dikkat amacına hizmet yok. Zamanlama, sıralama ve davranışı hafif değişiklikler perception önemli ölçüde etkileyebilir ve maliyetli ve verimsiz bir animasyon arasındaki fark yaratabilir.

-   Animasyon bir şey, dikkat çekmek için kullanırken **kullanıcı kesintiye değer olduğundan emin olun**'s düşünce eğitin.

-   **İlerleme veya durum gösterilirken** animasyon aracılığıyla:

    -   Temel işlemin ne zaman ilerledikten değil ilerleme taşıma gösteren durdurun.

    -   Belirsiz işlemleri kararlı işlemlerden ayırmak.

    -   Bir animasyon tanımlanabilen tamamlama ve hata durumları olduğundan emin olun.

    -   Durumu göster ve gerçek kullanımı için ek bilgi sağlayarak gerçek değeri olduğundan emin olun etkisi animasyonları kullanımını en aza indirin. Örnekler arasında geçici durum değişikliklerini ve acil durumlar bulunur

#### <a name="animation-donts"></a>Animasyon yapılmaması gerekenler:

-   Küçük hareketleri (küçük ayak izine hareket) kullanmayın. Yavaşça tercih nesneleri taşınmadan değiştirir.

-   Büyük bir alanı ekran gerçek boyutunuzu gerçekleşmesi animasyonları kullanmayın. Boyutundan bağımsız olarak, bu stil animasyonun dikkat kullanıcıya dağıtıyor.

-   Kullanıcı şu anda odaklanmıştır nesnesine ilgisi olmayan veya etkileşim animasyonları kullanmayın.

-   Yanıp Durdur sağlamak için bir yanıp sönen bildirime yanıt vermek için kullanıcı zorlama gibi durumunu sıfırlamak için kullanıcı etkileşimi gerektiren animasyonları kullanmayın. Herhangi bir yolla normalde bunları kapatmak yeterli olmalıdır.

Bu en iyi uygulamalar hakkında daha fazla bilgi için bkz. [animasyon desenleri](../../extensibility/ux-guidelines/animations-for-visual-studio.md#BKMK_AnimationPatterns).

### <a name="animation-metrics"></a>Animasyon ölçümleri

-   Sistem görünüşte 10 milisaniyeden kısa kullanıcı hareketleri tepki.

-   Animasyonlu Geçişi tamamlamak için 500 milisaniyeden uzun sürmez.

-   Daha uzun süreleri gerektiren geçişleri için telafi yollarından biri, iki bölüme ayırın sağlamaktır. Örneğin, bir animasyon ilk bölümü tarafından içerik Soluklaşan kapsayıcıya (en fazla 500 milisaniye cinsinden) ardından boş içerik kapsayıcı (en fazla 500 milisaniye) olabilir.

-   Hesaplanabilir yükleme süreleri için determinant İlerleme göstergesi (ilerleme yüzdesi bitti göstergesi) tercih edilir.

-   İmleç veya katıştırılmış dönen animasyon (yükleme veya çalışma göstergesi) gibi bir meşgul göstergesi hesaplanamaz yükleme süreleri için uygundur.

### <a name="animation-as-communicator"></a>Animasyon communicator olarak
Visual STUDİO'da animasyon yalnızca bir iletişim aracı çalışır.  Kullanıcı arabiriminde (örneğin, bir menü açar veya kapatır) yapısal değişiklikler gibi bilgileri çeşitli iletişim kurmak için kullanılır. Animasyon, karmaşık sistemleri, yükleme ilerleme durumunu görselleştirme gibi zamana bağımlı davranışını görselleştirmenize yardımcı olabilir. Animasyonları, uyarılar ve bildirimler ile dikkat çekmek için de kullanılabilir.

 UI animasyonları, genellikle dört şekilde işlev: görselleştirin, dikkat çekmek, benzetimi, ve yanıt sürelerini/ilerleme göstergeleri.

#### <a name="visualize"></a>Görselleştirin
Animasyon, üç boyutlu nesneler yapısını vurgulamak ve kullanıcıların, uzamsal yapılarını görselleştirmek kolaylaştırır. Bunu başarmak için animasyon dolu bir daire nesneyi döndürme için yavaş geri ve İleri etkinleştirmek veya nesne yakın getirin ve biraz geçişi veya odağı vurgulamak için boyutunu artırın.

Üç boyutlu nesneler kullanıcı denetimi ile Tasarımcı önceden (program aracılığıyla veya el ile) belirlemelisiniz taşınmış olabilir ancak nasıl en iyi nesneyi en iyi bir anlayış sağlayan bir taşıma animasyon ekleme. Bu, animasyon can programlanmış sonra kullanıcı, nesneyi işlemek nasıl anlamak kullanıcı tarafından denetlenen hareketleri gerektirdiğinde kullanıcı tarafından nesnenin üzerine imleci yerleştirerek etkinleştirilmesi. Tek bir eksen ya da aynı anda yönünü taşıma sınırı; ya da ölçeklendirin, döndürme, veya Çevir, ancak aynı anda birden fazla desteklemez.

Veri ilişkileri, durumu, yönlerini Görselleştir kategorisi içerir yapısı, dizisi ve saat.

##### <a name="data"></a>Veri
Karmaşık ve değişken bilgilerini göstermektedir:

-   Grafikler gibi görselleştirmelerin bilgi üstünden geçme

-   Bir dizi Adımlama, Kılavuzlu Tur ve disk belleği

-   Ayrıntılarını çağırma işaret eden ve belirli bilgileri vurgulama

-   Ayrıntılar ve ek bilgiler üzerine odaklanan öğeyi planlamanızda

-   Bir yapısal ya da kuruluş gösterimden diğerine morfingu prvku.

-   Zaman zaman kaydırıcıları koşu shuttle tekerlekleri ve Aktarım denetimleri (Yürüt, durdurma ve duraklatma) temsil eden değişiklikler

##### <a name="relationships"></a>İlişkiler

-   Öğeleri birbirleriyle nasıl ilişki kuracağını veya belirli bir öğe için hangi öğeleri arasında ilişki gösterilmektedir.

-   Hiyerarşileri ve üst-alt veya eşdüzey ilişkilerini Göster

-   Başka bir öğe olarak çoğaltılır

-   Bir öğe başka bir öğeye en aza indirir.

-   Bir öğe diğerine tethered tamamen

##### <a name="state"></a>Durum

-   İçerik güncelleştirmeleri

-   Kullanıcı odak ve seçimi

-   İlerleme durumu

-   Hatalar

##### <a name="structure"></a>Yapı

-   Bir düğümde yapısı özetleme

-   Reorienting

-   En aza indirmek ve en üst düzeye çıkarmak, veya genişletme ve daraltma

##### <a name="sequence"></a>Dizisi

-   Slayt gösterisi dizisi

-   Resimleri çevirme

##### <a name="time"></a>Zaman

-   Zaman zaman lapse ve yayını değişimini Göster

-   Çöp, Geri Al ve Yinele Taşı

-   Geçmiş durumuna

#### <a name="attract-attention"></a>Dikkatini
Hedef birkaç dışında tek bir öğe için kullanıcının dikkat çekmek veya güncelleştirilmiş bilgileri için kullanıcıyı uyarmak için ise, bir animasyon uygun olabilir. Örneğin, uygulama başlangıç sayfanızı Başlarken Sayfa yüklendikten sonra yere slaytları bir düğme kullanmak istemiyorsunuz.

Bir kural olarak, son taşınan öğeyi ekranda kullanıcının dikkatini çektiğini.  Animasyonlu öğelerin sıralı, kullanıcının dikkatini son hareket eden nesnenin izler.

##### <a name="alert"></a>Uyarı

-   Kullanıcıyı uyarmak, dikkatini, ilerleme durumunu gösterir

-   Bir şey doğru veya yanlış yapıldığını gösterir veya ilerleme durumunu veya ilerlemesini değişiklikleri göster

-   Çevrimiçi daha fazla bilgi bulmak veya geçerli görevle ilgili öğrenme gibi bir görev sırasında kullanıcılara sor

##### <a name="notifications"></a>Bildirimler

-   Kullanıcı bir hata durumu hakkında uyar

-   Bunlar başka bir şeye katılmayı isteyip istemediğinizi görmek için kullanıcının kesme

-   Yavaşça bir işlemin tamamlandığını kullanıcıyı bilgilendirmeniz veya indirme işlemi tamamlandıktan sonra değiştirildi, ister.

#### <a name="simulate"></a>Benzetimi
Bu kategori, physicality ve işlenemez kapsar.

-   Nesnelerin nereden geldiğini veya bunlar için nereye gösterilmektedir.

-   Genişlet ve Daralt veya açın ve Kapat

-   Yatay kaydırma ve sayfası açar

-   Yığın ve z-sıralamasıyla

-   Döngüsü ve accordion

-   Çevirme ve döndürme kullanıcı Arabirimi

#### <a name="response-and-progress-indicators"></a>Yanıt ve ilerleme göstergeleri
İlerleme göstergesi, birkaç önemli avantajları vardır:

-   Her iki kararlı ve belirsiz ilerleme göstergeleri sistem değil kilitlendi ve bu sorun üzerinde çalıştığı kullanıcı reassure.

-   Kararlı göstergeleri bir güvenliymiş bitiş tarihine yakın almanın yanı sıra bir fikir ne kadar eylem boyunca İlerliyor kullanıcıya sağlayın.

##  <a name="BKMK_AnimationPatterns"></a> Animasyon desenleri

### <a name="overview"></a>Genel Bakış
Visual Studio içinde animasyon, belirli bir işlevi kullanıcı üretkenliğini hindering olmadan yapacak yöneliktir. Genellikle, Visual Studio içinde animasyon olması gerekir:

-   Küçük ve örtük

-   Doğal ve gerçekçi

-   İnce ve subdued

-   Hızlı ve verimli

-   Esnek, hurried değil

Bu çizim, Visual Studio için öneririz animasyon stilleri gösterir. Hiçbir animasyon veya belirerek / Kıs gibi ince animasyonları en sık kullanılır. Sınırlı bir uygulama gibi genişletin ve sözleşme taşıma animasyon, değişiklik ve Döndürme X ve Y konumu.

![Visual Studio için önerilen animasyon stiller](../../extensibility/ux-guidelines/media/1202-a_vsanimstyles.png "1202 a_VSAnimStyles")<br />Visual Studio için önerilen animasyon stilleri

#### <a name="appear-and-disappear"></a>Görünür ve kaybolur
Bu desen ile bir öğe görülemediğinden görünüme giden ve geri geçiş animasyon olmadan geçer.

![Görünür ve animasyon kaybolur](../../extensibility/ux-guidelines/media/1202-b_appearanddisappear.png "1202 b_AppearAndDisappear")<br />Görünür ve animasyon kaybolur

##### <a name="correct-usage"></a>Doğru kullanımı
Yeni kullanıcı Arabirimi öğeleri, böylece kullanıcı dikkatinizin obstructed ne kaybolur veya anında görünür gerekir. Ayrıca, yavaş değişen animasyonları görünmesi ve görünmez olur stiliyle gerçekleşmeyeceğini bir performans Sürükle olarak algılanan.

##### <a name="incorrect-usage"></a>Yanlış kullanımı
Çalışmalarını ne kadar aniden hiçbir fikriniz kullanıcının kullanıcı Arabirimi görüntülenir ve bir animasyon ekleme ile bağlamsal anlamak yardımcı olur.

##### <a name="animation-properties"></a>Animasyon özellikleri
Gecikme süresi genellikle sıfır saniyedir.

##### <a name="examples"></a>Örnekler
-   Araç pencereleri otomatik gizleme

-   Klavye etkinleştirilmiş Düzenleyicisi IntelliSense ve parametre Yardımı gibi kullanıcı Arabirimi

-   Genişletme ve daraltma kod bölgeleri

#### <a name="fade-in-and-fade-out"></a>Belirme ve fade-out
Bu desen ile UI öğesi görünür değil (opaklığı % 0) geçişleri görünür (% 100 opaklık) ya da tam tersi.

![Belirme ve fade-out animasyon](../../extensibility/ux-guidelines/media/1202-c_fadeinfadeout.png "1202 c_FadeInFadeOut")<br />Belirme ve fade-out animasyon

##### <a name="correct-usage"></a>Doğru kullanımı
Bu, en sık UI animasyon önerilir. İlgi akışını kesintiye uğratmadan ekler zarif bir etkisidir. Bazı durumlarda, kullanıcı bile bir animasyon olduğunu sorunsuz bir perceiving ve kullanıcı Arabirimi sistemi akan fark etmiş olabileceğiniz değil.

##### <a name="animation-properties"></a>Animasyon özellikleri

-   Opaklık başlatılıyor: % Belirme, fade-out %100 0

-   Opaklık bitiş: Belirme, %0 fade-out için %100

-   Süresi: 200 milisaniye cinsinden tek başına bir birleşimi animasyon dizisinin bir parçası kullanıldığında 100 milisaniye

-   Kolaylaştırıcı stili: Inout Sinüs

##### <a name="examples"></a>Örnekler

-   Araç pencereleri otomatik gizleme

-   Menü Aç ve Kapat

-   Arka plan ve ön plan sekmesine geçiş

#### <a name="color-blend-from-a-to-b"></a>Renk blend'e a B
Bu desen ile rengi bir kullanıcı Arabirimi öğesi, b rengine değiştirir.

![Renk blend animasyon](../../extensibility/ux-guidelines/media/1202-d_colorblend.png "1202 d_ColorBlend")<br />Renk blend animasyon

##### <a name="correct-usage"></a>Doğru kullanımı
Bir kullanıcı Arabirimi öğesi rengi bir içerik veya durumu diğerine değiştiğinde bir animasyonlu geçişi.

##### <a name="animation-properties"></a>Animasyon özellikleri

-   Başlangıç rengi: Özel kullanıcı Arabirimi

-   Bitiş rengi: Özel kullanıcı Arabirimi

-   Süresi: 200 milisaniye cinsinden tek başına bir birleşimi animasyon dizisinin bir parçası kullanıldığında 100 milisaniye

-   Kolaylaştırıcı stili: Inout Sinüs

##### <a name="examples"></a>Örnekler

-   Belge penceresi durumu geçişleri (etkin ve etkin ve etkin olmayan en son)

-   Araç penceresi durumu geçişleri (odaklı ve plana odaklanmadan)

#### <a name="expand-and-contract"></a>Genişlet ve Daralt
Bu desen ile X, Y veya her iki yönde de UI öğesini genişletir.

![Genişletin ve sözleşme animasyon](../../extensibility/ux-guidelines/media/1202-e_expandcontract.png "1202 e_ExpandContract")<br />Genişletin ve animasyon sözleşme

##### <a name="correct-usage"></a>Doğru kullanımı
Bir kullanıcı Arabirimi öğesi boyutu bir bağlamdan diğerine değiştiğinde bir animasyonlu geçişi.

##### <a name="animation-properties"></a>Animasyon özellikleri

-   Ölçek x: % veya belirli boyutu (piksel cinsinden)

-   Y Ölçek: % veya belirli boyutu (piksel cinsinden)

-   Bağlantı konumu: genellikle (sağdan sola diller için) sol veya sağ üst köşede (için sağdan sola diller)

-   Süresi: 200 milisaniye cinsinden tek başına bir birleşimi animasyon dizisinin bir parçası kullanıldığında 100 milisaniye

##### <a name="examples"></a>Örnekler

-   Mimari Gezgini paneli genişletme ve daraltma

-   Visual Studio 2017 başlangıç sayfası öğesi genişletme ve daraltma

#### <a name="x-y-position-change"></a>X-Y Konum Değiştir
Bu düzende, X veya Y konumunu veya her ikisini de UI öğesi değiştirir.

![X-Y konumunu değiştir animasyon](../../extensibility/ux-guidelines/media/1202-f_xypositionchange.png "1202 f_XYPositionChange")<br />X-Y konumu değişiklik animasyon

##### <a name="correct-usage"></a>Doğru kullanımı
Bir kullanıcı Arabirimi öğesi konumu bir bağlamdan diğerine değiştiğinde bir animasyonlu geçişi olarak.

##### <a name="animation-properties"></a>Animasyon özellikleri

-   Başlangıç X ve Y konumu: Özel kullanıcı Arabirimi

-   Bitiş X ve Y konumu: Özel kullanıcı Arabirimi

-   Hareket yolu: yok

-   Süresi: 200 milisaniye cinsinden tek başına bir birleşimi animasyon dizisinin bir parçası kullanıldığında 100 milisaniye

-   Kolaylaştırıcı stili: Inout Sinüs

##### <a name="example"></a>Örnek
Sekme yeniden sıralama

#### <a name="rotate"></a>Döndür
Bu düzende, kullanıcı Arabirimi öğesi döndürür.

![Kullanıcı Arabirimi öğesi döndürme animasyon](../../extensibility/ux-guidelines/media/1202-g_rotate.png "1202 g_Rotate")<br />Kullanıcı Arabirimi öğesi döndürme animasyon

##### <a name="correct-usage"></a>Doğru kullanımı
Yalnızca belirsiz dönen İlerleme göstergesi için.

##### <a name="animation-properties"></a>Animasyon özellikleri

-   Dönüş derecesini: 360

-   Dönüş Merkezi: nesnenin orta

-   Süre: sürekli

##### <a name="example"></a>Örnek
Belirsiz İlerleme göstergesi (dönen)

### <a name="common-shell-ui-actions-and-recommended-animations"></a>Ortak Kabuk UI eylemlerini ve önerilen animasyonları

#### <a name="tab-open"></a>Açık sekmesi
![Sekme açık animasyon](../../extensibility/ux-guidelines/media/1202-h_tabopen.png "1202 h_TabOpen")<br />Sekme açık animasyon

-   Stil: görüntülenir

-   Süre: sıfır saniye

#### <a name="tab-close"></a>Sekmesini kapatın
![Sekme Kapat animasyon](../../extensibility/ux-guidelines/media/1202-i_tabclose.png "1202 i_TabClose")<br />Sekme Kapat animasyon

-   Stili: X konumu değiştirin

-   Süresi: 200 milisaniye

#### <a name="tab-reorder"></a>Sekme yeniden sıralama
![Visual Studio'da yeniden düzenleme animasyon sekmesinde](../../extensibility/ux-guidelines/media/1202-j_tabreorder.png "1202 j_TabReorder")<br />Sekme yeniden sıralama animasyon

-   Stili: X konumu değiştirin

-   Süresi: 200 milisaniye

#### <a name="close-floating-document"></a>Kayan belgeyi Kapat
![Belge animasyon kayan Kapat](../../extensibility/ux-guidelines/media/1202-k_closefloatingdocument.png "1202 k_CloseFloatingDocument")<br />Kapat kayan belge animasyon

-   Stil: görüntülenir

-   Süresi: 200 milisaniye

#### <a name="window-state-transition"></a>Pencere durum geçişi
![Pencere durum geçişi animasyon](../../extensibility/ux-guidelines/media/1202-l_windowstatetransition.png "1202 l_WindowStateTransition")<br />Pencere durum geçişi animasyon

-   Stil: diğer windows ile tutarlı olması için belgeyi Kapat animasyon tanımlayın geçerli işletim sistemi sağlar.

-   Süresi: 200 milisaniye

#### <a name="menu-open"></a>Menü Aç
![Menü Aç animasyon](../../extensibility/ux-guidelines/media/1202-m_menuopen.png "1202 m_MenuOpen")<br />Menü Aç animasyon

-   Stil: belirme

-   Süresi: 200 milisaniye

#### <a name="menu-close"></a>Menüsünü Kapat
![Menüsünü Kapat animasyon](../../extensibility/ux-guidelines/media/1202-n_menuclose.png "1202 n_MenuClose")<br />Menüsünü Kapat animasyon

-   Stil: fade-out

-   Süresi: 200 milisaniye

#### <a name="auto-hide-tool-window-reveal"></a>Otomatik gizleme araç penceresini göster
![Otomatik gizleme araç penceresini gösterme animasyon](../../extensibility/ux-guidelines/media/1202-o_autohidetoolwindowreveal.png "1202 o_AutoHideToolWindowReveal")<br />Araç penceresini gösterme animasyon otomatik gizleme

-   Stil: görüntülenir

-   Süre: sıfır saniye