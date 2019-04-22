---
title: Kodu yeniden düzenleme
description: Mac ve hızlı eylemler için Visual Studio'yu kullanarak kod iyileştirme.
author: conceptdev
ms.author: crdun
ms.date: 03/29/2019
ms.assetid: C7782BF3-016F-4B41-8A81-85FC540A1A8F
ms.custom: video
ms.openlocfilehash: 48e290fddd1c4b7c95ac5e76cb6cf5908247e6f6
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58856521"
---
# <a name="refactoring"></a>Yeniden Düzenle

Kodu yeniden düzenleme, yeniden düzenleme, yeniden yapılandırmayı ve kodu Genel davranışını değişmeyen sağlarken mevcut kodu açıklamak için bir yoldur.

Yeniden düzenleme, veya herhangi başka bir geliştirici ya koda başvurabilir kullanıcı için fazla kullanım, okunabilir ve sürdürülebilir yaparak daha iyi bir kod tabanına üretir.

Roslyn, Microsoft'un açık kaynak .NET derleyici platformu ile tümleştirme Mac için Visual Studio için daha fazla yeniden düzenleme işlemleri sağlar.

## <a name="renaming"></a>Yeniden adlandırma

*Yeniden Adlandır* komutu yeniden düzenleme tüm kod tanımlayıcısı (örneğin, bir sınıf adı, özellik adı vb.) tüm tanımlayıcı örneklerini bulun ve bunları değiştirmek için kullanılabilir. Bir sembol yeniden adlandırmak için sağ tıklayın ve seçin **yeniden adlandır...** , veya **Cmd (⌘) + R** anahtar bağlama:

![Menü öğesini yeniden adlandırma](media/refactoring-renaming1.png)

Bu, simge ve tüm başvuruları vurgular. Yeni bir ad yazarak başlattığınızda kodunuzdaki tüm başvurularını otomatik olarak değiştirir ve değişikliklerinizi tuşlarına basarak onaylayabilirsiniz **Enter**:

![Yeniden adlandırma ve tanımlayıcı](media/refactoring-renaming2.png)

## <a name="quick-actions"></a>Hızlı Eylemler

Hızlı Eylemler, kolayca yeniden düzenleme sağlar, oluşturmak veya aksi halde kodu tek eylemle değiştirin.

Hızlı eylemler için kullanılabilir:

* Bir kod Çözümleyicisi Kuralı ihlali bir kod düzeltmesini uygulayın
* Bir kod Çözümleyicisi Kuralı ihlali Gizle
* Yeniden düzenleme (örneğin, satır içi geçici değişken) uygulama
* Kod oluşturma (örneğin, bir yerel değişken ekleme)

Ampul kullanarak hızlı Eylemler uygulanabilir ![ampul](media/quick-actions-light-bulb-icon.png) veya tornavida ![tornavida simgesi](media/quick-actions-screwdriver-icon.png) simgeleri veya basarak **seçeneği (⌥)** +  **Girin** imlecinizi bir eylem olduğu kullanılabilir kod satırına olduğunda. Gördüğünüz hata ampul ![hata ampul simgesini](media/quick-actions-error-light-bulb-icon.png) hata belirten bir kırmızı dalgalı çizgi yoktur ve Visual Studio, bu hata için bir düzeltme sahiptir.

Herhangi bir dilde üçüncü taraflara özel tanılama ve öneriler, örneğin bir SDK'ın bir parçası olarak sağlayabilir ve Visual Studio ampuller bu kurallara dayalı vurgulamasında kullanılır.

### <a name="quick-action-icons"></a>Hızlı eylem simgeleri
Hızlı eylem kullanılabilir olduğunda görüntülenen simge, kullanılabilir düzeltme veya yeniden düzenleme tür gittiğinin belirtisini verir. *Tornavida* ![tornavida simgesi](media/quick-actions-screwdriver-icon.png) simgesi gösterir yalnızca kodunu değiştirmek kullanılabilir eylemleri vardır, ancak bunları mutlaka kullanmamalısınız. *Sarı bir ampul* ![ampul](media/quick-actions-light-bulb-icon.png) simgesi gösterir kullanılabilir eylemler, *gereken* kodunuzu geliştirmek için yapın. *Hata ampul* ![hata ampul simgesini](media/quick-actions-error-light-bulb-icon.png) simgesi gösterir, kodunuzdaki bir hatayı düzeltir bir eylem yoktur.

### <a name="to-see-a-light-bulb-or-screwdriver"></a>Ampul veya tornavida görmek için

- Bir düzeltme varsa, bir hatanın konumda fare geldiğinizde ampuller kendiliğinden görünür.

   ![Ampul fare vurgulama ile](media/refactoring-lightbulb-hover.png)

- Giriş işaretini bir hızlı eylem kullanılabilir kod satırına taşıdığınızda ampuller ve tornavidalar düzenleyicinin sol kenar boşluğunda görünür.

- Tuşuna **seçeneği (⌥)**+**Enter** kullanılabilir hızlı Eylemler ve yeniden düzenlemeler listesini görmek için herhangi bir satırında.

![İçerik öğeleri görüntüle](media/refactoring-context-action.png)

Herhangi bir bağlam eylemleri üzerine geldiğinizde, bir önizleme ne eklenecek veya kodunuz içinden kaldırıldı sağlar.

![Seçeneği girin içerik öğeleri](media/refactoring-image2a.png)

Bu seçenekleri etkinleştirmek için seçmelisiniz *açık dosyaların kaynak analizini etkinleştir* seçeneklerinde **Mac için Visual Studio > Tercihler > Metin Düzenleyicisi > kaynak çözümleme**:

![Kaynak analizi etkinleştirme](media/refactoring-options.png)

Etkin veya devre dışı göz atarak önerilebilir, 100'den fazla olası eylemler vardır **Mac için Visual Studio > Tercihler > kaynak çözümleme > C# > kod eylemleri** seçerek veya yanındaki kutuyu seçimini Eylem:

![C# kaynak çözümleme eylemleri](media/refactoring-image3a.png)

### <a name="common-quick-actions"></a>Yaygın hızlı Eylemler

Yaygın hızlı eylemler hakkında daha fazla bilgi [yaygın hızlı Eylemler](/visualstudio/ide/common-quick-actions) makalesi.

## <a name="source-analysis"></a>Kaynak analizi

Kaynak analizi, kodunuzun çalışma sırasında altı çizili olası hataları ve stili ihlalleri tarafından analiz ederek bağlam eylem olarak otomatik sağlama giderir.

Metin Düzenleyicisi sağ tarafında kaydırma çubuğu görüntüleyerek herhangi bir zamanda tüm herhangi bir dosya için kaynak analiz sonuçlarını görüntüleyebilirsiniz:

![Kaynak analizi kenar çubuğu](media/refactoring-image4a.png)

Üst daireye tıklayarak, her öneri yüksek öneme sahip sorunlar ilk gösteren yineleyebilirsiniz. Bir tek tek sonuç veya satır geldiğinizde bağlam eylemleri sabit sorunu görüntüler:

![Kaynak analizi öğesi](media/refactoring-image5.png)

## <a name="related-video"></a>İlgili Video

> [!Video https://channel9.msdn.com/Shows/Visual-Studio-Toolbox/Visual-Studio-for-Mac-Refactoring-Code/player]

## <a name="see-also"></a>Ayrıca bkz.

- [Hızlı Eylemler (Windows için Visual Studio)](/visualstudio/ide/quick-actions)
- [(Windows için Visual Studio) kodu yeniden düzenleyin](/visualstudio/ide/refactoring-in-visual-studio)