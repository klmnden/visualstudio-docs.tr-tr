---
title: '5\. Adım: Formunuza denetimler ekleme'
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: dc2746f4-0b5c-4674-9ef7-f40f94150f52
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: e69c75b00ddb98148e9985820e577031ead0a275
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68918806"
---
# <a name="step-5-add-controls-to-your-form"></a>5\. Adım: Formunuza denetimler ekleme
Bu adımda, formunuza <xref:System.Windows.Forms.PictureBox> denetim <xref:System.Windows.Forms.CheckBox> ve denetim gibi denetimler eklersiniz. Ardından formunuza denetimler <xref:System.Windows.Forms.Button> eklersiniz.

![video](../data-tools/media/playvideo.gif)bağlantısı bu konunun video sürümü için bkz [. öğretici 1: Visual Basic-video 2](http://go.microsoft.com/fwlink/?LinkId=205211) veya [öğretici 1 ' de bir resim Görüntüleyicisi oluşturun: Video 2 C# ](http://go.microsoft.com/fwlink/?LinkId=205200)' de bir resim görüntüleyici oluşturun. Bu videolar, Visual Studio 'nun önceki bir sürümünü kullanır, bu nedenle bazı menü komutlarında ve diğer kullanıcı arabirimi öğelerinde küçük farklılıklar vardır. Ancak, kavramlar ve yordamlar Visual Studio 'nun geçerli sürümünde benzer şekilde çalışır.

## <a name="to-add-controls-to-your-form"></a>Formunuza denetim eklemek için

1. **Araç kutusu** sekmesine gidin (VISUAL Studio IDE 'nin sol tarafında bulunur) ve **ortak denetimler** grubunu genişletin. Bu, formlarda gördüğünüz en yaygın denetimleri gösterir.

2. Formda **TableLayoutPanel** denetimini seçin. TableLayoutPanel 'in seçili olduğunu doğrulamak için, adının **Özellikler** penceresinin en üstündeki açılan liste kutusunda göründüğünden emin olun. **Özellikler** penceresinin üst kısmındaki açılan liste kutusunu kullanarak da form denetimleri seçebilirsiniz. Bu şekilde bir denetim seçilmesi, fare ile küçük bir denetim seçmekten daha kolay olabilir.

3. Formunuza PictureBox denetimi eklemek için **PictureBox** öğesine çift tıklayın. TableLayoutPanel formunuzu dolduracak şekilde yerleştirilmiş olduğundan, IDE, PictureBox denetimini ilk boş hücreye (sol üst köşe) ekler.

4. Yeni PictureBox denetimini seçin ve ardından yeni PictureBox denetimindeki siyah üçgeni seçerek aşağıdaki resimde gösterildiği gibi görev listesini görüntüleyin.

     ![PictureBox görevleri](../ide/media/express_pictureboxtasks.png)<br/>***PictureBox*** *Görevler*

    > [!NOTE]
    > Yanlışlıkla TableLayoutPanel içinde yanlış denetim türü eklerseniz, bunu silebilirsiniz. Denetime sağ tıklayın ve sonra bağlam menüsünde **Sil** ' i seçin. Ayrıca, menü çubuğunu kullanarak formdan denetimleri kaldırabilirsiniz. Menü çubuğunda,**geri al** **Düzenle** > ' yi seçin veya**Sil**' i **düzenleyin** > .

5. **Ana kapsayıcı Içinde yerleştirmeyi** seçin bağlantısı. Bu, PictureBox **Dock** özelliğini **Fill**olarak ayarlar. Bunu görmek için **PictureBox** denetimini seçip seçin, **Özellikler** penceresine gidin ve **Dock** özelliğinin **Fill**olarak ayarlandığından emin olun.

6. Yalnızca **ColumnSpan** özelliğini değiştirerek PictureBox 'ı her iki sütuna da yayın. **PictureBox** denetimini seçin ve **ColumnSpan** özelliğini **2**olarak ayarlayın. Ayrıca, PictureBox boş olduğunda boş bir çerçeve göstermek istersiniz. **BorderStyle** özelliğini **Fixed3D**olarak ayarlayın.

    > [!NOTE]
    > PictureBox 'niz için bir **ColumnSpan** özelliği görmüyorsanız, PictureBox 'ın TableLayoutPanel yerine forma eklenmesi olasıdır. Bu hatayı onarmak için, **PictureBox**'ı seçin, silin, **TableLayoutPanel**öğesini seçin ve ardından yeni bir PictureBox ekleyin.

7. Formda **TableLayoutPanel** öğesini seçin ve ardından forma onay kutusu denetimi ekleyin. Tablodaki bir sonraki boş hücreye yeni bir CheckBox denetimi eklemek için **araç kutusu** ' nda **onay** kutusu öğesine çift tıklayın. PictureBox, TableLayoutPanel içindeki ilk iki hücreyi kullandığından, CheckBox denetimi sol alt hücreye eklenir. **Metin** özelliğini seçin ve aşağıdaki resimde gösterildiği gibi,sözcük uzatılmasına yazın.

     ![Esnetme özelliği ile TextBox denetimi](../ide/media/express_pictureviewercheckbox.png)<br/>***Metin kutusu*** *ile denetim* ***Uzat*** *özelliği*

8. Formda **TableLayoutPanel** öğesini seçin ve ardından **araç kutusunda** **kapsayıcılar** grubuna gidin (TableLayoutPanel denetiminizi aldığınız yerdir) ve **FlowLayoutPanel** öğesine çift tıklayarak, yeni bir denetim eklemek için PictureBox (sağ alt). Ardından, FlowLayoutPanel 'i TableLayoutPanel 'e yerleştirin (FlowLayoutPanel 'in siyah üçgen görev listesinde **Ana kapsayıcıda yerleştir** ' i seçerek ya da FlowLayoutPanel 'in **Dock** özelliğini **Fill**olarak ayarlayarak).

    > [!NOTE]
    > <xref:System.Windows.Forms.FlowLayoutPanel> , Düzenlidir satırlarındaki diğer denetimleri sırasıyla bir kapsayıcı olarak düzenler. Bir FlowLayoutPanel 'i yeniden boyutlandırdığınızda, tüm denetimlerini tek bir satırda düzenlemek için yer varsa, bunu yapar. Aksi takdirde, bunları diğer satırlarda, biri diğerinin üstüne yerleştirir. Dört düğme tutmak için bir FlowLayoutPanel kullanacaksınız. Ekler eklendiğinde, bir tane üzerine bir tane düzenlensin, düğmeleri eklemeden önce FlowLayoutPanel 'in seçildiğinden emin olun. Daha önce her hücrenin yalnızca bir denetim tutabilmesine rağmen, TableLayoutPanel 'in sağ alt hücresinde dört düğme denetimi vardır. Bunun nedeni, diğer denetimleri tutan bir hücreye bir denetim koyabilmeniz. Bu tür bir denetime kapsayıcı denir ve FlowLayoutPanel bir kapsayıcıdır.

## <a name="to-add-buttons"></a>Düğme eklemek için

1. Eklediğiniz yeni FlowLayoutPanel 'i seçin. **Araç kutusundaki** **ortak denetimlere** gidin ve FlowLayoutPanel 'e **button1** adlı bir düğme denetimi eklemek için **düğme** öğesine çift tıklayın. Başka bir düğme eklemek için tekrarlayın. IDE zaten **button1** adlı bir düğme olduğunu belirler ve bir sonraki bir sonrakini çağırır.

2. Genellikle, **araç kutusunu**kullanarak diğer düğmeleri eklersiniz. Bu kez, **button2**' ı seçin ve ardından menü çubuğunda**kopyayı** **Düzenle** > ' yi seçin (veya **CTRL**+**C**tuşlarına basın). Düğme kopyasını yapıştırmak için menü çubuğunda,**yapıştırmayı** **Düzenle** > ' yi (veya **CTRL**+**V**tuşlarına basın) seçin. Şimdi yapıştırın. IDE artık FlowLayoutPanel 'e **Button3** ve **Button4** eklendi.

    > [!NOTE]
    > Herhangi bir denetimi kopyalayabilir ve yapıştırabilirsiniz. IDE adları ve yeni denetimleri mantıksal bir şekilde koyar. Bir kapsayıcıya bir denetim yapıştırırsanız, IDE yerleştirme için bir sonraki mantıksal alanı seçer.

3. İlk düğmeyi seçin ve **Text** özelliğini **bir resim gösterecek**şekilde ayarlayın. Sonra, **resmi temizlemek**, **arka plan rengini ayarlamak**ve **kapatmak**için sonraki üç düğmenin **Text** özelliklerini ayarlayın.

4. Sonraki adım düğmeleri boyutlandırmanız ve panelin sağ tarafına hizalanacak şekilde düzenlenmeleri. **FlowLayoutPanel** ' i seçin ve **FlowDirection** özelliğine bakın. Bunu, **RightToLeft**olarak ayarlanmış olacak şekilde değiştirin. Her ne kadar, düğmeler kendilerini hücrenin sağına doğru hizalamalıdır ve **bir resim göster** düğmesi sağ tarafta olacak şekilde sıralarını tersine çevirir.

    > [!NOTE]
    > Düğmeler hala yanlış sıralamayla varsa, bunları herhangi bir sırada yeniden düzenlemek için FlowLayoutPanel etrafında düğmeleri sürükleyebilirsiniz. Bir düğme seçip sola veya sağa sürükleyebilirsiniz.

5. Kapatmak için **Kapat** düğmesini seçin. **CTRL** tuşunu basılı tutun ve diğer üç düğmeyi seçerek tümünün seçili olmaları gerekir. Tüm düğmeler seçili olsa da, **Özellikler** penceresine gidin ve **AutoSize** özelliğine kaydırın. Bu özellik, düğmesine metnin tümüne sığacak şekilde otomatik olarak yeniden boyutlandırılacağını söyler. Bunu **true**olarak ayarlayın. Düğmeleriniz artık doğru şekilde boyutlandırılıp doğru sırada olmalıdır. (Dört düğme seçildiği sürece, tüm dört **AutoSize** özelliklerini de aynı anda değiştirebilirsiniz.) Aşağıdaki resimde dört düğme gösterilmektedir.

     ![Dört düğme içeren resim görüntüleyici](../ide/media/express_autosize.png)<br/>***Resim görüntüleyici*** *dört düğme ile*

6. Şimdi yeni düzenlendiği formu görmek için programınızı yeniden çalıştırın. Düğmeleri seçip onay kutusu henüz bir şey yapmaz, ancak yakında çalışacaktır.

## <a name="to-continue-or-review"></a>Devam etmek veya gözden geçirmek için

- Sonraki öğretici adımına gitmek için bkz [. 6. Adım: Düğme denetimlerinizi](../ide/step-6-name-your-button-controls.md)adlandırın.

- Önceki öğretici adımına dönmek için bkz [. 4. Adım: Bir TableLayoutPanel denetimiyle](../ide/step-4-lay-out-your-form-with-a-tablelayoutpanel-control.md)formunuzu düzenleyin.
