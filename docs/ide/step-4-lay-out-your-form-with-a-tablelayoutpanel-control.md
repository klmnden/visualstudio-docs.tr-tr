---
title: '4. Adım: TableLayoutPanel denetimi ile formunuzu düzenleme'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: conceptual
ms.assetid: 61acde79-e115-4bad-bb06-1fbe37717a3e
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 529665d342275611ab13253229fb8a2abde035fe
ms.sourcegitcommit: 01334abf36d7e0774329050d34b3a819979c95a2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/07/2019
ms.locfileid: "55853870"
---
# <a name="step-4-lay-out-your-form-with-a-tablelayoutpanel-control"></a>4. Adım: TableLayoutPanel denetimi ile formunuzu düzenleme
Bu adımda eklediğiniz bir <xref:System.Windows.Forms.TableLayoutPanel> form denetimi. TableLayoutPanel, özel olarak daha sonra ekleyeceksiniz formda denetimleri düzgün şekilde hizalamaya yardımcı olur.

 ![video bağlantısı](../data-tools/media/playvideo.gif)bu konunun video sürümü için bkz: [öğretici 1: Visual Basic'te - Video 2 resim görüntüleyici oluşturma](http://go.microsoft.com/fwlink/?LinkId=205211) veya [öğretici 1: İçinde resim görüntüleyici oluşturma C# -Video 2](http://go.microsoft.com/fwlink/?LinkId=205200). Bazı menü komutlarında ve diğer kullanıcı arabirimi öğelerinde küçük farklılıklar olduğundan bu videolarda Visual Studio'nun önceki bir sürümü kullanın. Ancak, kavramlar ve yordamlar benzer şekilde Visual Studio'nun geçerli sürümünde çalışır.

## <a name="to-lay-out-your-form-with-a-tablelayoutpanel-control"></a>Formunuzu bir TableLayoutPanel denetimiyle düzenlemek için

1.  Visual Studio IDE'nin sol tarafında bulun **araç kutusu** sekmesi. Seçin **araç kutusu** sekmesinde ve **araç kutusu** görünür. (Veya menü çubuğunda, **görünümü** > **araç kutusu**.)

2.  Yanındaki küçük üçgen sembolünü seçin **kapsayıcıları** grubu, aşağıdaki resimde gösterildiği gibi açın.

     ![Kapsayıcılar grubu](../ide/media/express_toolbox.png)
**kapsayıcıları** grubu

3.  Formunuza düğmeler, onay kutuları ve etiketler gibi denetimler ekleyebilirsiniz. TableLayoutPanel denetiminde çift **araç kutusu**. (Ya da denetimi araç kutusundan forma sürükleyebilirsiniz.) Bunu yaptığınızda aşağıdaki resimde gösterildiği gibi IDE TableLayoutPanel denetimi form ekler.

     ![TableLayoutPanel denetimi](../ide/media/express_formtablelayout.png)
**TableLayoutPanel** denetimi

    > [!NOTE]
    >  Formunuza başlığıyla içinde bir pencere görünürse, TableLayoutPanel ekledikten sonra **TableLayoutPanel görevleri**, herhangi bir yeri kapatmak için form içinde seçin. Bu pencere hakkında daha fazla öğreticinin ilerleyen bölümlerinde öğreneceksiniz.

     Bildirim nasıl **araç kutusu** sekmesini seçtiğinizde formunuzun kapsayacak şekilde genişler ve bunun dışında herhangi bir yeri seçtikten sonra kapatır. Bu IDE otomatik gizleme özelliğidir. Açıp pencereler için geçiş otomatik gizleme ve kilitleme penceresinin üst sağ üst köşedeki Raptiye simgesini seçerek açabilirsiniz. Raptiye simgesi aşağıdaki gibi görünür.

     ![Raptiye simgesi](../ide/media/express_pushpintoolbox.png)
**Raptiye** simgesi

4.  TableLayoutPanel seçili emin olun. Açılan listenin en üstündeki bakarak hangi denetimin seçili olduğunu doğrulayabilirsiniz **özellikleri** penceresinde, aşağıdaki resimde gösterildiği gibi.

     ![TableLayoutPanel denetimini gösteren Özellikler penceresi](../ide/media/express_controlspropwin.png)
**özellikleri** gösteren penceresi **TableLayoutPanel** denetimi

5.  Seçin **alfabetik** araç çubuğunda düğme **özellikleri** penceresi. Bu özellikler listesinden neden **özellikleri** penceresi, bu öğreticide özellikleri bulmak daha kolay bulabilmesini sağlar alfabetik sırada görüntüleyin.

6.  Aşağı açılan listesidir üst kısmındaki denetim seçiciyi **özellikleri** penceresi. Bu örnekte, bir denetim adlı gösterir `tableLayoutPanel1` seçilir. Ya da bir alanda göre seçerek denetimleri seçebilirsiniz **Windows Form Tasarımcısı** veya denetim seçiciden seçerek. TableLayoutPanel seçili, bulma **Dock** özelliği ve **Dock**, ayarlanması **hiçbiri**. Bir açılan liste okunu değerin yanında görüntülendiğine dikkat edin. Oku seçin ve ardından **dolgu** düğmesini (ortadaki büyük düğme), aşağıdaki resimde gösterildiği gibi.

     ![Doldur seçili Özellikler penceresi](../ide/media/express_docktable.png)
**özellikleri** penceresiyle **dolgu** seçili

     *Yerleştirme* Visual Studio'da pencere başka bir pencereye veya alana IDE'de bağlı olduğu başvuruyor. Örneğin, **özellikleri** penceresi - yani eklenmemiş ve Visual Studio - yerleştirilmemiş veya takılmamış karşı yerleştirilmiş **Çözüm Gezgini**.

7.  TableLayoutPanel ayarladıktan sonra **Dock** özelliğini **dolgu**, panel formun tamamını kaplar. Formu yeniden boyutlandırırsanız, TableLayoutPanel takılı kalır ve kendisini sığacak şekilde yeniden boyutlandırır.

    > [!NOTE]
    >  TableLayoutPanel, Microsoft Office Word'ün bir tablo gibi çalışır: Satırları ve sütunları vardır ve tek bir hücre birçok satırı ve sütunu kapsayabilir. Her hücre bir denetimi kontrol eder (düğme, onay kutusu veya etiket) barındırabilir. TableLayoutPanel denetiminiz olur bir <xref:System.Windows.Forms.PictureBox> denetimi üst satırı, kapsayan bir <xref:System.Windows.Forms.CheckBox> denetimi, sol alttaki hücreye ve dört <xref:System.Windows.Forms.Button> kendi sağ alt hücresinde denetimleri.

8.  Şu anda TableLayoutPanel, iki eşit boyutta satıra ve iki eşit boyutta sütuna sahiptir. Size en üst satır ve sağ sütun için bunları yeniden boyutlandırın gerekiyor. İçinde **Windows Form Tasarımcısı**, Tablelayoutpanel'i seçin. Sağ üst köşedeki gibi görünen bir küçük siyah üçgen düğme yoktur.

     ![Üçgen düğme](../ide/media/express_iconblacktriangle.gif)
**üçgen** düğmesi

     Bu düğme denetimi yardımcı olan görevleri olduğunu gösterir özelliklerini otomatik olarak ayarlayın.

9. Aşağıdaki resimde gösterildiği gibi denetim görev listesinde görüntülemek üzere üçgeni seçin.

     ![TableLayoutPanel görevleri](../ide/media/express_tablepanel.png)
**TableLayoutPanel** görevleri

10. Seçin **satırları ve sütunları Düzenle** görüntülenecek olan görevi **sütun ve satır stilleri** penceresi. Seçin **Column1**, emin olma yüzde 15 boyutunu ayarlayın **yüzde** düğmesi seçili olduğunu ve **15** içinde **yüzde** kutusu. (Bu bir <xref:System.Windows.Forms.NumericUpDown> denetimi, bir sonraki öğreticide kullanacaksınız.) Seçin **Sütun2** ve yüzde 85 olarak ayarlayın. Seçmeyin **Tamam** pencere kapanacağından düğmesini henüz. (Ancak bunu yaparsanız, görev listesini kullanarak yeniden açabilirsiniz.)

     ![TableLayoutPanel sütun ve satır stilleri](../ide/media/vs_tablelayoutpanel_setup.png)
**TableLayoutPanel** sütun ve satır stilleri

11. Gelen **Göster** açılan pencerenin en üstünde **satırları**. Ayarlama **Satır1** yüzde 90 ve **satır2** yüzde 10.

12. Seçin **Tamam** düğmesi. Tablelayoutpanel'inizin şimdi büyük bir üst satırı, küçük bir alt satırı, küçük bir sol sütunu ve büyük bir sağ sütunu olması gerekir. Satırları ve sütunları TableLayoutPanel içindeki seçerek boyutlandırabilirsiniz **tableLayoutPanel1** form ve sonra bunun satır ve sütun kenarlıklarını sürükleyerek.

     ![Yeniden boyutlandırılan TableLayoutPanel ile Form1](../ide/media/vs_formafterlayoutpanel.png)
**Form1** ile yeniden boyutlandırılmış **TableLayoutPanel**

## <a name="to-continue-or-review"></a>Devam etmek veya gözden geçirmek için

-   Sonraki öğretici adımına gitmek için bkz: [5. adım: Formunuza denetimler ekleme](../ide/step-5-add-controls-to-your-form.md).

-   Önceki öğretici adımına dönmek için bkz: [3. adım: Form özelliklerinizi ayarlama](../ide/step-3-set-your-form-properties.md).
