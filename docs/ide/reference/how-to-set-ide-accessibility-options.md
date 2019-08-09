---
title: 'Nasıl yapılır: IDE erişilebilirlik seçeneklerini ayarlama'
description: Visual Studio 'da kendi tümleşik geliştirme ortamının (IDE), okuma güçlüğü çeken kişiler ve yazma sınırlaması olan kişiler de dahil olmak üzere herkesin kullanması için daha kolay hale gelen erişilebilirlik seçeneklerini nasıl ayarlayacağınızı öğrenin.
ms.date: 08/22/2017
ms.topic: conceptual
helpviewer_keywords:
- accessibility [Visual Studio]
ms.assetid: ddc96c4c-0600-46c1-8267-7dce4c44ad24
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 7a0b5835333bf8cd41ab653108054e2d3dd4c73e
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68919279"
---
# <a name="how-to-set-ide-accessibility-options"></a>Nasıl yapılır: IDE erişilebilirlik seçeneklerini ayarlama

> [!TIP]
> Son erişilebilirlik güncelleştirmeleri hakkında daha fazla bilgi edinmek için [Visual Studio 2017 sürüm 15,3](https://devblogs.microsoft.com/visualstudio/accessibility-improvements-in-visual-studio-2017-version-15-3/) blog gönderisine bakın.

[!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)]az görme zorluğu olan kişilerin ve yazma zorluğu sınırlı kişiler için okumayı kolaylaştıran özellikler içerir. Bu özellikler, düzenleyicilerde metnin boyut ve renginin değiştirilmesini, araç çubuklarındaki metin ve düğmelerin boyutunu değiştirmeyi, yöntemlerin ve parametrelerin otomatik olarak tamamlanmasını de bir kaç tane ad edileceğini içerir.

Ayrıca, [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] en sık yazılan karakterlerin daha erişilebilir olmasını sağlayan Dvorak klavye düzenlerini destekler. Ayrıca, ile [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)]kullanılabilen varsayılan kısayol tuşlarını özelleştirebilirsiniz. Daha fazla bilgi için [tanımlama ve özelleştirme klavye kısayolları](../../ide/identifying-and-customizing-keyboard-shortcuts-in-visual-studio.md).

> [!NOTE]
> Gördüğünüz iletişim kutuları ve menü komutları, etkin ayarlarınıza ve ürün sürümüne bağlı olarak Yardım menüsünde açıklanana göre farklılık gösterebilir. Ayarlarınızı değiştirmek için seçin **içeri ve dışarı aktarma ayarları** üzerinde **Araçları** menüsü. Daha fazla bilgi için [ayarlarına](../environment-settings.md#reset-settings).

## <a name="editors-dialogs-and-tool-windows"></a>Düzenleyiciler, diyaloglar ve araç pencereleri

Varsayılan olarak, içindeki [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] iletişim kutuları ve araç pencereleri işletim sistemiyle aynı yazı tipi boyutunu ve renklerini kullanır. IDE, iletişim kutuları, araç çubukları ve araç pencerelerinin çerçevesinin renk ayarları bir renk düzenini temel alarak: açık veya koyu. Geçerli renk temasını [Genel, ortam, Seçenekler iletişim kutusunda](../../ide/reference/general-environment-options-dialog-box.md)değiştirebilirsiniz.

Ayrıca, düzenleyicinin kod görünümünde açılır pencereleri de görüntüleyebilirsiniz. Bu pencereler geçerli nesne üzerindeki kullanılabilir Üyeler ve bir işlevi veya ifadeyi tamamlamaya yönelik parametreler için sizi uyarır. Yazma güçlüğü çekiyorsanız, bu pencereler yararlı olabilir. Ancak, bu kişiler, bazı kullanıcılar için sorunlu olabilecek kod düzenleyicisine odaklanmayı engellemez. Bu pencereleri devre dışı bırakarak, Seçenekler iletişim kutusunu açıp **otomatik liste üyelerini** ve **parametre bilgilerini** **metin düzenleyicisinde**, **tüm diller**, **genel** sayfasında bulunan Seçenekler iletişim kutusunda temizleyerek temizleyebilirsiniz.

Tümleşik geliştirme ortamındaki (IDE) pencereleri, çalışma şeklinize en uygun şekilde yeniden düzenleyebilirsiniz. Her bir araç penceresini yerleştirme, kaydırma, gizleme veya otomatik olarak gizleme yapabilirsiniz.

Pencere düzenlerini değiştirme hakkında daha fazla bilgi için bkz. [Özelleştirme pencere düzenleri](../../ide/customizing-window-layouts-in-visual-studio.md).

### <a name="changing-the-size-of-text"></a>Metnin boyutunu değiştirme

**Komut** penceresi, **anlık** pencere ve **Çıkış** penceresi gibi metin tabanlı araç pencerelerinin ayarlarını, **Araçlar** iletişim kutusundaki **ortam** seçeneklerinin **yazı tipi ve renkler** bölmesinde değiştirebilirsiniz. **Ayarları göster** açılan listesinde **[tüm metin araç pencereleri]** seçildiğinde, varsayılan ayar **öğe ön planı** ve **öğe arka plan** açılan listelerinde **varsayılan** olarak listelenir. Ayrıca, metnin düzenleyicide nasıl görüntüleneceği için ayarları değiştirebilirsiniz.

#### <a name="to-change-the-size-of-text-in-text-based-tool-windows-and-editors"></a>Metin tabanlı araç pencereleri ve düzenleyicilerde metnin boyutunu değiştirmek için

1. **Araçlar** menüsünde **Seçenekler**' i seçin.

2. **Ortam** klasöründeki **yazı tiplerini ve renkleri** seçin.

3. **Ayarları göster** açılan menüsünde bir seçenek belirleyin.

     Bir düzenleyicideki metnin yazı tipi boyutunu değiştirmek için **metin düzenleyici**' yi seçin.

     Metin tabanlı araç penceresinde metnin yazı tipi boyutunu değiştirmek için **[tüm metin araç pencereleri]** öğesini seçin.

     Bir düzenleyicideki Araç Ipucu metninin yazı tipi boyutunu değiştirmek için **Düzenleyici araç ipucu**' nu seçin.

     Ekstre tamamlama açılır penceresinde metin yazı tipi boyutunu değiştirmek için, **ekstre tamamlama**' yı seçin.

4. **Görüntüleme öğelerinden** **düz metin**' i seçin.

5. **Yazı tipi**' nde yeni bir yazı tipi türü seçin.

6. **Boyut**' da, yeni bir yazı tipi boyutu seçin.

    > [!NOTE]
    > Metin tabanlı araç pencereleri ve düzenleyicilerinin metin boyutunu sıfırlamak için **Varsayılanları Kullan**' ı seçin.

7. **Tamam**’ı seçin.

### <a name="change-the-colors-that-are-used-in-the-ide"></a>IDE 'de kullanılan renkleri değiştirme

Ayrıca, düzenleyicideki metin, kenar boşluğu göstergeleri, boşluk ve kod öğeleri için varsayılan renkleri değiştirmeyi de seçebilirsiniz.

> [!NOTE]
> İşletim sisteminizdeki tüm uygulama pencereleri için yüksek karşıtlık renkleri kullanmak istiyorsanız sol <strong>alt +</strong>sol **SHIFT + PRINT Screen**tuşlarına basın. Açıksa, yüksek karşıtlık renklerini tam olarak uygulamak için kapatın ve yeniden açın [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)]. [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)]

#### <a name="to-change-the-color-of-items-in-the-editor"></a>Düzenleyicideki öğelerin rengini değiştirmek için

1. **Araçlar** menüsünde **Seçenekler**' i seçin.

2. **Ortam** klasöründe, **yazı tipleri ve renkler**' i seçin.

3. **Ayarları göster**bölümünde **metin düzenleyici**' yi seçin.

4. **Görüntüleme öğelerinden** **düz metin**, **Gösterge kenar boşluğu**, **görünür**boşluk, **HTML öznitelik adı**veya **XML özniteliği**gibi görüntülemesi gereken görünümü olan bir öğe seçin.

5. Aşağıdaki seçeneklerden görüntüleme ayarları ' nı seçin: **Öğe ön planı**, **öğe arka planı**ve **kalın**.

6. **Tamam**’ı seçin.

## <a name="toolbars"></a>Araç Çubukları

Araç çubuğu kullanılabilirliğini ve erişilebilirliğini geliştirmek için araç çubuğu düğmelerine metin ekleyebilirsiniz.

### <a name="to-assign-text-to-toolbar-buttons"></a>Araç çubuğu düğmelerine metin atamak için

1. **Araçlar** menüsünde **Özelleştir**' i seçin.

2. **Özelleştir** Iletişim kutusunda **Komutlar** sekmesini seçin.

3. **Araç çubuğu** ' nu seçin ve ardından metnini görüntülemeyi düşündüğünüz düğmeyi içeren araç çubuğu adını seçin.

4. Listede, değiştirmek istediğiniz komutu seçin.

5. **Seçimi Değiştir**' i seçin.

6. **Görüntü ve metin**seçin.

### <a name="to-modify-the-displayed-text-in-a-button"></a>Bir düğmedeki görüntülenecek metni değiştirmek için

1. **Seçimi Değiştir**' i yeniden seçin.

2. **Ad**alanına bitişik, Ekle seçili düğme için yeni bir başlık girin.

## <a name="see-also"></a>Ayrıca bkz.

* [Visual Studio'nun erişilebilirlik özellikleri](../../ide/reference/accessibility-features-of-visual-studio.md)
* [Erişilebilir uygulamalar tasarlamak için kaynaklar](../../ide/reference/resources-for-designing-accessible-applications.md)