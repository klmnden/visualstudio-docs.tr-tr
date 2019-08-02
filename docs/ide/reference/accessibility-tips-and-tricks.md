---
title: Visual Studio için erişilebilirlik ipuçları ve püf noktaları
description: Engelli kişiler de dahil olmak üzere, Visual Studio tümleşik geliştirme ortamının (IDE) herkesin kullanması için daha erişilebilir hale getirmenize yardımcı olabilecek ipuçları ve püf noktaları hakkında daha fazla bilgi edinin.
ms.date: 08/02/2019
ms.topic: conceptual
helpviewer_keywords:
- accessibility [Visual Studio]
ms.assetid: 6b491d88-f79e-4686-8841-857624bdcfda
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 5a3a70f061ea4fd6dd51a3badbed922675b99fba
ms.sourcegitcommit: b56dc6fadc6c924beed36bb4c2ccc16cf6bcfa1c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/02/2019
ms.locfileid: "68740241"
---
# <a name="accessibility-tips-and-tricks-for-visual-studio"></a>Visual Studio için erişilebilirlik ipuçları ve püf noktaları

> [!TIP]
> Erişilebilirlik güncelleştirmeleri hakkında daha fazla bilgi edinmek için [Visual Studio 2017 sürüm 15,3](https://devblogs.microsoft.com/visualstudio/accessibility-improvements-in-visual-studio-2017-version-15-3/) blog gönderisine bakın.

Visual Studio, ekran okuyucular ve diğer yardımcı teknolojilerle uyumlu yerleşik erişilebilirlik özelliklerine sahiptir. Bu konuda, yalnızca klavye ile görevleri gerçekleştirmek için kullanabileceğiniz ortak kısayol tuş birleşimleri ve görünürlüğü geliştirmek için yüksek karşıtlıklı Temalar kullanma hakkında bilgiler yer almaktadır. Ayrıca, kodunuzun hakkındaki yararlı bilgileri göstermek için ek açıklamaların nasıl kullanılacağını ve derleme ve kesme noktası olayları için ses ipuçları ayarlamayı gösterir.

> [!NOTE]
> Bu konu, Windows üzerinde Visual Studio için geçerlidir. Mac için Visual Studio için bkz. [Mac için Visual Studio Için erişilebilirlik](/visualstudio/mac/accessibility).

## <a name="save-your-ide-settings"></a>IDE ayarlarınızı kaydetme

 Pencere düzeninizi, klavye eşleme düzeninizi ve diğer Tercihlerinizi kaydederek IDE deneyiminizi özelleştirebilirsiniz. Daha fazla bilgi için bkz. [Visual STUDIO IDE 'Yi kişiselleştirme](../../ide/personalizing-the-visual-studio-ide.md).

## <a name="modify-your-ide-for-high-contrast-viewing"></a>IDE 'nizi yüksek karşıtlıklı görüntüleme için değiştirme

Bazı katlara, bazı renklerin görülmesi daha zordur. Kodlarken, ancak tipik "Yüksek Karşıtlık" temalarını kullanmak istemediğinizde daha fazla karşıtlık isterseniz, artık "mavi (ekstra Karşıtlık)" teması sunuyoruz.

  ![Mavi temayı ve mavi ekstra Karşıtlık temasını karşılaştırın](media/blue-extra-contrast-theme.png)

## <a name="use-annotations-to-reveal-useful-information-about-your-code"></a>Kodunuzla ilgili yararlı bilgileri açığa çıkarmak için ek açıklamaları kullanın

Visual Studio Düzenleyicisi, screwsürücü ve ampul simgeleri, hata ve uyarı "dalgalı çizgiler", yer işaretleri vb. gibi belirli noktalarda bir kod satırı üzerinde Özellikler ve özellikler hakkında bilgi sahibi olan "donnments" adlı birçok metni içerir. "Satır ek açıklamalarını göster" komut kümesini kullanarak bu donatıcılıkları bulmanıza ve sonra gezinmenize yardımcı olun.

  ![Satır ek açıklamalarını göster komut kümesini kullanın](media/show-line-annotations-command-set.png)

## <a name="access-toolbars-by-using-shortcut-key-combinations"></a>Kısayol tuşu kombinasyonlarını kullanarak araç çubuklarına erişin

Visual Studio IDE 'nin birçok araç penceresi gibi araç çubukları vardır. Aşağıdaki kısayol tuş birleşimleri bunlara erişmenize yardımcı olur.

|Özellik|Açıklama|Anahtar birleşimi|
|-------------|-----------------| - |
|IDE araç çubukları|Standart araç çubuğunda ilk düğmeyi seçin.|**Alt**, **CTRL** + **sekmesi**|
|Araç penceresi araç çubukları|Odağı bir araç penceresinde araç çubuklarına taşıyın. <br> <br> **NOT:** Bu, çoğu araç penceresi için geçerlidir, ancak yalnızca odak bir araç penceresidir. Ayrıca, ALT anahtardan önce SHIFT tuşunu seçmeniz gerekir. Takım Gezgini gibi bazı araç pencerelerinin ALT tuşunu seçmeden önce bir süre için SHIFT tuşunu basılı tutmanız gerekir.|**SHIFT**alt + |
|Araç Çubukları|Sonraki araç çubuğunda ilk öğeye git (bir araç çubuğu odağa sahip olduğunda).|**CTRL**sekmesi + |

### <a name="other-useful-shortcut-key-combinations"></a>Diğer faydalı kısayol tuşu birleşimleri

Diğer bazı faydalı kısayol tuş birleşimleri şunlardır.

|Özellik|Açıklama|Anahtar birleşimi|
|-------------|-----------------| - |
|IDE|Yüksek Karşıtlık açma ve kapatma. <br> <br> **NOT:** Standart Windows kısayolu|**Sol alt + sol SHIFT + PrtScn**|
|İletişim kutusu|İletişim kutusunda onay kutusu seçeneğini belirleyin veya temizleyin. <br> <br> **NOT:** Standart Windows kısayolu|**'Nu**|
|Bağlam menüleri|Bir bağlam açın (sağ tıklama) menüsü. <br> <br> **NOT:** Standart Windows kısayolu|**SHIFT**F10 + |
|Menüler|Kısayol tuşlarını kullanarak bir menü öğesine hızlıca erişin. Komutu etkinleştirmek için **alt** tuşunu ve ardından bir menüdeki altı çizili harfleri seçin. Örneğin, Visual Studio 'da Proje Aç iletişim kutusunu görüntülemek için **alt** + **F** + **O** + **P**'yi seçin.  <br><br> **NOT:** Standart Windows kısayolu|Alt +  **[harf]**|
|Arama kutusu|Visual Studio 'da arama özelliğini kullanın.|**CTRL** + **Q**|
|Araç penceresi|Araç kutusu sekmeleri arasında hareket edin.|CTRL + **yukarı ok**<br /><br /> and<br /><br /> CTRL + **aşağı ok**|
|Araç penceresi|Araç kutusundan bir form veya tasarımcıya denetim ekleyin.|**Girin**|
|Seçenekler iletişim kutusu: > Klavye ortamı|**Kısayol tuşlarına basın** seçeneğinde girilen bir tuş birleşimini silin.|**Geri Al**|
|Bildirimler araç penceresi|İki klavye kısayol tuşu birleşimini ve diğeri tarafından izlenen bildirimler araç penceresini açın. Ardından, ok tuşlarını kullanarak bir bildirimi seçerek bunu seçin.| **T** +  **&#92;** <br>**CTRL**N + |

> [!NOTE]
> İletişim kutuları ve menü komutları gördüğünüz açıklanana Yardım'da, etkin ayarlarınıza ve sürüm bağlı olarak farklı olabilir.

## <a name="use-the-sound-applet-to-set-build-and-breakpoint-cues"></a>Derleme ve kesme noktası ipuçlarını ayarlamak için ses uygulamasını kullanın

Visual Studio program olaylarına bir ses atamak için Windows 'daki ses uygulamasını kullanabilirsiniz. Özellikle, aşağıdaki program olaylarına sesler atayabilirsiniz:

* Kesme noktası isabeti
* Derleme iptal edildi
* Oluşturma başarısız oldu
* Derleme başarılı oldu

Şöyle:

1. Windows 10 çalıştıran bir bilgisayardaki **arama** kutusunda, **sistem seslerini Değiştir**yazın.

   ![Windows 10 ' da arama kutusu](media/type-here-to-search.png)

   (Alternatif olarak, Cortana etkinse, "Hey Cortana" deyin ve "sistem seslerini değiştirme" deyin.

2. **Sistem seslerini Değiştir**' e çift tıklayın.

   ![Windows 10 ' da arama sonuçları](media/change-system-sounds.png)

3. **Ses** iletişim kutusunda, **sesler** sekmesine tıklayın. <br><br>
   Ardından, **Program olayları**' nda, **Microsoft Visual Studio**' ye kaydırın ve seçtiğiniz olaylara uygulamak istediğiniz sesleri seçin.

   ![Windows 10 ' da ses uygulamasının sesler sekmesi](media/sound-applet.png)

4. **Tamam**'ı tıklatın.

## <a name="see-also"></a>Ayrıca bkz.

* [Visual Studio'nun erişilebilirlik özellikleri](../../ide/reference/accessibility-features-of-visual-studio.md)
* [Nasıl yapılır: Visual Studio 'da menüleri ve araç çubuklarını özelleştirme](../../ide/how-to-customize-menus-and-toolbars-in-visual-studio.md)
* [Visual Studio IDE'yi kişiselleştirme](../../ide/personalizing-the-visual-studio-ide.md)
* [Microsoft Erişilebilirlik](https://www.microsoft.com/Accessibility)
* [Erişilebilirlik (Mac için Visual Studio)](/visualstudio/mac/accessibility)