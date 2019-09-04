---
title: '7\. Adım: Formunuza Iletişim kutusu bileşenleri ekleme'
ms.date: 08/30/2019
ms.assetid: ea98c55e-6213-4893-ba7b-f19d7f119527
ms.topic: tutorial
ms.prod: visual-studio-windows
ms.technology: vs-ide-general
ms.devlang:
- csharp
- vb
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 58721610a493283ff0bed8fca9cf6e6f6d668c4d
ms.sourcegitcommit: 9c07ae6fb18204ea080c8248994a683fa12e5c82
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/04/2019
ms.locfileid: "70293474"
---
# <a name="step-7-add-dialog-components-to-your-form"></a>7\. Adım: Formunuza iletişim kutusu bileşenleri ekleme

Programınızın resim dosyalarını açmasını ve bir arka plan rengi seçmesini etkinleştirmek için, bu adımda formunuza bir <xref:System.Windows.Forms.OpenFileDialog> bileşen <xref:System.Windows.Forms.ColorDialog> ve bileşen eklersiniz.

Bir bileşen, bazı yollarla denetim gibidir. Formunuza bir bileşen eklemek için **araç kutusunu** kullanın ve **Özellikler penceresini kullanarak özelliklerini ayarlarsınız** . Ancak, bir denetimin aksine formunuza bir bileşen eklemek, kullanıcının formda görebileceği görünür bir öğe eklemez. Bunun yerine, kodla tetikleyebileceğiniz belirli davranışları sağlar. Bu, bir **Dosya Aç** iletişim kutusu açan bir bileşendir.

## <a name="to-add-dialog-components-to-your-form"></a>Formunuza iletişim kutusu bileşenleri eklemek için

1. **Windows Form Tasarımcısı** (**Form1.cs [Design]** ) öğesini seçin ve ardından **araç kutusundan** **iletişim** kutusu grubunu açın.

    > [!NOTE]
    > **Araç kutusundaki** **iletişim** kutusu grubunda, sizin için birçok yararlı iletişim kutusu açan bileşenler bulunur. Bu, dosyaları açmak ve kaydetmek, klasörlere gözatmak ve yazı tipi ve renkler seçmek için kullanılabilir. Bu projede iki iletişim kutusu bileşeni kullanıyorsunuz: OpenFileDialog ve ColorDialog.

1. Formunuza **OpenFileDialog1** adlı bir bileşen eklemek Için, **OpenFileDialog**öğesine çift tıklayın. Formunuza **colorDialog1** adlı bir bileşen eklemek Için **araç kutusunda** **ColorDialog** ' a çift tıklayın. (Bunu bir sonraki öğretici adımında kullanırsınız.) Aşağıdaki görüntüde gösterildiği gibi, eklediğiniz iki iletişim kutusu bileşeninin bir simgesine sahip **Windows Form Tasarımcısı** ( **Resim Görüntüleyicisi** formunun altında) altında bir alan görmeniz gerekir.

     ![İletişim kutusu bileşenleri](../ide/media/express_dialogsadded.png)<br>***Iletişim kutusu*** *Bileşenler*

1. **Windows Form Tasarımcısı**altındaki alanda bulunan **OpenFileDialog1** simgesini seçin. İki özellik ayarlayın:

    - **Filter** özelliğini aşağıdaki gibi ayarlayın (kopyalayabilir ve yapıştırabilirsiniz):

        ```
        JPEG Files (*.jpg)|*.jpg|PNG Files (*.png)|*.png|BMP Files (*.bmp)|*.bmp|All files (*.*)|*.*
        ```

    - **Title** özelliğini şu şekilde ayarlayın: **Bir resim dosyası seçin**

         **Filtre** özelliği ayarları, **resim dosyası seç** iletişim kutusunda görünecek dosya türü türlerini belirtir.

    > [!TIP]
    > Farklı bir uygulamadaki **Dosya Aç** iletişim kutusunun bir örneğini görmek için, **Not defteri** veya **Paint**' i açın ve menü çubuğunda **Dosya** > **Aç**' ı seçin. Dosya adı ' nın yanında dosya türünü seçmenizi sağlayan bir açılan listenin yanında yer alan bir açılır liste olduğunu unutmayın. <br/><br/>Uygulamanızı ayarlamak için **OpenFileDialog** bileşenindeki **Filter** özelliğini kullandınız. Ayrıca, **başlık** ve **filtre** özelliklerinin **Özellikler** penceresinde nasıl kalın olduğuna dikkat edin. IDE, varsayılan değerlerinden değiştirilmiş olan özellikleri göstermek için bunu yapar.

## <a name="next-steps"></a>Sonraki adımlar

* Sonraki öğretici adımına gitmek için bkz [. 8. Adım: Resim göster düğmesi olay işleyicisi](../ide/step-8-write-code-for-the-show-a-picture-button-event-handler.md)için kod yazın.

* Önceki öğretici adımına dönmek için bkz [. 6. Adım: Düğme denetimlerinizi](../ide/step-6-name-your-button-controls.md)adlandırın.

## <a name="see-also"></a>Ayrıca bkz.

* [Öğretici 2: Süreli matematik testi oluşturma](tutorial-2-create-a-timed-math-quiz.md)
* [Öğretici 3: Eşleşen bir oyun oluşturun](tutorial-3-create-a-matching-game.md)
