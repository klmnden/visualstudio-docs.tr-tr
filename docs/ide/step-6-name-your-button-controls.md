---
title: '6. Adım: Düğme denetimlerinizi adlandırma'
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 56b3baa3-651e-4ad4-8942-e334c5c57158
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 9dbee780f2153003e870dbe0dbbb15b721a009df
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63442028"
---
# <a name="step-6-name-your-button-controls"></a>6. Adım: Düğme denetimlerinizi adlandırma
Yalnızca bir tane <xref:System.Windows.Forms.PictureBox> formunuzdaki. Onu eklediğinizde IDE otomatik olarak bunu adlı **pictureBox1**. Yalnızca bir tane <xref:System.Windows.Forms.CheckBox>, olarak adlandırılmış **checkBox1**. Bir süre sonra biraz kod yazacaksınız ve bu kod CheckBox'a ve PictureBox'a başvuracaktır. Olmadığı için bu denetimlerin her birinden yalnızca biri gördüğünüzde ne anlama geldiğini bilirsiniz **pictureBox1** veya **checkBox1** kodunuzda.

> [!NOTE]
> Adları Visual Basic'te, herhangi bir denetim adının varsayılan ilk harfi ilk harf olduğundan **PictureBox1**, **CheckBox1**ve benzeri.

 Formunuzda dört düğme vardır ve IDE bunları adlı **button1**, **button2**, **button3**, ve **button4**. Yalnızca geçerli adlarına bakarak hangi düğmesi olduğunu bilemezsiniz **Kapat** düğmesi ve hangisinin **resim Göster** düğmesi. İşte bu nedenle düğme denetimlerinize daha açıklayıcı adlar vermek yararlıdır.

 ![video bağlantısı](../data-tools/media/playvideo.gif)bu konunun video sürümü için bkz: [öğretici 1: Visual Basic'te - Video 3 resim görüntüleyici oluşturma](http://go.microsoft.com/fwlink/?LinkId=205213) veya [öğretici 1: İçinde resim görüntüleyici oluşturma C# -Video 3](http://go.microsoft.com/fwlink/?LinkId=205202). Bazı menü komutlarında ve diğer kullanıcı arabirimi öğelerinde küçük farklılıklar olduğundan bu videolarda Visual Studio'nun önceki bir sürümü kullanın. Ancak, kavramlar ve yordamlar benzer şekilde Visual Studio'nun geçerli sürümünde çalışır.

## <a name="to-name-your-button-controls"></a>Düğme denetimlerinizi adlandırmak için

1. Form üzerinde seçin **Kapat** düğmesi. (Tüm düğmeler seçiliyse hala varsa, seçin **Esc** seçimini iptal etmek için tuşa.) Kaydırın **özellikleri** penceresini görene kadar **(ad)** özelliği. ( **(Ad)** özelliği, Özellikler alfabetik olduğunda en olan.) Adla değiştirin **closeButton**, aşağıdaki resimde gösterildiği gibi.

     ![CloseButton adıyla Özellikler penceresi](../ide/media/express_setnameproperty.png)
**özellikleri** penceresiyle **closeButton** adı

    > [!NOTE]
    > İçin düğmenizin adını değiştirmeyi denerseniz **closeButton**, Kapat ve düğme sözcükleri arasına bir boşluk koyun, IDE bir hata iletisi görüntüler: "Özellik değeri geçerli değil." Denetim adlarında boşluklara (ve diğer birkaç karaktere) izin verilmez.

2. Diğer üç düğmeyi yeniden adlandır **Arkaplandüğmesi**, **Temizledüğmesi**, ve **showButton**. Denetim Seçici açılan listesini seçerek adları doğrulayabilirsiniz **özellikleri** penceresi. Yeni düğme adları görüntülenir.

3. Çift **resim Göster** formundaki düğmesi. Alternatif, **resim Göster** formda düğmesine ve ardından **Enter** anahtarı. Bunu yaptığınızda, IDE adlı ana penceresinde bir ek sekme açar **Form1.cs** (**Form1.vb** Visual Basic kullanılıyorsa). Bu sekme aşağıdaki resimde gösterildiği gibi formun arkasındaki kod dosyasını gösterir.

     ![Visual C Form1.cs sekmesi&#35; kod](../ide/media/express_showbuttoncode.png)
**Form1.cs** Visual ile sekmesindeki C# kod

4. Bu kod parçası üzerinde odaklanın. (Seçin **VB** aşağıda Visual Basic kullanıyorsanız kod Visual Basic sürümünü görüntülemek için sekmesinde.)

     [!code-vb[VbExpressTutorial1Step6#1](../ide/codesnippet/VisualBasic/step-6-name-your-button-controls_1.vb)]
     [!code-csharp[VbExpressTutorial1Step6#1](../ide/codesnippet/CSharp/step-6-name-your-button-controls_1.cs)]

     Kodun adı aradığınız `showButton_Click()`. İçin kod dosyasını açtığınızda IDE bunu formun koduna eklemiştir **showButton** düğmesi. Bir formda bir denetim için kod dosyasını açtığınızda, tasarım zamanında, zaten mevcut değilse denetim için kod oluşturulur. Olarak da bilinen bu kod, bir *yöntemi*, programınızı çalıştırıp denetimi - bu durumda, seçin çalışır **resim Göster** düğmesi.

    > [!NOTE]
    > Bu öğreticide, otomatik olarak oluşturulan Visual Basic kodu parantez arasındaki her şey kaldırılarak basitleştirilmiştir `()`. Bu her gerçekleştiğinde, aynı kodu kaldırabilirsiniz. Programınız her iki şekilde çalışır. Öğreticiler kalanı için otomatik olarak oluşturulan herhangi bir kod mümkün olduğunda basitleştirilecektir.

5. Seçin **Windows Form Tasarımcısı** sekmesine (**Form1.cs [Design]** görselde C#, **Form1.vb [Design]** Visual Basic'te) ve ardından içinkoddosyasınıaçın **Resmi Temizle** formun koduna bunun için bir yöntem oluşturmak için düğme. Bu, kalan iki düğme için yineleyin. Her defasında IDE formun kod dosyasına yeni bir yöntem ekler.

6. Birden fazla yöntem eklemek için kod dosyasını açın. **onay kutusu** denetim **Windows Form Tasarımcısı** IDE ekleme yapmak için bir `checkBox1_CheckedChanged()` yöntemi. Bu yöntem, her kullanıcı seçer veya temizler onay kutusunu çağrılır.

    > [!NOTE]
    > Bir programda çalışırken, Kod Düzenleyicisi arasında genellikle taşıyın ve **Windows Form Tasarımcısı**. IDE, projenizde gezinmeyi kolaylaştırır. Kullanım **Çözüm Gezgini** açmak için **Windows Form Tasarımcısı** çift tıklayarak *Form1.cs* görselde C# veya *Form1.vb* içinde Visual Basic veya menü çubuğunda, **görünümü** > **Tasarımcısı**.

     Aşağıdaki yeni kod, Kod düzenleyicisinde gördüğünüz gösterir.

     [!code-vb[VbExpressTutorial1Step6#2](../ide/codesnippet/VisualBasic/step-6-name-your-button-controls_2.vb)]
     [!code-csharp[VbExpressTutorial1Step6#2](../ide/codesnippet/CSharp/step-6-name-your-button-controls_2.cs)]

     Eklediğiniz beş yönteme adlı *olay işleyicileri*, (örneğin, bir kullanıcı bir düğmeyi veya bir kutuyu seçmesi) bir olay gerçekleştiğinde programınız onları çağırır.

     Tasarım zamanında IDE'de bir denetimin kodunu görüntülediğinizde, yoksak Visual Studio denetim için olay işleyicisi yöntemi ekler. Örneğin, bir düğmeye çift tıkladığınızda IDE için bir olay işleyicisi ekler, <xref:System.Windows.Forms.Control.Click> (kullanıcı bir düğme seçtiği) olay. Bir onay kutusunu çift tıkladığınızda IDE için bir olay işleyicisi ekler, <xref:System.Windows.Forms.CheckBox.CheckedChanged> (kullanıcı seçerse ya da kutuyu her olarak adlandırılır) olayı.

     Bir denetim için bir olay işleyici ekledikten sonra ona herhangi bir zamanda döndürebilir **Windows Form Tasarımcısı** denetimi çift tıklayarak veya menü çubuğundan seçme **görünümü**  >  **Kod**.

     Programları derleme ve yöntemler (olay işleyicileri dahil), istediğiniz herhangi bir ad olabilir adları önemlidir. IDE ile bir olay işleyicisi eklediğinizde, denetimin adını ve işlenen olayı temel alan bir ad oluşturur. Örneğin, adlı bir düğme için tıklama olayı **showButton** çağrılır `showButton_Click()` olay işleyicisi yöntemi. Ayrıca, açılış ve kapanış ayraçlarını `()` genellikle yöntemleri ele belirtmek üzere yöntem adından sonra eklenir. İstediğiniz bir kod değişkeni adını değiştirmeye karar verirseniz, kod içindeki değişkene sağ tıklayın ve ardından **yeniden düzenleme** > **Yeniden Adlandır**. Koddaki bu değişkenin tüm örnekleri yeniden adlandırılır. Bkz: [yeniden düzenlemeyi yeniden adlandırma](../ide/reference/rename.md) daha fazla bilgi için.

## <a name="to-continue-or-review"></a>Devam etmek veya gözden geçirmek için

- Sonraki öğretici adımına gitmek için bkz: [adım 7: Formunuza iletişim kutusu bileşenleri ekleme](../ide/step-7-add-dialog-components-to-your-form.md).

- Önceki öğretici adımına dönmek için bkz: [5. adım: Formunuza denetimler ekleme](../ide/step-5-add-controls-to-your-form.md).
