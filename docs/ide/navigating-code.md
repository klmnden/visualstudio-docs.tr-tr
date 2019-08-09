---
title: Kod Gezinti komutları
ms.date: 08/14/2018
ms.topic: conceptual
helpviewer_keywords:
- code editor, navigation
- code editor, go to
- code editor, go to definition
- code editor, go to line
- code editor, peek definition
- code editor, navigation bar
- go to definition
- peek definition
- go to line
- go to
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 1263b7a0ae65731eb618ffc925ff0f6310be0f4d
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68919509"
---
# <a name="navigate-code"></a>Koda git

Visual Studio, düzenleyicide kod gezinmek için birçok yol sunar. Bu konu, kodunuzda gezinmek için farklı yollar özetler ve daha fazla ayrıntıya gidecek konuların bağlantılarını sağlar.

## <a name="navigate-backward-and-navigate-forward-commands"></a>Geriye git ve Ileri git komutları

Ekleme işlemini taşımak için **geri git** (**CTRL**+ **-** ) ve **İleri** git (**CTRL**+**Shift**+ **-** ) düğmeleri araç çubuğunda kullanılabilir önceki konumlara işaret edin veya önceki bir konumdan daha yeni bir konuma geri dönmek için. Bu düğmeler, ekleme noktasının son 20 konumunu korur. Bu komutlar Ayrıca **Görünüm** menüsünde **geri git** ' ın altında ve **İleri git**' in altında bulunur.

![İleri ve geri gezinti düğmeleri](../ide/media/vs2017_nav_buttons.png)

## <a name="navigation-bar"></a>Gezinti çubuğu

Kod temelindeki koda gitmek için **Gezinti çubuğunu** (kod penceresinin en üstündeki açılan kutular) kullanabilirsiniz. Doğrudan buna gitmek için bir tür veya üye seçebilirsiniz. Visual Basic, C#veya C++ kod tabanında kod düzenlediğinizde gezinti çubuğu görüntülenir. Kısmi bir sınıfta, geçerli kod dosyası dışında tanımlanan Üyeler devre dışı bırakılabilir (gri renkte görünürler).

![Kod gezinti çubuğu](../ide/media/vside_navigation_bar.png)

Açılır kutuların etrafında aşağıdaki gibi gezinebilirsiniz:

- Geçerli dosyanın ait olduğu başka bir projeye gitmek için sol taraftaki açılan kutuda seçin.

- Bir sınıfa veya türe gitmek için ortadaki açılan kutuda seçin.

- Bir yordama veya bir sınıfın diğer üyesine doğrudan gitmek için sağ açılan kutuda bunu seçin.

- Odağı kod penceresinden gezinti çubuğuna kaydırmak için **CTRL**+**F2**tuş birleşimine basın.

- Odağı gezinti çubuğundaki kutudan kutuya kaydırmak için **Tab** tuşuna basın.

- Odağa sahip olan ve kod penceresine döndürülen gezinti çubuğu öğesini seçmek için **ENTER** tuşuna basın.

- Gezinti çubuğundan bir şeyi seçmeden koda odaklanmak için **ESC** tuşuna basın.

Gezinti çubuğunu gizlemek için, **metin düzenleyici tüm diller** ayarlarında (**Araçlar** > **Seçenekler** > **metin düzenleyici** > **tüm diller**) **Gezinti çubuğu** seçeneğini değiştirin veya ayrı dillerin ayarlarını değiştirebilirsiniz.

## <a name="find-all-references"></a>Tüm başvuruları Bul

Çözümdeki seçili öğenin tüm başvurularını bulur. Bunu, büyük bir yeniden düzenleme için olası yan etkileri denetlemek veya "ölü" kodu doğrulamak için kullanabilirsiniz. Sonuçlar arasında geçmek için **F8** tuşuna basın. Daha fazla bilgi için [kodunuzdaki başvuruları bulma](finding-references.md).

Giriş | İşlev
------------ | ---
**Klavye** | Metin imlecinizi bir yere tür adının içine yerleştirin ve **Shift**+**F12** tuşlarına basın
**Fare** | Sağ tıklama menüsünden **tüm başvuruları bul** ' u seçin

## <a name="reference-highlighting"></a>Başvuru vurgulama

Kaynak kodunda bir simgeye tıkladığınızda, söz konusu simgenin tüm örnekleri belgede vurgulanır. Vurgulanan semboller, bildirim ve başvuru içerebilir ve **tüm başvuruları** içeren diğer birçok sembol döndürülür. Bunlar sınıfların, nesnelerin, değişkenlerin, yöntemlerin ve özelliklerin adlarını içerir. Visual Basic kodda, birçok denetim yapısı için anahtar sözcükler de vurgulanır. İleri veya önceki vurgulanan simgeye gitmek için **CTRL**+**SHIFT**+**aşağı ok** veya **CTRL**+**SHIFT**+**yukarı ok**tuşlarına basın. **Araç**seçenekleri ortam yazı tipi veRenkler > vurgulanan başvuru bölümünde vurgulama rengini değiştirebilirsiniz. >  >  > 

## <a name="go-to-commands"></a>Komutlara git

Git ' in altındaki **Düzenle** menüsünde bulunan aşağıdaki komutlara gidin:

- **Satıra git** (**CTRL**+**G**): Etkin belgede belirtilen satır numarasına git.

- **Tümüne git** (**CTRL**+**T** veyaCTRL+ **,** ): Belirtilen satıra, türe, dosyaya, üyeye veya simgeye taşıyın.

- **Dosyaya git** (**CTRL**+**1**,CTRL+**F**): Çözümdeki belirtilen dosyaya taşıyın.

- **Son dosyaya git** (**CTRL**+**1**,CTRL+**R**): Çözümdeki belirtilen, son ziyaret edilen dosyaya taşı.

- **Türe git** (**CTRL**+**1**,CTRL+**T**): Çözümdeki belirtilen türe taşıyın.

- **Üyeye git** (**CTRL**+**1**, **CTRL**+ı): Çözümdeki belirtilen üyeye git.

- **Simgeye git** (**CTRL**+**1**,CTRL+**S**): Çözümdeki belirtilen simgeye taşıyın.

Visual Studio 2017 sürüm 15,8 ve sonraki sürümlerde, aşağıdaki gezinti komutlarına **Git** de kullanılabilir:

- **Dosyadaki bir sonraki soruna git** (**Alt**+**PgDn**) ve **dosyadaki bir önceki soruna git** (**alt**+**PgUp**)

- **Son düzenleme konumuna git** (**CTRL**+vardiyasıgeri+**Al**)

Bu komutlar hakkında daha fazla bilgi Için bkz. [komutları kullanarak kodu bulma](../ide/go-to.md) bölümüne bakın.

## <a name="go-to-definition"></a>Tanıma Git

Tanıma git, sizi seçili öğenin tanımına götürür. Daha fazla bilgi için bkz. [Tanıma Git ve açıklama açıklaması](../ide/go-to-and-peek-definition.md).

Giriş | İşlev
------------ | ---
**Klavye** | Metin imlecinizi bir yere tür adının içine yerleştirin ve **F12** tuşuna basın
**Fare** | Tür adına sağ tıklayın ve **Tanıma Git** ' i seçin veya **CTRL** tuşuna basın ve tür adına tıklayın

## <a name="peek-definition"></a>Tanıma göz at

Göz atma tanımı, seçili öğenin tanımını, kod düzenleyicisindeki geçerli konumunuzla uzaklaşmadan bir pencerede görüntüler. Daha fazla bilgi için [nasıl yapılır: Özeti Açıklama](../ide/how-to-view-and-edit-code-by-using-peek-definition-alt-plus-f12.md) ' yı kullanarak görüntüleyin ve düzenleyin ve tanım [ve bakış tanımına gidin](../ide/go-to-and-peek-definition.md).

Giriş | İşlev
------------ | ---
**Klavye** | Metin imlecinizi bir yere tür adının içine yerleştirin ve **alt**+**F12** tuşlarına basın
**Fare** | Tür adına sağ tıklayın ve bakış **tanımı** ' nı seçin veya **CTRL** tuşuna basın veya tür adına tıklayın ( **göz atma görünümünde aç seçeneğinde açık tanımı** varsa)

## <a name="go-to-implementation"></a>Uygulamaya git

Uygulamaya git ' i kullanarak, temel bir sınıftan gezinebilirsiniz veya uygulamalarına bir tür ekleyebilirsiniz. Birden çok uygulama varsa, bunları **sembol sonuçları bul** penceresinde listelendiğini göreceksiniz:

Giriş | İşlev
------------ | ---
**Klavye** | Metin imlecinizi bir yere tür adının içine yerleştirin ve **CTRL**+**F12** tuşlarına basın
**Fare** | Tür adına sağ tıklayın ve **uygulamaya git** ' i seçin.

## <a name="call-hierarchy"></a>Çağrı Hiyerarşisi

[Çağrı hiyerarşisi penceresindeki](../ide/reference/call-hierarchy.md)bir yönteme ve bir yöntemine yapılan çağrıları görüntüleyebilirsiniz:

Giriş | İşlev
------------ | ---
**Klavye** | Metin imlecinizi bir yere tür adının içine yerleştirin ve **CTRL**+**K**, **CTRL**+**T** tuşlarına basın
**Fare** | Üye adına sağ tıklayın ve **Çağrı hiyerarşisini görüntüle** ' yi seçin.

## <a name="next-method-and-previous-method-commands-visual-basic"></a>Next yöntemi ve önceki yöntem komutları (Visual Basic)

Visual Basic kod dosyalarında, ekleme noktasını farklı yöntemlere taşımak için bu komutları kullanın. **Sonraki yöntemi** **Düzenle** > veya**önceki yöntemi** **Düzenle** > seçeneğini belirleyin.

## <a name="structure-visualizer"></a>Yapı Görselleştirici

Kod düzenleyicisinde yapı görselleştiricisi özelliği, *Yapı Kılavuzu satırları* -kod tabanınızda eşleşen küme ayraçları belirten dikey kesikli çizgiler gösterir. Bu, mantıksal blokların nerede başlayıp bitmekte olduğunu görmeyi kolaylaştırır.

![Yapı Görselleştirici](../ide/media/vside_structure_visualizer.png)

Yapı Kılavuzu satırlarını devre dışı bırakmak için, **Araçlar** > **Seçenekler** > **metin Düzenleyicisi** > **genel** ' e gidin ve **yapıyı göster kılavuz çizgileri** kutusunu temizleyin.

## <a name="enhanced-scroll-bar"></a>Gelişmiş kaydırma çubuğu

Kodunuzun bir kuşbakışı görünümünü almak için, bir kod penceresinde gelişmiş kaydırma çubuğunu kullanabilirsiniz. Harita modunda, imleci kaydırma çubuğunu yukarı ve aşağı taşıdığınızda kodun önizlemelerini görebilirsiniz. Daha fazla bilgi için [nasıl yapılır: Kaydırma çubuğunu](../ide/how-to-track-your-code-by-customizing-the-scrollbar.md)özelleştirerek kodunuzu izleyin.

## <a name="codelens-information"></a>CodeLens bilgileri

Kod düzenleyicisinde CodeLens kullandığınızda, değişiklikler ve bu değişiklikleri kimin yaptığını, başvuruları, hataları, iş öğelerini, kod incelemelerini ve birim test durumunu oluşturan belirli kod hakkındaki bilgileri bulabilirsiniz. CodeLens, Team Foundation Server Visual Studio Enterprise kullandığınızda bir başlık görünümü gibi çalışır. Bkz. [kod değişikliklerini ve diğer geçmişi bulma](../ide/find-code-changes-and-other-history-with-codelens.md).

## <a name="see-also"></a>Ayrıca bkz.

- [Kod Düzenleyicisi özellikleri](../ide/writing-code-in-the-code-and-text-editor.md)
- [Çağrı hiyerarşisini görüntüle](../ide/reference/call-hierarchy.md)
