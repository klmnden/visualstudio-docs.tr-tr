---
title: '6\. Adım: Düğme denetimlerinizi adlandırma'
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- csharp
- vb
ms.assetid: 56b3baa3-651e-4ad4-8942-e334c5c57158
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 2051ac669c52480d62ee0d0a79c5a165bff502fc
ms.sourcegitcommit: 59e5758036223ee866f3de5e3c0ab2b6dbae97b6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/23/2019
ms.locfileid: "68416600"
---
# <a name="step-6-name-your-button-controls"></a>6\. Adım: Düğme denetimlerinizi adlandırma
Formunuz üzerinde yalnızca bir <xref:System.Windows.Forms.PictureBox> tane vardır. Bunu eklediğinizde, IDE otomatik olarak **PictureBox1**olarak adlandırılır. Yalnızca **CheckBox1**adlı bir <xref:System.Windows.Forms.CheckBox>tane vardır. Yakında bazı kodlar yazacaksınız ve bu kod CheckBox ve PictureBox öğesine başvuracaktır. Bu denetimlerden yalnızca biri olduğundan, kodunuzda **PictureBox1** veya **CheckBox1** gördüğünüz zaman ne anlama geldiğini bilirsiniz.

> [!NOTE]
> Visual Basic, herhangi bir denetim adının varsayılan ilk harfi ilk tepdir, bu nedenle adlar **PictureBox1**, **CheckBox1**vb. olur.

 Formunuzda dört düğme vardır ve bunları **button1**, **button2**, **BUTTON3**ve **Button4**olarak adlandırılan IDE. Yalnızca geçerli adlarına bakarak, hangi düğmenin **kapatma** düğmesi olduğunu ve hangilerinin **resim göster** düğmesi olduğunu bilemezsiniz. Bu nedenle, düğme denetimlerinizi daha bilgilendirici adlar yararlı olur.

 ![video](../data-tools/media/playvideo.gif)bağlantısı bu konunun video sürümü için bkz [. öğretici 1: Visual Basic-video 3](http://go.microsoft.com/fwlink/?LinkId=205213) veya [öğretici 1 ' de bir resim Görüntüleyicisi oluşturun: Video 3 C# ](http://go.microsoft.com/fwlink/?LinkId=205202)' te bir resim Görüntüleyicisi oluşturun. Bu videolar, Visual Studio 'nun önceki bir sürümünü kullanır, bu nedenle bazı menü komutlarında ve diğer kullanıcı arabirimi öğelerinde küçük farklılıklar vardır. Ancak, kavramlar ve yordamlar Visual Studio 'nun geçerli sürümünde benzer şekilde çalışır.

## <a name="to-name-your-button-controls"></a>Düğme denetimlerinizi adlandırmak için

1. Formda, **Kapat** düğmesini seçin. (Tüm düğmeler seçiliyse, seçimi iptal etmek için **ESC** tuşunu seçin.) **(Ad)** özelliğini görene kadar **Özellikler** penceresinde kaydırma yapın. ( **(Ad)** özelliği, Özellikler alfabetik olduğunda üst kısımdaki bir yakındır.) Aşağıdaki resimde gösterildiği gibi, adı **CloseButton**olarak değiştirin.

     ![CloseButton **adı ile** CloseButton](../ide/media/express_setnameproperty.png)
ad**özellikleri** penceresiyle Özellikler penceresi

    > [!NOTE]
    > Düğme adını **CloseButton**olarak değiştirmeyi denerseniz, kapat ve düğme arasında bir boşluk ile IDE bir hata iletisi görüntüler: "Özellik değeri geçerli değil." Denetim adlarında boşluklara (ve diğer birkaç karaktere) izin verilmez.

2. Diğer üç düğmeyi backgroundButton,  **clearButton**ve **showButton**olarak yeniden adlandırın. **Özellikler** penceresinde denetim Seçicisi açılan listesini seçerek adları doğrulayabilirsiniz. Yeni düğme adları görüntülenir.

3. Formdaki **resim göster** düğmesine çift tıklayın. Alternatif olarak, formda **bir resim göster** düğmesini seçin ve ardından **ENTER** tuşunu seçin. Bunu yaptığınızda IDE, **Form1.cs** adlı ana pencerede ek bir sekme açar (Visual Basic kullanıyorsanız**Form1. vb** ). Bu sekme, aşağıdaki resimde gösterildiği gibi, formun arkasındaki kod dosyasını gösterir.

     ![Görsel C# kod içeren Visual C&#35; Code](../ide/media/express_showbuttoncode.png)
**Form1.cs** sekmesi ile Form1.cs sekmesi

4. Kodun bu bölümüne odaklanın. (Kodun Visual Basic sürümünü görüntülemek için Visual Basic kullanıyorsanız aşağıdaki **vb** sekmesini seçin.)

     [!code-vb[VbExpressTutorial1Step6#1](../ide/codesnippet/VisualBasic/step-6-name-your-button-controls_1.vb)]
     [!code-csharp[VbExpressTutorial1Step6#1](../ide/codesnippet/CSharp/step-6-name-your-button-controls_1.cs)]

     Adlandırılan `showButton_Click()`koda bakıyorsunuz. IDE bunu, **showButton** düğmesi için kod dosyasını açtığınızda formun koduna eklemiştir. Tasarım zamanında, bir formdaki denetim için kod dosyasını açtığınızda, zaten mevcut değilse denetim için kod oluşturulur. *Yöntem*olarak bilinen bu kod, programınızı çalıştırdığınızda çalışır ve bu durumda, **bir resim göster** düğmesi.

    > [!NOTE]
    > Bu öğreticide, otomatik olarak oluşturulan Visual Basic kodu, `()`parantezler arasındaki her şeyi kaldırarak basitleştirilmiştir. Bu her gerçekleştiğinde, aynı kodu kaldırabilirsiniz. Programınız her iki şekilde de çalışır. Öğreticilerin geri kalanı için, mümkün olduğunda otomatik olarak oluşturulan tüm kodlar basitleştirilir.

5. **Windows Form Tasarımcısı** sekmesini bir kez daha seçin (**Form1.cs [Design]** with C#Visual, **Form1. vb [Design]** Visual Basic) ve ardından formun kodunda bir yöntem oluşturmak için **Resmi Temizle** düğmesini açmak üzere kod dosyasını açın. Bunu kalan iki düğme için tekrarlayın. Her seferinde IDE, formun kod dosyasına yeni bir yöntem ekler.

6. Bir yöntemi daha eklemek için, IDE 'nin bir `checkBox1_CheckedChanged()` Yöntem eklemesini sağlamak üzere **Windows Form Tasarımcısı** **onay kutusu** denetimi için kod dosyasını açın. Bu yöntem, Kullanıcı onay kutusunu seçtiğinde veya temizlediğinde çağrılır.

    > [!NOTE]
    > Bir program üzerinde çalışırken genellikle kod Düzenleyicisi ve **Windows Form Tasarımcısı**arasında geçiş yapabilirsiniz. IDE, projenizde gezinmeyi kolaylaştırır. **Windows Form Tasarımcısı** açmak için **Çözüm Gezgini** kullanın Visual Basic, Visual C# veya *Form1. vb* içindeki *Form1.cs* çift tıklayarak ya da menü çubuğunda, **Görünüm** > **Tasarımcısı**' nı seçin.

     Aşağıdaki kod düzenleyicisinde gördüğünüz yeni kodu gösterir.

     [!code-vb[VbExpressTutorial1Step6#2](../ide/codesnippet/VisualBasic/step-6-name-your-button-controls_2.vb)]
     [!code-csharp[VbExpressTutorial1Step6#2](../ide/codesnippet/CSharp/step-6-name-your-button-controls_2.cs)]

     Eklediğiniz beş yöntem *olay işleyicileri*olarak adlandırılır, çünkü bir olay (Kullanıcı bir düğme seçme veya bir kutu seçme gibi) olduğunda programınız bunları çağırır.

     Tasarım zamanında IDE 'deki bir denetimin kodunu görüntülediğinizde, Visual Studio bir tane değilse denetim için bir olay işleyici yöntemi ekler. Örneğin, bir düğmeye çift tıkladığınızda IDE, <xref:System.Windows.Forms.Control.Click> olayı için bir olay işleyicisi ekler (Kullanıcı düğmeyi seçtiğinde çağrılır). Bir onay kutusunu çift tıklattığınızda, IDE, <xref:System.Windows.Forms.CheckBox.CheckedChanged> olayı için bir olay işleyicisi ekler (Kullanıcı kutuyu seçtiğinde veya temizlediğinde çağrılır).

     Bir denetim için bir olay işleyicisi ekledikten sonra, denetime çift tıklayarak veya menü çubuğunda**kodu** **görüntüle** > ' yi seçerek **Windows Form Tasarımcısı** istediğiniz zaman buna dönebilirsiniz.

     Programlar oluştururken adlar önemlidir ve Yöntemler (olay işleyicileri dahil) istediğiniz herhangi bir ada sahip olabilir. IDE ile bir olay işleyicisi eklediğinizde, denetimin adına ve işlenmekte olan olaya göre bir ad oluşturur. Örneğin, **showButton** adlı bir düğmenin Click olayına `showButton_Click()` olay işleyicisi yöntemi denir. Ayrıca, yöntemlerin açıklanmakta olduğunu `()` göstermek için, açma ve kapatma parantezleri genellikle yöntem adından sonra eklenir. Kod değişkeni adını değiştirmek istediğinize karar verirseniz, koddaki değişkene sağ tıklayıp**yeniden** **Düzenle** > ' yi seçin. Koddaki bu değişkenin tüm örnekleri yeniden adlandırılır. Daha fazla bilgi için bkz. [yeniden düzenlemeyi yeniden adlandırma](../ide/reference/rename.md) .

## <a name="to-continue-or-review"></a>Devam etmek veya gözden geçirmek için

- Sonraki öğretici adımına gitmek için bkz [. 7. Adım: Formunuza](../ide/step-7-add-dialog-components-to-your-form.md)iletişim kutusu bileşenleri ekleyin.

- Önceki öğretici adımına dönmek için bkz [. 5. Adım: Formunuza](../ide/step-5-add-controls-to-your-form.md)denetimler ekleyin.
