---
title: Erişilebilirlik
description: Bu makalede Mac için Visual Studio erişilebilirlik özellikleri ve bunların nasıl etkinleştiribilecekleri açıklanır.
author: conceptdev
ms.author: crdun
ms.date: 04/17/2019
ms.assetid: 2C4AAC2E-3B4A-4496-8BE0-1F5A7F81D1CA
ms.openlocfilehash: 13b8d40a6ab31d7178e95a3896afa1c85c804f6c
ms.sourcegitcommit: a124076dfd6b4e5aecda4d01984fee7b0c034745
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2019
ms.locfileid: "68787637"
---
# <a name="accessibility"></a>Erişilebilirlik

Mac için Visual Studio aşağıdaki erişilebilirlik özelliklerine sahiptir ve farklı yeteneklere sahip kişiler için daha erişilebilir hale getirir:

- Çözüm ve düzenleyici defterlerindeki metin büyütme
- Metin düzenleyicilerde boyut seçenekleri
- Düzenleyicilerde özelleştirme rengi
- Klavye ile gezinme
- Kısayol özelleştirmesi
- Yöntemler ve parametreler için kod tamamlama

Apple, bu özelliklere ek olarak, VoiceOver ve dikte gibi özel gereksinimlere sahip kullanıcılara yardımcı olmak için çeşitli araçlar sağlar.

MacOS 'taki erişilebilirlik özellikleri hakkında daha fazla bilgi için [Apple 'ın Web sitesine](https://www.apple.com/accessibility/mac/)bakın.

## <a name="enabling-macos-assistive-technologies-in-visual-studio-for-mac"></a>Mac için Visual Studio 'de macOS yardımcı teknolojilerini etkinleştirme

MacOS yardımcı teknolojileri için Mac için Visual Studio desteği varsayılan olarak kapalıdır. Etkinleştirmek için şu adımları izleyin:

1. **Visual Studio 'ya gidin (menü) > tercihler > diğer > erişilebilirliği**

2. **Erişilebilirliği etkinleştir** onay kutusunu işaretleyin:

   ![Tercihler Erişilebilirlik onay kutusu](media/accessibility-preferences.png)

3. Visual Studio 'Yu yeniden başlatmak ve Apple 'ın yardımcı teknolojileri desteğini etkinleştirmek için **Visual Studio 'Yu yeniden Başlat** düğmesini seçin.

## <a name="how-to-use-keyboard-navigation"></a>Nasıl yapılır: Klavye gezintisi kullanma

Klavye gezintisi desteği macOS 'ta oluşturulmuştur, ancak en kapsamlı deneyimlere sahip olmak için macOS 'u **tüm denetimlere**gitmek üzere ayarlamanız gerekir:

![Sistem Tercihleri klavye tüm denetimler](media/accessibility-preferences-keyboard.png)

**Tüm denetimlere** **tam klavye erişiminin** ayarlanması, bir pencere veya iletişim kutusundaki tüm denetimlerde gezinmeniz sağlar. Ardından, kullanarak denetimleri seçebilirsiniz:

- Denetimlerle ileri git sekmesi
- Denetimlerle geriye doğru gitmek için SHIFT-TAB
- Okların yönündeki denetimler arasında hareket etmek için ok tuşları
- Metin alanı kutularından denetim sekmesi
- Boşluk çubuğuna basmak, şu anda odaklanmış olan denetimi etkinleştirir.

## <a name="how-to-enable-and-use-voiceover"></a>Nasıl yapılır: VoiceOver 'i etkinleştirme ve kullanma

VoiceOver 'ı  **&#8984; etkinleştirmek veya devre dışı bırakmak için + F5**

VoiceOver komutları, bu kılavuzda, **VO** 'Nin **VoiceOver yardımcı** uygulamasındaki değiştirici kümesine başvurduğu **VO +_tuşu_**  olarak görünür. Varsayılan değiştirici **Ctrl + Alt**' dir. Örneğin, VoiceOver değiştiriciye bağlı olarak, **VO + d** , **Ctrl + Alt + d**anlamına gelir. Breçekimi için imleç anahtarlarına, **sol** ve **sağ**, vb. olarak başvurulur.

Mac için Visual Studio Kullanıcı arabiriminde gezinmek için aşağıdaki tuş bileşimlerini kullanın:

- **VO + sağ/sol**: Kullanıcı arabirimi öğeleri arasında gezinme
  - VoiceOver, denetimin etiketini ve türünü duyuracaktır ve bununla nasıl etkileşim kuracağınızı açıklar.
- **VO + SHIFT + aşağı/yukarı**: Bir öğenin içine/dışına adımla
  - Bir öğenin içindeyken, içindeki öğelerin etrafında gezinmek için **VO + sola/sağa** ' yı kullanabilirsiniz.
- **VO + boşluk**: Bir denetimle seçme/ile etkileşim kurma
- **VO + Y**: Mac için Visual Studio menü çubuğuyla etkileşim kurma

VoiceOver kullanma hakkında daha fazla bilgi edinmek ve komutların kapsamlı bir listesini almak için lütfen aşağıdaki kılavuzlara bakın:

- [Apple VoiceOver kullanmaya başlama kılavuzu](https://support.apple.com/en-us/guide/voiceover-guide/welcome/web)
- [MacOS içindeki VoiceOver komutları](http://lab.dotjay.com/notes/voiceover-commands/)

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio 'nun erişilebilirlik özellikleri (Windows üzerinde)](/visualstudio/ide/reference/accessibility-features-of-visual-studio)
