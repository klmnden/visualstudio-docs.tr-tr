---
title: '4\. Adım: TableLayoutPanel denetimi ile formunuzu düzenleme'
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 61acde79-e115-4bad-bb06-1fbe37717a3e
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 269fa26b89ab1ca9165efa8eb8971731f078ec60
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68925932"
---
# <a name="step-4-lay-out-your-form-with-a-tablelayoutpanel-control"></a>4\. Adım: TableLayoutPanel denetimi ile formunuzu düzenleme
Bu adımda formunuza bir <xref:System.Windows.Forms.TableLayoutPanel> denetim eklersiniz. TableLayoutPanel, daha sonra ekleyeceğiniz formdaki denetimleri düzgün şekilde hizalamaya yardımcı olur.

![video](../data-tools/media/playvideo.gif)bağlantısı bu konunun video sürümü için bkz [. öğretici 1: Visual Basic-video 2](http://go.microsoft.com/fwlink/?LinkId=205211) veya [öğretici 1 ' de bir resim Görüntüleyicisi oluşturun: Video 2 C# ](http://go.microsoft.com/fwlink/?LinkId=205200)' de bir resim görüntüleyici oluşturun. Bu videolar, Visual Studio 'nun önceki bir sürümünü kullanır, bu nedenle bazı menü komutlarında ve diğer kullanıcı arabirimi öğelerinde küçük farklılıklar vardır. Ancak, kavramlar ve yordamlar Visual Studio 'nun geçerli sürümünde benzer şekilde çalışır.

## <a name="to-lay-out-your-form-with-a-tablelayoutpanel-control"></a>Bir TableLayoutPanel denetimiyle formunuzu düzenlemek için

1. Visual Studio IDE 'nin sol tarafında **araç kutusu** sekmesini bulun. **Araç kutusu** sekmesini seçin ve **araç kutusu** görüntülenir. (Veya menü çubuğunda **Görünüm** > **araç kutusu**' nu seçin.)

2. Aşağıdaki resimde gösterildiği gibi, açmak için **kapsayıcılar** grubunun yanındaki küçük üçgen sembolünü seçin.

     ![Kapsayıcılar grubu](../ide/media/express_toolbox.png)
**kapsayıcılar** grubu

3. Formunuza düğmeler, onay kutuları ve Etiketler gibi denetimler ekleyebilirsiniz. **Araç kutusunda**TableLayoutPanel denetimine çift tıklayın. (Veya, denetimi araç kutusu ' ndan form üzerine sürükleyebilirsiniz.) Bunu yaptığınızda, IDE aşağıdaki resimde gösterildiği gibi formunuza bir TableLayoutPanel denetimi ekler.

     ![TableLayoutPanel denetimi](../ide/media/express_formtablelayout.png)
**TableLayoutPanel** denetimi

    > [!NOTE]
    > TableLayoutPanel ' i ekledikten sonra, formunuzda **TableLayoutPanel görevleri**başlıklı bir pencere görünürse, kapatmak için formun içinde herhangi bir yeri seçin. Bu pencere hakkında daha sonra öğreticide daha fazla bilgi edineceksiniz.

     **Araç kutusu** , sekmesini seçerken formunuzu nasıl genişlettiğine ve bunun dışında herhangi bir yeri seçtikten sonra kapandığına dikkat edin. Bu, IDE otomatik gizleme özelliğidir. Pencerenin sağ üst köşesinde bulunan raptiye simgesini seçerek otomatik gizlemeyi açıp bir yere kilitlemek için bu simgeyi etkinleştirebilir veya devre dışı bırakabilirsiniz. Raptiye simgesi aşağıdaki gibi görünür.

     ![Raptiye simgesi](../ide/media/express_pushpintoolbox.png)
**raptiye** simgesi

4. Bu öğeyi seçerek TableLayoutPanel 'in seçili olduğundan emin olun. Aşağıdaki resimde gösterildiği gibi, **Özellikler** penceresinin en üstündeki açılan listeye bakarak hangi denetimin seçildiğini doğrulayabilirsiniz.

     ![TableLayoutPanel denetimini gösteren TableLayoutPanel](../ide/media/express_controlspropwin.png)
denetim**özellikleri** penceresini gösteren Özellikler penceresi

5. **Özellikler** penceresinde araç çubuğundan **alfabetik** düğmesini seçin. Bu, Özellikler penceresindeki özelliklerin listesinin alfabetik sırayla görüntülenmesine neden olur, bu da bu öğreticide özellikleri bulmayı kolaylaştırır.

6. Denetim Seçicisi, **Özellikler** penceresinin üst kısmındaki açılan bir listesidir. Bu örnekte, çağrılan `tableLayoutPanel1` bir denetimin seçili olduğunu gösterir. **Windows Form Tasarımcısı** bir alanı seçerek veya denetim seçicinden seçim yaparak denetimleri seçebilirsiniz. TableLayoutPanel seçili olduğuna göre **Dock** özelliğini bulun ve **yok**olarak ayarlanması gereken **Yerleştir**' i seçin. Değerin yanında bir açılan okun göründüğünü unutmayın. Oku seçin ve ardından aşağıdaki resimde gösterildiği gibi **doldur** düğmesini (ortadaki büyük düğme) seçin.

     ![Seçili](../ide/media/express_docktable.png)
olan**Özellikler** penceresi **Fill** seçiliyken Özellikler penceresi

     Visual Studio 'ya *yerleştirme* , BIR pencerenin IDE 'deki başka bir pencere veya alana Eklenme anlamına gelir. Örneğin, **Özellikler** penceresi yerleştirilmemiş olabilir. Bu, Visual Studio içinde iliştirilmemiş ve serbest bir şekilde taşınabilir veya **Çözüm Gezgini**göre sabitlenebilir.

7. TableLayoutPanel **Dock** özelliğini **Fill**olarak ayarladıktan sonra, panel formun tamamını doldurur. Formu yeniden boyutlandırırsanız, TableLayoutPanel sabitlenmiş kalır ve kendisini sığacak şekilde yeniden boyutlandırır.

    > [!NOTE]
    > TableLayoutPanel Microsoft Office Word 'de bir tablo gibi çalışmaktadır: Satırlar ve sütunlar içerir ve tek bir hücre birden fazla satıra ve sütuna yayılabilir. Her hücre bir denetim (bir düğme, onay kutusu veya etiket gibi) tutabilir. TableLayoutPanel 'niz, en üstteki <xref:System.Windows.Forms.PictureBox> satırı, sol alt hücresinde bir <xref:System.Windows.Forms.CheckBox> denetimi ve sağ alt hücresinde dört <xref:System.Windows.Forms.Button> denetimi kapsayan bir denetime sahip olur.

8. Şu anda TableLayoutPanel 'in iki eşit boyutta satırı ve iki eşit boyutlu sütunu vardır. En üstteki satır ve sağ sütunun her ikisi de daha büyük olması için bunları yeniden boyutlandırmanız gerekiyor. **Windows Form Tasarımcısı**, TableLayoutPanel ' i seçin. Sağ üst köşede, aşağıdaki gibi görünen küçük bir siyah üçgen düğmesi vardır.

     ![Üçgen düğme](../ide/media/express_iconblacktriangle.gif)
**üçgen** düğmesi

     Bu düğme, denetimin özelliklerini otomatik olarak ayarlamanıza yardımcı olan görevler olduğunu gösterir.

9. Aşağıdaki resimde gösterildiği gibi, denetimin görev listesini göstermek için üçgeni seçin.

     ![TableLayoutPanel görevleri](../ide/media/express_tablepanel.png)
**TableLayoutPanel** görevleri

10. **Sütun ve satır stilleri** penceresini göstermek için **satırları ve sütunları Düzenle** görevini seçin. **Sütun1**' yi seçin ve yüzde düğmesinin seçili olduğundan emin olun ve **yüzde** kutusuna **15** girerek boyutunu yüzde 15 olarak ayarlayın. (Bu, sonraki <xref:System.Windows.Forms.NumericUpDown> bir öğreticide kullanacağınız bir denetimdir.) **Sütun2** 'yi seçin ve yüzde 85 olarak ayarlayın. Pencere kapandığı için **Tamam** düğmesini henüz seçmeyin. (Ancak bunu yaparsanız, görev listesini kullanarak yeniden açabilirsiniz.)

     ![TableLayoutPanel sütunu ve satır stilleri](../ide/media/vs_tablelayoutpanel_setup.png)
**TableLayoutPanel** sütun ve satır stilleri

11. Pencerenin üst kısmındaki **göster** açılan listesinden **Satırlar**' ı seçin. **Row1** değerini yüzde 90 ve **Row2** olarak ayarlayın.

12. Seçin **Tamam** düğmesi. TableLayoutPanel, artık büyük bir üst satıra, küçük bir alt satıra, küçük bir sol sütuna ve büyük bir sağ sütuna sahip olmalıdır. TableLayoutPanel içindeki satırları ve sütunları formda **tableLayoutPanel1** seçerek ve sonra satır ve sütun kenarlıklarını sürükleyerek yeniden boyutlandırabilirsiniz.

     ![Yeniden boyutlandırılmış **TableLayoutPanel** ile](../ide/media/vs_formafterlayoutpanel.png)
yeniden boyutlandırılan TableLayoutPanel**Form1**

## <a name="to-continue-or-review"></a>Devam etmek veya gözden geçirmek için

- Sonraki öğretici adımına gitmek için bkz [. 5. Adım: Formunuza](../ide/step-5-add-controls-to-your-form.md)denetimler ekleyin.

- Önceki öğretici adımına dönmek için bkz [. Adım 3: Form özelliklerinizi](../ide/step-3-set-your-form-properties.md)ayarlayın.
