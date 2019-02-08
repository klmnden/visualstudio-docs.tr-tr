---
title: '7. Adım: Formunuza iletişim kutusu bileşenleri ekleme'
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: ea98c55e-6213-4893-ba7b-f19d7f119527
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: bab093c450a7913ea0f1d3e94b6d04e287c6c539
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55911084"
---
# <a name="step-7-add-dialog-components-to-your-form"></a>7. Adım: Formunuza iletişim kutusu bileşenleri ekleme
Programınızın resim dosyalarınızı açmasını ve bu adımda, bir arka plan rengini seçin etkinleştirmek için bir <xref:System.Windows.Forms.OpenFileDialog> bileşeni ve bir <xref:System.Windows.Forms.ColorDialog> formunuza bileşen.

 Bazı açılardan denetim gibi bir bileşenidir. Kullandığınız **araç kutusu** formunuza ve sizin için bir bileşen eklemek için ayarlama özelliklerini kullanarak **özellikleri** penceresi. Ancak denetimden farklı olarak formunuza bir bileşen eklemek, kullanıcının formda görebileceği görünür bir öğe eklemez. Bunun yerine, kod ile tetikleyebileceğiniz belirli davranışlar sağlar. Açılır bir bileşendir bir **açık dosya** iletişim kutusu.

 ![video bağlantısı](../data-tools/media/playvideo.gif)bu konunun video sürümü için bkz: [öğretici 1: Visual Basic'te - Video 3 resim görüntüleyici oluşturma](http://go.microsoft.com/fwlink/?LinkId=205213) veya [öğretici 1: İçinde resim görüntüleyici oluşturma C# -Video 3](http://go.microsoft.com/fwlink/?LinkId=205202). Bazı menü komutlarında ve diğer kullanıcı arabirimi öğelerinde küçük farklılıklar olduğundan bu videolarda Visual Studio'nun önceki bir sürümü kullanın. Ancak, kavramlar ve yordamlar benzer şekilde Visual Studio'nun geçerli sürümünde çalışır.

## <a name="to-add-dialog-components-to-your-form"></a>Formunuza iletişim kutusu bileşenleri eklemek için

1.  Seçin **Windows Form Tasarımcısı** (**Form1.cs [Design]** veya **Form1.vb [Design]**) ve ardından açın **iletişim kutuları** grubu **Araç kutusu**.

    > [!NOTE]
    >  **İletişim kutuları** grubu **araç kutusu** açma ve dosyaları kaydetmek, klasörlere göz atma ve yazı tiplerini ve renkleri seçmek için kullanılabilecek pek çok yararlı iletişim kutuları, açılan bileşenden oluşur. Bu projede iki iletişim kutusu bileşeni kullanırsınız: OpenFileDialog ve ColorDialog.

2.  Adlı bir bileşen eklemek için **openFileDialog1** formunuza, çift **OpenFileDialog**. Adlı bir bileşen eklemek için **colorDialog1** formunuza, çift **ColorDialog** içinde **araç kutusu**. (Bir sonraki Eğitmen adımında kullanın.) Sayfanın alt kısmında bir alan görmelisiniz **Windows Form Tasarımcısı** (altındaki **resim görüntüleyici** form) sahip bir simge her biri, eklediğiniz iki iletişim kutusu bileşenleri için aşağıdaki resimde gösterildiği gibi.

     ![İletişim kutusu bileşenleri](../ide/media/express_dialogsadded.png)
**iletişim** bileşenleri

3.  Seçin **openFileDialog1** kısmındaki alanındaki simgenin **Windows Form Tasarımcısı**. İki özellikleri ayarlayın:

    -   Ayarlama **filtre** özelliğini aşağıdaki (kopyalayın ve yapıştırın):

        ```
        JPEG Files (*.jpg)|*.jpg|PNG Files (*.png)|*.png|BMP Files (*.bmp)|*.bmp|All files (*.*)|*.*
        ```

    -   Ayarlama **başlık** özelliğini aşağıdaki: **Bir resim dosyası seçin**

         **Filtre** özellik ayarları görüntülenecek dosya türlerinin çeşitlerini belirtir **Resim Seç** dosya iletişim kutusu.

    > [!NOTE]
    >  Bir örnek görmek için **Dosya Aç** farklı bir uygulama Aç iletişim kutusunda **not defteri** veya **Boya**ve menü çubuğunda, **dosya**  >  **Açık**. Nasıl olduğuna dikkat edin bir **dosya türü** altındaki aşağı açılan listeden. Yalnızca kullanılan **filtre** özelliğinde **OpenFileDialog** kurmak için bileşen. Ayrıca, nasıl **başlık** ve **filtre** özellikleri kalın **özellikleri** penceresi. IDE, varsayılan değerleri değiştirilmiş özellikleri size göstermek için yapar.

## <a name="to-continue-or-review"></a>Devam etmek veya gözden geçirmek için

-   Sonraki öğretici adımına gitmek için bkz: [adım 8: Bir resim düğme olayı işleyicisi Göster için kod yazma](../ide/step-8-write-code-for-the-show-a-picture-button-event-handler.md).

-   Önceki öğretici adımına dönmek için bkz: [adım 6: Düğme denetimlerinizi adlandırma](../ide/step-6-name-your-button-controls.md).
