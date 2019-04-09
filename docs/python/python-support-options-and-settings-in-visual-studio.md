---
title: Seçenekler ve Python için ayarlar
description: Visual Studio'da Python kodunu ve projeleri ile ilgili çeşitli ayarlar için bir başvuru.
ms.date: 03/13/2019
ms.topic: reference
f1_keywords:
- VS.ToolsOptionsPages.Python_Tools
- VS.ToolsOptionsPages.Python_Tools.General
- VS.ToolsOptionsPages.Python_Tools.Debugging
- VS.ToolsOptionsPages.Python_Tools.Diagnostics
- VS.ToolsOptionsPages.Python_Tools.Experimental
- VS.ToolsOptionsPages.Python_Tools.Interactive_Windows
- VS.ToolsOptionsPages.Text_Editor.Python.Advanced
author: JoshuaPartlow
ms.author: joshuapa
manager: jillfra
ms.workload:
- python
- data-science
ms.openlocfilehash: d917f0211a0888fa2a712b0c010cf6177823c223
ms.sourcegitcommit: 0e22ead8234b2c4467bcd0dc047b4ac5fb39b977
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59365804"
---
# <a name="options-for-python-in-visual-studio"></a>Visual Studio'da Python için seçenekleri

Python seçenekleri görüntülemek için kullanın **Araçları** > **seçenekleri** menü komutu, emin **tüm ayarları göster** seçilir ve ardından gidin  **Python**:

::: moniker range="vs-2017"
![Python Seçenekleri iletişim kutusu, Genel sekmesi](media/options-general.png)
::: moniker-end
::: moniker range=">=vs-2019"
![Python Seçenekleri iletişim kutusu, Genel sekmesi](media/options-general-2019.png)
::: moniker-end

Vardır ayrıca ek Python özgü seçenekler **metin düzenleyici** > **Python** > **Gelişmiş** sekmesinde ve  **Ortam** > **yazı tipleri ve renkler** sekmesindeki **metin düzenleyici** grubu.

> [!Note]
> **Deneysel** grubu olan özellikler hala geliştirme aşamasındadır ve burada belgelenmeyen seçenekleri içerir. Bunlar genellikle gönderilerinde üzerinde açıklanmıştır [Microsoft blog Python Mühendisliği](https://devblogs.microsoft.com/python/).

## <a name="general-options"></a>Genel Seçenekler

(**Araçları** > **seçenekleri** > **Python** sekmesini.)

| Seçenek | Varsayılan | Açıklama |
| --- | --- | --- |
| **Sanal ortamlar oluşturulurken çıkış penceresini göster**| Açık | Clear önlemek için **çıkış** görüntülenmesini penceresi. |
| **Yüklerken veya paketlerini kaldırma çıkış penceresini göster** | Açık | Clear önlemek için **çıkış** görüntülenmesini penceresi. |
| **Ortamlar oluşturmak için bildirimler çubuğunu göster** | Açık | *Yalnızca Visual Studio 2019.* Ne zaman bu seçeneği belirleyin ve kullanıcı içeren bir proje açılır bir *requirements.txt* veya *environment.yml* dosya, Visual Studio, bir bilgi çubuğu ile bir sanal oluşturma önerilerinde bulunma görüntüler ortam ya da conda ortam varsayılan genel ortam kullanmak yerine sırasıyla. |
| **Paketleri yüklemek için bildirimler çubuğunu göster** | Açık | *Yalnızca Visual Studio 2019.* Ne zaman bu seçeneği belirleyin ve kullanıcı içeren bir proje açılır bir *requirements.txt* dosya (ve varsayılan genel ortam kullanmıyor) Visual Studio, geçerli yüklü paketleri ile bu gereksinimleri karşılaştırır ortam. Herhangi bir paket yoksa, Visual Studio bu bağımlılıkların yüklemek için bir istem görüntüler. |
| **Her zaman paket yöneticileri, yönetici olarak çalıştır** | Kapalı | Her zaman yükseltir `pip install` ve tüm ortamlara benzer Paket Yöneticisi işlemleri. Ortamı gibi bir dosya sistemi korumalı alanda yer alıyorsa paketleri yüklenirken, Visual Studio için yönetici ayrıcalıkları ister *c:\Program dosyaları*. Bu komut isteminde yükleme komutunu yalnızca bir bu ortam için her zaman yükseltmesine seçebilirsiniz. Bkz: [paketleri sekmesinde](python-environments-window-tab-reference.md#packages-tab). |
| **Tamamlanma veritabanı ilk kullanımında otomatik olarak oluştur** | Açık | *Visual Studio 2017 sürüm 15.5 ve önceki ve sonraki sürümler için IntelliSense veritabanı kullanılırken geçerlidir.* Bunu kullanan kod yazarken tamamlama için bir kitaplık veritabanı önceliklendirir. Daha fazla bilgi için [IntelliSense sekmesini](python-environments-window-tab-reference.md#intellisense-tab). |
| **Sistem genelinde ise PYTHONPATH değişkenleri yoksay** | Açık | Visual Studio ortamları ve projeleri arama yollarını belirtmek için daha doğrudan bir yolu sağladığından ise PYTHONPATH varsayılan olarak sayılır. Bkz: [arama yolları](search-paths.md) Ayrıntılar için. |
| **Bağlantılı dosyaları eklerken güncelleştirme arama yolları** | Açık | Ayarlanırsa, ekleme, bir [bağlı dosya](managing-python-projects-in-visual-studio.md#linked-files) projeye güncelleştirmeleri [arama yolları](search-paths.md) böylece IntelliSense tamamlanma veritabanına bağlı dosya klasörünün içeriğini içerebilir. İçeriklerin tamamlama veritabanından hariç tutmak için bu seçeneği temizleyin. |
| **İçeri aktarılan uyar, modül bulunamıyor** | Açık | Temiz bir içeri aktarılan modül bildiğinizde uyarıları bastırmak için bu seçeneği şu anda kullanılamıyor ancak Aksi takdirde kodu işlemi etkilemez. |
| **Rapor olarak tutarsız girinti** | **Uyarılar** | Python yorumlayıcısı kapsamını belirlemek için uygun girintisini yoğun bir şekilde bağlı olduğundan, varsayılan olarak Visual Studio kodlama hatalar gösterebilir tutarsız girintileri algıladığında uyarı verir. Kümesine **hataları** daha katı olacak şekilde, programın bu gibi durumlarda, çıkmak neden olur. Bu davranış tamamen devre dışı bırakmak için seçin **yoksa**. |
| **Anket/haber denetle** | **Haftada bir** | *Visual Studio 2017 ve önceki sürümleri.* Varsa bir web sayfasıyla Python ilgili anketler ve haber öğelerini içeren bir pencere açmak Visual Studio izin sıklığını ayarlar. Seçenekler **hiçbir zaman**, **günde bir kez**, **haftada bir kez**, ve **ayda bir kez**. |
| **Tüm gizli kalıcı iletişim kutuları sıfırlama** düğmesi | yok | Farklı iletişim kutularını sağlayan seçenekleri gibi **bunu bir daha gösterme**. Bu seçenekleri temizleyin ve yeniden açmak için iletişim kutularını neden için bu düğmeyi kullanın. |

::: moniker range="vs-2017"
![Python Seçenekleri iletişim kutusu, Genel sekmesi](media/options-general.png)
::: moniker-end
::: moniker range=">=vs-2019"
![Python Seçenekleri iletişim kutusu, Genel sekmesi](media/options-general-2019.png)
::: moniker-end

::: moniker range=">=vs-2019"
## <a name="conda-options"></a>Conda seçenekleri

(**Araçları** > **seçenekleri** > **Python** > **Conda** sekmesini.)

| Seçenek | Varsayılan | Açıklama |
| --- | --- | --- |
| **Conda yürütülebilir dosya yolu** | (boş) | Bir tam yolunu belirtir *conda.exe* Python iş yüküyle eklenmiştir. varsayılan Miniconda yükleme güvenmek yerine yürütülebilir. Burada başka bir yol belirtilmezse, varsayılan yükleme ve kayıt defterinde belirtilen diğer conda.exe yürütülebilir üzerinde öncelik kazanır. El ile Anaconda veya Miniconda daha yeni bir sürümünü yükleyin veya varsayılan 64-bit distro yerine bir 32-bit distro kullanmak istiyorsanız bu ayarı değiştirebilirsiniz. |

![Python Seçenekleri iletişim kutusu, dil sunucu sekmesi](media/options-conda.png)

::: moniker-end

## <a name="debugging-options"></a>Hata ayıklama seçenekleri

(**Araçları** > **seçenekleri** > **Python** > **hata ayıklama** sekmesini.)

| Seçenek | Varsayılan | Açıklama |
| --- | --- | --- |
| **Hatalar bulunduğunda çalıştırmadan önce sor** | Açık | Ne zaman, ister hataları içeren kodu çalıştırmak istediğinizi onaylamak için ayarlayın. Uyarıyı devre dışı bırakmak için bu seçeneği temizleyin. |
| **İşlem olağan dışı çıktığında giriş bekle**<br/><br/>**İşlem normal şekilde çıktığında giriş bekle** | Üzerinde (her ikisi için) | Visual Studio'dan başlatılan bir Python programını kendi konsol penceresinde çalışır. Varsayılan olarak, pencereyi nasıl programdan çıkılır bağımsız olarak kapatmadan önce bir tuşa basın bekler. Bu istem kaldırmak ve pencereyi otomatik olarak kapatmak için bu seçeneklerin ikisi de ya da temizleyin. |
| **Hata ayıklama çıktı penceresine program çıktısı tee** | Açık | Hem bir ayrı konsol penceresi hem de Visual Studio program çıkışı görüntüler **çıkış** penceresi. Yalnızca ayrı konsol penceresinde çıkışının görüntülenmesi için bu seçeneği temizleyin. |
| **SystemExit özel sıfır çıkış kodu ile Kes** | Kapalı | Ayarla, bu özel durum hata ayıklayıcıyı durdurur. Açık olduğunda, hata ayıklayıcı kesme olmadan çıkar. |
| **Python standart kitaplık hata ayıklamayı etkinleştir** | Kapalı | Standart Kitaplığı kaynak kodunu içine Adımlama için hata ayıklama sırasında mümkün kılar, ancak başlatmak hata ayıklayıcının sürelerini artırır.|
| **İşlev dönüş değeri göster** | Açık | *Yalnızca Visual Studio 2019.* İşlev dönüş değerleri görüntüler **Yereller** penceresi sonra bir işlevin Adımlama çağrısı hata ayıklayıcıda (F10) |
| **Eski hata ayıklayıcıyı kullanın** | Kapalı | *Yalnızca Visual Studio 2019.* Eski hata ayıklayıcı varsayılan olarak kullanmak üzere Visual Studio bildirir. Daha fazla bilgi için [hata ayıklama - kullanım eski hata ayıklayıcı](debugging-python-in-visual-studio.md#use-the-legacy-debugger). |

::: moniker range="vs-2017"
![Python Seçenekleri iletişim kutusu, hata ayıklama sekmesi](media/options-debugging.png)
::: moniker-end
::: moniker range=">=vs-2019"
![Python Seçenekleri iletişim kutusu, hata ayıklama sekmesi](media/options-debugging-2019.png)
::: moniker-end

## <a name="diagnostics-options"></a>Tanılama seçenekleri

(**Araçları** > **seçenekleri** > **Python** > **tanılama** sekmesini.)

| Seçenek | Varsayılan | Açıklama |
| --- | --- | --- |
| **Protokoly analýzy içerir** | Açık | Tanılama bir dosyaya kaydedilirken yüklü Python ortamları analiziyle ilgili veya bunları düğmeleri kullanarak panoya kopyalanırken ayrıntılı günlükleri içerir. Bu seçenek, oluşturulan dosyanın boyutunu önemli ölçüde artırabilir, ancak genellikle IntelliSense sorunlarını tanılamak için gerekli değildir. |
| **Tanılama dosyaya Kaydet** düğmesi | yok | Bir dosya adı için ister ve ardından bir metin dosyasına günlüğe kaydeder. |
| **Tanılama Panoya Kopyala** düğmesi | yok | Günlüğün tamamen Pano'ya yerleştirir; Bu işlem günlüğü boyutuna bağlı olarak biraz zaman alabilir. |

![Python Seçenekleri iletişim kutusu, Tanılama sekmesi](media/options-diagnostics.png)

## <a name="interactive-windows-options"></a>Etkileşimli Windows seçenekleri

(**Araçları** > **seçenekleri** > **Python** > **etkileşimli Windows** sekmesini.)

| Seçenek | Varsayılan | Açıklama |
| --- | --- | --- |
| **Komut dosyaları** | yok | Uygulamak başlangıç betikleri için genel bir klasörü belirtiyor **etkileşimli** tüm ortamları için windows. Bkz: [başlatma komut dosyaları](python-environments-window-tab-reference.md#startup-scripts). Ancak, bu özellik şu anda çalışmıyor unutmayın. |
| **Yukarı/aşağı okları geçmişi gidin** | Açık | Geçmişte gezinmek için ok tuşlarını kullanan **etkileşimli** penceresi. İçinde gezinmek için ok tuşlarını kullanmak için bu ayarı temizlemek **etkileşimli** penceresi bunun yerine çıkış. |
| **Tamamlama modu** | **Yalnızca işlev çağrıları olmadan ifadeleri değerlendirme** | İçinde bir ifade üzerinde kullanılabilir üyeler belirleme işlemi **etkileşimli** penceresi, yan etkileri veya birden çok kez çağrılan işlevleri açabilecek geçerli tamamlanmamış ifade değerlendirme gerektirebilir. Varsayılan ayar **nevyhodnocovat işlev çağrıları olmadan yalnızca** bir işlevi çağırmak için görünür, ancak diğer ifadeleri değerlendirir ifadeler dışlar. Örneğin, değerlendirir `a.b` ama `a().b`.  **Nikdy nevyhodnocovat** tüm yan-önerileri yalnızca normal IntelliSense altyapısı kullanılarak etkileri engeller. **Tüm nevyhodnocovat** yan etkileri bağımsız olarak öneriler almak için tam ifadeyi değerlendirir. |
| **Statik analiz önerileri Gizle** | Kapalı | Ayarlandığında, ifadenin değerlendirilmesi yoluyla elde edilen yalnızca önerileri görüntüler. İle birleştirildiğinde **tamamlama modunu** değer **Nikdy nevyhodnocovat**, hiçbir faydalı tamamlamalar görünür **etkileşimli** penceresi. |

![Python Seçenekleri iletişim kutusu, etkileşimli Windows sekmesi](media/options-interactive-windows.png)

::: moniker range=">=vs-2019"
## <a name="language-server-options"></a>Dil sunucusu seçenekleri

(**Araçları** > **seçenekleri** > **Python** > **dil sunucu** sekmesini.)

| Seçenek | Varsayılan | Açıklama |
| --- | --- | --- |
| **Tamamlamalar Typeshed gelen devre dışı bırak** | Kapalı | Visual Studio IntelliSense normalde Typeshed paketlenmiş bir sürümü kullanır (bir dizi *.pyi* dosyaları) tür ipuçlarını standart kitaplığı ve üçüncü taraf kitaplıklar için Python 2 ve Python 3 için bulunamadı. Bu ayar ile birlikte gelen TypeShed davranışı devre dışı bırakır. |
| **Özel Typeshed yol** | (boş) | Ayarlanırsa, Visual Studio ile birlikte gelen sürümü yerine bu yolda Typeshed dosyaları kullanıyorsa. Yoksayın **Typeshed gelen tamamlama devre dışı bırak** ayarlanır. |

![Python Seçenekleri iletişim kutusu, dil sunucu sekmesi](media/options-language-server.png)

::: moniker-end

## <a name="advanced-python-editor-options"></a>Gelişmiş Python Düzenleyici Seçenekleri

(**Araçları** > **seçenekleri** > **metin düzenleyici** > **Python**  >   **Gelişmiş** sekmesini.)

### <a name="completion-results"></a>Tamamlama sonuçları

| Seçenek | Varsayılan | Açıklama |
| --- | --- | --- |
| **Üye tamamlama üyelerini kesişimi görüntüler.** | Kapalı | Ayarlandığında, tüm olası türleri tarafından desteklenen tek tamamlamaları gösterir. |
| **Arama dizesini temel alan filtre listesi** | Açık | Yazdığınız sırada tamamlama önerileri ve filtreleme uygular (varsayılan denetlenir). |
| **Tamamlamalar tüm tanımlayıcıları için otomatik olarak göster** | Açık | Her iki Düzenleyicisi'nde tamamlamaları devre dışı bırakmak için bu seçeneği temizleyin ve **etkileşimli** windows. |

### <a name="selection-in-completion-list"></a>Tamamlama listesindeki seçim

| Seçenek | Varsayılan | Açıklama |
| --- | --- | --- |
| **Aşağıdaki karakterleri yazarak işlendi** | **{}\[\]().,:;+-*/%&&#124;^~=<>#@\\** | Bu karakterler bir karakter yazarak tamamlama kaydetmeye uygun olacak şekilde bir tamamlama listeden seçebilirsiniz. tanımlayıcı genellikle izleyin. Kaldırın veya belirli karakter istenen listesine ekleyin.  |
| **İşlemeler geçerli tamamlama girin** | Açık | Ayarlandığında, **Enter** anahtar seçer ve şu anda seçilmiş tamamlanma karakterler olarak yukarıdaki uygular (ancak Elbette, karakter için hiç **Enter** bu listesine doğrudan Git uygulanamadı şekilde!). |
| **Yeni bir satır eklemek, tam yazılmış kelimenin sonuna enter** | Kapalı | Varsayılan olarak görünen tüm sözcük tamamlama açılır ve ENTER tuşuna yazarsanız **Enter**, o tamamlama işleyin. Tanımlayıcı yazmayı bitirdikten sonra bu seçeneği ayarlayarak, etkili bir şekilde tamamlamaları işleme gibi **Enter** yeni bir satır ekler. |

### <a name="miscellaneous-options"></a>Çeşitli seçenekleri

| Seçenek | Varsayılan | Açıklama |
| --- | --- | --- |
| **Dosyalar açıldığında anahat moduna gir** | Açık | Otomatik olarak Visual Studio düzenleyicisinde anahat oluşturma özelliğini bir Python kodu dosyası açılırken açın. |
| **Yapıştırma REPL istemleri kaldırıldı** | Açık | Kaldırır **>>>** ve **...**  koddan kolayca aktarılmasına izin vererek yapıştırılan metin **etkileşimli** Düzenleyici penceresine. Bu karakterleri diğer kaynaklardan yapıştırırken korumak istiyorsanız bu seçeneği temizleyin. |
| **Türlerine göre renk adı** | Açık | Sözdizimi renklendirme Python kodunda sağlar. |

![Gelişmiş sekmesi, Python Düzenleyici Seçenekleri iletişim](media/options-editor-advanced.png)

## <a name="fonts-and-colors-options"></a>Yazı tipleri ve renkler seçenekleri

(**Ortam** > **yazı tipleri ve renkler** sekmesindeki **metin düzenleyici** grup.)

Python seçenekleri adlarını tüm ön eki **Python** ve kendinden açıklamalıdır. Tüm Visual Studio renk temaları varsayılan yazı tipini 10nk Consolas normal olan (kalın değil). Varsayılan renkler tema göre değişir. Varsayılan ayarlarla metin okunması zor bulursanız, genellikle, bir yazı tipi veya rengini değiştirin.

![Python yazı tipi ve renk seçeneklerini](media/options-fonts-and-colors.png)
