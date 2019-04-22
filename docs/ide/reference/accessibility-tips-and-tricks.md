---
title: Erişilebilirlik ipuçları ve püf noktaları için Visual Studio
description: Engelli kişiler de dahil olmak üzere ipuçları ve Visual Studio tümleşik geliştirme ortamı (IDE) kullanmak herkes için daha erişilebilir hale gelmesine yardımcı olabilecek öneriler hakkında daha fazla bilgi edinin.
ms.date: 02/21/2019
ms.topic: conceptual
helpviewer_keywords:
- accessibility [Visual Studio]
ms.assetid: 6b491d88-f79e-4686-8841-857624bdcfda
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: e86791e77d5c8f6eb1e6b88ac663e1f11cc53e1e
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58789698"
---
# <a name="accessibility-tips-and-tricks-for-visual-studio"></a>Erişilebilirlik ipuçları ve püf noktaları için Visual Studio

> [!TIP]
> Erişilebilirlik güncelleştirmeler hakkında daha fazla bilgi edinmek için [erişilebilirlik geliştirmeleri Visual Studio 2017 sürüm 15.3](https://devblogs.microsoft.com/visualstudio/accessibility-improvements-in-visual-studio-2017-version-15-3/) blog gönderisi.

Visual Studio, ekran okuyucuların ve diğer yardımcı teknolojiler ile uyumlu olan yerleşik erişilebilirlik özelliği içerir. Bu konu, yalnızca klavyeyle veya görevleri gerçekleştirmek için kullanabilirsiniz ve yüksek karşıtlıklı tema görünürlüğünü artırmak için kullanma hakkında bilgi içeren ortak kısayol tuş birleşimleri listeler. De kodunuz hakkında yararlı bilgiler açığa çıkarmak için ek açıklamalar kullanmayı gösterir ve ses ayarlama olayları oluşturma ve kesme noktası için ipuçları.

> [!NOTE]
> Bu konu, Windows üzerinde Visual Studio için geçerlidir. Mac için Visual Studio için bkz: [Mac için Visual Studio için erişilebilirlik](/visualstudio/mac/accessibility).

## <a name="save-your-ide-settings"></a>IDE ayarlarınızı kaydedin

 Pencere düzeniniz, klavye eşleme şemasını ve diğer tercihlerinizi kaydederek IDE deneyiminizi özelleştirebilirsiniz. Daha fazla bilgi için [Visual Studio IDE'yi kişiselleştirme](../../ide/personalizing-the-visual-studio-ide.md).

## <a name="modify-your-ide-for-high-contrast-viewing"></a>IDE'nizi yüksek karşıtlık görüntülemek için değiştirin

Bazı yeni başlayanlar için bazı renklerini görmek daha zordur. Daha fazla Karşıtlık, kod olarak istiyor, ancak normal "Yüksek Karşıtlık" temaları kullanmak istemiyorsanız bir "Mavi (ekstra kontrast)" temasına sunuyoruz.

  ![Mavi daha fazla karşıtlık teması ve mavi tema karşılaştırın](media/blue-extra-contrast-theme.png)

## <a name="use-annotations-to-reveal-useful-information-about-your-code"></a>Kodunuz hakkında yararlı bilgiler açığa çıkarmak için ek açıklamalarını kullanma

Visual Studio düzenleyicisinde, "vb. yer işaretleri, özellikleri ve tornavida ve ampul simgeleri, hata ve uyarı"squiggles"gibi bir kod satırında belirli noktalarda özellikleri hakkında bilmeniz olanak tanıyan birçok metin Kenarlıklar" içerir. Ve ardından bu Kenarlıklar arasında gezinebilirsiniz yardımcı olmak için set "Satır ek açıklamalarını göster" komutunu kullanabilirsiniz.

  ![Satır ek açıklamalarını göster komut kümesini kullan](media/show-line-annotations-command-set.png)

## <a name="access-toolbars-by-using-shortcut-key-combinations"></a>Kısayol tuş birleşimleri kullanarak erişim araç çubukları

Visual Studio IDE, birçok araç pencereleri gibi araç çubukları sahiptir. Aşağıdaki kısayol tuş birleşimleri bunlara erişmenize yardımcı olur.

|Özellik|Açıklama|Tuş bileşimi|
|-------------|-----------------| - |
|IDE araç çubukları|Standart araç çubuğundaki ilk düğmeyi seçin.|**Alt**, **Ctrl** + **sekmesi**|
|Araç penceresi araç çubukları|Araç penceresi araç çubuklarını odağı taşıyın. <br> <br> **NOT:** Bu, çoğu araç pencerelerinin, ancak yalnızca odak araç penceresinde olduğunda çalışır. Ayrıca, ALT tuşunu önce SHIFT tuşunu seçmeniz gerekir. Takım Gezgini gibi bazı araç pencerelerinin, ALT tuşunu seçerek önce kısa bir süre için SHIFT tuşunu basılı gerekir.|**Shift** + **Alt**|
|Araç Çubukları|Sonraki araç ilk öğenin (araç odağa sahip olduğunda) gidin.|**CTRL** + **sekmesi**|

### <a name="other-useful-shortcut-key-combinations"></a>Diğer yararlı bir kısayol tuş birleşimleri

Bazı diğer yararlı kısayol tuş birleşimleri arasında şunlar yer alır.

|Özellik|Açıklama|Tuş bileşimi|
|-------------|-----------------| - |
|IDE|Yüksek Karşıtlık açıp geçin. <br> <br> **NOT:** Standart Windows kısayol|**Sol Alt + Sol Shift + PrtScn**|
|İletişim kutusu|İletişim kutusunda bir onay kutusu seçeneğini kaldırın veya seçin. <br> <br> **NOT:** Standart Windows kısayol|**ARA ÇUBUĞU**|
|Bağlam menüleri|(Sağ tıklama) bağlam menüsünü açın. <br> <br> **NOT:** Standart Windows kısayol|**Shift** + **F10**|
|Menüler|Bir menü öğesi, Hızlandırıcı tuşlarıyla hızlıca erişin. Seçin **Alt** bir menü komutu etkinleştirmek için altı çizili harfler arkasından anahtarı. Örneğin, Visual Studio'da proje Aç iletişim kutusunu görüntülemek için seçtiğiniz **Alt** + **F** + **O**  +  **P**.  <br><br> **NOT:** Standart Windows kısayol|**Alt** + **[harf]**|
|Arama kutusu|Visual Studio'da arama özelliğini kullanın.|**CTRL** + **Q**|
|Araç penceresi|Araç kutusu sekmeleri arasında taşıyın.|**CTRL** + **UPARROW**<br /><br /> and<br /><br /> **CTRL** + **DARALTILDI**|
|Araç penceresi|Bir denetimi araç kutusundan bir form veya Tasarımcısı ekleyin.|**Girin**|
|Seçenekler iletişim kutusu: Ortam > klavye|Girilen bir tuş bileşimi Sil **kısayol tuşlarına basın** seçeneği.|**Geri Al**|

> [!NOTE]
> Gördüğünüz iletişim kutuları ve menü komutları, etkin ayarlarınıza ve ürün sürümüne bağlı olarak Yardım menüsünde açıklanana göre farklılık gösterebilir.

## <a name="use-the-sound-applet-to-set-build-and-breakpoint-cues"></a>Ses uygulaması derleme ve kesme noktası ipucu ayarlamak için kullanın

Ses için Visual Studio program olayları atamak için Windows Ses uygulaması kullanabilirsiniz. Özellikle, aşağıdaki program olaylara ses atayabilirsiniz:

* Kesme noktası İsabeti
* Derleme iptal edildi
* Derleme başarısız oldu
* Derleme başarılı

İşte nasıl:

1. İçinde **arama** türü olan Windows 10 çalıştıran bir bilgisayarda kutusu **değiştirme sistem seslerini**.

   ![Windows 10'daki arama kutusu](media/type-here-to-search.png)

   (Alternatif olarak, etkin Cortana varsa, "Hey Cortana" söyleyin ve sonra "Sistem seslerini Değiştir" deyin.)

2. Çift **değiştirme sistem seslerini**.

   ![Windows 10'daki arama sonuçları](media/change-system-sounds.png)

3. İçinde **ses** iletişim kutusu, tıklayın **sesleri** sekmesi. <br><br>
   Ardından **Program olayları**, kaydırma **Microsoft Visual Studio**, seçtiğiniz olaylara uygulamak istediğiniz ses seçin.

   ![Windows 10'daki ses uygulaması sesleri sekmesi](media/sound-applet.png)

4. **Tamam**'ı tıklatın.

## <a name="see-also"></a>Ayrıca bkz.

* [Visual Studio'nun erişilebilirlik özellikleri](../../ide/reference/accessibility-features-of-visual-studio.md)
* [Nasıl yapılır: Menüleri ve Visual Studio araç çubuklarını özelleştirme](../../ide/how-to-customize-menus-and-toolbars-in-visual-studio.md)
* [Visual Studio IDE'yi kişiselleştirme](../../ide/personalizing-the-visual-studio-ide.md)
* [Microsoft Erişilebilirlik](https://www.microsoft.com/Accessibility)
* [Erişilebilirlik (Mac için Visual Studio)](/visualstudio/mac/accessibility)