---
title: '5\. Adım: Formunuza denetimler ekleme'
ms.date: 08/30/2019
ms.assetid: dc2746f4-0b5c-4674-9ef7-f40f94150f52
ms.topic: tutorial
ms.prod: visual-studio-windows
ms.technology: vs-ide-general
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: b88af1a0ac1ec51f57d3aa339c2c2ec4adb45134
ms.sourcegitcommit: 6eed0372976c0167b9a6d42ba443f9a474b8bb91
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/19/2019
ms.locfileid: "71119004"
---
# <a name="step-5-add-controls-to-your-form"></a>5\. Adım: Formunuza denetimler ekleme

Bu adımda, formunuza <xref:System.Windows.Forms.PictureBox> denetim <xref:System.Windows.Forms.CheckBox> ve denetim gibi denetimler eklersiniz. Ardından formunuza denetimler <xref:System.Windows.Forms.Button> eklersiniz.

## <a name="how-to-add-controls-to-your-form"></a>Formunuza denetimler ekleme

1. Visual Studio IDE 'nin sol tarafındaki **araç kutusu** sekmesini seçin (veya **CTRL**+**alt**+**X**tuşlarına basın) ve ardından **ortak denetimler** grubunu genişletin. Bu, formlarda gördüğünüz en yaygın denetimleri gösterir.

1. Formunuza PictureBox denetimi eklemek için **PictureBox** öğesine çift tıklayın. TableLayoutPanel formunuzu dolduracak şekilde yerleştirilmiş olduğundan, IDE, PictureBox denetimini ilk boş hücreye (sol üst köşe) ekler.

1. Yeni PictureBox denetimini seçin ve ardından yeni **PictureBox denetimindeki siyah** üçgeni seçerek aşağıdaki ekran görüntüsünde gösterildiği gibi görev listesini görüntüleyin.

    ![PictureBox görevleri](../ide/media/express_pictureboxtasks.png)<br/>PictureBox * * * *Görevler**

    > [!NOTE]
    > Yanlışlıkla TableLayoutPanel içinde yanlış denetim türü eklerseniz, bunu silebilirsiniz. Denetime sağ tıklayın ve sonra bağlam menüsünde **Sil** ' i seçin. Ayrıca, menü çubuğunu kullanarak formdan denetimleri kaldırabilirsiniz. Menü çubuğunda,**geri al** **Düzenle** > ' yi seçin veya**Sil**' i **düzenleyin** > .

1. **PictureBox** denetimindeki **PictureBox görevleri** menüsünde, **ana kapsayıcı içinde yerleştir** bağlantısını seçin. Bu, PictureBox **Dock** özelliğini **Fill**olarak ayarlar. Bunu görmek için **PictureBox** denetimini seçip seçin, **Özellikler** penceresine gidin ve **Dock** özelliğinin **Fill**olarak ayarlandığından emin olun.

1. Yalnızca **ColumnSpan** özelliğini değiştirerek PictureBox 'ı her iki sütuna da yayın. **PictureBox**'da **PictureBox** denetimini seçin ve **ColumnSpan** özelliğini **2**olarak ayarlayın. Ayrıca, PictureBox boş olduğunda boş bir çerçeve göstermek istersiniz. **BorderStyle** özelliğini **Fixed3D**olarak ayarlayın.

    > [!NOTE]
    > PictureBox 'niz için bir **ColumnSpan** özelliği görmüyorsanız, PictureBox 'ın TableLayoutPanel yerine forma eklenmesi olasıdır. Bu hatayı onarmak için, **PictureBox**'ı seçin, silin, **TableLayoutPanel**öğesini seçin ve ardından yeni bir PictureBox ekleyin.

1. Formda **TableLayoutPanel** öğesini seçin ve ardından forma onay kutusu denetimi ekleyin. Tablodaki bir sonraki boş hücreye yeni bir CheckBox denetimi eklemek için **araç kutusu** ' nda **onay** kutusu öğesine çift tıklayın. PictureBox, TableLayoutPanel içindeki ilk iki hücreyi kullandığından, CheckBox denetimi sol alt hücreye eklenir. Aşağıdaki görüntüde gösterildiği gibi **metin** özelliğini seçin ve sözcük **uzatılmasına**yazın.

    ![Esnetme özelliği ile TextBox denetimi](../ide/media/express_pictureviewercheckbox.png)<br/>***Metin kutusu*** *ile denetim* ***Uzat*** *özelliği*

1. Formda **TableLayoutPanel** öğesini seçin ve ardından **araç kutusunda** **kapsayıcılar** grubuna gidin (TableLayoutPanel denetiminizi aldığınız yerdir) ve **FlowLayoutPanel** öğesine çift tıklayarak son hücreye yeni bir denetim ekleyin (alt sağ). Ardından, TableLayoutPanel içindeki FlowLayoutPanel 'i yerleştirin. Bunu, FlowLayoutPanel 'in siyah üçgen görev listesinde **Ana kapsayıcıda yerleştir** ' i seçerek ya da FlowLayoutPanel **Dock** özelliğini **Fill**olarak ayarlayarak yapabilirsiniz.

    > [!NOTE]
    > <xref:System.Windows.Forms.FlowLayoutPanel> , Bir satırdaki diğer denetimleri izleyen bir kapsayıcıdır. Bir FlowLayoutPanel 'i yeniden boyutlandırdığınızda, tüm denetimlerini tek bir satırda yerleştirir. Aksi takdirde, bunları diğer satırlarda, biri diğerinin üstüne yerleştirir. <br/><br/>Burada dört düğme tutacak bir FlowLayoutPanel kullanacaksınız. Düğmeleri eklediğinizde düğmeler bir üst üste düzenlensin, düğmeleri eklemeden önce FlowLayoutPanel 'i seçtiğinizden emin olun. <br/><br/>(Genellikle, her hücrede yalnızca bir denetim bulunur. Bu örnekte, TableLayoutPanel 'in sağ alt hücresi dört düğme denetimi içerir. Neden?  FlowLayoutPanel, diğer denetimleri tutan bir hücrede bir denetim olan bir kapsayıcı denetimi olduğundan.)

## <a name="to-add-buttons"></a>Düğme eklemek için

1. Eklediğiniz yeni FlowLayoutPanel 'i seçin. **Araç kutusundaki** **ortak denetimlere** gidin ve FlowLayoutPanel 'e **button1** adlı bir düğme denetimi eklemek için **düğme** öğesine çift tıklayın. Başka bir düğme eklemek için tekrarlayın. IDE zaten **button1** **adlı bir düğme**olduğunu belirler ve bir sonraki bir sonrakini çağırır.

1. Genellikle, **araç kutusunu**kullanarak diğer düğmeleri eklersiniz. Bu kez, **button2**' ı seçin ve ardından menü çubuğundan**kopyayı** **Düzenle** > ' yi seçin (veya **CTRL**+**C**tuşlarına basın). Sonra, düğme kopyasını yapıştırmak için menü çubuğundan**yapıştırmayı** **Düzenle** > ' yi (veya **CTRL**+**V**tuşlarına basın) seçin. Şimdi yapıştırın. IDE 'nin FlowLayoutPanel 'e **Button3** ve **Button4** eklediğine dikkat edin.

    > [!NOTE]
    > Herhangi bir denetimi kopyalayabilir ve yapıştırabilirsiniz. IDE adları ve yeni denetimleri mantıksal bir şekilde koyar. Bir kapsayıcıya bir denetim yapıştırırsanız, IDE yerleştirme için bir sonraki mantıksal alanı seçer.

1. İlk düğmeyi seçin ve **Text** özelliğini **bir resim gösterecek**şekilde ayarlayın. Sonra, **resmi temizlemek**, **arka plan rengini ayarlamak**ve **kapatmak**için sonraki üç düğmenin **Text** özelliklerini ayarlayın.

1. Düğmeleri boyutlandıralım ve panelin sağ tarafına hizalanacak şekilde düzenlemenizi sağlar. **FlowLayoutPanel** ' i seçin ve **FlowDirection** özelliğine bakın. Bunu, **RightToLeft**olarak ayarlanmış olacak şekilde değiştirin.

   Düğmeler, hücrenin sağ tarafına hizalanmalıdır ve **bir resim göster** düğmesi sağ tarafta olacak şekilde sıralarını tersine çevirir.

    > [!NOTE]
    > Düğmeler hala yanlış sıralamayla varsa, bunları herhangi bir sırada yeniden düzenlemek için FlowLayoutPanel etrafında düğmeleri sürükleyebilirsiniz. Bir düğme seçip sola veya sağa sürükleyebilirsiniz.

1. Kapatmak için **Kapat** düğmesini seçin. Daha sonra düğmeleri aynı anda seçmek için **CTRL** tuşuna basın ve basılı tutun ve bunları da seçin.

   Tüm düğmeleri seçtikten sonra **Özellikler** penceresine gidin ve **AutoSize** özelliğine kaydırın. Bu özellik, düğmesine metnin tümüne sığacak şekilde otomatik olarak yeniden boyutlandırılacağını söyler. Bunu **true**olarak ayarlayın.

   Düğmeleriniz artık doğru şekilde boyutlandırılıp doğru sırada olmalıdır. (Dört düğme seçildiği sürece, tüm dört **AutoSize** özelliklerini de aynı anda değiştirebilirsiniz.) Aşağıdaki görüntüde dört düğme gösterilmektedir.

    ![Dört düğme içeren resim görüntüleyici](../ide/media/express_autosize.png)<br/>***Resim görüntüleyici*** *dört düğme ile*

1. Şimdi yaptığınız değişiklikleri görmek için programınızı yeniden çalıştırın.

   Düğmelerin ve onay kutusunun hiçbir şey&mdash;yapmadığına, ancak yakında yapacağından emin olun.

## <a name="to-continue-or-review"></a>Devam etmek veya gözden geçirmek için

* Sonraki öğretici adımına gitmek için bkz  **[. 6. Adım: Düğme denetimlerinizi](../ide/step-6-name-your-button-controls.md)** adlandırın.

* Önceki öğretici adımına dönmek için bkz [. 4. Adım: Bir TableLayoutPanel denetimiyle](../ide/step-4-lay-out-your-form-with-a-tablelayoutpanel-control.md)formunuzu düzenleyin.

## <a name="see-also"></a>Ayrıca bkz.

* [Öğretici 2: Süreli matematik testi oluşturma](tutorial-2-create-a-timed-math-quiz.md)
* [Öğretici 3: Eşleşen bir oyun oluşturun](tutorial-3-create-a-matching-game.md)
