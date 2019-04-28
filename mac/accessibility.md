---
title: Erişilebilirlik
description: Bu makale, Mac ve bunların nasıl etkinleştirilebilir için Visual Studio'nun erişilebilirlik özellikleri tanıtır.
author: conceptdev
ms.author: crdun
ms.date: 04/17/2019
ms.assetid: 2C4AAC2E-3B4A-4496-8BE0-1F5A7F81D1CA
ms.openlocfilehash: 383f9fb46341eec78fa2daa59bba31dde89ac437
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62985287"
---
# <a name="accessibility"></a>Erişilebilirlik

Mac için Visual Studio, daha erişilebilir farklı yeteneklerini kişilere yönelik getirerek aşağıdaki erişilebilirlik özelliklerine sahiptir:

- Çözüm ve Düzenleyicisi bölmeleri içinde metin büyütme
- Metin düzenleyicilerde boyut seçenekleri
- Düzenleyicilerde özelleştirme rengi
- Klavye ile gezinme
- Kısayol özelleştirme
- Yöntem ve parametreler için kod tamamlama

Bu özelliklerin yanı sıra Apple VoiceOver ve yazdırma gibi özel gereksinimleri olan kullanıcılara yardımcı olmak için araçlar sağlar.

MacOS erişilebilirlik özellikleri hakkında daha fazla bilgi için bkz. [Apple'nın Web sitesi](https://www.apple.com/accessibility/mac/).

## <a name="enabling-macos-assistive-technologies-in-visual-studio-for-mac"></a>Mac için Visual Studio'da yardımcı teknolojiler macOS etkinleştirme

Visual Studio Mac desteği macOS yardımcı teknolojiler için varsayılan olarak kapalıdır. Bunu etkinleştirmek için aşağıdaki adımları izleyin:

1. Git **Visual Studio (menü) > Tercihler > Diğer > Erişilebilirlik**

2. Denetleme **etkinleştirme erişilebilirlik** onay kutusu:

   ![Tercihler Erişilebilirlik onay kutusu](media/accessibility-preferences.png)

3. Seçin **Visual Studio'yu yeniden başlatın** düğmesine Visual Studio'yu yeniden başlatın ve Apple'nın yardımcı teknolojiler için destek etkinleştirin.

## <a name="how-to-use-keyboard-navigation"></a>Nasıl yapılır: Klavye gezintisini kullanma

Klavye gezintisi desteği, macOS'ya sağ oluşturulur, ancak gitmek için macOS için en kapsamlı karşılaştığınız için ayarlamalısınız **tüm denetimleri**:

![Tüm denetimleri sistem tercihleri klavye](media/accessibility-preferences-keyboard.png)

Ayarı **tam klavye erişim** için **tüm denetimleri** pencerede veya iletişim tüm denetimleri yoluyla gitmenizi sağlar. Denetimleri kullanarak daha sonra seçebilirsiniz:

- Denetim boyunca ileri gitmek için sekmesinde
- Shift-Sekme denetim boyunca geriye Git
- Oklar yönünü denetimlerin arasında gezinmek için ok tuşları
- Metin alanı kutuları dışında denetim sekmesi
- Boşluk çubuğuna basarak, odağı denetiminde şu anda etkinleştirir.

## <a name="how-to-enable-and-use-voiceover"></a>Nasıl yapılır: Etkinleştirme ve VoiceOver kullanma

Etkinleştirme veya devre dışı VoiceOver tuşuna  **&#8984; CTRL + F5**

VoiceOver komutlar görünür bu kılavuzdaki **VO + * anahtarı*** yapabildiği **VO** kümesinde değiştiricisi başvurduğu **VoiceOver yardımcı programı** uygulama. Varsayılan değiştiricisi **Ctrl + Alt**. Örneğin, VoiceOver değiştiricisi bağlı olarak **VO + M** anlamına gelir **Ctrl + Alt + M**. Konuyu uzatmamak amacıyla, imleç anahtarları için olarak anılacaktır **sol** ve **sağ**vb.

Kullanıcı arabirimi Mac için Visual Studio gitmek için şu tuş bileşimleri kullanın:

- **VO + sağ / sol**: Kullanıcı arabirimi öğeleri arasında gezinme
    - VoiceOver etiket ve denetim türünü duyurmak ve etkileşim açıklanmaktadır.
- **VO + üst karakter + aşağı / ayarlama**: Adım içine / dışına bir öğe
    - Kullanabileceğiniz bir öğesi içinde bir kez **VO + sol / sağ** içindeki öğeleri geçici olarak gezinmek için.
- **VO + Ara çubuğu**: Bir denetimle etkileşim / seçin
- **VO + M**: Menü çubuğu Mac için Visual Studio ile etkileşim kurma

VoiceOver ve kapsamlı komutların listesini kullanarak daha fazla bilgi için lütfen aşağıdaki kılavuzlara bakın:

- [Apple VoiceOver Başlangıç Kılavuzu](https://support.apple.com/en-us/guide/voiceover-guide/welcome/web)
- [MacOS voiceOver komutları](http://lab.dotjay.com/notes/voiceover-commands/)

## <a name="see-also"></a>Ayrıca bkz.

- [(Windows üzerinde) Visual Studio'nun erişilebilirlik özellikleri](/visualstudio/ide/reference/accessibility-features-of-visual-studio)
