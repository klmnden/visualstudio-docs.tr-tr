---
title: '8\. Adım: Resim göster düğmesi olay işleyicisi için kod yazma'
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- csharp
- vb
ms.assetid: 07f4ec00-cda4-42f4-98bb-37edc7167de7
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 01193111cd1c9e89dbdf32847499b6f79008b27d
ms.sourcegitcommit: 59e5758036223ee866f3de5e3c0ab2b6dbae97b6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/23/2019
ms.locfileid: "68416940"
---
# <a name="step-8-write-code-for-the-show-a-picture-button-event-handler"></a>8\. Adım: Resim göster düğmesi olay işleyicisi için kod yazma

Bu adımda, **bir resim göster** düğmesinin şu şekilde çalıştığını yaparsınız:

- Kullanıcı bu düğmeyi seçtiğinde program bir <xref:System.Windows.Forms.OpenFileDialog> kutu açar.

- Bir Kullanıcı bir resim dosyası açarsa, program içinde <xref:System.Windows.Forms.PictureBox>bu resmi gösterir.

IDE 'de kod yazmanıza yardımcı olan, IntelliSense adlı güçlü bir araç vardır. Kod girerken, IDE, girdiğiniz kısmi sözcüklerin önerilen tamamlarla bir kutu açar. Bundan sonra ne yapmak istediğinizi belirlemeyi dener ve listeden seçtiğiniz son öğeyi otomatik olarak atlar. Listede gezinmek için yukarı veya aşağı okları kullanabilir veya seçimleri daraltmak için harfleri yazmaya devam edebilirsiniz. İstediğiniz seçeneği gördüğünüzde, seçmek için **sekme** tuşunu seçin. Veya gerekmiyorsa, önerileri yoksayabilirsiniz.

![video](../data-tools/media/playvideo.gif)bağlantısı bu konunun video sürümü için bkz [. öğretici 1: Visual Basic-video 4](https://msdn.microsoft.com/vstudio/gg315355.aspx)' te bir resim Görüntüleyicisi oluşturun. Bu videoda, Visual Studio 'nun önceki bir sürümü kullanılmaktadır, bu nedenle bazı menü komutlarında ve diğer kullanıcı arabirimi öğelerinde hafif farklılıklar vardır. Ancak, kavramlar ve yordamlar Visual Studio 'nun geçerli sürümünde benzer şekilde çalışır.

## <a name="to-write-code-for-the-show-a-picture-button-event-handler"></a>Resim göster düğmesi olay işleyicisi için kod yazmak için

1. **Windows Form Tasarımcısı** gidin ve **resim göster** düğmesine çift tıklayın. IDE hemen kod tasarımcısına gider ve imlecinizi, daha önce eklediğiniz `showButton_Click()` yöntemin içinde olacak şekilde taşıdır.

2. İki küme `i` ayracı `{ }`arasına boş satıra bir yazın. (Visual Basic, ve `Private Sub...` `End Sub`arasındaki boş satıra yazın.) Aşağıdaki resimde gösterildiği gibi bir **IntelliSense** penceresi açılır.

     ![Visual C&#35; Code ile IntelliSense](../ide/media/express_ifintellisense.png)

3. **IntelliSense** penceresi, sözcüğü `if`vurgulamalıdır. (Değilse, küçük harf `f`girin ve bu işlem olur.) **IntelliSense** penceresinin yanındaki küçük bir *araç ipucu* kutusunun Açıklama, **if ifadesi için kod parçacığı**gibi göründüğünü fark edebilirsiniz. (Visual Basic araç ipucu, bunun bir parçacık olduğunu ancak biraz farklı bir ifade olduğunu da belirtir.) Bu kod parçacığını kullanmak istiyorsanız, kodunuza eklemek `if` için **sekme** tuşunu seçin. Sonra `if` kod parçacığını kullanmak için **Tab** tuşunu yeniden seçin. (Başka bir yerde tercih ederseniz **IntelliSense** penceresi kaybolduysa, üzerine `i` geri yazıp yeniden yazın ve **IntelliSense** penceresi tekrar açılır.)

     ![Visual C&#35; kodu](../ide/media/express_highlighttrue.png)

4. Daha sonra, bir **Dosya Aç** iletişim kutusunu açmak için daha fazla kod girmek üzere IntelliSense 'i kullanırsınız. Kullanıcı **Tamam** düğmesini seçerse, PictureBox kullanıcının seçtiği dosyayı yükler. Aşağıdaki adımlarda kodun nasıl girilmesi gösterilmektedir ve çok sayıda adım olsa da yalnızca birkaç tuş vuruşu vardır:

    1. Kod parçacığında **doğru** seçili metinle başlayın. Üzerine `op` yazmak için yazın. (Visual Basic, ilk Cap ile başlayıp yazın `Op`.)

    2. **IntelliSense** penceresi açılır ve **OpenFileDialog1**görüntüler. Seçmek için **sekme** tuşunu seçin. (Visual Basic bir başlangıç üst sınırı ile başlar, bu nedenle **OpenFileDialog1**görürsünüz. **OpenFileDialog1** seçildiğinden emin olun.)

         Hakkında `OpenFileDialog`daha fazla bilgi için bkz. [OpenFileDialog](<xref:System.Windows.Forms.OpenFileDialog>).

    3. Bir nokta (`.`) yazın (birçok programcı bu noktayı çağırır.) **OpenFileDialog1**sonrasında bir nokta yazdığınızdan, bir **IntelliSense** penceresi açılır ve tüm **OpenFileDialog** bileşeni özellikleri ve yöntemleri ile doldurulur. Bunlar, **Windows Form Tasarımcısı**' de seçerken **Özellikler** penceresinde görüntülenen özelliklerden aynıdır. Ayrıca, bileşene bir şeyler (bir iletişim kutusu aç gibi) yapacağını söyleyen yöntemler de seçebilirsiniz.

        > [!NOTE]
        > **IntelliSense** penceresi her iki özelliği ve yöntemi gösterebilir. Neyin gösterilmekte olduğunu belirlemek için, **IntelliSense** penceresindeki her öğenin sol tarafındaki simgeye bakın. Her yöntemin yanında bir bloğun bir resmini ve her bir özelliğin yanındaki bir wrana (ya da Spanner) resmini görürsünüz. Her olayın yanında bir şimşek simgesi de vardır. Bu resimler aşağıda gösterildiği gibi görüntülenir.

         ![Yöntem simgesi](../ide/media/express_iconmethod.png)

         ![Özellik simgesi](../ide/media/express_iconproperty.png)

         ![Olay simgesi](../ide/media/express_iconevent.png)

    4. Başlangıç türü `ShowDialog` (büyük/küçük harf, IntelliSense için önemli değildir). Yöntemi dosya Aç iletişim kutusunu gösterecektir.  `ShowDialog()` Pencerede **ShowDialog**vurgulandıktan sonra **sekme** tuşunu seçin. Ayrıca, "ShowDialog" ifadesini vurgulayabilir ve yardım almak için **F1** tuşunu seçebilirsiniz.

         `ShowDialog()` Yöntemi hakkında daha fazla bilgi edinmek için bkz. [ShowDialog yöntemi](<xref:System.Windows.Forms.Form.ShowDialog%2A>).

    5. Bir denetim veya bileşen üzerinde bir yöntem kullandığınızda ( *bir yöntemi çağırmak*olarak adlandırılır), parantez eklemeniz gerekir. Bu nedenle, içindeki `ShowDialog`"g" dan hemen sonra açma ve kapatma parantezleri girin: `()`Şimdi "openFileDialog1. ShowDialog ()" şeklinde görünmelidir.

        > [!NOTE]
        > Yöntemler, herhangi bir programın önemli bir parçasıdır ve bu öğretici, yöntemlerin kullanılması için çeşitli yollar göstermiştir. Bir bileşenin yöntemini çağırmak için, **OpenFileDialog** bileşeni `ShowDialog()` yöntemini nasıl adlandırmış olursunuz. Bir Kullanıcı bir düğme seçtiğinde bir iletişim kutusu ve resim açan `showButton_Click()` yöntemi olarak adlandırılan, programınızın sizin oluşturduğunuz gibi işlemler yapması için kendi yöntemlerinizi oluşturabilirsiniz.

    6. Görsel C#için bir boşluk ekleyin ve ardından iki eşittir işareti (`==`) ekleyin. Visual Basic için bir boşluk ekleyin ve sonra tek bir eşittir işareti (`=`) kullanın. (Görsel C# ve Visual Basic farklı eşitlik işleçleri kullanır.)

    7. Başka bir boşluk ekleyin. Bunu yaptığınızda, başka bir **IntelliSense** penceresi açılır. Yazın `DialogResult` ve bu sekmeyi eklemek için **sekme** tuşunu seçin.

        > [!NOTE]
        > Bir yöntemi çağırmak için kod yazdığınızda bazen bir değer döndürür. Bu durumda, **OpenFileDialog** bileşeninin <xref:System.Windows.Forms.CommonDialog.ShowDialog> yöntemi bir <xref:System.Windows.Forms.DialogResult> değer döndürür. DialogResult, iletişim kutusunda ne olduğunu belirten özel bir değerdir. Bir **OpenFileDialog** bileşeni kullanıcının **Tamam** veya `ShowDialog()` **iptal**' i seçmelerini sağlayabilir, bu nedenle yöntemi ya `DialogResult.Cancel`da `DialogResult.OK` döndürür.

    8. DialogResult değeri **IntelliSense** penceresini açmak için bir nokta yazın. Harfi `O` girin ve **Tamam 'ı**eklemek için **sekme** tuşunu seçin.

         DialogResult hakkında daha fazla bilgi edinmek için bkz. [DialogResult](<xref:System.Windows.Forms.DialogResult>).

        > [!NOTE]
        > Kodun ilk satırı tamamlanmalıdır. Görsel C#için aşağıdaki olmalıdır.
        >
        >  `if (openFileDialog1.ShowDialog() == DialogResult.OK)`
        >
        >  Visual Basic için aşağıdaki olmalıdır.
        >
        >  `If OpenFileDialog1.ShowDialog() = DialogResult.OK Then`

    9. Şimdi bir kod satırı ekleyin. Yazabilir (veya kopyalayabilir ve yapıştırabilirsiniz), ancak eklemek için IntelliSense kullanmayı düşünün. IntelliSense ile ne kadar tanıdık olduğunu öğrenin, kendi kodunuzu daha hızlı yazabilirsiniz. Son `showButton_Click()` yönteminiz aşağıdaki gibi görünür.

         [!code-csharp[VbExpressTutorial1Step8#1](../ide/codesnippet/CSharp/step-8-write-code-for-the-show-a-picture-button-event-handler_1.cs)]
         [!code-vb[VbExpressTutorial1Step8#1](../ide/codesnippet/VisualBasic/step-8-write-code-for-the-show-a-picture-button-event-handler_1.vb)]

## <a name="to-continue-or-review"></a>Devam etmek veya gözden geçirmek için

- Sonraki öğretici adımına gitmek için bkz [. Adım 9: Kodunuzu](../ide/step-9-review-comment-and-test-your-code.md)gözden geçirin, yorum yapın ve test edin.

- Önceki öğretici adımına dönmek için bkz [. 7. Adım: Formunuza](../ide/step-7-add-dialog-components-to-your-form.md)iletişim kutusu bileşenleri ekleyin.
