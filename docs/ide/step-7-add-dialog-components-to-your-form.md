---
title: '7\. Adım: Formunuza Iletişim kutusu bileşenleri ekleme'
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: ea98c55e-6213-4893-ba7b-f19d7f119527
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: bf6769535082e49d891c7065cc18eb05967dc192
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68925865"
---
# <a name="step-7-add-dialog-components-to-your-form"></a>7\. Adım: Formunuza iletişim kutusu bileşenleri ekleme
Programınızın resim dosyalarını açmasını ve bir arka plan rengi seçmesini etkinleştirmek için, bu adımda formunuza bir <xref:System.Windows.Forms.OpenFileDialog> bileşen <xref:System.Windows.Forms.ColorDialog> ve bileşen eklersiniz.

Bir bileşen, bazı yollarla denetim gibidir. Formunuza bir bileşen eklemek için **araç kutusunu** kullanın ve Özellikler penceresini kullanarak özelliklerini ayarlarsınız. Ancak, bir denetimin aksine formunuza bir bileşen eklemek, kullanıcının formda görebileceği görünür bir öğe eklemez. Bunun yerine, kodla tetikleyebileceğiniz belirli davranışları sağlar. Bu, bir **Dosya Aç** iletişim kutusu açan bir bileşendir.

![video](../data-tools/media/playvideo.gif)bağlantısı bu konunun video sürümü için bkz [. öğretici 1: Visual Basic-video 3](http://go.microsoft.com/fwlink/?LinkId=205213) veya [öğretici 1 ' de bir resim Görüntüleyicisi oluşturun: Video 3 C# ](http://go.microsoft.com/fwlink/?LinkId=205202)' te bir resim Görüntüleyicisi oluşturun. Bu videolar, Visual Studio 'nun önceki bir sürümünü kullanır, bu nedenle bazı menü komutlarında ve diğer kullanıcı arabirimi öğelerinde küçük farklılıklar vardır. Ancak, kavramlar ve yordamlar Visual Studio 'nun geçerli sürümünde benzer şekilde çalışır.

## <a name="to-add-dialog-components-to-your-form"></a>Formunuza iletişim kutusu bileşenleri eklemek için

1. **Windows Form Tasarımcısı** (**Form1.cs [Design]** veya **Form1. vb [Design]** ) seçin ve ardından **araç kutusunda** **iletişim** kutusu grubunu açın.

    > [!NOTE]
    > **Araç kutusundaki** **iletişim** kutusu grubunda, sizin için birçok yararlı iletişim kutusu açan bileşenler bulunur. Bu, dosyaları açmak ve kaydetmek, klasörlere gözatmak ve yazı tipi ve renkler seçmek için kullanılabilir. Bu projede iki iletişim kutusu bileşeni kullanıyorsunuz: OpenFileDialog ve ColorDialog.

2. Formunuza **OpenFileDialog1** adlı bir bileşen eklemek Için, **OpenFileDialog**öğesine çift tıklayın. Formunuza **colorDialog1** adlı bir bileşen eklemek Için **araç kutusunda** **ColorDialog** ' a çift tıklayın. (Bunu bir sonraki öğretici adımında kullanırsınız.) Aşağıdaki resimde gösterildiği gibi, eklediğiniz iki iletişim kutusu bileşeninin bir simgesine sahip **Windows Form Tasarımcısı** ( **Resim Görüntüleyicisi** formunun altında) altında bir alanı görmeniz gerekir.

     ![İletişim kutusu](../ide/media/express_dialogsadded.png)
bileşenleri**iletişim kutusu** bileşenleri

3. **Windows Form Tasarımcısı**altındaki alanda bulunan **OpenFileDialog1** simgesini seçin. İki özellik ayarlayın:

    - **Filter** özelliğini aşağıdaki gibi ayarlayın (kopyalayabilir ve yapıştırabilirsiniz):

        ```
        JPEG Files (*.jpg)|*.jpg|PNG Files (*.png)|*.png|BMP Files (*.bmp)|*.bmp|All files (*.*)|*.*
        ```

    - **Title** özelliğini şu şekilde ayarlayın: **Bir resim dosyası seçin**

         **Filtre** özelliği ayarları, **resim dosyası seç** iletişim kutusunda görünecek dosya türü türlerini belirtir.

    > [!NOTE]
    > Farklı bir uygulamadaki **Dosya Aç** iletişim kutusunun bir örneğini görmek için, **Not defteri** veya **Paint**' i açın ve menü çubuğunda **Dosya** > **Aç**' ı seçin. En altta bulunan bir **dosya türü** aşağı açılan listesi hakkında dikkat edin. Bunu ayarlamak için **OpenFileDialog** bileşeninde **Filter** özelliğini kullandınız. Ayrıca, **başlık** ve **filtre** özelliklerinin **Özellikler** penceresinde nasıl kalın olduğuna dikkat edin. IDE, varsayılan değerlerinden değiştirilmiş olan özellikleri göstermek için bunu yapar.

## <a name="to-continue-or-review"></a>Devam etmek veya gözden geçirmek için

- Sonraki öğretici adımına gitmek için bkz [. 8. Adım: Resim göster düğmesi olay işleyicisi](../ide/step-8-write-code-for-the-show-a-picture-button-event-handler.md)için kod yazın.

- Önceki öğretici adımına dönmek için bkz [. 6. Adım: Düğme denetimlerinizi](../ide/step-6-name-your-button-controls.md)adlandırın.
